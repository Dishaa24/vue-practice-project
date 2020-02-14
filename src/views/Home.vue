<template>
  <div class="home">
    <AddPost />
    <postList v-bind:posts="posts"/>
  </div>
</template>

<script>
import axios from "axios";
import AddPost from "@/views/AddPost.vue";
import postList from "../views/postList.vue";

export default {
  name: 'home',
  components: {
    AddPost,
    postList
  },
  data(){
    return{
      posts:[],
      errors:[],
    }
  },
  created(){
    axios.get(`https://jsonplaceholder.typicode.com/posts?_limit=5`)
    .then(res => {
      this.posts = res.data
    })
    .catch(e => {this.errors.push(e)});
  }
} 
</script>
