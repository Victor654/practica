<template>
  <div class="login">
    <div class="login__mobile">
      <div class="login__mobile--header">
        <img src="https://www.cocoreservas.com/public/img/login/Logo_top.png" />
      </div>
      <div class="login__mobile--title">
        <h2>Estamos en constante</h2>
        <h1>EVOLUCIÓN</h1>
      </div>
    </div>
    <div class="login__left-side">
      <div class="login__left-side--logotop">
        <img src="https://www.cocoreservas.com/public/img/login/Logo_top.png" />
      </div>
      <h2>Estamos en constante</h2>
      <h1>EVOLUCIÓN</h1>
      <img
        class="login__left-side--img"
        src="https://www.cocoreservas.com/public/img/login/bg_img_left.svg"
      />
    </div>
    <div class="login__right-side">
      <LoginForm />
    </div>
  </div>
</template>

<script>
import LoginForm from "@/components/LoginForm";

export default {
  name: "login",
  components: {
    LoginForm
  }
};
</script>

<style lang="scss" scoped>
.login {
  height: 100vh;
  text-align: left;
  display: grid;
  grid-template-columns: 1fr 1fr;
  &__mobile {
    display: none;
  }
  &__left-side {
    background: linear-gradient(-45deg, rgb(22, 31, 41), rgb(35, 58, 84));
    &--logotop {
      margin-left: 11%;
      margin-top: 40px;
    }
    h2 {
      color: $color-white;
      margin: 100px 0px 0px 11%;
      font-size: 24px;
      font-weight: 400;
    }
    h1 {
      margin: 0px 0px 0px 11%;
      font-size: 28px;
      font-weight: 800;
    }
    &--img {
      width: 50%;
      height: auto;
      position: fixed;
      bottom: 0;
    }
  }
  &__right-side {
    justify-self: center;
    align-self: center;
    width: 50%;
  }
}

@media (max-width: 766px) {
  .login {
    display: block;
    &__mobile {
      display: block;
      &--header {
        background: linear-gradient(-45deg, rgb(22, 31, 41), rgb(35, 58, 84));
        height: 100px;
        padding-top: 16px;
        text-align: center;
      }
      &--title {
        text-align: center;
        h2 {
          color: $secondary-color;
          margin-top: 30px;
          margin-bottom: 0;
          font-size: 24px;
          font-weight: 400;
        }
        h1 {
          margin-top: 5px;
          font-size: 32px;
          font-weight: 800;
          margin-bottom: 21px;
        }
      }
    }
    &__left-side {
      display: none;
    }
    &__right-side {
      width: 100%;
    }
  }
}
</style>
