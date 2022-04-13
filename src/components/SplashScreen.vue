<template>
  <div>
    <div class="splashscreen">
      <img src="@/assets/cashflow-icon.svg" alt="Logo" />
      <h1><span>Cash</span>Flow</h1>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="css" scoped>
.splashscreen {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100vh;
}
h1 {
  color: var(--brand-blue);
}
h1 span {
  color: var(--brand-green);
}
</style>
