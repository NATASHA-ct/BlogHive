<template>
   <div id="wrapper">
          <!-- header -->
          <header class="header">
            <div class="header-text">
              <h1>The BlogHive</h1>
              <h4>Home of Whispered Words:Dive into the Secrets of the Mind & Ignite your Imagination......!</h4>
            </div>
            <div class="overlay"></div>

             
          </header>
          <main class="container">
                    <!-- CHANGES WITH PAGE -->
                    <!-- router view checks if the route entered by user exist in the router js -->
                    <router-view></router-view>
          </main>
          <!-- sidebar -->
          <div class="sidebar" :class="{showOverlay: overlayVisibility}">
            <span class="closeButton" @click="hideOverlay" >&times;</span>
            <p class="brand-title"><a href="">BlogHive</a></p>

            <div class="side-links">
              <ul>
                <li><router-link :to="{ name: 'Home' }" @click="hideOverlay">Home</router-link></li>
                <li><router-link :to="{ name: 'Blogs' }" @click="hideOverlay">Blog</router-link></li>
                <li><router-link :to="{ name: 'About' }" @click="hideOverlay">About</router-link></li>
                <li><router-link :to="{ name: 'Contact' }" @click="hideOverlay">Contact</router-link></li>
                <li><router-link :to="{ name: 'Login' }" @click="hideOverlay">Login</router-link></li>
                <li><router-link :to="{ name: 'Register' }" @click="hideOverlay">Register</router-link></li>
              </ul>
            </div>

            <!-- sidebar footer -->
            <footer class="sidebar-footer">
              <div>
                <a href=""><i class="fab fa-facebook-f"></i></a>
                <a href=""><i class="fab fa-instagram"></i></a>
                <a href=""><i class="fab fa-twitter"></i></a>
              </div>

              <small>The BlogHive</small>
            </footer>
          </div>
          <!-- Menu Button -->
          <div class="menuButton" @click="showOverlay">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
          </div>
          <!-- main -->
         
          <!-- Main footer -->
          <footer class="main-footer">
            <div>
              <a href=""><i class="fab fa-facebook-f"></i></a>
              <a href=""><i class="fab fa-instagram"></i></a>
              <a href=""><i class="fab fa-twitter"></i></a>
            </div>
            <small> Created by @Natasha Tatenda Chirombe</small>
          </footer>
        </div>

</template>

<script>
export default {
  data(){
    return{
      overlayVisibility:true,
    }
  },
  methods:{
    showOverlay(){
      this.overlayVisibility = true;
    },
    hideOverlay(){
      this.overlayVisibility = false;
    }
  }
}
</script>

<style scoped>
.showOverlay{
  width: 100%;
  z-index: 9999;
}

</style>