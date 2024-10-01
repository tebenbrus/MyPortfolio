<template>
  <nav class="bg-gray-800 p-4 shadow-md w-full fixed top-0 left-0 z-10">
    <div class="container mx-auto flex justify-between items-center">
      <router-link to="/myprofile" class="text-white font-bold text-xl">My Portfolio</router-link>
      <div>
        <ul class="flex space-x-6 text-white">
          <li>
            <router-link
              to="/myprofile"
              class="hover:text-gray-300 transition duration-200 pb-2"
              :class="{ 'border-b-2 border-blue-500': isActive('/myprofile') }"
            >
              Home
            </router-link>
          </li>
          <li>
            <router-link
              to="/about"
              class="hover:text-gray-300 transition duration-200 pb-2"
              :class="{ 'border-b-2 border-blue-500': isActive('/about') }"
            >
              About Me
            </router-link>
          </li>
          <li>
            <router-link
              to="/resume"
              class="hover:text-gray-300 transition duration-200 pb-2"
              :class="{ 'border-b-2 border-blue-500': isActive('/resume') }"
            >
              Certificate/Resume
            </router-link>
          </li>
          <li>
            <router-link
              to="/admin"
              class="hover:text-gray-300 transition duration-200 pb-2"
              :class="{ 'border-b-2 border-blue-500': isActive('/admin') }"
            >
              Admin
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  methods: {
    isActive(route) {
      return this.$route.path === route;
    }
  }
};
</script>
