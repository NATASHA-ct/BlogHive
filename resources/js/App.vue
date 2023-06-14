<template>
   <div id="wrapper">
          <!-- header -->
          <main class="container">
            <router-view
            @update-sidebar="updateSidebar"
            @show-edit-success="showEditSuccess"
            :editSuccess="editSuccess"
            :key="$route.path"
          ></router-view>
          </main>
          <!-- sidebar -->
          <div class="sidebar" :class="{showOverlay: overlayVisibility}">
            <span class="closeButton" @click="hideOverlay" >&times;</span>
            <p class="brand-title"><a href="">BlogHive</a></p>

          <div class="side-links">
          <ul>
            <li>
              <router-link @click="hideOverlay" :to="{ name: 'Home' }"
                >Home</router-link
              >
            </li>
            <li>
              <router-link @click="hideOverlay" :to="{ name: 'Blogs' }"
                >Blogs</router-link
              >
            </li>
            <li>
              <router-link @click="hideOverlay" :to="{ name: 'About' }"
                >About</router-link
              >
            </li>
            <li>
              <router-link @click="hideOverlay" :to="{ name: 'Contact' }"
                >Contact</router-link
              >
            </li>
            <li v-if="!loggedIn">
              <router-link @click="hideOverlay" :to="{ name: 'Register' }"
                >Register</router-link
              >
            </li>
            <li v-if="!loggedIn">
              <router-link @click="hideOverlay" :to="{ name: 'Login' }"
                >Login</router-link
              >
            </li>
            <li v-if="loggedIn">
              <router-link @click="hideOverlay" :to="{ name: 'Dashboard' }"
                >Dashboard</router-link
              >
            </li>
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
  data() {
    return {
      overlayVisibility: false,
      loggedIn: false,
      editSuccess: false,
    };
  },
 methods: {
    ShowOverlay() {
      this.overlayVisibility = true;
    },
    hideOverlay() {
      this.overlayVisibility = false;
    },
    updateSidebar() {
      this.loggedIn = !this.loggedIn;
    },
    showEditSuccess() {
      this.editSuccess = true;
    },
  },
  mounted() {
    if (localStorage.getItem("authenticated")) {
      this.loggedIn = true;
    } else {
      this.loggedIn = false;
    }
  },
};
</script>

<style scoped>
.showOverlay{
  width: 100%;
  z-index: 9999;
}

</style>