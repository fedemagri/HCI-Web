<script setup lang="ts">
    import AppDivision from '@/components/AppDivision.vue';
    import AppHeaderPrimaryScreen from '@/components/AppHeaderPrimaryScreen.vue';
    import BodyGrid from '@/components/BodyGrid.vue';
    import ButtonsNavBar from '@/components/ButtonsNavBar.vue';
    import Section from '@/components/Section.vue';

    const pesos = 25.761;
    const centavos = 57;

</script>

<template>
    <!--<AppHeaderSecondary title="Más" />-->
    <AppHeaderPrimaryScreen />

    <v-main class="main-container" fluid>
      
        <ButtonsNavBar />
        <BodyGrid>
            <AppDivision class="ma-4" cols="12" sm="6" md="4">
            <Section class="ma-3">
                <v-container class="inside-section">

                    <h2 class="text-colortext2">Hola, Nombre de usuario</h2>
                    
                    <v-divider class="my-2"/>
                    
                    <p class="text-weight-light text-colortext2">Dinero disponible</p>
                    
                    <v-container class="money-container">
                        <h1 class="text-weight-bold text-colortext2">${{pesos}}</h1>
                        <v-container class="cents-container">
                            <p class="text-colortext2">{{centavos}}</p>
                        </v-container>
                        <v-icon size="32" class="text-colortext2 mr-2">mdi-eye</v-icon>
                    </v-container>

                    <v-divider class="my-2"/>

                    <v-container class="functions-container">
                        <v-btn size="x-large" icon="mdi-cash-fast" color="primary" elevation="4"/>
                        <v-btn size="x-large" icon="mdi-cash-fast" color="primary" elevation="4"/>
                        <v-btn size="x-large" icon="mdi-cash-fast" color="primary" elevation="4"/>
                    </v-container>
                    
                    <v-divider class="my-2"/>
                </v-container>
            </Section>

            <Section class="ma-3">
                <v-container class="inside-section">
                    <p class="text-weight-light text-colortext2">Medios de pago</p>
                    <v-container class="card bg-lime-darken-4 rounded">
                        <p> •••• •••• •••• 4444 </p>
                    </v-container>
                </v-container>
            </Section>
            
            </AppDivision>
    
            <AppDivision class="ma-6" cols="12" sm="6" md="4">
                <Section class="ma-3">

                </Section>
            </AppDivision>
        </BodyGrid>

    </v-main>

</template>

<style>
    .main-container{
        display: flex;
        flex-direction: column;
    }
    .inside-section {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 100%;
        justify-content: flex-start;
    }
    .money-container{
        display:flex;
        flex-direction: row;
        align-items: center;
        padding: 0px;
    }
    .cents-container{
        display:flex;
        flex-direction: column;
        justify-content: flex-start;
        padding: 0px;
        margin: 0px;
        height: 100%;
    }
    .functions-container{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding-left: 12%;
        padding-right: 12%;
    }
</style>