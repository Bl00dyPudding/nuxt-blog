<template>
  <el-card
      shadow="cover"
      :body-style="{padding: 0}"
      class="post"
  >
    <header slot="header" class="post-header">
      <h3>1234567</h3>
      <small>
        <i class="el-icon-time"></i>
        {{new Date().toLocaleString()}}
      </small>
    </header>
    <div class="post-body">
      <img
          src="https://cdn2.tu-tu.ru/image/pagetree_node_data/1/bb1dcb9933b840889a1306a81f976b78/"
          alt=""
          class="post-image"
      >
    </div>
    <footer class="post-footer">
      <el-button round @click="openPost">Открыть</el-button>
      <span>
        <i class="el-icon-message"></i>
        666
      </span>
    </footer>
  </el-card>
</template>

<script>
export default {
  name: "Post",
  methods: {
    openPost () {
      //
    }
  }
}
</script>

<style lang="scss" scoped>
  .post {
    margin-bottom: 1.5rem;
  }

  .post-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .post-image {
    width: 100%;
    height: auto;
  }

  .post-body {
    //margin-bottom: 1rem;
  }

  .post-footer {
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
