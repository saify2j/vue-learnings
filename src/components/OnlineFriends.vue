<template>
    <div id="online-freinds">
        <h1>Online Currently</h1>
        <div v-for="(friend,index) in friends" :key="index">
            <div v-if="friend.online">
                <span>{{ friend.name }}</span>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'OnlineFriends',
    props: ['friends'],    
    data(){
        return {
            
        }   
    }
}
</script>