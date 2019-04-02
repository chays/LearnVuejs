<template>
  <div class="column nav-home">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand" >     
        <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample" v-bind:class="{'is-active':isActive}" @click='isActiveToggle'>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div id="navbarBasicExample" class="navbar-menu" v-bind:class="{'is-active':isActive}">
        <div class="navbar-start">
          <router-link class="navbar-item" to="/" active-class="is-active" exact  @click.native="navItemsClick('/')">
            Home
          </router-link>
          <router-link class="navbar-item" to="/about" active-class="is-active" exact  @click.native="navItemsClick('/about')">
            About
          </router-link>   
          <router-link class="navbar-item" to="/projects" active-class="is-active" exact  @click.native="navItemsClick('/projects')">
            Projects
          </router-link>
          <router-link class="navbar-item" to="/blog" active-class="is-active" exact  @click.native="navItemsClick('/blog')">
            Blog
          </router-link>
        </div>      
      </div>
      <div class="navbar-end" v-show="isActive2">로1고</div>
    </nav>
  </div>
</template>

<script>
export default {
  data:() => {
    return{
      isActive: false,
      isActive2: false,
    }
  },

  beforeCreate:function(){
    console.log("beforeCreate");
  },
  created:function(){
    console.log('create');
    // document.addEventListener('DOMContentLoaded', () => {

    //   // Get all "navbar-burger" elements
    //   const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

    //   // Check if there are any navbar burgers
    //   if ($navbarBurgers.length > 0) {

    //     // Add a click event on each of them
    //     $navbarBurgers.forEach( el => {
    //       el.addEventListener('click', () => {

    //         // Get the target from the "data-target" attribute
    //         const target = el.dataset.target;
    //         const $target = document.getElementById(target);

    //         // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
    //         el.classList.toggle('is-active');
    //         $target.classList.toggle('is-active');
    //       });
    //     });
    //   }

    // });
  },
  methods:{
    isActiveToggle(){
      this.isActive=!this.isActive;  
    },

    navItemsClick(path){
     if (path == '/') {
       this.isActive2 = false
     } else {
       this.isActive2 = true
     }
   }

    //navItemClick(){
      // console.log("ss")
      // const $navItems = document.querySelector('.navbar-menu');
      // const $navMenu = document.querySelector('.navbar-burger');
      // $navItems.classList.remove('is-active');
      // $navMenu.classList.remove('is-active');

      // const $navItems = document.querySelectorAll('.navbar-item');
      //let curr = this.$router.history.current.path;
      //console.log(curr, this.$router)
      // for(let res in this.$router.options.routes) {
      //   let obj = this.$router.options.routes[res]
      //   //  console.log(obj)
      //   if (obj.path == curr && curr === '/') {
      //     // $navItems[res].classList.add('is-active')  
      //     this.isActive = false
      //     console.log('ok', obj.path)
      //   } else {
      //     this.isActive = true
      //     console.log('no')
      //   }
      // }

      // if (curr == '/') {
      //   this.isActive = false
      //   console.log(curr)
      // } else {
      //   this.isActive = true
      // }

   // }

    // navItemsClick(){
    //   console.log("ss")
    //   const $navItems = document.querySelectorAll('.navbar-item');

    //   let curr = this.$router.history.current.path
      
    //   for(let res in this.$router.options.routes) {
    //     let obj = this.$router.options.routes[res]

    //     if (obj.path == curr) {
    //       $navItems[res].classList.add('is-active')
    //     } else {
    //       // 

    //     }
    //   }

    // }
  }
}
</script>
