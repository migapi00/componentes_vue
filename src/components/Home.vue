<!-- <template>
    <div>{{ obj }}</div>
</template>

<script>
// import { ref } from 'vue';
import { reactive, watch } from 'vue';

export default {
    setup() {
        // const counter = ref(0);
        const obj = reactive({counter:0});
        // setInterval(() => { counter.value++}, 500);

        setInterval(() => { obj.counter++ }, 500);

        watch(
            () => obj.counter,
            (valor, anterior) => {
                console.log(valor, anterior);
            }
        );

        return {
            obj,
        }
    },
}
</script>  -->

<template>
    <h1>{{ text }}</h1>
    <h2>{{ counter }}</h2>
  </template>
  
  <script>
  import { ref, watch } from "vue"
  
  export default {
    setup() {
      const text = ref('Hello World')
      const counter = ref(0)
  
      text.value = 'Hello Vue!'
  
      setInterval(() => {
        counter.value++
      }, 1500)
  
      watch(counter, (newValue, oldValue) => {
        console.log(`old: ${oldValue} - new: ${newValue}`)
      })
  
      return {
        text,
        counter,
      }
    }
  }
  </script>