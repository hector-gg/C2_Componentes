<template>
    <div>{{ obj }}</div>
</template>
<script>
// import { ref } from "vue"; varibales
import { reactive } from "vue"; // objetos
export default {
    setup() {
        // const counter = ref(0);
        // setInterval(() => counter.value++, 500);
        const obj = reactive({ counter: 0 });
        setInterval(() => obj.counter++, 500);

        return {
            obj,
        };
    },
};
</script>
