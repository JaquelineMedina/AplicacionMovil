<template>
    <ion-page>
        <menu-principal></menu-principal>
        <ion-header :translucent="true">
            <ion-toolbar class="toolbar">
                <ion-buttons slot="start">
                    <ion-menu-button @click="openMenu"> </ion-menu-button>
                </ion-buttons>
                <ion-title>SERVICIOS</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content class="ion-padding" :fullscreen="true">
            <ion-grid>
                <ion-row>
                    <ion-col size-lg="3" size-md="3" size-sm="12" v-for="producto in lista" :key="producto.id">
                        <ion-card class="div-info-producto">
                            <div class="img-container" :style="{ backgroundImage: 'url(' + producto.imagen + ')' }">
                                <div class="img-container__blur"></div>
                                <ion-img class="img-container__front" :src="producto.imagen"></ion-img>
                            </div>
                            <ion-card-header>
                                <ion-card-title class="nombre-producto">{{ producto.nombre }}</ion-card-title>
                            </ion-card-header>
                            <ion-card-content>
                                <p class="descripcion-producto">
                                    {{ producto.descripcion }}
                                </p>
                                <ion-card-subtitle class="precio-producto">{{ producto.precio }}</ion-card-subtitle>
                                <router-link class="router" to='/carrito'>
                                    <ion-button class="boton-producto" color="secondary">Comprar</ion-button>
                                </router-link>
                            </ion-card-content>
                        </ion-card>
                    </ion-col>
                </ion-row>
            </ion-grid>
        </ion-content>
    </ion-page>
</template>

<script>

import {
    IonContent,
    IonHeader,
    IonTitle,
    IonToolbar,
    IonGrid,
    IonCol,
    IonRow,
    IonButton,
    IonCard,
    IonCardContent,
    IonCardHeader,
    IonCardSubtitle,
    IonCardTitle,
    IonImg,
    IonMenuButton,
    IonButtons,
    IonPage
} from "@ionic/vue";

import { defineComponent } from "vue";
import MenuPrincipal from './MenuPage.vue'

export default defineComponent({
    name: "ProductosPage",
    components: {
        IonContent,
        IonHeader,
        IonTitle,
        IonToolbar,
        MenuPrincipal,
        IonGrid,
        IonCol,
        IonRow,
        IonButton,
        IonCard,
        IonCardContent,
        IonCardHeader,
        IonCardSubtitle,
        IonCardTitle,
        IonImg,
        IonMenuButton,
        IonButtons,
        IonPage
    },
    data() {
        return {
            lista: [
                {
                    id: 1,
                    imagen: '/assets/img/paqe1.png',
                    nombre: 'Paquete 1 Asesorias ',
                    descripcion: 'Incluye: Como definir los obejtivos, Asesorias de como iniciar tu negocio o empresa, Como ahorrar en tus productos, Saber a que clientes va dirigido tu negocio, Revisiones de estrategias ',
                    precio: '$5,500',
                },
                {
                    id: 2,
                    imagen: '/assets/img/paqe1.png',
                    nombre: 'Paquete 2 Publicidad',
                    descripcion: 'Incluye: Publicidad mediante videos promocionales, Historias de instagram y facebook, Flyers, Infografias animadas',
                    precio: '$4,500',
                },
                {
                    id: 3,
                    imagen: '/assets/img/paqe.png',
                    nombre: 'Paquete 3 Publicidad y Asesorias',
                    descripcion: 'Incluye:Lo antes mencionado en anteriores paquetes',
                    precio: '$4,500',
                },
               
            ]
        }
    }
});
</script>