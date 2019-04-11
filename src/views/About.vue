<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-back-button></ion-back-button>
        </ion-buttons>
        <ion-title>About</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <ion-item>
        <ion-label position="stacked">There you go 1</ion-label>
        <ion-input></ion-input>
      </ion-item>

      <ion-item>
        <ion-label position="stacked">There you go 2</ion-label>
        <ion-input></ion-input>
      </ion-item>

      <ion-item>
        <ion-label position="stacked">There you go 3</ion-label>
        <ion-input></ion-input>
      </ion-item>

      <ion-list>
        <ion-item>
          <ion-label>Pokémon Yellow</ion-label>
        </ion-item>
        <ion-item>
          <ion-label>Mega Man X</ion-label>
        </ion-item>
        <ion-item>
          <ion-label>The Legend of Zelda</ion-label>
        </ion-item>
        <ion-item>
          <ion-label>Pac-Man</ion-label>
        </ion-item>
        <ion-item>
          <ion-label>Super Mario World</ion-label>
        </ion-item>
      </ion-list>

      <div class="about">
        <ion-button @click="goBack()">Go back</ion-button>
      </div>
    </ion-content>
  </div>
</template>

<script>
export default {
  methods: {
    goBack() {
      this.$router.go(-1)
    },
  }, 
}
</script>
