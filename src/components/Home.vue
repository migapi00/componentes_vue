<template>
    <!-- <div>{{firstName }} {{ lastName }}</div> -->
    <div>{{ fullName }} </div>
</template>
  
<script>
import { ref, computed } from "vue"

export default {
    setup() {
        const firstName = ref("Luis");
        const lastName = ref("Garcia");

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