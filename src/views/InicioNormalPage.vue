<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar class="toolbar">
        <ion-title>INICIO</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-card class="container-ini">
        <ion-card-header>
            <ion-toolbar class="titulo">
        <ion-title class="titulo">HACEMOS CRECER TU NEGOCIO </ion-title>
        <ion-title class="titulo">resplandece</ion-title>

      </ion-toolbar>
        </ion-card-header>

        <ion-text>
          <p>El control de tus productos smart al alcance de tu mano.</p>
          <p class="desc">Innovación, cálidad y compromiso.</p>
        </ion-text>
        <ion-img
          src="/assets/img/fotis.png" class="img-user-container"
        ></ion-img>
      </ion-card>


       


    </ion-content>

    
  </ion-page>
</template>

<script>
import {
  IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
  IonImg
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "HomePage",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonImg
  },
  data(){
    
  }
});


</script>
