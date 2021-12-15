<template>
    <ul>
        <li><button>Poor</button></li>
        <li><button>Average</button></li>
        <li><button>Great</button></li>
    </ul>
</template>


<style scoped>
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