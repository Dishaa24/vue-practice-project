<template>
    <div class="post-details">
        <div class="card mb-3">
            <div class="card-body">
                <h3>{{post.title}}</h3>
                <p> {{post.body}}</p>
            </div>
        </div>
    </div>
</template>

<script>

import axios from "axios"; 

export default {
   name:"postDetails", 
   data(){
       return {
           id: this.$route.params.id,
           post:[],
           
       }
   },
     created(){
    axios.get(`https://jsonplaceholder.typicode.com/posts/${this.id}`)
    .then(res => {
      this.post = res.data;
    })
    .catch(e => {this.errors.push(e)});
  },

}


</script>

<style>

</style>