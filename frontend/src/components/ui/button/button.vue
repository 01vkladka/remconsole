<template>

  <button
    class="ui-button"
    :class="`ui-button--${variant}`"
    type="button"
    @click="isOpen = true"
  >

    {{ text }}

  </button>

  <Modal
    :is-open="isOpen"
    @close="isOpen = false"
  />

</template>

<script setup>
import { ref } from 'vue';

import Modal from '@components/ui/Modal/Modal.vue';

import './button.scss';

defineProps({

  text: {
    type: String,
    default: 'кнопка',
  },

  variant: {
    type: String,
    default: 'primary',
  },

});

const isOpen = ref(false);
</script>