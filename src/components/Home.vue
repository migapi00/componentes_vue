<template>
    <!-- <div>{{firstName }} {{ lastName }}</div> -->
    <div>{{ fullName }} </div>
    <div>{{ username }} </div>
    <button ref="btn">Click!</button>

</template>
  
<script>
import { ref, computed, toRefs, inject, watch } from "vue"

export default {
    props: {
    firstName: String, 
    lastName: String,
},

    setup(props) {

        const btn = ref(null);
        console.log(btn.value);

        watch (btn, (value) => {
            console.log(value);
        });
        
        const { firstName, lastName} = toRefs(props);

        const fullName = computed(
            () => {
                return `${firstName.value} ${lastName.value}`;
            });
        
        const username = inject("username");

        return {
            fullName,
            username,
            btn
        };
    }
}
</script>