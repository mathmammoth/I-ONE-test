<template>
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="p-10">
    <a class="text-4xl text-bold" href="#">Nuxt SSR</a>
    
    <div class="collapse navbar-collapse">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="pt-5">
            <nuxt-link exact no-prefetch active-class="active" class="nav-link" aria-current="page" to="/">
                Home
          </nuxt-link>
        </li>
        <li class="pt-5">
           <nuxt-link active-class="active" class="nav-link" aria-current="page" to="/users">
                Users
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>
