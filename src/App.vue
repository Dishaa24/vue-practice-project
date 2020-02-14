<template>
  <div id="app">
    <Header siteTitle="Samriddhi Engineering Works " />
        <div class="container-fluid">
            <router-view />
        </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  components: {
  Header 
  }
};
</script>



<style>
body {
  background:rgb(148, 142, 142);
}

.container {
  max-width: 900px;
  
}

.card {
  background:rgb(71, 64, 64); 
}

.card-body {
  color: rgb(166, 245, 21);
}

.card-body a {
  color: rgb(165, 160, 214);
  
}

</style>
