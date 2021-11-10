<template>
  <a-row class="inputConteiner" >
    <input placeholder="Nombre" type="text" v-model="name" />
    <p>{{ name }}</p>
    <input placeholder="Apellido" type="text" v-model="lastName" />
    <p>{{ lastName }}</p>
    <input placeholder="imagen" type="text" v-model="img" @keyup.enter="addperson"/>
    <button @click="addperson">agregar</button>
    <li v-for="persona of personas" :key="persona">
      {{ persona.nombre }}-{{ persona.apellido }}
      <img v-bind="persona.imagen">
      <img :src="persona.imagen" height="150px">
    </li>
  </a-row>
</template>

<script>
export default {
  name: "InputStates",
  data() {
    return {
      name: "",
      lastName: "",
      img:"",
      personas: [
        {
          nombre: "",
          apellido: "",
          imagen: "",
        },
      ],
    };
  },
  methods: {
    addperson (){
        this.personas.push({
            nombre:this.name,apellido:this.lastName, imagen:this.img
        })
        this.name='',
        this.lastName='',
        this.img=''
    }
  },
};
</script>

<style>
.inputConteiner {
  margin-top: 50px;
}

</style>