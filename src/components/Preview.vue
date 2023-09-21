<script>
import Popup from "./Popup.vue";
import PopupPhoneVue from "./PopupPhone.vue";

export default {
  data() {
    return {
      message: "Test",
    };
  },
  methods: {
    test() {},
  },
  components: {
    Popup,
    PopupPhoneVue,
  },
  props: {
    activePopupPhoneVue: false,
    activePopup: false,
    activeContantFooter: true,
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
          <h4 class="content__name__header">Michelle Appleton</h4>
          <p class="content__name__data">28 Jun 2020</p>
        </div>
        <button @click="activePopup = !activePopup" class="content__button">
          <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
            <path
              fill="#6E8098"
              d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"
            />
          </svg>
        </button>
      </div>
      <div v-if="!activePopupPhoneVue" class="content__footer__phone">
        <img class="content__img" src="/public/avatar-michelle.jpg" alt="avatar" />
        <div class="content__name">
          <h4 class="content__name__header">Michelle Appleton</h4>
          <p class="content__name__data">28 Jun 2020</p>
        </div>
        <button @click="activePopupPhoneVue = !activePopupPhoneVue" class="content__button">
          <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
            <path
              fill="#6E8098"
              d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"
            />
          </svg>
        </button>
      </div>
      <PopupPhoneVue v-else class="Popup__Phone__Vue"></PopupPhoneVue>
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
/* .content {
  margin-left: 40px;
  margin-right: 35px;
} */
.content__header {
  margin-top: 30px;
  font-size: small;
  margin-left: 40px;
  margin-right: 35px;
}
.content__main {
  margin-top: 20px;
  font-size: smaller;
  margin-left: 40px;
  margin-right: 35px;
}
.content__footer {
  margin-top: 20px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-bottom: 10px;
}

.content__img {
  width: 15%;
  border-radius: 50%;
}
.content__name {
  margin-top: 5px;
  margin-right: 25px;
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
}
.content__footer__phone {
  display: none;
}

@media (max-width: 719px) {
  .container {
    width: 100%;
    height: auto;
    display: inline-block;
  }
  .content__footer {
    display: none;
  }
  .content__footer__phone {
    margin-top: 20px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-bottom: 10px;
  }
  .img__1 {
    width: 100%;
    height: 300px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    border-bottom-left-radius: 0;
  }
  .content {
  }
  .content__main {
    margin-right: 28px;
  }
  .Popup__Phone__Vue {
    margin-top: 20px;
  }
}
</style>
