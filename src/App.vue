<template>
  <div class="min-h-screen bg-gray-50 text-gray-900 font-sans">
    <!-- Navbar -->
    <header class="bg-white shadow-md sticky top-0 z-50">
      <nav class="max-w-6xl mx-auto flex justify-between items-center p-4">
        <div class="flex items-center gap-2">
          <i class="fas fa-code text-blue-600 text-xl"></i>
          <h1 class="text-2xl font-bold">Ariel<span class="text-blue-600">Portfolio</span></h1>
        </div>
        <ul class="hidden md:flex gap-6">
          <li><a href="#about" class="hover:text-blue-600 transition-colors duration-300 flex items-center gap-1 nav-link" :class="{ 'active': activeSection === 'about' }" @click="setActiveSection('about')"><i class="fas fa-user text-sm"></i>About</a></li>
          <li><a href="#skills" class="hover:text-blue-600 transition-colors duration-300 flex items-center gap-1 nav-link" :class="{ 'active': activeSection === 'skills' }" @click="setActiveSection('skills')"><i class="fas fa-tools text-sm"></i>Skills</a></li>
          <li><a href="#education" class="hover:text-blue-600 transition-colors duration-300 flex items-center gap-1 nav-link" :class="{ 'active': activeSection === 'education' }" @click="setActiveSection('education')"><i class="fas fa-graduation-cap text-sm"></i>Education</a></li>
          <li><a href="#experience" class="hover:text-blue-600 transition-colors duration-300 flex items-center gap-1 nav-link" :class="{ 'active': activeSection === 'experience' }" @click="setActiveSection('experience')"><i class="fas fa-briefcase text-sm"></i>Experience</a></li>
          <li><a href="#projects" class="hover:text-blue-600 transition-colors duration-300 flex items-center gap-1 nav-link" :class="{ 'active': activeSection === 'projects' }" @click="setActiveSection('projects')"><i class="fas fa-project-diagram text-sm"></i>Projects</a></li>
          <li><a href="#contact" class="hover:text-blue-600 transition-colors duration-300 flex items-center gap-1 nav-link" :class="{ 'active': activeSection === 'contact' }" @click="setActiveSection('contact')"><i class="fas fa-envelope text-sm"></i>Contact</a></li>
        </ul>
        <button class="md:hidden text-gray-700" @click="toggleMobileMenu">
          <i class="fas fa-bars text-xl"></i>
        </button>
      </nav>
      
      <!-- Mobile Menu -->
      <div v-if="mobileMenuOpen" class="md:hidden bg-white py-4 px-4 shadow-lg">
        <ul class="space-y-3">
          <li><a href="#about" class="block py-2 hover:text-blue-600 transition-colors" @click="closeMobileMenu">About</a></li>
          <li><a href="#skills" class="block py-2 hover:text-blue-600 transition-colors" @click="closeMobileMenu">Skills</a></li>
          <li><a href="#education" class="block py-2 hover:text-blue-600 transition-colors" @click="closeMobileMenu">Education</a></li>
          <li><a href="#experience" class="block py-2 hover:text-blue-600 transition-colors" @click="closeMobileMenu">Experience</a></li>
          <li><a href="#projects" class="block py-2 hover:text-blue-600 transition-colors" @click="closeMobileMenu">Projects</a></li>
          <li><a href="#contact" class="block py-2 hover:text-blue-600 transition-colors" @click="closeMobileMenu">Contact</a></li>
        </ul>
      </div>
    </header>

    <!-- Hero Section -->
    <section
      class="flex flex-col items-center justify-center text-center py-20 bg-gray-800  from-blue-500 to-purple-600 text-white relative overflow-hidden"
    >
      <div class="absolute top-0 left-0 w-full h-full opacity-10">
        <div class="absolute top-10 left-10 w-20 h-20 bg-white rounded-full"></div>
        <div class="absolute top-40 right-20 w-16 h-16 bg-white rounded-full"></div>
        <div class="absolute bottom-20 left-1/4 w-24 h-24 bg-white rounded-full"></div>
      </div>
      <div class="relative z-10">
