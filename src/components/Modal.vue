<template>
    <div class="ion-page">
        <div class="ion-padding">
            <h1>{{face}}</h1>
        </div>

        <div style="float: right;">
            <ion-button color="primary" @click="close()">Hide, yo kids</ion-button>
            <ion-button color="light" @click="close()">Hide, yo wife</ion-button>
        </div>        
    </div>
</template>

<script>
export default {
    name: 'modal',
    props: {
        face: {
            type: String,
            default: '',
        },
    },
    methods: {
        close() {
            this.$ionic.modalController.dismiss()
        },
    },
}
</script>
