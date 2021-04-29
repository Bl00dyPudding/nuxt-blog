<template>
  <el-card
      shadow="cover"
      :body-style="{padding: 0}"
      class="post"
  >
    <header slot="header" class="post-header">
      <h3>{{ post.title }}</h3>
      <small>
        <i class="el-icon-time"></i>
        {{ new Date(post.date).toLocaleString() }}
      </small>
    </header>
    <div class="post-body">
      <img
          :src="post.imageUrl"
          alt=""
          class="post-image"
      >
    </div>
    <footer class="post-footer">
      <el-button round @click="openPost">Открыть</el-button>
      <span>
        <i class="el-icon-message"></i>
        {{ post.comments.length }}
      </span>
    </footer>
  </el-card>
</template>

<script>
export default {
  name: "Post",
  props: {
    post: {
      type: Object,
      required: true
    }
  },
  methods: {
    openPost () {
      const postId = this.post._id
      this.$router.push('/post/' + postId)
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
