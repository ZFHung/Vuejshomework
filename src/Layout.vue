<template>
  <nav>
    <ul class="menu menu-horizontal bg-base-200 rounded-box">
      <li>
        <router-link to="/" class="btn btn-info">Home</router-link>
      </li>
      <li>
        <router-link to="/about" class="btn btn-active btn-accent">About me</router-link>
      </li>
      <li>
        <router-link to="/privacy" class="btn btn-active btn-primary"
          >Privacy</router-link
        >
      </li>
    </ul>
  </nav>
  <main>
    <router-view></router-view>
  </main>
</template>
