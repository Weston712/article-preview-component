<script>
import Popup from "./Popup.vue";

export default {
  data() {
    return {
      activePopupPhoneVue: false,
      activePopup: false,
      activeContantFooter: true,
    };
  },
  computed: {
    svgColor: function () {
      this.activePopup = true;
    },
  },
  components: {
    Popup,
  },
};
</script>

<template>
  <div class="container">
    <img class="img__1" src="/public/drawers.jpg" alt="foto" />
    <article class="content">
      <header class="content__header">
        <h1>Shift the overall look and feel by adding these wonderful touches to furniture in your home</h1>
      </header>
      <main class="content__main">
        <p>
          Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and uninviting. I’ve
          got some simple tips to help you make any room feel complete.
        </p>
      </main>
      <div class="content__footer">
        <img class="content__img" src="/public/avatar-michelle.jpg" alt="avatar" />
        <div class="content__name">
          <span class="content__name__header">Michelle Appleton</span>
          <p class="content__name__data">28 Jun 2020</p>
        </div>

        <button :class="{ btnSvgColor: activePopup }" @click="activePopup = !activePopup" class="content__button">
          <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
            <path
              class="content__button"
              :class="{ white: activePopup }"
              d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"
            />
          </svg>
        </button>
      </div>
      <div v-if="activeContantFooter" class="content__footer__phone">
        <img class="content__img" src="/public/avatar-michelle.jpg" alt="avatar" />
        <div class="content__name">
          <h4 class="content__name__header">Michelle Appleton</h4>
          <p class="content__name__data">28 Jun 2020</p>
        </div>
        <button @click="activeContantFooter = !activeContantFooter" class="content__button">
          <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
            <path
              fill="#6E8098"
              d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"
            />
          </svg>
        </button>
      </div>
      <div v-else class="container__popup__phone">
        <p class="popup__header">SHARE</p>
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20">
            <path
              fill="#FFF"
              d="M18.896 0H1.104C.494 0 0 .494 0 1.104v17.793C0 19.506.494 20 1.104 20h9.58v-7.745H8.076V9.237h2.606V7.01c0-2.583 1.578-3.99 3.883-3.99 1.104 0 2.052.082 2.329.119v2.7h-1.598c-1.254 0-1.496.597-1.496 1.47v1.928h2.989l-.39 3.018h-2.6V20h5.098c.608 0 1.102-.494 1.102-1.104V1.104C20 .494 19.506 0 18.896 0z"
            />
          </svg>
        </span>
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="17">
            <path
              fill="#FFF"
              d="M20 2.172a8.192 8.192 0 01-2.357.646 4.11 4.11 0 001.804-2.27 8.22 8.22 0 01-2.605.996A4.096 4.096 0 0013.847.248c-2.65 0-4.596 2.472-3.998 5.037A11.648 11.648 0 011.392 1a4.109 4.109 0 001.27 5.478 4.086 4.086 0 01-1.858-.513c-.045 1.9 1.318 3.679 3.291 4.075a4.113 4.113 0 01-1.853.07 4.106 4.106 0 003.833 2.849A8.25 8.25 0 010 14.658a11.616 11.616 0 006.29 1.843c7.618 0 11.922-6.434 11.663-12.205A8.354 8.354 0 0020 2.172z"
            />
          </svg>
        </span>
        <span>
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20">
            <path
              fill="#FFF"
              d="M10 0C4.478 0 0 4.477 0 10c0 4.237 2.636 7.855 6.356 9.312-.088-.791-.167-2.005.035-2.868.182-.78 1.172-4.97 1.172-4.97s-.299-.6-.299-1.486c0-1.39.806-2.428 1.81-2.428.852 0 1.264.64 1.264 1.408 0 .858-.545 2.14-.828 3.33-.236.995.5 1.807 1.48 1.807 1.778 0 3.144-1.874 3.144-4.58 0-2.393-1.72-4.068-4.177-4.068-2.845 0-4.515 2.135-4.515 4.34 0 .859.331 1.781.745 2.281a.3.3 0 01.069.288l-.278 1.133c-.044.183-.145.223-.335.134-1.249-.581-2.03-2.407-2.03-3.874 0-3.154 2.292-6.052 6.608-6.052 3.469 0 6.165 2.473 6.165 5.776 0 3.447-2.173 6.22-5.19 6.22-1.013 0-1.965-.525-2.291-1.148l-.623 2.378c-.226.869-.835 1.958-1.244 2.621.937.29 1.931.446 2.962.446 5.522 0 10-4.477 10-10S15.522 0 10 0z"
            />
          </svg>
        </span>
        <button v-on:click="activeContantFooter = !activeContantFooter" class="popup__btn__phone">
          <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
            <path
              d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"
            />
          </svg>
        </button>
      </div>
      <Popup v-show="activePopup"></Popup>
    </article>
  </div>
</template>

<style scoped>
.container {
  width: 700px;
  height: 300px;
  margin-right: 15px;
  display: flex;
  margin-left: 15px;
  border-radius: 10px;
  background-color: white;
}
.img__1 {
  width: 38%;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
}

.content__header {
  margin-top: 30px;
  font-size: small;
  margin-left: 40px;
  margin-right: 35px;
  color: #4f5868;
}
.content__main {
  margin-top: 20px;
  font-size: smaller;
  margin-left: 40px;
  margin-right: 35px;
  font-size: 13px;
  color: #b2b7c1;
}
.content__footer {
  margin-top: 20px;
  display: flex;
  align-items: center;
}

.content__img {
  margin-left: 40px;
  width: 15%;
  border-radius: 50%;
}
.content__name {
  margin-top: 5px;
  margin-right: 25px;
  margin-left: 20px;
}
.content__name__header {
  color: #525863;
}
.content__name__data {
  color: #b6bcc4;
  margin: 0;
  padding: 0;
}
.content__button {
  width: 35px;
  height: 35px;
  border-radius: 50px;
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: hsl(210, 46%, 95%);
  cursor: pointer;
  fill: #6e8098;
  margin-left: auto;
  margin-right: 40px;
}
.white {
  fill: white;
  background-color: #6e8098;
}

.btnSvgColor {
  background-color: #6e8098;
}
.content__footer__phone {
  display: none;
}

@media (max-width: 719px) {
  .container {
    width: 100%;
    height: auto;
    display: inline-block;
    margin-top: 15px;
    margin-bottom: 15px;
  }
  .content__footer {
    display: none;
  }
  .content__footer__phone {
    display: flex;
    align-items: center;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  .img__1 {
    width: 100%;
    height: 300px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    border-bottom-left-radius: 0;
  }

  .Popup__Phone__Vue {
    margin-top: 20px;
  }
  .container__popup__phone {
    display: none;
    margin-top: 20px;
  }
  @media (max-width: 719px) {
    .container__popup__phone {
      width: 100%;
      height: 60px;
      display: flex;
      border-bottom-left-radius: 10px;
      border-bottom-right-radius: 10px;
      background-color: hsl(217, 19%, 35%);
      justify-content: space-evenly;
      align-items: center;
    }
    .content__name {
      font-size: smaller;
    }
    .content__name__header {
      margin: 0;
      padding: 0;
    }
    .popup__header {
      font-size: small;
      letter-spacing: 4px;
      color: #9fa7b2;
    }
    .popup__btn__phone {
      width: 30px;
      height: 30px;
      border-radius: 50px;
      border: none;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #6e8098;
      cursor: pointer;
      fill: white;
    }
  }
}
</style>
