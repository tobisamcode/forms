<template>
    <ul>
        <li :class="{active: activeOption === 'poor'}"><button type="button" @click="activate('poor')">Poor</button></li>
        <li :class="{active: activeOption === 'average'}"><button type="button" @click="activate('average')">Average</button></li>
        <li :class="{active: activeOption === 'great'}"><button type="button" @click="activate('great')">Great</button></li>
    </ul>
</template>


<script>
export default {
    props: ['modalValue'],
    emits: ['update:modalValue'],
    data() {
        return {
            activeOption: this.modalValue
        };
    },
    methods: {
        activate(option) {
            this.activeOption = option;
            this.$emit('update:modalValue', option);
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