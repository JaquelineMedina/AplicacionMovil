<template>
  <ion-page>
    <menu-principal></menu-principal>
    <ion-header :translucent="true">
      <ion-toolbar class="toolbar">
        <ion-buttons slot="start">
          <ion-menu-button @click="openMenu"> </ion-menu-button>
        </ion-buttons>
        <ion-title>SOBRE NOSOTROS</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-card class="container-nos">
        <ion-img
          src="/assets/img/jhtl.png"
          class="img-nosotros"
        ></ion-img>

        <ion-card-header>
          <ion-card-title class="container-nos_title">¿QUIENES SOMOS?</ion-card-title>
        </ion-card-header>
        <ion-text>
          <p class="descripcion">
            Increase Corp, es una empresa dedicada a darle publicidad a un negocio o proyecto, que recién acaba de emprender, así como darle el seguimiento y ser la guía de las pequeñas empresas que desean emprender, o que simplemente tienen su negocio pero no saben como hacerlo funcionar. Ofrecemos incrementar tus ventas, y aparte de ofrecer la publicidad, daremos asesorías para que puedas crecer de una manera fantástica.
          </p>
        </ion-text>

        <ion-card-title class="container-nos_title">NUESTRO OBJETIVO</ion-card-title>
        <ion-text>
          <p class="descripcion">
            Nuestro objetivo es ayudarte a desarrollar un proyecto que abarque las necesidades del emprendimiento para hacerlo más potencial a través de tecnologías que ayuden a crecer a aquellos negocios/empresas/proyectos,etc.
          </p>
        </ion-text>

        <ion-card-title class="container-nos_title">CONOCE A NUESTRO TEAM</ion-card-title>

        <ion-slides pager="true">

      <ion-slide>

      <img src="assets/img/liz.png">
      
      </ion-slide>


       <ion-slide>

      <img src="assets/img/jaq.png">
      
      </ion-slide>


       <ion-slide>

      <img src="assets/img/slider2.png">
      
      </ion-slide>

</ion-slides>
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
  IonImg,
  IonCard,
  IonText,
  IonCardHeader,
  IonCardTitle,
} from "@ionic/vue";
import { defineComponent } from "vue";
import MenuPrincipal from "./MenuPage.vue";

export default defineComponent({
  name: "NosotrosPage",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonImg,
    MenuPrincipal,
    IonCard,
    IonText,
    IonCardHeader,
    IonCardTitle,
  },
  data() {},
});
</script>