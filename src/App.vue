<template>
  <div class="app">
    I am {{name}}.
    I am {{age}} Years old.
    <button @click="changeName('kyaw kyaw')">
      Change Name
    </button> 
    <button @click="changeAge(45)">
      Change Name
    </button> 
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  components: {

  },
  data(){
    return{
      name: 'Thuta',
      age: 21 as number | string
    }
  },
  methods: {
    changeName(name: string){
      this.name = name;
    },
    changeAge(age: number){
      this.age = age;
    }
  }
});
</script>

<style>

</style>
