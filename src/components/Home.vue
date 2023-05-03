<template>
    <div>{{ obj }}</div>
</template>

<script>
// import { ref } from 'vue';
import { reactive } from 'vue';

export default {
    setup() {
        // const counter = ref(0);
        const obj = reactive({counter:0});
        // setInterval(() => { counter.value++}, 500);

        setInterval(() => { obj.counter++ }, 500);

        return {
            obj,
        }
    },
}
</script> 