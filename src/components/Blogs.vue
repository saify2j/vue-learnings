<template>
    <div>
        <h3>{{ title }}</h3>
        <div v-for="todo in todos" :key="todo.id">
            <h1>{{ todo.title }}</h1>
            <p>{{ todo.completed }}</p>
        </div>
        <button @click="say()"> Say</button>
        <div id="something">

        </div>
        <button @click="doSomething()">DO Something</button>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    name:'Blogs',
    data(){
        return {
            todos:[],
            title: 'TO DO LIST'
        }
    },
    methods:{
        say: function () {
            alert("hello")
        },
        doSomething: function(){
            let div = document.getElementById('something')
            div.innerHTML =`<p>I did Something</p>`
        }
    },
    
    created(){
        axios.get('https://jsonplaceholder.typicode.com/todos/').then(response=>{
            this.todos= response.data
        })
    },

}
</script>
/* eslint-disable */ 