<template>
  <div id="app">
    <div class="container">
      <nav-app />
      <div class="content">
        <header-app />
        <div class="main">
          <div>
            <button class="button" @click="showDialog()">Hola</button>
          </div>
        </div>
      </div>
    </div>
    <div class="popup">
      <div class="popup popup__overlay" @click="hideDialog()"></div>
      <div class="popup popup__main">
        <div class="popup popup__main popup__main__content">
          <span
            class="popup popup__main popup__main__content popup__main__content__close-btn"
            @click="hideDialog()"
          >
            &times;
          </span>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum nostrum quos, maxime
            cum, molestias quasi tenetur repudiandae quos unde voluptate eveniet quis debitis fuga
            accusamus dignissimos.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavApp from '@/components/common/NavApp.vue';
import HeaderApp from '@/components/common/HeaderApp.vue';

export default {
  name: 'App',
  components: {
    NavApp,
    HeaderApp,
  },
  methods: {
    showDialog() {
      const popup = document.querySelector('.popup');
      const popupMain = document.querySelector('.popup__main');

      popup.style.display = 'flex';
      popupMain.style.cssText = 'animation:slide-in .5s ease; animation-fill-mode: forwards';
    },
    hideDialog() {
      const popup = document.querySelector('.popup');
      const popupMain = document.querySelector('.popup__main');

      popupMain.style.cssText = 'animation:slide-out .5s ease; animation-fill-mode: forwards';

      setTimeout(() => {
        popup.style.display = 'none';
      }, 500);
    },
  },
  mounted() {
    const popup = document.querySelector('.popup');

    popup.style.display = 'none';
  },
};
</script>

<style lang="scss" src="@/assets/scss/main.scss"></style>
