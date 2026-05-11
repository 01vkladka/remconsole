<template>

  <div>

    <!-- BUTTON -->

    <button
      class="lead-button"
      @click="isOpen = true"
    >
      {{ buttonText }}
    </button>

    <!-- POPUP -->

    <transition name="popup">

      <div
        v-if="isOpen"
        class="lead-popup"
        @click.self="closePopup"
      >

        <div class="lead-popup__box">

          <button
            class="lead-popup__close"
            @click="closePopup"
          >
            ×
          </button>

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
                type="submit"
                :disabled="loading"
              >

                {{ loading
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

  </div>

</template>

<script setup>
import { ref } from 'vue';

import './lead-popup.scss';

const props = defineProps({

  buttonText: {
    type: String,
    default: 'оставить заявку',
  },

});

const isOpen = ref(false);

const loading = ref(false);

const success = ref(false);

const form = ref({
  name: '',
  contact: '',
  message: '',
});

const closePopup = () => {

  isOpen.value = false;

  loading.value = false;

  setTimeout(() => {

    success.value = false;

  }, 200);
};

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