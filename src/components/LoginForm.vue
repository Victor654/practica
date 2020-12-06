<template>
  <div class="login-form">
    <h3>Inicia sesión</h3>
    <div class="login-form--input">
      <label for="user">Usuario:</label> <br />
      <input type="text" id="user" placeholder="Ingresa tu usuario" />
    </div>
    <div class="login-form--input password">
      <label for="password">Contraseña:</label> <br />
      <input type="text" id="password" placeholder="Ingresa tu contraseña" />
    </div>
    <div class="login-form--button">
      <button type="submit">Ingresar</button>
    </div>
    <div class="login-form--forgot-pass">
      <a href="#">Olvidé mi contraseña</a>
    </div>
    <div class="login-form--notes">
      <p>Todos los derechos reservados COCO TECNOLOGÍAS S.A.S</p>
    </div>
    <!-- <img class="login-form--img" src="https://www.cocoreservas.com/public/img/login/coco_bg.svg" /> -->
  </div>
</template>

<script>
export default {
  name: "LoginForm"
};
</script>

<style lang="scss" scoped>
.login-form {
  color: $secondary-color;
  z-index: 100;
  h3 {
    text-align: center;
    font-size: 3vw;
  }
  &--input {
    margin-top: 60px;
    label {
      font-weight: 800;
    }
    input {
      margin: 8px 0;
      @include login-input;
    }
  }
  &--button {
    text-align: center;
    margin-top: 40px;
    button {
      @include primary-button;
    }
  }
  &--forgot-pass {
    margin-top: 20px;
    font-size: 14px;
    text-align: center;
    font-weight: 400;
    a {
      color: rgb(175, 175, 175);
    }
  }
  &--notes {
    position: fixed;
    bottom: 0px;
    p {
      color: rgba(175, 175, 175, 0.4);
      font-size: 12px;
      font-weight: 200;
    }
  }
  &--img {
    position: absolute;
    bottom: 0px;
    right: 0;
    width: 39%;
    z-index: 0;
  }
}

.password {
  margin-top: 30px;
}

@media (max-width: 766px) {
  .login-form {
    h3 {
      font-size: 40px;
      margin-bottom: 50px;
      font-weight: 700;
    }
    &--img {
      width: 100%;
    }
    &--input {
      width: 100%;
      text-align: center;
      br {
        display: none;
      }
      label {
        display: block;
        width: 90%;
        margin: 0 auto;
        text-align: left !important;
      }
      input {
        width: 85%;
        margin: 8px auto;
      }
    }
    &--button {
      width: 100%;
      button {
        width: 42%;
        font-size: 22px;
      }
    }
    &--notes {
      width: 100%;
      p {
        text-align: center;
        font-size: 11px;
      }
    }
  }
}
</style>
