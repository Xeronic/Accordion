<template>
  <div class="c-accordion">
    <div class="c-accordion-head" @click="toggleAccordion">
      <span>{{ title }}</span>
      <i :class="isShow ? 'fas fa-angle-down': 'fas fa-angle-right'" />
    </div>
    <div class="c-accordion-body" :style="{height: height}">
      <div class="body-text">
        <slot name="Body" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  props: ["title"],
  data() {
    return {
      isShow: false,
      element: null,
      height: 0 + "px"
    };
  },

  methods: {
    toggleAccordion() {
      this.isShow = !this.isShow;

      if (this.isShow) {
        this.element = document.querySelector(".body-text");
        window.el = this.element;
        this.height = window.getComputedStyle(this.element).height;
      } else {
        this.height = 0;
      }
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  position: relative;
}
.c-accordion {
  margin: 0 auto;
  width: 50vw;
}

.c-accordion-head {
  box-sizing: border-box;
  display: flex;
  font-size: 24px;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  text-align: left;
  background-color: palevioletred;
  padding: 32px 16px;
  transition: all 1s ease-in-out;
}

.c-accordion-body {
  height: 0;
  overflow: hidden;
  background-color: palegoldenrod;
  transition: all 0.225s ease-in-out;
}

.body-text {
  overflow: auto;
  padding: 32px 16px;
  bottom: 0;
  position: absolute;
  width: 100%;
}

.c-accordion-body.collapse {
}
</style>
