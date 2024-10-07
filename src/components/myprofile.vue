<template>
  <div class="relative flex flex-col items-center justify-center min-h-screen bg-gray-100">
    
    <!-- Background image -->
    <div class="absolute top-0 left-0 w-full h-1/2 bg-cover bg-center" :style="{ backgroundImage: `url(${backgroundImage})` }" data-aos="fade-down">
    </div>

    <!-- Profile image -->
    <div class="relative mt-32 z-10" data-aos="zoom-in">
      <div class="w-40 h-40 rounded-full overflow-hidden mb-4 border-4 border-black shadow-lg transform hover:scale-105 transition-transform duration-500 hover:shadow-2xl">
        <img src="@/assets/profile.jpg" alt="Your Profile Picture" class="w-full h-full object-cover"/>
      </div>
    </div>

    <div data-aos="fade-up" class="text-center">
      <h1 class="text-4xl font-bold mb-2 hover:text-blue-500 transition-colors duration-500 ">
        Steven Bruce Asis
      </h1>
      <h2 class="text-1xl font-bold mb-2 hover:text-blue-500 transition-colors duration-500 ">
        Aspiring Data Analyst
      </h2>
      <p class="text-lg text-gray-600 mb-2 hover:text-blue-500 transition-colors duration-500 ">
        Age: 22
      </p>
      <p class="text-lg text-gray-600 mb-2 hover:text-blue-500 transition-colors duration-500 ">
        Email: bruceasis0@gmail.com
      </p>
      <p class="text-lg text-gray-600 mb-2 hover:text-blue-500 transition-colors duration-500 ">
        Motorola St. Doña Nicasia Puyat Subdivision, Brgy. Commonwealth, Quezon City
      </p>
    </div>

    <!-- Social Media -->
    <div class="flex space-x-6 mt-4 justify-center" data-aos="fade-up">
      <!-- LinkedIn -->
      <a href="https://www.linkedin.com/in/steven-asis/" target="_blank" class="hover:scale-110 transform transition-transform duration-300 hover:shadow-xl">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-500 hover:text-blue-700 transition-colors" viewBox="0 0 24 24" fill="currentColor">
          <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.761 0 5-2.239 5-5v-14c0-2.761-2.239-5-5-5zm-11 19h-3v-10h3v10zm-1.5-11.5c-.966 0-1.5-.621-1.5-1.5 0-.879.534-1.5 1.5-1.5s1.5 .621 1.5 1.5c0 .879-.534 1.5-1.5 1.5zm13.5 11.5h-3v-5.5c0-1.379-.621-2.5-2-2.5s-2 1.121-2 2.5v5.5h-3v-10h3v1.379c.695-1.103 1.812-1.379 3-1.379 2.283 0 4 1.744 4 4.5v5.5z"/>
        </svg>
      </a>

      <!-- GitHub -->
      <a href="https://github.com/tebenbrus" target="_blank" class="hover:scale-110 transform transition-transform duration-300 hover:shadow-xl">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-gray-700 hover:text-gray-900 transition-colors" viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.387.6.113.82-.258.82-.577v-2.26c-3.338.725-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.757-1.333-1.757-1.09-.745.083-.729.083-.729 1.205.085 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.107-.776.418-1.305.76-1.604-2.665-.307-5.466-1.332-5.466-5.93 0-1.31.469-2.38 1.236-3.22-.124-.306-.536-1.54.117-3.213 0 0 1.008-.322 3.301 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.293-1.552 3.3-1.23 3.3-1.23.653 1.674.241 2.907.118 3.213.768.84 1.235 1.91 1.235 3.22 0 4.61-2.803 5.62-5.475 5.922.43.372.81 1.102.81 2.222v3.293c0 .322.217.694.825.577 4.765-1.588 8.2-6.084 8.2-11.387 0-6.627-5.373-12-12-12z"/>
        </svg>
      </a>

      <!-- Facebook -->
      <a href="https://www.facebook.com/tebenbrus" target="_blank" class="hover:scale-110 transform transition-transform duration-300 hover:shadow-xl">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-600 hover:text-blue-800 transition-colors" viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 2.04c-5.523 0-10 4.478-10 10 0 4.992 3.657 9.128 8.438 9.878v-6.99h-2.54v-2.888h2.54v-2.19c0-2.507 1.493-3.89 3.777-3.89 1.095 0 2.24.195 2.24.195v2.465h-1.263c-1.244 0-1.63.771-1.63 1.562v1.858h2.773l-.443 2.888h-2.33v6.99c4.78-.75 8.437-4.886 8.437-9.878 0-5.522-4.477-10-10-10z"/>
        </svg>
      </a>

      <!-- Phone Call -->
      <a href="tel:+639456104330" class="hover:scale-110 transform transition-transform duration-300 hover:shadow-xl">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-gray-500 hover:text-gray-700 transition-colors" viewBox="0 0 24 24" fill="currentColor">
          <path d="M17.707 12.293l-4-4a.999.999 0 0 0-1.414 0l-1 1a.999.999 0 0 0 0 1.414l1 1 4-4a.999.999 0 0 0 0-1.414zM3 19.293a2.001 2.001 0 0 1-1.707-2.707 3.978 3.978 0 0 1 1.127-1.707c.659-.659 1.414-.823 2.293-.707.293.035.647.065 1.012.248.537.263.874.76 1.707 1.593.483.483 1.087.708 1.779 1.14.293.172.593.33.939.398 1.06.21 2.38-.008 3.947-1.54s1.717-2.884 1.54-3.947c-.068-.346-.226-.646-.398-.939-.432-.692-.657-1.296-1.14-1.779-.833-.833-1.33-1.17-1.593-1.707-.183-.365-.213-.719-.248-1.012-.116-.879.048-1.634.707-2.293a3.978 3.978 0 0 1 1.707-1.127 2.001 2.001 0 0 1 2.707 1.707 15.054 15.054 0 0 1-.707 7.293 18.015 18.015 0 0 1-5.707 5.707 15.054 15.054 0 0 1-7.293.707z"/>
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
import backgroundImage from '@/assets/background.png';

export default {
  name: "ProfileView",
  data() {
    return {
      backgroundImage
    };
  }
};
</script>
