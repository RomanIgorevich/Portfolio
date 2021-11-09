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

<style lang="scss">
.modal__wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  transition: opacity 0.3s ease;
  right: 0;
  z-index: 998;
  background-color: rgba(00, 00, 00, 0.48);
}
.modal__content {
  overflow: auto;
  position: relative;
  width: 50%;
  max-height: 90%;
  padding: $padding * 2;
  background-color: $fon;
  border: 1px solid #dcdfe6;
  transition: all 0.3s ease;
  z-index: 999;
}
.modal__header {
  display: flex;
  align-self: center;
  justify-content: space-between;
  padding-bottom: $padding * 2;
  .button-close {
    cursor: pointer;
    display: block;
    position: relative;
  }
  .button-close::before {
    content: url("../assets/svg/cancel-circle.svg");
    position: absolute;
    top: 0;
    right: 0;
  }
}
.modal__body {
  text-align: center;
}
.modal__text {
  padding: 0 0 $padding 0;
  text-align: left;
}
.link-site {
  display: inline-block;
  padding: $padding/2 $padding;
  border: 2px solid #949393;
  color: $color;
  margin-top: $padding;
}
.modal-enter,
.modal-leave-active {
  opacity: 0;
}
.modal-enter .modal-content,
.modal-leave-active .modal-content {
  transform: scale(1.8);
}
</style>
