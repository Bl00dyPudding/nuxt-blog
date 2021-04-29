<template>
  <div class="error-layout">
    <div class="error-content">
      <h1>Ошибка 404</h1>
      <nuxt-link to="/">
        <el-button>На главную</el-button>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "error",
  head() {
    return {
      title: `Ошибка 404 | ${process.env.appName}`
    }
  }
}
</script>

<style scoped>
  .error-layout {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .error-content {
    text-align: center;
    color: #128BCB;
    margin-bottom: 1rem;
    margin-top: 4rem;
  }
</style>
