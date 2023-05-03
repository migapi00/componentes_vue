<template>
    <!-- <div>{{firstName }} {{ lastName }}</div> -->
    <div>{{ fullName }} </div>
    <div>{{ username }} </div>

</template>
  
<script>
import { ref, computed, toRefs, inject } from "vue"

export default {
    props: {
    firstName: String, 
    lastName: String,
},

    setup(props) {
        
        const { firstName, lastName} = toRefs(props);

        const fullName = computed(
            () => {
                return `${firstName.value} ${lastName.value}`;
            });
        
        const username = inject("username");

        return {
            fullName,
            username
        };
    }
}
</script>