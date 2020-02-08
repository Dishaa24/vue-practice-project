<template>
      
      <nav id="nav" class="navbar navbar-expand-lg bg-dark mb-3">
         <div class="container-fluid">
            <router-link to="/" class="navbar-brand">{{siteTitle}}</router-link> 
              <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ml-auto">
                  <li class="nav-item active">
                    <router-link to="/" class="nav-link">Home</router-link> 
                  </li>
                  <li class="nav-item">
                      <router-link to="/about" class="nav-link">About</router-link>
                  </li>
                </ul>
             </div> 
          </div> 
        </nav>

</template>

<script>

export default {
  name: 'Header',
  props:{
    siteTitle: String
  },
  }

  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.navbar {
  background: yellow;
}

.navbar-nav a{
  color:white;
  padding: 0 15px;
  display: block;
}
</style>
 