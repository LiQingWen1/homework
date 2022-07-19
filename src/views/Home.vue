<template>
  <div class="home">
    <lButton>默认按钮</lButton>
    <lButton type="primary"  >成功按钮</lButton>
    <lButton type="danger" >危险按钮</lButton>
    <lButton type="warning" >警告按钮</lButton>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data () {
    return {
      flag: false
    }
  },
  components: {
    lButton: () => import('../components/button/index.vue')
  },
  methods: {
    handleSubmit () {
      this.flag = true
      setTimeout(() => {
        console.log('123')
        this.flag = false
      }, 3000)
    }
  }
}
</script>
