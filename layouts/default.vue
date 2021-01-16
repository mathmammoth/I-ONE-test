<template>
  <div>
    <PostList />
    <main>
      <div class="">
        <Nuxt />
      </div>
    </main>
  </div>
</template>

<script>
  import PostList from '@/components/PostList'
  export default {
    components: {
      PostList
    }

  }
</script>

