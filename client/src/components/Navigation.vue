<template>
  <header class="header">
      <!-- Main Navbar-->
      <nav class="navbar navbar-expand-lg fixed-top">
        <div class="search-area">
          <div class="search-area-inner d-flex align-items-center justify-content-center">
            <div class="close-btn"><i class="icon-close"></i></div>
            <div class="row d-flex justify-content-center">
              <div class="col-md-8">
                <form action="#">
                  <div class="form-group">
                    <input type="search" name="search" id="search" placeholder="What are you looking for?">
                    <button type="submit" class="submit"><i class="icon-search-1"></i></button>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
        <div class="container">
          <!-- Navbar Brand -->
          <div class="navbar-header d-flex align-items-center justify-content-between">
            <!-- Navbar Brand --><a href="#" class="navbar-brand">Mini CMS</a>
            <!-- Toggle Button-->
            <button type="button" data-toggle="collapse" data-target="#navbarcollapse" aria-controls="navbarcollapse" aria-expanded="false" aria-label="Toggle navigation" class="navbar-toggler"><span></span><span></span><span></span></button>
          </div>
          <!-- Navbar Menu -->
          <div id="navbarcollapse" class="collapse navbar-collapse">
            <ul class="navbar-nav ml-auto">
              <li class="nav-item"><a href="#" class="nav-link" @click.prevent="hideDetail">Home</a>
              </li>
              <li class="nav-item"><a href="addpost" class="nav-link" @click.prevent="showAdd" v-show="logedIn">Add Post</a>
              </li>
              <li class="nav-item"><a href="#" class="nav-link" @click.prevent="logout" v-show="logedIn">Log Out</a>
              </li>
              <li class="nav-item"><a href="login" class="nav-link" @click.prevent="showLogin" v-show="!logedIn">Log in</a>
              </li>
            </ul>
            <div class="navbar-text"><a href="#" class="search-btn"><i class="fa fa-search"></i></a></div>
          </div>
        </div>
      </nav>
    </header>
</template>

<script>
export default {
  name: 'Navigation',
  props: {
    logedIn: Boolean
  },
  methods: {
    showLogin() {
      this.$emit('show-login')
    },
    logout() {
      this.$emit('logout')
    },
    hideDetail() {
      this.$emit('hide-detail')
    },
    showAdd() {
      this.$emit('show-add')
    }
  }
}
</script>

<style>
</style>