<div class="w-32 h-32 mx-auto mb-6 rounded-full bg-gradient-to-r from-blue-400 to-purple-500 flex items-center justify-center shadow-lg overflow-hidden" data-aos="zoom-in">
      <img 
        src="/images/myfoto.jpg" 
        alt="Ariel Photo" 
        class="w-full h-full object-cover"
      >
    </div>
        <h2 class="text-4xl md:text-6xl font-bold" data-aos="zoom-in">Hi, I'm Ariel <span class="inline-block animate-bounce">🚀</span></h2>
        <p class="mt-4 text-lg md:text-xl" data-aos="fade-up" data-aos-delay="200">
          Fullstack Developer | Tech. Enthusiast
        </p>
<!-- Alternatif 2: Grid Layout untuk Mobile -->
<div class="mt-8 grid grid-cols-1 sm:flex gap-3 w-full max-w-md mx-auto" data-aos="fade-up" data-aos-delay="400">
  <!-- Baris 1: View Work + Download CV -->
  <div class="flex gap-3 col-span-2">
    <a href="#projects"
      class="flex-1 px-4 py-3 bg-white text-blue-600 rounded-lg font-semibold shadow hover:bg-gray-50 transition-all duration-300 flex items-center justify-center gap-2 text-sm min-h-[48px]"
    >
      <i class="fas fa-arrow-down"></i>
      <span class="whitespace-nowrap">View Work</span>
    </a>
    
    <a 
      href="/files/cvariel.pdf" 
      download
      class="flex-1 px-4 py-3 bg-emerald-500 text-white rounded-lg font-semibold hover:bg-emerald-600 transition-all duration-300 flex items-center justify-center gap-2 text-sm min-h-[48px]"
    >
      <i class="fas fa-file-pdf"></i>
      <span class="whitespace-nowrap">Download CV</span>
    </a>
  </div>
  
  <!-- Baris 2: Contact Me (full width) -->
  <a href="#contact"
    class="col-span-2 px-4 py-3 bg-transparent border-2 border-white text-white rounded-lg font-semibold hover:bg-white hover:text-blue-600 transition-all duration-300 flex items-center justify-center gap-2 text-sm min-h-[48px]"
  >
    <i class="fas fa-envelope"></i>
    Contact Me
  </a>
</div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="max-w-5xl mx-auto py-16 px-4" data-aos="fade-right">
      <div class="flex items-center gap-3 mb-8">
        <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
        <h3 class="text-3xl font-bold">About Me</h3>
        <div class="flex-1 h-1 bg-blue-600 rounded-full"></div>
      </div>
      <div class="bg-white rounded-2xl shadow-lg p-8">
        <div class="flex flex-col md:flex-row gap-8 items-center">
          <div class="md:w-1/3 flex justify-center">
<div class="w-48 h-48 rounded-full bg-gradient-to-r from-blue-100 to-purple-100 flex items-center justify-center shadow-md overflow-hidden">
          <img 
            src="/images/fotoku.jpg" 
            alt="Ariel Photo" 
            class="w-full h-full object-cover"
          >
        </div>
          </div>
          <div class="md:w-2/3">
            <p class="text-lg leading-relaxed mb-6">
              I am a fresh graduate of Informatics Engineering at Sebelas Maret University who has a great interest and enthusiasm for software and web development. 
              I have studied various relevant courses such as Algorithms and Programming, Object Oriented Programming, Web Programming, 
              Database Practice to support my future career.
            </p>
            <div class="grid grid-cols-2 gap-4">
              <div class="flex items-center gap-2">
                <i class="fas fa-check text-blue-600"></i>
                <span>Team Communication</span>
              </div>
              <div class="flex items-center gap-2">
                <i class="fas fa-check text-blue-600"></i>
                <span>Detail-Oriented</span>
              </div>
              <div class="flex items-center gap-2">
                <i class="fas fa-check text-blue-600"></i>
                <span>Problem Solving</span>
              </div>
              <div class="flex items-center gap-2">
                <i class="fas fa-check text-blue-600"></i>
                <span>Creative Thinking</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

