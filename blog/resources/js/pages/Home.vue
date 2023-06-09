<template>
    <div>
          <h2 class="header-title">Latest Blog Posts</h2>
            <section class="cards-blog latest-blog">
              <div class="card-blog-content">
                <img src="images/pic1.jpg" alt="" />
                <p>
                  2 hours ago
                  <span style="float: right">Written By </span>
                </p>
                <h4 style="font-weight: bolder">
                   <router-link :to="{ name: 'BlogPage', params: { slug: 'Benefits-of-Getting-Covid-19-Vaccination' } }">Benefits of Getting Covid 19 Vaccination</router-link>
                </h4>
              </div>

              <div class="card-blog-content">
                <img src="images/pic2.jpg" alt="" />
                <p>
                  23 hours ago
                  <span style="float: right">Written By </span>
                </p>
                <h4 style="font-weight: bolder">
               <router-link :to="{ name: 'BlogPage', params: { slug: 'Top-10-Music-Stories-Never-Told' } }">Top 10 Music Stories Never Told</router-link>
                    
                </h4>
              </div>

              <div class="card-blog-content">
                <img src="images/pic3.jpg" alt="" />
                <p>
                  2 days ago
                  <span style="float: right">Written By </span>
                </p>
                <h4 style="font-weight: bolder">
                    <router-link :to="{ name: 'BlogPage', params: { slug: 'WRC-Safari-Rally-Back-To-Kenya-After-19 Years' } }">WRC Safari Rally Back To Kenya After 19 Years</router-link>
                    
                </h4>
              </div>

              <div class="card-blog-content">
                <img src="images/pic4.jpg" alt="" />
                <p>
                  3 days ago
                  <span style="float: right">Written By </span>
                </p>
                <h4 style="font-weight: bolder">
                <router-link :to="{name:'BlogPage', params:{slug:'Premier-League-2021/2022-Fixtures'}}">Premier League 2021/2022 Fixtures</router-link>
                </h4>
              </div>
            </section>
    </div>
</template>