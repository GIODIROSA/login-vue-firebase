<template>
  <div>
    <button @click="logOut">LoginOut</button>

  </div>
</template>

<script>
import firebase from 'firebase'
export default {
  data() {
    return {
    }
  },
  methods: {
    logOut() {
      firebase.auth().signOut()
      .then(() => alert('Usuario deslogueados'))
    }
  },
  created(){
console.log(firebase.auth().currentUser)
  }

}
</script>

<style>

</style>