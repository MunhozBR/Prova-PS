<template>
  <b-navbar id="colornav" toggleable type="dark" variant="">
    <b-navbar-brand href="http://localhost:3000"><img class="camera" src="~/static/images/camera.png" alt=""> IstaPics</b-navbar-brand>

    <b-navbar-toggle target="navbar-toggle-collapse">
      <template #default="{  }">
        <a href="http://localhost:3000"><img class="user1" src="~/static/images/usericon.png" alt=""></a>
      </template>
    </b-navbar-toggle>

    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="http://localhost:3000">Login</b-nav-item>
        
        
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<style>
.user1{
  width: 1.5em; 
}
.camera{
  width: 2em;
}
#colornav{
  background: linear-gradient(90deg, rgba(125,0,69,1) 13%, rgba(122,45,84,1) 92%);
}
</style>

<script>
export default {}
</script>