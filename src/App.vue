<template>
  <div id="app">
    <h1> {{username}} </h1>
    <small-user-profile v-for="(user , i) in users" :key="i" :user="users[i]">

    </small-user-profile>
  </div>
</template>

<script>
import SmallUserProfile from '@/components/SmallUserProfile.vue'

export default {
  methods: {
    handle_username: function(name){
this.username = name
    },
  },
  data(){
    return {
      username: undefined,
      users: [
        {
        name: `Frank`,
        age: 21,
        is_premium: false,
        id:1
      },
      {
        name: `jeff`,
        age: 28,
        is_premium: true,
        id:2
      }
      ]
    }
  },
  name: 'App',
  components: {
    SmallUserProfile,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
