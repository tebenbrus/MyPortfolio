<template>
    <div class="bg-gray-200 min-h-screen p-6">
      <NavBar /> <!-- Navbar remains at the top -->
  
      <div class="container mx-auto mt-8 bg-white p-6 rounded shadow-md">
        <!-- Tabs -->
        <div class="flex space-x-4 mb-6">
          <button
            class="px-4 py-2 rounded-md text-white"
            :class="{
              'bg-blue-600': activeTab === 'home',
              'bg-gray-400': activeTab !== 'home',
            }"
            @click="activeTab = 'home'"
          >
            Home
          </button>
          <button
            class="px-4 py-2 rounded-md text-white"
            :class="{
              'bg-blue-600': activeTab === 'about',
              'bg-gray-400': activeTab !== 'about',
            }"
            @click="activeTab = 'about'"
          >
            About Me
          </button>
          <button
            class="px-4 py-2 rounded-md text-white"
            :class="{
              'bg-blue-600': activeTab === 'resume',
              'bg-gray-400': activeTab !== 'resume',
            }"
            @click="activeTab = 'resume'"
          >
            Certificates/Resume
          </button>
        </div>
  
        <!-- Home Page Section -->
        <div v-if="activeTab === 'home'">
          <h2 class="text-2xl font-bold mb-4">Edit Home Page</h2>
          <div class="mb-4">
            <label class="block font-semibold">Profile Picture</label>
            <input
              v-model="homePage.profilePicture"
              type="text"
              placeholder="Image URL"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Name</label>
            <input
              v-model="homePage.name"
              type="text"
              placeholder="Full Name"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Profession</label>
            <input
              v-model="homePage.profession"
              type="text"
              placeholder="Profession"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Age</label>
            <input
              v-model="homePage.age"
              type="text"
              placeholder="Age"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Email</label>
            <input
              v-model="homePage.email"
              type="email"
              placeholder="Email"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Address</label>
            <input
              v-model="homePage.address"
              type="text"
              placeholder="Address"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">LinkedIn</label>
            <input
              v-model="homePage.linkedIn"
              type="text"
              placeholder="LinkedIn Profile"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">GitHub</label>
            <input
              v-model="homePage.github"
              type="text"
              placeholder="GitHub Profile"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Facebook</label>
            <input
              v-model="homePage.facebook"
              type="text"
              placeholder="Facebook Profile"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Phone Number</label>
            <input
              v-model="homePage.phoneNumber"
              type="text"
              placeholder="Phone Number"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <button class="px-4 py-2 bg-blue-600 text-white rounded" @click="saveHome">
            Save Changes
          </button>
        </div>
  
        <!-- About Me Section -->
        <div v-if="activeTab === 'about'">
          <h2 class="text-2xl font-bold mb-4">Edit About Me</h2>
          <div class="mb-4">
            <label class="block font-semibold">Profile Picture</label>
            <input
              v-model="aboutPage.profilePicture"
              type="text"
              placeholder="Image URL"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
          <div class="mb-4">
            <label class="block font-semibold">Description</label>
            <textarea
              v-model="aboutPage.description"
              placeholder="About Me Description"
              class="w-full p-2 border border-gray-300 rounded"
            ></textarea>
          </div>
  
          <!-- Skills Table -->
          <h3 class="text-xl font-bold mt-4 mb-2">Skills</h3>
          <table class="w-full border">
            <thead>
              <tr>
                <th class="border p-2 text-left">Skill</th>
                <th class="border p-2 text-left">Percentage</th>
                <th class="border p-2">Actions</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(skill, index) in aboutPage.skills" :key="index">
                <td class="border p-2">
                  <input v-model="skill.name" type="text" class="w-full p-2 border rounded" />
                </td>
                <td class="border p-2">
                  <input v-model="skill.percentage" type="text" class="w-full p-2 border rounded" />
                </td>
                <td class="border p-2 text-center">
                  <button @click="removeSkill(index)" class="text-red-500">Delete</button>
                </td>
              </tr>
            </tbody>
          </table>
          <div class="mt-4">
            <button @click="addSkill" class="px-4 py-2 bg-green-600 text-white rounded">
              Add Skill
            </button>
          </div>
          <button class="px-4 py-2 bg-blue-600 text-white rounded mt-4" @click="saveAbout">
            Save Changes
          </button>
        </div>
  
        <!-- Certificates/Resume Section -->
        <div v-if="activeTab === 'resume'">
          <h2 class="text-2xl font-bold mb-4">Edit Certificates/Resume</h2>
  
          <!-- Certificates Table -->
          <h3 class="text-xl font-bold mt-4 mb-2">Certificates</h3>
          <table class="w-full border">
            <thead>
              <tr>
                <th class="border p-2 text-left">Certificate URL</th>
                <th class="border p-2">Actions</th>
              </tr>
            </thead>
            <tbody>
                <tr v-for="(certificate, index) in resumePage.certificates" :key="index">
                    <td class="border p-2">
                    <input
                    v-model="resumePage.certificates[index]"
                    type="text"
                    placeholder="Certificate URL"
                    class="w-full p-2 border rounded"
                    />
                </td>
                <td>
                    <button @click="removeCertificate(index)" class="text-red-500">Delete</button>
                </td>
                </tr>
            </tbody>
          </table>
          <div class="mt-4">
            <button @click="addCertificate" class="px-4 py-2 bg-green-600 text-white rounded">
              Add Certificate
            </button>
          </div>
  
          <!-- Resume -->
          <div class="mt-4">
            <label class="block font-semibold">Resume URL</label>
            <input
              v-model="resumePage.resumeURL"
              type="text"
              placeholder="Resume URL"
              class="w-full p-2 border border-gray-300 rounded"
            />
          </div>
  
          <button class="px-4 py-2 bg-blue-600 text-white rounded mt-4" @click="saveResume">
            Save Changes
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeTab: "home",
        homePage: {
          profilePicture: "https://example.com/profile.jpg",
          name: "Steven Bruce Asis",
          profession: "Aspiring Data Analyst",
          age: 22,
          email: "bruceasis0@gmail.com",
          address: "Motorola St. Doña Nicasia Puyat Subdivision, Brgy. Commonwealth, Quezon City",
          linkedIn: "https://www.linkedin.com/in/steven-asis/",
          github: "https://github.com/tebenbrus",
          facebook: "https://www.facebook.com/tebenbrus",
          phoneNumber: "+639456104330",
        },
        aboutPage: {
          profilePicture: "https://example.com/profile.jpg",
          description: "I am a 4th-year Computer Science student...",
          skills: [
            { name: "JavaScript", percentage: 70 },
            { name: "VueJS", percentage: 60 },
          ],
        },
        resumePage: {
          certificates: [
            "https://example.com/cert1.jpg",
            "https://example.com/cert2.jpg",
          ],
          resumeURL: "https://example.com/resume.pdf",
        },
      };
    },
    methods: {
      // Home page methods
      saveHome() {
        alert("Home page information saved!");
      },
      // About page methods
      addSkill() {
        this.aboutPage.skills.push({ name: "", percentage: 0 });
      },
      removeSkill(index) {
        this.aboutPage.skills.splice(index, 1);
      },
      saveAbout() {
        alert("About Me information saved!");
      },
      // Certificates/Resume methods
      addCertificate() {
        this.resumePage.certificates.push("");
      },
      removeCertificate(index) {
        this.resumePage.certificates.splice(index, 1);
      },
      saveResume() {
        alert("Certificates/Resume information saved!");
      },
    },
  };
  </script>
  
