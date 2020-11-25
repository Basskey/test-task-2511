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
            <input type="email" placeholder="Email Address" class="form__input" required>
            <input type="password" placeholder="Password" class="form__input" required>
            <button class="form__button form__button--submit" type="submit">Continue</button>
            <span class="form__social-note">or Connect with Social Media</span>
            <button class="form__button form__button--social form__button--twitter">Sign In With Twitter</button>
            <button class="form__button form__button--social form__button--facebook">Sign In With Facebook</button>
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

  html {
    height: 100%;
  }

  body {
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
    display: flex;
    justify-content: space-between;
    width: 1253px;
    border-radius: 43px;
    margin: 20px 95px;
    background: url('././assets/bg-box.svg') center;
    background-size: cover;
    mix-blend-mode: normal;

    &__content {
      display: flex;
      flex-direction: column;
      padding: 96px 58px 96px 76px; //вообще я предпочитаю округлять до кратных 5, либо до ближайшего значния по сетке
      flex-grow: 1;
      color: #FFFFFF;
      &::before {
        content: url('././assets/shopping_cart.svg');
        align-self: flex-end;
      }
    }

    &__title {
      margin-top: 220px;
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
        padding-top: 46px;
        background-color: rgba(255, 255, 255, .73);
      }
    }

    &__form {
      width: 594px;
      height: 100%;
      border-radius: 41px;
      padding: 87px 72px 70px;
      background: #FFFFFF;
      mix-blend-mode: normal;
    }

    .form {
      display: flex;
      flex-direction: column;
      justify-content: center;
      text-align: center;

      &__subtitle {
        margin-bottom: 50px;
        font-size: 20px;
        line-height: 1.2em;
        letter-spacing: 0.4px;
        color: #808080;
      }

      &__input {
        height: 55px;
        padding: 0 45px;
        margin-bottom: 22px;
        border: 1px solid #FFFFFF;
        border-radius: 42.5px;
        font-size: 14px;
        line-height: 1.2em;
        letter-spacing: 0.315151px;
        background: #F0F0F0;
        color: #A0A0A0;
        transition: .5s;
        outline: none; //я понимаю что отключать аутлайны это не очень user-friendly, однако мнение на этот счет спорное, а явных аутлайнов в макете не задано
        &:last-of-type {
          margin-bottom: 31px;
        }
        &:focus {
          border-color: #6ED4FF;
        }
        &::placeholder {
          color: #A0A0A0;
        }
      }

      &__button {
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        height: 55px;
        padding: 0 40px;
        margin-bottom: 22px;
        border-radius: 27.5px;
        border: none;
        font-size: 14px;
        line-height: 1.2em;
        font-weight: 400;
        letter-spacing: 1px;
        color: #FFFFFF;
        transition: .3s;
        outline: none;
        cursor: pointer;
        &:last-child {
          margin-bottom: 0;
        }
        &:hover {
          opacity: 1;
        }

        &--submit {
          background: linear-gradient(90deg, #6ED4FF 34.25%, #8FFFA3 96.88%);
          mix-blend-mode: normal;
          text-transform: uppercase;
          letter-spacing: 4.2px;
          opacity: 0.79;
          font-weight: 500;
          margin: 0;
          &::after {
            content: url('././assets/btn-arrow.svg');
            position: absolute;
            right: 25px;
          }
        }

        &--social {
          padding-left: 95px;
          justify-content: flex-start;
          &::before {
            content: '';
            display: flex;
            justify-content: center;
            align-items: center;
            width: 35px;
            height: 100%;
            position: absolute;
            left: 40px;
          }
        }

        &--twitter {
          background: linear-gradient(270deg, #67E4FE 0%, #35ABD3 52.4%);
          &::before {
            content: url('././assets/twitter.svg');
          }
        }

        &--facebook {
          background: linear-gradient(270deg, #3FA3E8 11.18%, #277EBB 63.9%);
          &::before {
            content: url('././assets/facebook.svg');
          }
        }
      }

      &__social-note {
        font-size: 13px;
        line-height: 1.2em;
        letter-spacing: 0.531818px;
        color: #8B8B8B;
        margin: 31px auto;
      }
    }
  }
</style>
