<template>
    <ul>
        <li :class="{active: modelValue === 'poor'}"><button type="button" @click="activate('poor')">Poor</button></li>
        <li :class="{active: modelValue === 'average'}"><button type="button" @click="activate('average')">Average</button></li>
        <li :class="{active: modelValue === 'great'}"><button type="button" @click="activate('great')">Great</button></li>
    </ul>
</template>


<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue'],
    // data() {
    //     return {
    //         activeOption: this.modelValue
    //     };
    // },
    methods: {
        activate(option) {
            this.$emit('update:modelValue', option);
        }
    }
}
</script>


<style scoped>
.active {
    background-color: rgb(219, 90, 219);
}

.active button{
    color: white
}

ul {
    list-style: none;
    margin: .5rem 0;
    padding: 0;
    display: flex;
}

li {
    margin: 0 1rem;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

button {
    font: inherit;
    border: none;
    overflow: hidden;
    background-color: transparent;
    cursor: pointer;
}
</style>