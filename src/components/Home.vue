<template>
    <div>{{ obj }}</div>
    <!-- <div>{{ counter }}</div> -->
</template>
<script>
import { ref } from "vue"; //Valores
import { reactive, watch } from "vue"; // objetos
export default {
    setup() {
        // const counter = ref(0); //ref
        // setInterval(() => counter.value++, 500); //ref
        const obj = reactive({ counter: 0 });
        setInterval(() => obj.counter++, 500);
        watch(
            () => obj.counter,
            (valor, anterior) => {
                //reactive
                // watch(counter, (valor, anterior) => { //ref
                console.log(valor, anterior);
            }
        );

        return {
            obj,
        };
    },
};
</script>
