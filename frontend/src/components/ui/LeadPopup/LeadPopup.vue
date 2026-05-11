<template>

  <transition name="popup">

    <div
      v-if="isOpen"
      class="lead-popup"
      @click="closePopup"
    >

      <div
        class="lead-popup__box"
        @click.stop
      >

        <!-- CLOSE -->

        <button
          class="lead-popup__close"
          type="button"
          @click="closePopup"
        >
          ×
        </button>

        <!-- CONTENT -->

        <div class="lead-popup__content">

          <span class="lead-popup__label">
            заявка
          </span>

          <h2 class="lead-popup__title">
            ОБСУДИМ
            <br />
            РЕМОНТ
          </h2>

          <p class="lead-popup__description">
            Оставьте контакты —
            ответим сегодня.
          </p>

          <!-- FORM -->

          <form
            class="lead-form"
            @submit.prevent="submitForm"
          >

            <input
              v-model="form.name"
              type="text"
              placeholder="Ваше имя"
            />

            <input
              v-model="form.contact"
              type="text"
              placeholder="Telegram или телефон"
            />

            <textarea
              v-model="form.message"
              placeholder="Что случилось?"
            ></textarea>

            <button
              class="lead-form__submit"
              type="submit"
              :disabled="loading"
            >

              {{
                loading
                  ? 'отправка...'
                  : 'отправить заявку'
              }}

            </button>

            <div
              v-if="success"
              class="lead-form__success"
            >
              Заявка отправлена
            </div>

          </form>

        </div>

      </div>

    </div>

  </transition>

</template>

<script setup>
import {
  ref,
  onMounted,
  onUnmounted,
} from 'vue';

import './lead-popup.scss';

/* STATE */

const isOpen = ref(false);

const loading = ref(false);

const success = ref(false);

const form = ref({
  name: '',
  contact: '',
  message: '',
});

/* OPEN */

const openPopup = () => {

  isOpen.value = true;
};

/* CLOSE */

const closePopup = () => {

  isOpen.value = false;

  loading.value = false;

  success.value = false;
};

/* EVENTS */

onMounted(() => {

  window.addEventListener(
    'open-lead-popup',
    openPopup
  );
});

onUnmounted(() => {

  window.removeEventListener(
    'open-lead-popup',
    openPopup
  );
});

/* SUBMIT */

const submitForm = async () => {

  if (loading.value) return;

  loading.value = true;

  try {

    const response = await fetch('/lead', {

      method: 'POST',

      headers: {
        'Content-Type': 'application/json',
      },

      body: JSON.stringify({
        name: form.value.name,
        contact: form.value.contact,
        message: form.value.message,
      }),

    });

    if (!response.ok) {
      throw new Error('Ошибка');
    }

    success.value = true;

    form.value = {
      name: '',
      contact: '',
      message: '',
    };

  } catch (error) {

    console.error(error);

    alert('Ошибка отправки');

  } finally {

    loading.value = false;
  }
};
</script>