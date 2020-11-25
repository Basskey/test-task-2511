<template>
  <div id="app">
    <div class="welcome">
      <div class="welcome__content">
        <h2 class="welcome__title">Welcome Page</h2>
        <span class="welcome__subtitle">Sign in to continue access pages</span>
      </div>
      <form action="" class="welcome__form form">
        <h2 class="form__title">Sign In</h2>
        <span class="form__subtitle">Sign in to continue access pages</span>
        <input type="text" placeholder="Email Address" class="form__input">
        <input type="text" placeholder="Password" class="form__input">
        <button class="form__button form__button--submit">Continue</button>
        <span class="form__social-note">or Connect with Social Media</span>
        <button class="form__button form__button--social form__button--twitter">Sign In With Twitter</button>
        <button class="form__button form__button--social form__button--twitter">Sign In With Facebook</button>
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
