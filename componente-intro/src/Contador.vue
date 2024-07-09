<template>
    <div class="contador">
        <span>{{ contador }}</span>
        <button @click="adicionar">+</button>
        <button @click="subtrair">-</button>
    </div>
</template>

<script>
import { ref } from 'vue';

export default {
    name: 'ContadorComponent',
    setup() {
        const contador = ref(0);

        const adicionar = () => {
            contador.value++;
        };

        const subtrair = () => {
            contador.value--;
        };

        return {
            contador,
            adicionar,
            subtrair
        };
    }
};
</script>

<style>
.contador span {
    border-bottom: 1px solid #ccc;
    height: 30px;
    padding: 5px 25px;
}

.contador button {
    height: 30px;
    width: 30px;
    border-radius: 15px;
    background-color: coral;
    color: #fff;
    margin-left: 10px;
    outline: none;
}
</style>
