<template>
  <div class="container">
    <h2>Componente Dos</h2>
    <div class="row">
      <div class="col-md-5">
        <div class="card shadow-lg">
          <div class="card-body">
            <p class="h3">Hola <span class="fw-bold">{{ this.msg }}</span></p>
            <button class="btn btn-success m-1" @click="greet('Good Morning')">Good Morning</button>
            <button class="btn btn-warning m-1" @click="greet('Good Afternoon')">Good Afternoon</button>
            <button class="btn btn-danger m-1" @click="greet('Good Evening')">Good Evening</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ComponentDos',
  data: ()=>{
    return {
      msg : ''
    }
  },
  methods: {
    greet(value) {
      this.msg = value 
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
