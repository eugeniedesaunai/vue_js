<template>
  <div class="hello">
    <h1>{{ msg }} {{ name }}</h1>
  </div>
  <p v-if="age < 20"> down {{ age }} </p>
  <p v-else-if="age > 20 && age < 30"> middle {{ age }} </p>
  <p v-else> up {{ age }} </p>
  <hr>
  <ul>
    <li v-for="(friend, index) of friends" :key="index">
      {{ friend }}
    </li>
  </ul>
  <button v-on:click="mymethod">Click</button>
  <button v-on:click="mymethod">Clicjgccjk</button>
  <button v-on:click="mymethod">lcek</button>
</template>

<script>
export default {
  name: 'HelloWorld',
  // props est la variable choisi dans le parent app.vue
  data() {
    return {
      name: "Eugénie",
      age: 5,
      friends: ['riri', 'fifi', 'loulou']
    }
  },
  props: {
    msg: String
  },
  methods: {
    mymethod(event) {
      this.age = this.age + 1,
        console.log(event)
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
