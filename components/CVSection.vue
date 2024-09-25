<template>
    <section class="container py-5">
      <div class="card shadow-lg p-4">
        <div class="text-center mb-4">
          <img :src="profilePicture" alt="Profile Picture" class="rounded-circle" width="150" height="150" />
          <h1 class="mt-3">{{ fullName }}</h1>
          <h4>{{ jobTitle }}</h4>
        </div>
  
        <div class="mb-4">
          <h2>About Me</h2>
          <p>{{ aboutMe }}</p>
        </div>
  
        <div class="mb-4">
          <h2>Experience</h2>
          <ul>
            <li v-for="experience in experiences" :key="experience.id">
              <strong>{{ experience.company }} - {{ experience.position }}</strong>
              <p>{{ experience.description }}</p>
            </li>
          </ul>
        </div>
  
        <div class="mb-4">
          <h2>Skills</h2>
          <ul class="list-inline">
            <li v-for="skill in skills" :key="skill" class="list-inline-item">
              <span class="badge bg-primary">{{ skill }}</span>
            </li>
          </ul>
        </div>
  
        <div>
          <h2>Contact</h2>
          <p>Email: {{ email }}</p>
          <p>Phone: {{ phone }}</p>
        </div>
      </div>
    </section>
</template>
  
<script setup>
  const profilePicture = '/profile.jpg'; // Ganti dengan path gambar Anda
  const fullName = 'John Doe';
  const jobTitle = 'Software Developer';
  const aboutMe = 'I am a passionate software developer with 5 years of experience.';
  const experiences = [
    { id: 1, company: 'Company A', position: 'Frontend Developer', description: 'Developed web applications using Vue.js and Nuxt.js.' },
    { id: 2, company: 'Company B', position: 'Backend Developer', description: 'Built RESTful APIs using Node.js and Express.' }
  ];
  const skills = ['JavaScript', 'Vue.js', 'Nuxt.js', 'Node.js', 'Bootstrap'];
  const email = 'john.doe@example.com';
  const phone = '+1234567890';
</script>
  
<style scoped>
  .container {
    max-width: 800px;
  }
</style>
  