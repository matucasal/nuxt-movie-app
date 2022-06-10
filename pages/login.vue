<template>
  <div class="login-layout">
    <div class="form-wrapper">
      <h2 class="">
        Login
      </h2>
      <form>
        <label for="email" class="">Email</label>
        <input id="email required" type="email">
        <label for="password" class="">Password</label>
        <input id="password required" type="password">
        <button type="submit" @click.prevent="login">
          Submit
        </button>
      </form>
    </div>
  </div>
</template>

<script>
export default {

  methods: {
    login () {
      this.$auth.loginWith('laravelSanctum', {
        data: {
          email: 'matias@matias.com',
          password: 'matias'
        }
      })
    }
  }
}
</script>

<style lang="scss" scoped>

/*login-layout section*/
.login-layout{
  border: 1px solid red;
  min-height: 90vh;
  flex-wrap: wrap;
  @include flex (center,center, row);
}

/*Form element*/
.form-wrapper{
  margin: 5vh;
  padding: 10vh;
  width: 150vh;
  flex: 0;
  background-color:#e3e3e3;
  border-radius: 25px;
}

.form-wrapper h2{
  font-size: $header1;
  margin-bottom: 3vh;
  color: black;
}


.form-wrapper label{
  display: block;
  color: black;
}

.form-wrapper input{
  display: block;
  margin: 3vh 0vh;
  background: $btn-background-color;
  color: white;
  border: none;
  padding: 2vh;
}

.form-wrapper button{
  margin-top: 3vh;
  padding: 5vh 12vh;
  background: $btn-special-color;
  color:white;
  border: none;
  width: 100%;
}

</style>
