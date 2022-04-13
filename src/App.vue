<template>
  <div>
    <Suspense>
      <template #default>
        <Home />
      </template>
      <template #fallback>
        <SplashScreen />
      </template>
    </Suspense>
  </div>
</template>

<script>
// import Home from "@/components/HomeComponent";
import SplashScreen from "@/components/SplashScreen";
import { defineAsyncComponent } from "vue";
export default {
  components: {
    SplashScreen,
    Home: defineAsyncComponent(
      () =>
        new Promise((resolve) => {
          setTimeout(() => {
            resolve(import("./components/HomeComponent"));
          }, 2500);
        })
    ),
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
