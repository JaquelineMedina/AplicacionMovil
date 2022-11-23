<template>
  <ion-page>
    <menu-principal></menu-principal>
    <ion-header :translucent="true">
      <ion-toolbar class="toolbar">
        <ion-buttons slot="start">
          <ion-menu-button @click="openMenu"></ion-menu-button>
        </ion-buttons>
        <ion-title>LOGIN</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-card class="card-container">

      <ion-img src="assets/img/cds.png" alt="The Wisconsin State Capitol building in Madison, WI at night"></ion-img>
        <ion-card-header>
          <ion-card-title class="card-container__title">INICIA SESIÓN</ion-card-title>
        </ion-card-header>

        <ion-card-content class="card-content">
          <ion-item class="card-content__label">
            <ion-label position="floating">E-mail</ion-label>
            <ion-input></ion-input>
          </ion-item>
          <ion-item class="card-content__label">
            <ion-label position="floating">Contraseña</ion-label>
            <ion-input type="password"></ion-input>
          </ion-item>

          <div class="button-container">
            <router-link class="router" to='/inicioCliente'>
              <ion-button class="button-container__style">INICIAR SESIÓN</ion-button>
            </router-link>
          </div>

          <div class="help-container">
            <p class="help-container__pass">¿Olvidaste tu contraseña?</p>
            <router-link class="router" to="/signup">
              <p class="help-container__signup">
                ¿No tienes usuario? Registrate aquí
              </p>
            </router-link>
          </div>
        </ion-card-content>
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
} from "@ionic/vue";
import { defineComponent } from "vue";
import MenuPrincipal from './MenuPage.vue'

export default defineComponent({
  name: "HomePage",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    MenuPrincipal
  },
});
</script>