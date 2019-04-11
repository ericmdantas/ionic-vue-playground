<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>Home</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content class="ion-padding">
      <div class="ion-text-center" v-show="loading">
        <ion-spinner name="dots"></ion-spinner>
      </div>
      <div v-show="!loading">
        <ion-text>Home</ion-text>
        <br>
        <ion-button @click="changeRoute()">Change route</ion-button>
        <ion-button @click="showModal()" color="danger">Show modal</ion-button>
      </div>      
    </ion-content>
  </div>
</template>

<script>
import Modal from "@/components/Modal.vue";
export default {
  name: "home",
  data() {
    return {
      loading: true
    }
  },
  methods: {
    changeRoute() {
      this.$router.push('/about')
    },
    async showModal() {
      const modal = await this.$ionic.modalController.create({
        component: Modal,
        componentProps: {
          propsData: {
            face: 'ಠ_ಠ'
          }
        }
      });
      await modal.present();
    }
  },
  mounted() {
    setTimeout(() => {
      this.loading = false
    }, 500)
  },
};
</script>