<template>
  <div id="app">
    <Header siteTitle="shouvik" />
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
  background:black;
}

.container {
  max-width: 900px;
}

.card {
  background:rgb(71, 64, 64);
}

.card-body {
  color: white;
}

.card-body a {
  color: rgb(233, 232, 225);
}

</style>
