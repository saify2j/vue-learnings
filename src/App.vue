<template>
  <div id="app">
     <Home/>
     <AllFriends :friends="friends" @delete="deleteFriend"/>
     <OnlineFriends :friends="friends"/>

  </div>
</template>

<script>
import Home from './components/Home'
import AllFriends from './components/AllFriends'
import OnlineFriends from './components/OnlineFriends'
export default {
  name: 'App',
  components: {
    Home,
    AllFriends,
    OnlineFriends
  },
  data(){
    return{
        friends: [
            { name:'saif', online: true},
            { name:'asif', online: true},
            { name:'rafi', online: false},
            { name:'rizvi', online: true},
            { name:'drew', online: false},
            
        ]
    }
  },
  methods:{
    deleteFriend(payload){
      this.friends = this.friends.filter(friend =>{
        return friend.name !==payload.name
      }

      )
      console.log(payload)
    }
  }
}
</script>