<template>
  <div class="modal__wrapper" @click="$emit('close')">
    <div class="modal__content" @click.stop="">
      <div class="modal__header">
        <h3 class="modal__title">{{ dataWork.title }}</h3>
        <span class="button-close" @click="$emit('close')"> </span>
      </div>
      <div class="modal__body">
        <p class="modal__text">{{ dataWork.textBig }}</p>
        <p class="modal__text"><strong>STACK:</strong> {{ dataWork.stack }}</p>
        <a class="link-site" :href="dataWork.link">Перейти на Github</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: {
    dataWork: {
      type: Object,
      required: true,
    },
  },
};
</script>
