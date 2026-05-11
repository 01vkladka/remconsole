<template>

  <button
    class="lead-button"
    @click="openPopup"
  >
    {{ text }}
  </button>

</template>

<script setup>
import './button.scss';

defineProps({

  text: {
    type: String,
    default: 'оставить заявку',
  },

});

const openPopup = () => {

  window.dispatchEvent(
    new CustomEvent('open-lead-popup')
  );
};
</script>