<template>
  <div class="login-container">
    <form @submit.prevent="login" class="login-form">
      <h2>Iniciar Sesión</h2>
      <div class="form-group">
        <label for="username">Usuario:</label>
        <input type="text" id="username" v-model.trim="username" placeholder="Ingresa tu usuario" required>
      </div>
      <div class="form-group">
        <label for="password">Contraseña:</label>
        <input type="password" id="password" v-model.trim="password" placeholder="Ingresa tu contraseña" required>
      </div>
      <button type="submit">Iniciar Sesión</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    login() {
      // Aquí iría la lógica para enviar los datos de inicio de sesión al servidor
      // Por simplicidad, este ejemplo solo muestra los datos en la consola
      console.log("Usuario:", this.username);
      console.log("Contraseña:", this.password);
      // Después de enviar los datos, podrías redirigir al usuario a otra página, por ejemplo:
      // this.$router.push('/dashboard');
    }
  }
};
</script>

<style scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin-top: -100px; /* Ajusta este valor según sea necesario */
}

.login-form {
  background: #f9f9f9;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

h2 {
  margin-top: 0;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  border-radius: 4px;
  border: 1px solid #ccc;
}

button {
  width: 100%;
  padding: 10px;
  border: none;
  border-radius: 4px;
  background-color: #007bff;
  color: #fff;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>
