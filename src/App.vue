<template>
  <div id="app" class="wrapper">
    <div class="welcome">
      <div class="welcome__content">
        <h2 class="welcome__title h2">Welcome Page</h2>
        <span class="welcome__subtitle">Sign in to continue access pages</span>
      </div>
      <div class="welcome__decorative-container">
        <div class="welcome__decorative-container">
          <form action="" class="welcome__form form">
            <h2 class="form__title h2">Sign In</h2>
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

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap');

  * {
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
  }

  html, body {
    width: 100%;
    min-height: 100%;
    margin: 0;
    display: flex;
  }

  .h2 {
    font-size: 52px;
    font-weight: 700;
    line-height: 1.22em;
    margin: 0 0 22px;
    letter-spacing: 0.472727px;
  }

  .wrapper {
    background-color: #5CC5B1;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .welcome {
    mix-blend-mode: normal;
    border-radius: 43px;
    display: flex;
    justify-content: space-between;
    width: 1253px;
    margin: 95px;
    background: url('././assets/bg-box.svg');
    background-size: cover;
    background-position: center;

    &__content {
      padding: 95px 75px;
      color: white;
    }

    &__subtitle {
      font-size: 24px;
      line-height: 1.2em;
      font-weight: 400;
      letter-spacing: 0.48px;
    }

    &__decorative-container {
      display: flex;
      border-radius: 41px;
      padding-top: 38px;
      background-color: rgba(255, 255, 255, .48);

      .welcome__decorative-container {
        background-color: rgba(255, 255, 255, .73);
      }
    }

    &__form {
      width: 594px;
      background: #FFFFFF;
      mix-blend-mode: normal;
      border-radius: 41px;
      height: 100%;
      padding: 87px 72px 70px;
    }

    .form {
      display: flex;
      flex-direction: column;
      justify-content: center;
      text-align: center;

      &__subtitle {
        color: #808080;
        margin-bottom: 50px;
        font-size: 24px;
        line-height: 1.2em;
      }

      &__input {
        height: 55px;
        background: #F0F0F0;
        border: 1px solid #FFFFFF;
        border-radius: 42.5px;
        padding: 0 45px;
        font-size: 14px;
        line-height: 1.2em;
        letter-spacing: 0.315151px;
        color: #A0A0A0;
        margin-bottom: 22px;
        &:last-of-type {
          margin-bottom: 31px;
        }
      }
    }
  }
</style>
