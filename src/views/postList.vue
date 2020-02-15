<template>
    <div class="post-list">
        <div class="card mb-3" v-for="post of posts" :key="post.id">
            <div class="card-body">
                <h3><router-link :to="`post-details/${post.id}`">{{post.title}}</router-link></h3>
                <p>{{post.body}}</p>
            </div>
        </div>
        <div class="card mb-3" v-if="errors && errors.length">
            <div class="card-body">
                <p>v-for="(error,index) of errors" :key="index">{{errors.message}}</p>
            </div>
        </div>

    </div>
</template>

<script>
export default {
   name:"postList", 
   props:["posts"],
   data: function() {
       return {
           errors: {}
       }
   }
};
</script>

<style>

</style>