<template lang="pug">
#app
  .container
    img(
      src="https://static.platzi.com/media/user_upload/Page%201-d8d869f4-7130-4ae9-9907-2fa809bd136a.jpg"
    )
    h1 Registro estación Platzi
    form
      label Nombre
      input#nombre(name="nombre", value="Eric")

      label Apellido
      input#usuario(name="usuario", value="Gomez")

      label Cargo
      input#cargo(name="cargo", value="Sistemas")

      .caja_button
        button.btn-action(type="submit") ENVIAR
</template>

<script>
export default {
  name: 'Reto1',
  components: {}
}
</script>

<style lang="scss">
  :root {
  /* --color_primary: #A3ECF3; */
    --color_primary: #00BFD6;
    --color_secondary: #FF9300;
    --color_text: #212121;
  }

  #app {
    font-family: Roboto;
    width:100%;
    display: flex;
    justify-content: center;
    font-size: 16px;
  }

  .container{
    width: 320px;
    height: 409px;
    padding: 16px;
  }

  h1{
    color: var(--color_primary);
  }

  label{
    color: var(--color_secondary);
  }

  label, input{
    display: block;
    width: 100%;
    font-weight: 500;
  }

  input{
      border: 0px;
      border-bottom: 1px solid var(--color_secondary);
      color: var(--color_text);
      margin-bottom: 16px;
      font-size: 24px;
  }

  button{
    background-color: var(--color_primary);
    color: #FFF;
    padding: 8px;
    width: 150px;
    border-radius: 4px;
  }

  .caja_button{
    display: flex;
    justify-content: flex-end;
    margin-bottom:16px;
  }

</style>
