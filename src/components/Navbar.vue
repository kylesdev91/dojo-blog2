<template>
<header>
  <div id="nav">
    <h1>The Dojo Blog</h1>
     <router-link class="homepage" to="/">Home</router-link>
     <router-link class="createpage" to="/create">Create</router-link>
         </div>
  </header>
</template>

<script>
export default {

}
</script>

<style>
.homepage {
  margin-left: 1000px;
}
.createpage {
  margin-right: 100px;
}
</style>