<!-- Skills Section -->
<section id="skills" class="bg-gray-50 py-16 px-4">
  <div class="max-w-5xl mx-auto" data-aos="fade-up">
    <div class="flex items-center gap-3 mb-8">
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
      <h3 class="text-3xl font-bold">Skills</h3>
      <div class="flex-1 h-1 bg-blue-600 rounded-full"></div>
    </div>
    <div class="bg-white rounded-2xl shadow-lg p-8">
      <div class="grid md:grid-cols-2 gap-8">
        <!-- Technical Skills -->
        <div>
          <h4 class="text-xl font-semibold mb-6 flex items-center gap-2">
            <i class="fas fa-laptop-code text-blue-600"></i>
            Technical Skills
          </h4>
          <div class="space-y-6">
            <div v-for="skill in technicalSkills" :key="skill.name">
              <div class="flex items-center justify-between mb-1">
                <div class="flex items-center gap-3">
                  <!-- Gambar Skill -->
                  <div class="w-6 h-6 flex items-center justify-center">
                    <img 
                      :src="skill.icon" 
                      :alt="skill.name + ' icon'"
                      class="w-5 h-5 object-contain"
                    >
                  </div>
                  <span class="font-medium">{{ skill.name }}</span>
                </div>
                <span class="text-gray-600 font-semibold">{{ skill.percentage }}%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress bg-blue-600" :style="{ width: skill.percentage + '%' }"></div>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Professional Skills -->
        <div>
          <h4 class="text-xl font-semibold mb-6 flex items-center gap-2">
            <i class="fas fa-user-tie text-blue-600"></i>
            Professional Skills
          </h4>
          <div class="space-y-6">
            <div v-for="skill in professionalSkills" :key="skill.name">
              <div class="flex justify-between mb-1">
                <span>{{ skill.name }}</span>
                <span>{{ skill.percentage }}%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress bg-green-600" :style="{ width: skill.percentage + '%' }"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

    <!-- Education Section -->
<!-- Education Section -->
<section id="education" class="py-16 px-4">
  <div class="max-w-5xl mx-auto" data-aos="fade-up">
    <div class="flex items-center gap-3 mb-8">
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
      <h3 class="text-3xl font-bold">Education</h3>
      <div class="flex-1 h-1 bg-blue-600 rounded-full"></div>
    </div>
    <div class="bg-white rounded-2xl shadow-lg p-6 hover:shadow-xl transition-all duration-300">
      <div class="flex flex-col md:flex-row items-center gap-6">
        <!-- Logo UNS -->
        <div class="flex-shrink-0 w-20 h-20 md:w-24 md:h-24 rounded-full bg-gradient-to-r from-blue-100 to-purple-100 flex items-center justify-center shadow-md">
          <img 
            src="/images/Logo-UNS.png" 
            alt="UNS Logo" 
            class="w-16 h-16 md:w-20 md:h-20 object-contain"
          >
        </div>
        
        <!-- Content -->
        <div class="flex-1 text-center md:text-left">
          <h4 class="text-xl md:text-2xl font-semibold mb-2">Sebelas Maret University</h4>
          <p class="text-gray-700 mb-3 md:mb-4">Associate Degree - Informatic Engineering</p>
          
          <!-- Info GPA dan Tahun -->
          <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start items-center">
            <!-- GPA -->
            <div class="flex items-center gap-2 bg-blue-50 px-4 py-2 rounded-lg">
              <i class="fas fa-star text-yellow-500 text-sm"></i>
              <span class="text-gray-700 text-sm md:text-base">
                GPA: <span class="font-bold text-blue-600">3.72 / 4.00</span>
              </span>
            </div>
            
            <!-- Tahun -->
            <div class="flex items-center gap-2 bg-gray-50 px-4 py-2 rounded-lg">
              <i class="fas fa-calendar-alt text-blue-500 text-sm"></i>
              <span class="text-gray-700 text-sm md:text-base">2022 - 2025</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Experience Section - Card Grid dengan AOS Staggered Flip -->
