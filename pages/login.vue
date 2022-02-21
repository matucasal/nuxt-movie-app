<template>
  <a href="#" @click.prevent="login" class="">Login</a>
</template>

<script>
export default {
  methods:{
    login(){
      console.log('abc')
      this.$auth.loginWith('laravelSanctum', {
        data:{
          email:'matias@matias.com',
          password:'matias'
        }
      })
    }
  }
}
</script>

<style>

</style>