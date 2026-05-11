<template>

  <Teleport to="body">

    <div
      v-if="isOpen"
      class="modal"
      @click="$emit('close')"
    >

      <div
        class="modal__wrapper"
        @click.stop
      >

        <button
          class="modal__close"
          @click="$emit('close')"
        >
          ×
        </button>

        <h3 class="modal__title">
          Оставить заявку
        </h3>

        <form class="modal__form">

          <input
            type="text"
            placeholder="Ваше имя"
          />

          <input
            type="text"
            placeholder="Телефон или Telegram"
          />

          <button type="submit">
            отправить
          </button>

        </form>

      </div>

    </div>

  </Teleport>

</template>

<script setup>
import './modal.scss';

defineProps({
  isOpen: Boolean,
});

defineEmits(['close']);
</script>