<template>
  <div>
    <h1>Аналитика по постам</h1>
    <Analytics
      :title="'Количество просмотров'"
      :labels="views.labels"
      :data="views.data"
    ></Analytics>
    <Analytics
        :title="'Количество комментариев'"
        :labels="comments.labels"
        :data="comments.data"
    ></Analytics>
  </div>
</template>

<script>
import Analytics from '@/components/admin/AnalyticsChart'
export default {
  layout: 'admin',
  middleware: ['admin-auth'],
  components: {
    Analytics
  },
  data () {
    return {
      views: '',
      comments: ''
    }
  },
  async asyncData({store}) {
    const {views, comments} = await store.dispatch('post/getAnalytics')
    return {views, comments}
  }
}
</script>

