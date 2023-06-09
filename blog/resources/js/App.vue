<template>
   <div id="wrapper">
          <!-- header -->
          <header class="header">
            <div class="header-text">
              <h1>The BlogHive</h1>
              <h4>Home of verified news...</h4>
            </div>
            <div class="overlay"></div>
          </header>

          <!-- sidebar -->
          <div class="sidebar">
            <span class="closeButton">&times;</span>
            <p class="brand-title"><a href="">BlogHive</a></p>

            <div class="side-links">
              <ul>
                <li><a class="active" href="index.html">Home</a></li>
                <li><a href="blog.html">Blog</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
              </ul>
            </div>

            <!-- sidebar footer -->
            <footer class="sidebar-footer">
              <div>
                <a href=""><i class="fab fa-facebook-f"></i></a>
                <a href=""><i class="fab fa-instagram"></i></a>
                <a href=""><i class="fab fa-twitter"></i></a>
              </div>

              <small>2024 Natasha Blog</small>
            </footer>
          </div>
          <!-- Menu Button -->
          <div class="menuButton">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
          </div>
          <!-- main -->
          <main class="container">
            <!-- CHANGES WITH PAGE -->
            <!-- router view checks if the route entered by user exist in the router js -->
            <router-view></router-view>
          </main>

          <!-- Main footer -->
          <footer class="main-footer">
            <div>
              <a href=""><i class="fab fa-facebook-f"></i></a>
              <a href=""><i class="fab fa-instagram"></i></a>
              <a href=""><i class="fab fa-twitter"></i></a>
            </div>
            <small> 2024 Natasha</small>
          </footer>
        </div>

</template>