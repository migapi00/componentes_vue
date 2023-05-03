<template>
    <!-- <div>{{firstName }} {{ lastName }}</div> -->
    <div>{{ fullName }} </div>
</template>
  
<script>
import { ref, computed, toRefs } from "vue"

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

        return {
            fullName,
        };
    }
}
</script>