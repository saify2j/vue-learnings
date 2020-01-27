<template>
    <div>
        <h3>{{ title }}</h3>
        <button @click="changeTitle"> Change Title</button>
    </div>
</template>
<script>
export default {
    name:'Blogs',
    data(){
        return {
            title: 'Dragonball Z'
        }
    },
    methods:{
        changeTitle(){
            this.title = 'Naruto'
        }
    },
    beforeCreate(){
        alert('hello before created')
    },
    created(){
        alert('hello after created')
    },
    beforeUpdate(){
        alert('before update')
    }
}
</script>
/* eslint-disable */ 