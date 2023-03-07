<template>
    <div>
        <h1>My Component</h1>
        <button @click="getData">Get Data</button>
    </div>
</template>


<script>
import axios from 'axios';

export default {
    name: 'MyComponent',
    methods: {
        getData() {
            axios.get('https://jsonplaceholder.typicode.com/todos/1')
                .then(response => {
                    console.log(response.data);
                })
                .catch(error => {
                    console.log(error);
                });
        }
    }
}
</script>