<section id="experience" class="bg-gray-50 py-16 px-4">
  <div class="max-w-6xl mx-auto">
    <div class="flex items-center gap-3 mb-12 justify-center" data-aos="fade-up">
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
      <h3 class="text-3xl font-bold text-center">Experience</h3>
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
    </div>
    
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div 
        v-for="(exp, index) in experiences" 
        :key="index"
        class="bg-white rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 p-6 border-l-4 border-blue-600 transform hover:-translate-y-2"
        :data-aos="index % 2 === 0 ? 'flip-left' : 'flip-right'"
        :data-aos-delay="index * 200"
      >
        <div class="flex items-center gap-4 mb-4">
          <!-- Jika title mengandung "MSIB" pakai gambar -->
          <div v-if="exp.title.includes('MSIB')" class="w-12 h-12 rounded-full bg-gradient-to-r from-blue-100 to-purple-100 flex items-center justify-center shadow-md overflow-hidden border border-gray-200">
            <img 
              src="/images/msib.png" 
              :alt="exp.company + ' logo'"
              class="w-8 h-8 object-contain"
            >
          </div>
          
          <!-- Selain itu pakai icon -->
          <div v-else class="w-12 h-12 rounded-full bg-gradient-to-r from-blue-100 to-purple-100 flex items-center justify-center shadow-md">
            <img 
              src="/images/logojbk.png" 
              :alt="exp.company + ' logo'"
              class="w-8 h-8 object-contain"
            >
          </div>
          
          <div>
            <h4 class="text-lg font-semibold">{{ exp.title }}</h4>
            <p class="text-blue-600 font-medium text-sm">{{ exp.company }}</p>
          </div>
        </div>
        
        <div class="flex items-center gap-2 mb-4 text-gray-500 text-sm">
          <i class="fas fa-calendar"></i>
          <span>{{ exp.period }}</span>
        </div>
        
        <p class="text-gray-700 mb-3 text-sm font-medium">{{ exp.description }}</p>
        
        <ul class="space-y-2">
          <li v-for="(achievement, i) in exp.achievements" :key="i" class="flex items-start gap-2 text-sm">
            <i class="fas fa-check text-green-500 mt-1 text-xs"></i>
            <span class="text-gray-600">{{ achievement }}</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- Projects Section dengan v-for -->
<section id="projects" class="py-16 px-4">
  <div class="max-w-6xl mx-auto">
    <div class="flex items-center gap-3 mb-10 justify-center">
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
      <h3 class="text-3xl font-bold text-center" data-aos="fade-up">Projects</h3>
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
    </div>
    <div class="grid md:grid-cols-3 gap-8">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-xl transition-all duration-300 group flex flex-col"
        data-aos="zoom-in-up"
        :data-aos-delay="(index + 1) * 200"
      >
        <div class="h-48 relative overflow-hidden">
          <img 
            v-if="project.useImage"
            :src="project.image" 
            :alt="project.title" 
            class="absolute inset-0 w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
          >
          <div v-else class="absolute inset-0 flex items-center justify-center" :class="project.gradient">
            <i :class="project.icon" class="text-white text-5xl"></i>
          </div>
          <div class="absolute inset-0 bg-black opacity-0 group-hover:opacity-10 transition-opacity duration-300"></div>
        </div>
        <div class="p-6 flex-1 flex flex-col">
          <h4 class="font-bold text-xl mb-2">{{ project.title }}</h4>
          <p class="text-gray-600 mb-4 flex-1">{{ project.description }}</p>
          <div class="flex flex-wrap gap-2 mb-4">
            <span v-for="(tech, techIndex) in project.technologies" :key="techIndex" class="px-3 py-1 text-xs rounded-full" :class="tech.color">
              {{ tech.name }}
            </span>
          </div>
          
          <!-- Button Container - Dinamis berdasarkan ketersediaan demo -->
          <div :class="project.demoUrl ? 'flex gap-2' : ''">
            <!-- Button Live Demo (hanya untuk Jababeka Learning) -->
            <a 
              v-if="project.demoUrl"
              :href="project.demoUrl" 
              target="_blank" 
              rel="noopener noreferrer"
              class="flex-1 px-4 py-2 bg-green-600 text-white rounded-lg hover:bg-green-700 transition-all duration-300 flex items-center justify-center gap-2 group/btn shadow-md"
            >
              <i class="fas fa-external-link-alt group-hover/btn:scale-110 transition-transform"></i>
              <span class="font-medium">Live Demo</span>
            </a>
            
            <!-- Button View Code -->
            <a 
              :href="project.githubUrl" 
              target="_blank" 
              rel="noopener noreferrer"
              :class="project.demoUrl ? 'flex-1' : 'w-full'"
              class="px-4 py-2 bg-gray-800 text-white rounded-lg hover:bg-gray-900 transition-all duration-300 flex items-center justify-center gap-2 group/btn shadow-md"
            >
              <i class="fab fa-github text-lg group-hover/btn:scale-110 transition-transform"></i>
              <span class="font-medium">View Code</span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

   <!-- Contact Section -->
