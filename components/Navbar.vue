<template>
   <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand tag="h1" class="mb-0">Mon appli</b-navbar-brand>

    <b-navbar-nav class="ml-auto">
        <li class="nav-item">
            <nuxt-link to="/admin/login" class="nav-link">Login</nuxt-link>
        </li>
    </b-navbar-nav>

  </b-navbar>
</template>
<script>
export default {
  name : "NavBar"
}
</script>