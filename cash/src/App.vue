<template>
  <Suspense>
    <!-- #default: nombre del slot -->
    <template #default>
      <!-- al terminar de cargar el splashScreen mostrara el Home -->
      <HomeCash />
    </template>
    <template #fallback>
         <!-- se cargara al inicio -->
        <SplashscreenCash/>
    </template>
  </Suspense>
</template>

<script>
import SplashscreenCash from "./components/SplashscreenCash.vue";
import { defineAsyncComponent } from "vue";
import HomeCash from "./components/HomeCash.vue";

export default {
  components: {
    SplashscreenCash,
    HomeCash: defineAsyncComponent(() => new Promise((resolve) => setTimeout(() => {
        resolve(import("./components/HomeCash.vue"));
    }, 2500))),
},
};
</script>

<style>
html,
body,
.app {
  min-height: 100vh;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
* {
  --brand-green: #04b500;
  --brand-blue: #0689b0;
}
</style>
