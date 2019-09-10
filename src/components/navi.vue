<template>
  <div>
    <nav class="nav">
      <div class="nav_logo">
        <h1>financal target</h1>
      </div>
      <div class="nav_plus">
        <h2>+</h2>
      </div>
    </nav>
      <div class="nav_generator"></div>
  </div>
</template>
<script>
</script>
<style>
.nav {
  height: 85px;
  width: 100%;
  background-color: white;
  border-bottom: 1px solid rgb(221, 221, 221);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 160px
}

.nav_generator {
  position: absolute;
  top: 0px;
  width: 0px;
  height: 100vh;
  width: 100vw;
  background-color: red;
  display: none;
}

@media (max-width: 1200px) {
  .nav {
    padding: 0 50px;
  }
}
</style>