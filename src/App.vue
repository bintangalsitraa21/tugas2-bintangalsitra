<template>
  <div id="app">
    <div class="background">
      <h1><strong style="color: yellow;">Selamat Datang di Aplikasi Input Data</strong></h1>
      <div>
        <label for="name"><strong style="color: yellow;">Nama:</strong></label>
        <input type="text" id="name" v-model="name" placeholder="Masukkan nama Anda" style="font-weight: bold; color: black;">
      </div>
      <div>
        <label for="email"><strong style="color: yellow;">Email:</strong></label>
        <input type="email" id="email" v-model="email" placeholder="Masukkan alamat email Anda" style="font-weight: bold; color: black;">
      </div>
      <button @click="submitData"><strong>Kirim</strong></button>
      <div v-if="submitted" class="result-container">
        <h2><strong>Data yang Dikirim:</strong></h2>
        <p><strong>Nama:</strong> {{ name }}</p>
        <p><strong>Email:</strong> {{ email }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      submitted: false
    };
  },
  methods: {
    submitData() {
      // Lakukan sesuatu dengan data yang dikirim
      console.log("<strong>Data yang dikirim:</strong>", this.name, this.email);
      // Set submitted menjadi true agar menampilkan data yang dikirim
      this.submitted = true;
    }
  }
}
</script>

<style scoped>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.background {
  background-color: #5080c7;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
}

input {
  margin-bottom: 10px;
}

.result-container {
  margin-top: 20px;
}
</style>
