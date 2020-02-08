<template>
    <div class="post-list">
        <div class="card" v-for="post of posts" :key="post.id">
            <div class="card-body">
                <h3>{{post.title}}</h3>
                <p>{{post.body}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
   name:"postList", 
   props:["posts"],
};
</script>

<style>

</style>