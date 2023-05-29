<script setup>

    import { ref } from 'vue'

    let Numero = ref()
    let Vector = ref([])
    Vector.value.length = 10

    const Calcular = function () {

    if(Numero.value < 0) {
        Numero.value*=-1;
    }

    if (Numero.value <= 100 && Numero.value != 0) {
        for (let i = 0; i < 10; i++) {
        Vector.value[i] = Numero.value * (i + 1)
        }
    }
    }
</script>

<template>
  <table>
    <tr>
      <td>{{ Numero }}x1 =</td>
      <td>{{ Vector[0] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x2 =</td>
      <td>{{ Vector[1] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x3 =</td>
      <td>{{ Vector[2] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x4 =</td>
      <td>{{ Vector[3] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x5 =</td>
      <td>{{ Vector[4] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x6 =</td>
      <td>{{ Vector[5] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x7 =</td>
      <td>{{ Vector[6] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x8 =</td>
      <td>{{ Vector[7] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x9 =</td>
      <td>{{ Vector[8] }}</td>
    </tr>
    <tr>
      <td>{{ Numero }}x10 =</td>
      <td>{{ Vector[9] }}</td>
    </tr>
  </table>

  <h1 v-show="Numero == 0">Nada, numero 0</h1>
  <h1 v-show="Numero > 100">Nada, numero muy grande</h1>

  <input type="text" v-model="Numero" />
  <button @click="Calcular">Click</button>
</template>

<style scoped></style>
