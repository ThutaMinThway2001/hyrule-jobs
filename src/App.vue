<template>
  <div class="app">
    <h1>
      {{jobs[0].location}}
    </h1>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue';
import Job from './types/Job'

export default defineComponent({
  name: 'App',
  components: {
    
  },
  setup(){
    // const state = reactive({
    //   name: 'Thuta',
    //   age: 21 as number | string
    // });

    // state.name = 'Kyaw Kyaw';
    // state.age = 23;

    // return {...toRefs(state)}

    const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])

    return {jobs}
  },
  methods: {
    // changeName(name: string){
    //   this.name = name;
    // },
    // changeAge(age: number){
    //   this.age = age;
    // }
  }
});
</script>

<style>

</style>
