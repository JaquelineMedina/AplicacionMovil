<template>
    <ion-menu side="start" content-id="principal">
        <ion-header :translucent="true">
            <ion-toolbar class="toolbar">
                <ion-title>MENÚ</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content>
            <ion-list>
                <ion-item v-for="pagina in lista" :key="pagina.titulo">
                    <ion-icon :src="pagina.icono" class="icono-menu"> </ion-icon>
                    <router-link class="router" :to="pagina.redirectTo">
                        <ion-label class="opciones-menu"> {{pagina.titulo}} </ion-label>
                    </router-link>
                </ion-item>
            </ion-list>
        </ion-content>
    </ion-menu>
    <ion-router-outlet id="principal"/>
</template>

<script>

import {
    IonContent,
    IonHeader,
    IonTitle,
    IonToolbar,
    IonMenu,
    IonIcon,
    IonLabel,
    IonList,
    IonItem,
    IonRouterOutlet,
    menuController
} from "@ionic/vue";

import { defineComponent } from "vue";

export default defineComponent({
    name: "MenuPrincipal",
    components: {
        IonContent,
        IonHeader,
        IonTitle,
        IonToolbar,
        IonMenu,
        IonList,
        IonItem,
        IonIcon,
        IonLabel,
        IonRouterOutlet
    },
    data() {
        return {
            lista: [
                { titulo: 'INICIO', icono: '/assets/icons/inicio1.svg', redirectTo: '/home' },
                { titulo: 'SOBRE NOSOTROS', icono: '/assets/icons/usuarios.svg', redirectTo: '/nosotros' },
                { titulo: 'SERVICIOS', icono: '/assets/icons/dolar.svg', redirectTo: '/productos' },
                { titulo: 'CONTACTANOS', icono: '/assets/icons/llamada-telefonica.svg', redirectTo: '/contacto' },
                { titulo: 'INICIO DE SESIÓN', icono: '/assets/icons/usuario.svg', redirectTo: '/login' },
                { titulo: 'REGISTRATE', icono: '/assets/icons/agregar-usuario.svg', redirectTo: '/signup' },
                // { titulo: 'Inicio (Administrador)', icono: '/assets/icons/inicio.svg', redirectTo: '/inicioCliente' },
                // { titulo: 'Carrito de Compras', icono: '/assets/icons/carrito.svg', redirectTo: '/carrito' },
                // { titulo: 'Administrar Producto', icono: '/assets/icons/admin-produc.svg', redirectTo: '/administrarProducto' },
                // { titulo: 'Configuración de Cuenta', icono: '/assets/icons/configuracion.svg', redirectTo: '/cuentaCliente' },
            ],
        };
    },
    methods: {
        openMenu() {
            menuController.enable(true);
            menuController.open();
        },
        closeMenu(){
            menuController.enable(true);
            menuController.close();
        }
        
    }
});
</script>