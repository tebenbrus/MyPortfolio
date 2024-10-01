<template>
  <div class="bg-gray-200 min-h-screen"> <!-- Gray background added here -->
    
    <!-- Navbar -->
    <NavBar /> <!-- Navbar remains at the top -->

    <!-- Container for Certificates and Resume -->
    <div class="container mx-auto p-6 mt-8"> <!-- Adjusted margin-top to remove extra white space -->
      
      <!-- Certificates Section -->
      <div class="mt-12">
        <h2 class="text-3xl font-bold text-center mb-8 hover:text-blue-500 transition-all duration-300 transform hover:scale-105 animate-fade-in-up">
          Certificates
        </h2>

        <!-- Certificate Star Layout -->
        <div class="grid grid-cols-2 gap-8 place-items-center mb-8 animate-fade-in-up"> <!-- First row with 2 certificates -->
          <img 
            src="@/assets/certificate0.jpg" 
            alt="Certificate 0" 
            class="w-full shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-2xl rounded-lg hover:rotate-3 hover:scale-110 transform hover:-translate-y-1 animate-fade-in"
            style="width: 400px; height: auto;" 
          />
          <img 
            src="@/assets/certificate1.jpg" 
            alt="Certificate 1" 
            class="w-full shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-2xl rounded-lg hover:rotate-3 hover:scale-110 transform hover:-translate-y-1 animate-fade-in"
            style="width: 400px; height: auto;"
          />
        </div>

        <div class="flex justify-center mb-8 animate-fade-in-up"> <!-- Middle row with 1 certificate -->
          <img 
            src="@/assets/certificate2.jpg" 
            alt="Certificate 2" 
            class="w-full shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-2xl rounded-lg hover:rotate-3 hover:scale-110 transform hover:-translate-y-1 animate-fade-in"
            style="width: 450px; height: auto;" 
          />
        </div>

        <div class="grid grid-cols-2 gap-8 place-items-center animate-fade-in-up"> <!-- Last row with 2 certificates -->
          <img 
            src="@/assets/certificate3.jpg" 
            alt="Certificate 3" 
            class="w-full shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-2xl rounded-lg hover:rotate-3 hover:scale-110 transform hover:-translate-y-1 animate-fade-in"
            style="width: 400px; height: auto;" 
          />
          <img 
            src="@/assets/certificate4.jpg" 
            alt="Certificate 4" 
            class="w-full shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-2xl rounded-lg hover:rotate-3 hover:scale-110 transform hover:-translate-y-1 animate-fade-in"
            style="width: 400px; height: auto;" 
          />
        </div>
      </div>

      <!-- Heading for Resume -->
      <h1 class="text-4xl font-bold mb-6 text-center hover:text-blue-500 transition-all duration-300 transform hover:scale-105 mt-12 animate-fade-in-up">
        My Resume
      </h1>

      <!-- Resume Section -->
      <div class="flex flex-col items-center justify-center">
        <!-- Resume Image -->
        <a href="https://drive.google.com/file/d/1U6Jqee-bP4hG8SEUuLOTe-N6DsrwHnOA/view" download="Steven_Asis_Resume.pdf">
          <img 
            src="@/assets/CV.jpg" 
            alt="Resume Image" 
            class="w-full max-w-4xl shadow-lg mb-4 transition-transform duration-300 hover:scale-105 hover:shadow-2xl rounded-lg hover:rotate-3 hover:scale-110 transform hover:-translate-y-1 animate-fade-in"
            style="width: 700px; height: auto;" 
          />
        </a>

        <!-- Download Button -->
        <a href="https://drive.google.com/uc?export=download&id=1qmLX6wVNKcytCMyfRm2ZOkZSnEl6X9hN" download="Steven_Asis_Resume.pdf" 
           class="mt-4 px-6 py-3 bg-blue-600 text-white font-semibold rounded-md hover:bg-blue-700 transition-transform duration-300 transform hover:scale-105 hover:shadow-lg animate-fade-in">
          Download Resume
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Resume",
};
</script>

<style>
@keyframes fade-in {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in {
  animation: fade-in 1s ease-in-out;
}

.animate-fade-in-up {
  animation: fade-in-up 1s ease-in-out;
}
</style>
