<template>
    <div :class="darkMode ? 'dark' : ''">
      <!-- Background Image -->
      <div class="relative bg-cover bg-center min-h-screen" :style="`background-image: url(${backgroundImage})`">
        <NavBar />
  
        <!-- About Me Section -->
        <section class="min-h-screen flex items-center justify-center text-center pt-25">
          <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col md:flex-row items-center md:items-start space-x-6" data-aos="fade-up">
            <!-- Image on the left with hover effect -->
            <div class="w-64 h-80 transform hover:scale-105 transition-transform duration-500">
              <img src="@/assets/image.jpg" alt="Profile Image" class="w-full h-full object-cover rounded-lg shadow-lg hover:shadow-2xl transition-shadow duration-500" />
            </div>
            <!-- Text content on the right -->
            <div class="text-left">
              <h2 class="text-4xl font-semibold mb-4 dark:text-white hover:text-blue-500 transition-colors duration-500">About Me</h2>
              <p class="text-lg max-w-lg dark:text-gray-300">
                I am currently a 4th Year college student pursuing a Bachelor of Science in Computer Science at New Era University. Throughout my academic journey, I have developed a strong foundation in programming, data analysis, and problem-solving. I identify myself as hard-working, responsible, and persistent in overcoming challenges and constantly pushing myself to improve. I am deeply passionate about using data to uncover insights and drive meaningful decisions. With a strong interest in data analytics, I aim to build a career as a Data Analyst where I can leverage my skills in data visualization, statistical analysis, and data manipulation to help organizations make informed decisions.
              </p>
            </div>
          </div>
        </section>
        
        <!-- Skills Section with animations and hover effects -->
        <section class="bg-white dark:bg-gray-800 py-12">
          <h3 class="text-3xl font-semibold text-center mb-8 dark:text-white hover:text-blue-500 transition-colors duration-500" data-aos="fade-in">Skills</h3>
          <div class="max-w-4xl mx-auto">
            
            <!-- Skill Bars with hover effects -->
            <div class="mb-6" data-aos="fade-right">
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700">Java</span>
                <span class="text-sm font-medium text-blue-700">85%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-blue-600 h-2.5 rounded-full hover:bg-blue-400 transition-colors duration-500" style="width: 85%;"></div>
              </div>
            </div>
            
            <div class="mb-6" data-aos="fade-right">
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-green-700">JavaScript</span>
                <span class="text-sm font-medium text-green-700">60%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-green-500 h-2.5 rounded-full hover:bg-green-400 transition-colors duration-500" style="width: 60%;"></div>
              </div>
            </div>
  
            <div class="mb-6" data-aos="fade-right">
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-purple-700">PHP</span>
                <span class="text-sm font-medium text-purple-700">60%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-purple-500 h-2.5 rounded-full hover:bg-purple-400 transition-colors duration-500" style="width: 60%;"></div>
              </div>
            </div>
  
            <div class="mb-6" data-aos="fade-right">
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-orange-700">SQL</span>
                <span class="text-sm font-medium text-orange-700">70%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-orange-500 h-2.5 rounded-full hover:bg-orange-400 transition-colors duration-500" style="width: 70%;"></div>
              </div>
            </div>
  
            <div class="mb-6" data-aos="fade-right">
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-500">VueJS</span>
                <span class="text-sm font-medium text-blue-500">60%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-blue-500 h-2.5 rounded-full hover:bg-blue-400 transition-colors duration-500" style="width: 60%;"></div>
              </div>
            </div>
  
          </div>
        </section>
      </div>
    </div>
  </template>
  
  <script>
  import backgroundImage from '../assets/background.jpg'; 
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  
  export default {
    data() {
      return {
        backgroundImage
      };
    },
    
    mounted() {
      AOS.init({
        duration: 1000, // Animation duration
        once: true, 
      });
    }
  };
  </script>
  