<section id="contact" class="bg-gray-50 py-16 px-4" data-aos="fade-up">
  <div class="max-w-5xl mx-auto">
    <div class="flex items-center gap-3 mb-8">
      <div class="w-10 h-1 bg-blue-600 rounded-full"></div>
      <h3 class="text-3xl font-bold">Contact Me</h3>
      <div class="flex-1 h-1 bg-blue-600 rounded-full"></div>
    </div>
    <div class="grid md:grid-cols-2 gap-12">
      <div>
        <h4 class="text-xl font-semibold mb-4">Get In Touch</h4>
        <p class="text-gray-600 mb-6">
          Feel free to reach out if you're looking for a developer, have a question, or just want to connect.
        </p>
        <div class="space-y-4">
          <!-- Email dengan mailto -->
          <a 
            :href="`mailto:${contactInfo.email}`"
            class="flex items-center gap-3 p-3 rounded-lg hover:bg-blue-50 transition-all duration-300 cursor-pointer group"
            data-aos="fade-right" 
            data-aos-delay="100"
          >
            <div class="w-10 h-10 rounded-full bg-blue-100 flex items-center justify-center group-hover:bg-blue-200 transition-colors">
              <i class="fas fa-envelope text-blue-600"></i>
            </div>
            <div>
              <p class="font-medium">Email</p>
              <p class="text-gray-600 group-hover:text-blue-600 transition-colors">{{ contactInfo.email }}</p>
            </div>
          </a>
          
          <!-- WhatsApp dengan wa.me -->
          <a 
            :href="`https://wa.me/${contactInfo.phone.replace(/\D/g, '')}`"
            target="_blank"
            rel="noopener noreferrer"
            class="flex items-center gap-3 p-3 rounded-lg hover:bg-green-50 transition-all duration-300 cursor-pointer group"
            data-aos="fade-right" 
            data-aos-delay="200"
          >
            <div class="w-10 h-10 rounded-full bg-green-100 flex items-center justify-center group-hover:bg-green-200 transition-colors">
              <i class="fab fa-whatsapp text-green-600"></i>
            </div>
            <div>
              <p class="font-medium">Phone / WhatsApp</p>
              <p class="text-gray-600 group-hover:text-green-600 transition-colors">{{ contactInfo.phone }}</p>
            </div>
          </a>
          
          <!-- Location (tetap biasa) -->
          <div 
            class="flex items-center gap-3 p-3 rounded-lg hover:bg-gray-100 transition-all duration-300"
            data-aos="fade-right" 
            data-aos-delay="300"
          >
            <div class="w-10 h-10 rounded-full bg-blue-100 flex items-center justify-center">
              <i class="fas fa-map-marker-alt text-blue-600"></i>
            </div>
            <div>
              <p class="font-medium">Location</p>
              <p class="text-gray-600">{{ contactInfo.location }}</p>
            </div>
          </div>
        </div>
      </div>
        <form @submit.prevent="submitContactForm" class="grid gap-4">
          <input 
            v-model="contactForm.name" 
            type="text" 
            placeholder="Your Name" 
            class="border border-gray-300 p-3 rounded-lg w-full focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all" 
            data-aos="fade-left" 
            data-aos-delay="100" 
            :disabled="isSending"
            required
          >
          <input 
            v-model="contactForm.email" 
            type="email" 
            placeholder="Your Email" 
            class="border border-gray-300 p-3 rounded-lg w-full focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all" 
            data-aos="fade-left" 
            data-aos-delay="200" 
            :disabled="isSending"
            required
          >
          <textarea 
            v-model="contactForm.message" 
            placeholder="Your Message" 
            rows="5" 
            class="border border-gray-300 p-3 rounded-lg w-full focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-all" 
            data-aos="fade-left" 
            data-aos-delay="300" 
            :disabled="isSending"
            required
          ></textarea>
          
          <button 
            type="submit" 
            :disabled="isSending"
            class="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-all flex items-center justify-center gap-2 disabled:bg-blue-400 disabled:cursor-not-allowed transform hover:scale-105 active:scale-95" 
            data-aos="zoom-in" 
            data-aos-delay="400"
          >
            <i v-if="isSending" class="fas fa-spinner fa-spin"></i>
            <i v-else class="fas fa-paper-plane"></i>
            {{ isSending ? 'Sending Message...' : 'Send Message' }}
          </button>
        </form>
    </div>
  </div>
