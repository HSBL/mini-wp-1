<template>
  <aside class="col-md-4">
    <!-- Widget [Search Bar Widget]-->
    <div class="widget search">
      <header>
        <h3 class="h6">Search the blog</h3>
      </header>
      <form action="#" class="search-form" @submit.prevent="search">
        <div class="form-group">
          <input type="search" placeholder="What are you looking for?" v-model="searchString">
          <button type="submit" class="submit"><i class="fa fa-search"></i></button>
        </div>
      </form>
    </div>
    <!-- Widget [Latest Posts Widget]-->
    <div class="widget latest-posts">
      <header>
        <h3 class="h6">Latest Posts</h3>
      </header>
      <div class="blog-posts"><a href="#">
          <div class="item d-flex align-items-center">
            <div class="image"><img src="https://image.flaticon.com/icons/svg/1907/1907567.svg" alt="..." class="img-fluid"></div>
            <div class="title"><strong>Alberto Savoia Can Teach You About</strong>
              <div class="d-flex align-items-center">
                <div class="views"><i class="icon-eye"></i> 500</div>
                <div class="comments"><i class="icon-comment"></i>12</div>
              </div>
            </div>
          </div></a><a href="#">
          <div class="item d-flex align-items-center">
            <div class="image"><img src="https://image.flaticon.com/icons/svg/1907/1907567.svg" alt="..." class="img-fluid"></div>
            <div class="title"><strong>Alberto Savoia Can Teach You About</strong>
              <div class="d-flex align-items-center">
                <div class="views"><i class="icon-eye"></i> 500</div>
                <div class="comments"><i class="icon-comment"></i>12</div>
              </div>
            </div>
          </div></a><a href="#">
          <div class="item d-flex align-items-center">
            <div class="image"><img src="https://image.flaticon.com/icons/svg/1907/1907567.svg" alt="..." class="img-fluid"></div>
            <div class="title"><strong>Alberto Savoia Can Teach You About</strong>
              <div class="d-flex align-items-center">
                <div class="views"><i class="icon-eye"></i> 500</div>
                <div class="comments"><i class="icon-comment"></i>12</div>
              </div>
            </div>
          </div></a></div>
    </div>
    <!-- Widget [Categories Widget]-->
    <!-- <div class="widget categories">
      <header>
        <h3 class="h6">Categories</h3>
      </header>
      <div class="item d-flex justify-content-between"><a href="#">Growth</a><span>12</span></div>
      <div class="item d-flex justify-content-between"><a href="#">Local</a><span>25</span></div>
      <div class="item d-flex justify-content-between"><a href="#">Sales</a><span>8</span></div>
      <div class="item d-flex justify-content-between"><a href="#">Tips</a><span>17</span></div>
      <div class="item d-flex justify-content-between"><a href="#">Local</a><span>25</span></div>
    </div> -->
    <!-- Widget [Tags Cloud Widget]-->
    <div class="widget tags">
      <header>
        <h3 class="h6">Tags</h3>
      </header>
      <ul class="list-inline">
        <li class="list-inline-item"><a href="#" class="tag" @click="searchTag(tag)" v-for="(tag, i) in tags" :key="i">#{{tag}}</a></li>
      </ul>
    </div>
  </aside>
</template>

<script>
export default {
  name: 'SideBar',
  data() {
    return {
      searchString: '',
      tags: [
        "Bussiness",
        "Technology",
        "kocak",
        "car"
      ]
    }
  },
  methods: {
    search() {
      this.$emit('search', this.searchString)
    },
    searchTag(payload) {
      this.$emit('search-tag', payload)
    }
  }
}
</script>

<style>

</style>