</section>

<!-- Footer Section - Fixed -->
<footer class="bg-gray-900 text-gray-300 py-8 mt-auto">
  <div class="max-w-6xl mx-auto px-4">
    <div class="flex flex-col md:flex-row justify-between items-center">
      <div class="flex items-center gap-2 mb-4 md:mb-0">
        <i class="fas fa-code text-blue-500"></i>
        <span class="text-xl font-bold">Ariel<span class="text-blue-500">Portfolio</span></span>
      </div>
      <div class="flex gap-6 mb-4 md:mb-0">
        <a v-for="(social, index) in socialLinks" :key="index" :href="social.url" class="hover:text-white transition-colors" target="_blank" rel="noopener">
          <i :class="social.icon" class="text-xl"></i>
        </a>
      </div>
      <div>
        <p class="text-sm">© {{ currentYear }} ArielPortfolio. All rights reserved.</p>
      </div>
    </div>
  </div>
</footer>
  </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';
import emailjs from '@emailjs/browser';

export default {
  name: 'App',
  data() {
    return {
       currentYear: new Date().getFullYear(),
      activeSection: 'home',
      mobileMenuOpen: false,
      technicalSkills: [
        { name: 'HTML/CSS', percentage: 90, icon: '/images/html.png'},
        { name: 'JavaScript', percentage: 85, icon: '/images/javascript.png'},
        { name: 'Vue.js', percentage: 80, icon: '/images/vuejs.png'},
        { name: 'Laravel', percentage: 75, icon: '/images/laravel.png'},
        { name: 'React.js', percentage: 70, icon: '/images/react.png'},
        { name: 'PHP', percentage: 80, icon: '/images/php.png'},
        { name: 'Python', percentage: 75, icon: '/images/python.png'},
        { name: 'Java', percentage: 75, icon: '/images/java.png'},
        { name: 'MySQL', percentage: 85, icon: '/images/mysql.png'}
      ],
      professionalSkills: [
        { name: 'Communication', percentage: 95 },
        { name: 'Teamwork', percentage: 90 },
        { name: 'Problem Solving', percentage: 85 },
        { name: 'Creativity', percentage: 80 },
        { name: 'Time Management', percentage: 85 },
        { name: 'Leadership', percentage: 75 },
        { name: 'Adaptability', percentage: 90 }
      ],
      experiences: [
        {
          title: 'MSIB Batch 6',
          company: 'PT Jababeka Tbk',
          period: 'Feb 2024 - Jun 2024',
          description: 'During this program, I successfully:',
          achievements: [
            'Improved system performance with query optimization and database structure',
            'Developed new features on purchasing platform based on Laravel',
            'Fixing Purchasing System bugs and issues',
            'Fixing annual budget calculation as well as reimburse and PUM functions',
            'Improved user interface to be more intuitive and responsive',
            'Coordinated with cross-divisional teams to ensure smooth system integration'
          ]
        },
        {
          title: 'MSIB Batch 7',
          company: 'PT Jababeka Tbk',
          period: 'Aug 2024 - Dec 2024',
          description: 'During this program, I successfully:',
          achievements: [
            'Designing UI/UX and prototype for Jababeka Learning (LMS)',
            'Developing front-end using Vue.js',
            'Creating CDM and PDM',
            'Developing back-end using Laravel 11',
            'Coordinated with cross-divisional teams to ensure smooth system integration'
          ]
        },
        {
          title: 'Kegiatan Magang Mahasiswa',
          company: 'PT Jababeka Tbk',
          period: 'Jan 2025 - Feb 2025',
          description: 'During this program, I successfully:',
          achievements: [
            'Deploying and integrating the website to be publicly accessible',
            'Improving features for better usability',
            'Conducting testing with Jababeka HR Director and staff',
            'Coordinated with cross-divisional teams to ensure smooth system integration'
          ]
        }
      ],
      projects: [
        {
          title: 'Jababeka Learning',
          description: 'Learning Management System (LMS) based on Laravel & Vue.js to manage training, certifications, and training recommendations at PT Jababeka Tbk.',
          gradient: 'bg-gradient-to-r from-blue-500 to-purple-600',
          useImage: true, // true = tampilkan gambar full
        image: '/images/lms.png',
          icon: 'fas fa-laptop-code',
           githubUrl: 'https://github.com/arielfajar/lms_jababeka.git',
           demoUrl: 'https://jababekalearning.com',
          technologies: [
            { name: 'Laravel', color: 'bg-blue-100 text-blue-800' },
            { name: 'Vue.js', color: 'bg-green-100 text-green-800' },
            { name: 'MySQL', color: 'bg-purple-100 text-purple-800' }
          ]
        },
        {
          title: 'JBPURC Jababeka',
          description: 'Jababeka Purchasing (JBPURC) web system for vendor management, purchase monitoring, and approval workflow optimization.',
          gradient: 'bg-gradient-to-r from-green-500 to-teal-600',
          useImage: true, // true = tampilkan gambar full
          image: '/images/purchasing.png',
          icon: 'fas fa-shopping-cart',
           githubUrl: 'https://github.com/arielfajar/purchasing_jababeka.git',
          technologies: [
            { name: 'Laravel', color: 'bg-blue-100 text-blue-800' },
            { name: 'AJAX', color: 'bg-green-100 text-green-800' },
            { name: 'JavaScript', color: 'bg-yellow-100 text-yellow-800' }
          ]
        },
        {
          title: 'Budgetting Jababeka',
          description: 'Jababeka Budgeting System for efficient digital financial planning and analysis.',
          gradient: 'bg-gradient-to-r from-purple-500 to-pink-600',
          useImage: true, // true = tampilkan gambar full
        image: '/images/budget.png',
          icon: 'fas fa-chart-line',
           githubUrl: 'https://github.com/arielfajar/budgeting_jababeka.git',
          technologies: [
            { name: 'Java', color: 'bg-blue-100 text-blue-800' },
            { name: 'GUI', color: 'bg-red-100 text-red-800' },
            { name: 'MySQL', color: 'bg-purple-100 text-purple-800' }
          ]
        }
      ],
      contactInfo: {
        email: 'ariel.fajarh@gmail.com',
        phone: '+62 888 0928 8941',
        location: 'Cikarang, Indonesia'
      },
      contactForm: {
        name: '',
        email: '',
        message: ''
      },
      socialLinks: [
        { 
          name: 'LinkedIn', 
          icon: 'fab fa-linkedin', 
          url: 'https://www.linkedin.com/in/arielfajarh' 
        },
        { 
          name: 'GitHub', 
          icon: 'fab fa-github', 
          url: 'https://github.com/arielfajar' 
        },
        { 
          name: 'Instagram', 
          icon: 'fab fa-instagram', 
          url: 'https://instagram.com/arielfajar' 
        }
      ]
    }
  },
  mounted() {
    // Initialize AOS
    AOS.init({
      duration: 800,
      // once: true,
      offset: 100
    });
    
    // Add scroll event listener to update active section
    window.addEventListener('scroll', this.handleScroll);
    
    // Initialize skill bars animation
    this.animateSkillBars();
    emailjs.init("eTFDsabna1YryLWcv");
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const sections = ['about', 'skills', 'education', 'experience', 'projects', 'contact'];
      const scrollPosition = window.scrollY + 100;

      for (const section of sections) {
        const element = document.getElementById(section);
        if (element) {
          const offsetTop = element.offsetTop;
          const offsetBottom = offsetTop + element.offsetHeight;

          if (scrollPosition >= offsetTop && scrollPosition < offsetBottom) {
            this.activeSection = section;
            break;
          }
        }
      }
    },
    animateSkillBars() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            const skillBars = entry.target.querySelectorAll('.skill-progress');
            skillBars.forEach(bar => {
              const width = bar.style.width;
              bar.style.width = '0';
              setTimeout(() => {
                bar.style.width = width;
              }, 200);
            });
          }
        });
      }, { threshold: 0.5 });

      const skillsSection = document.getElementById('skills');
      if (skillsSection) {
        observer.observe(skillsSection);
      }
    },
    setActiveSection(section) {
      this.activeSection = section;
    },
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen;
    },
    closeMobileMenu() {
      this.mobileMenuOpen = false;
    },
    async submitContactForm() {
      // Validasi form
      if (!this.contactForm.name || !this.contactForm.email || !this.contactForm.message) {
        this.showNotification('Please fill all fields', 'error');
        return;
      }

      this.isSending = true;

      try {
        const templateParams = {
          from_name: this.contactForm.name,
          from_email: this.contactForm.email,
          message: this.contactForm.message,
          to_email: 'ariel.fajarh@gmail.com',
          reply_to: this.contactForm.email
        };

        // Ganti dengan credentials Anda
        await emailjs.send(
          'service_sa69l58',      // Service ID Anda
          'template_ycyzcwy',     // Template ID Anda  
          templateParams,
          'eTFDsabna1YryLWcv'       // Public Key Anda
        );

        this.showNotification('🎉 Message sent successfully! I will get back to you soon.', 'success');
        this.resetContactForm();
        
      } catch (error) {
        console.error('Error sending email:', error);
        this.showNotification('❌ Failed to send message. Please try again later.', 'error');
      } finally {
        this.isSending = false;
      }
    },

    resetContactForm() {
      this.contactForm = {
        name: '',
        email: '',
        message: ''
      };
    },

    showNotification(message, type) {
      // Buat notifikasi custom yang lebih baik
      const notification = document.createElement('div');
      notification.className = `fixed top-4 right-4 p-4 rounded-lg shadow-lg z-50 transform transition-all duration-300 max-w-sm ${
        type === 'success' 
          ? 'bg-green-500 text-white border-l-4 border-green-600' 
          : 'bg-red-500 text-white border-l-4 border-red-600'
      }`;
      
      notification.innerHTML = `
        <div class="flex items-center gap-3">
          <i class="fas ${type === 'success' ? 'fa-check-circle' : 'fa-exclamation-circle'}"></i>
          <span>${message}</span>
        </div>
      `;
      
      document.body.appendChild(notification);
      
      // Animasi masuk
      setTimeout(() => {
        notification.style.transform = 'translateX(0)';
      }, 100);
      
      // Hilangkan setelah 5 detik
      setTimeout(() => {
        notification.style.transform = 'translateX(100%)';
        setTimeout(() => {
          notification.remove();
        }, 300);
      }, 5000);
    }
  }
}
</script>

<style scoped>
.skill-bar {
  height: 8px;
  background-color: #e5e7eb;
  border-radius: 4px;
  overflow: hidden;
}
.skill-progress {
  height: 100%;
  border-radius: 4px;
  transition: width 1s ease-in-out;
}
.nav-link.active {
  color: #3b82f6;
  font-weight: 600;
}
</style>
