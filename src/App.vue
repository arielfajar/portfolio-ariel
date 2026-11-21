<template>
  <div class="min-h-screen bg-white text-[#101828] font-['Inter'] overflow-x-hidden">
    <!-- Navbar -->
    <header class="bg-white/95 backdrop-blur border-b border-[#E3E6EA] sticky top-0 z-50">
      <nav class="max-w-6xl mx-auto flex justify-between items-center px-4 py-4">
        <div class="flex items-baseline gap-2.5">
          <span class="font-['Sora'] text-xl font-bold tracking-tight text-[#101828]">
            Ariel<span class="text-[#E76F51]">.</span>
          </span>
          <span class="hidden sm:inline text-xs font-medium text-[#667085] border-l border-[#D0D5DD] pl-2.5 tracking-wide">
            Fullstack Developer
          </span>
        </div>
        <ul class="hidden md:flex gap-8 text-sm font-medium text-[#475467]">
          <li><a href="#about" class="hover:text-[#2451B8] transition-colors duration-300 nav-link" :class="{ 'active': activeSection === 'about' }" @click="setActiveSection('about')">About</a></li>
          <li><a href="#skills" class="hover:text-[#2451B8] transition-colors duration-300 nav-link" :class="{ 'active': activeSection === 'skills' }" @click="setActiveSection('skills')">Skills</a></li>
          <li><a href="#education" class="hover:text-[#2451B8] transition-colors duration-300 nav-link" :class="{ 'active': activeSection === 'education' }" @click="setActiveSection('education')">Education</a></li>
          <li><a href="#experience" class="hover:text-[#2451B8] transition-colors duration-300 nav-link" :class="{ 'active': activeSection === 'experience' }" @click="setActiveSection('experience')">Experience</a></li>
          <li><a href="#projects" class="hover:text-[#2451B8] transition-colors duration-300 nav-link" :class="{ 'active': activeSection === 'projects' }" @click="setActiveSection('projects')">Projects</a></li>
          <li><a href="#contact" class="hover:text-[#2451B8] transition-colors duration-300 nav-link" :class="{ 'active': activeSection === 'contact' }" @click="setActiveSection('contact')">Contact</a></li>
        </ul>
        <a href="#contact" class="hidden md:inline-flex px-4 py-2 bg-[#101828] text-white rounded-lg text-sm font-medium hover:bg-[#2451B8] transition-colors duration-300">
          Let's talk
        </a>
        <button
          class="md:hidden text-[#101828] p-2 -mr-2 rounded-lg hover:bg-[#F7F8FA] transition-colors"
          aria-label="Toggle menu"
          @click="toggleMobileMenu"
        >
          <i :class="mobileMenuOpen ? 'fas fa-times' : 'fas fa-bars'" class="text-xl"></i>
        </button>
      </nav>

      <!-- Mobile Menu -->
      <transition
        enter-active-class="transition duration-200 ease-out"
        enter-from-class="opacity-0 -translate-y-2"
        enter-to-class="opacity-100 translate-y-0"
        leave-active-class="transition duration-150 ease-in"
        leave-from-class="opacity-100 translate-y-0"
        leave-to-class="opacity-0 -translate-y-2"
      >
        <div v-if="mobileMenuOpen" class="md:hidden bg-white py-4 px-4 border-t border-[#E3E6EA] shadow-lg">
          <ul class="space-y-1 text-[#475467] font-medium">
            <li><a href="#about" class="block py-3 px-2 rounded-lg hover:bg-[#F7F8FA] hover:text-[#2451B8] transition-colors" @click="closeMobileMenu">About</a></li>
            <li><a href="#skills" class="block py-3 px-2 rounded-lg hover:bg-[#F7F8FA] hover:text-[#2451B8] transition-colors" @click="closeMobileMenu">Skills</a></li>
            <li><a href="#education" class="block py-3 px-2 rounded-lg hover:bg-[#F7F8FA] hover:text-[#2451B8] transition-colors" @click="closeMobileMenu">Education</a></li>
            <li><a href="#experience" class="block py-3 px-2 rounded-lg hover:bg-[#F7F8FA] hover:text-[#2451B8] transition-colors" @click="closeMobileMenu">Experience</a></li>
            <li><a href="#projects" class="block py-3 px-2 rounded-lg hover:bg-[#F7F8FA] hover:text-[#2451B8] transition-colors" @click="closeMobileMenu">Projects</a></li>
            <li><a href="#contact" class="block py-3 px-2 rounded-lg hover:bg-[#F7F8FA] hover:text-[#2451B8] transition-colors" @click="closeMobileMenu">Contact</a></li>
          </ul>
        </div>
      </transition>
    </header>

    <!-- Hero Section -->
    <section class="max-w-6xl mx-auto px-4 py-12 md:py-24">
      <div class="grid md:grid-cols-5 gap-10 md:gap-12 items-center">
        <div class="order-2 md:order-1 md:col-span-3 text-center md:text-left" data-aos="fade-up">
          <p class="text-[#E76F51] font-semibold mb-3 text-sm md:text-base">Fullstack Developer</p>
          <h2 class="font-['Sora'] text-3xl sm:text-4xl md:text-5xl font-bold leading-tight mb-5 md:mb-6">
            Hi, I'm Ariel — I build practical web systems that get work done.
          </h2>
          <p class="text-[#475467] text-base md:text-lg leading-relaxed mb-8 max-w-xl mx-auto md:mx-0">
            Informatics Engineering graduate focused on web and software systems, with hands-on experience building
            internal systems for companies.
          </p>
          <div class="flex flex-col sm:flex-row sm:flex-wrap gap-3 items-stretch sm:items-center justify-center md:justify-start">
            <a href="#projects" class="min-h-[44px] px-5 py-3 bg-[#101828] text-white rounded-lg font-medium hover:bg-[#2451B8] transition-all duration-300 flex items-center justify-center gap-2">
              <i class="fas fa-arrow-down text-sm"></i> View Work
            </a>
            <a href="/files/cvariel.pdf" download class="min-h-[44px] px-5 py-3 border border-[#D0D5DD] text-[#101828] rounded-lg font-medium hover:border-[#2451B8] hover:text-[#2451B8] transition-all duration-300 flex items-center justify-center gap-2">
              <i class="fas fa-file-pdf text-sm"></i> Download CV
            </a>
            <a href="#contact" class="min-h-[44px] px-5 py-3 text-[#475467] rounded-lg font-medium hover:text-[#2451B8] transition-all duration-300 flex items-center justify-center gap-2">
              <i class="fas fa-envelope text-sm"></i> Contact Me
            </a>
          </div>
        </div>

        <div class="order-1 md:order-2 md:col-span-2 flex justify-center" data-aos="fade-up">
          <div class="relative w-48 h-48 sm:w-56 sm:h-56 md:w-64 md:h-64">
            <div class="absolute -inset-2.5 md:-inset-3 rounded-[2rem] bg-[#FBEEE9] -z-10"></div>
            <div class="w-full h-full rounded-[1.75rem] overflow-hidden border border-[#E3E6EA] shadow-sm bg-[#F7F8FA]">
              <img
                src="/images/myfoto.jpeg"
                alt="Ariel Photo"
                loading="eager"
                class="w-full h-full object-cover"
                @load="$emit('img-loaded')"
              >
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="max-w-5xl mx-auto py-12 md:py-16 px-4 scroll-mt-20">
      <div class="mb-8 md:mb-10" data-aos="fade-up">
        <h3 class="text-2xl md:text-3xl font-['Sora'] font-bold">About Me</h3>
      </div>
      <div class="flex flex-col md:flex-row gap-6 md:gap-10 items-start" data-aos="fade-up" data-aos-delay="100">
        <div class="md:w-1/3 w-full">
          <div class="w-full aspect-square rounded-2xl overflow-hidden border border-[#E3E6EA] bg-[#F7F8FA]">
            <img src="/images/fotoku.jpeg" alt="Ariel Photo" loading="lazy" class="w-full h-full object-cover">
          </div>
        </div>
        <div class="md:w-2/3">
          <p class="text-base md:text-lg leading-relaxed mb-6 text-[#344054]">
            As an Informatics Engineering graduate from Sebelas Maret University, I have a strong foundation in
            software development and a passion for building impactful web applications. I am passionate about
            translating conceptual ideas into real-world products, with a keen focus on performance, clean
            code, and an intuitive user experience.
          </p>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 sm:gap-4">
            <div class="flex items-center gap-2">
              <i class="fas fa-check text-[#2451B8]"></i>
              <span>Team Communication</span>
            </div>
            <div class="flex items-center gap-2">
              <i class="fas fa-check text-[#2451B8]"></i>
              <span>Detail-Oriented</span>
            </div>
            <div class="flex items-center gap-2">
              <i class="fas fa-check text-[#2451B8]"></i>
              <span>Problem Solving</span>
            </div>
            <div class="flex items-center gap-2">
              <i class="fas fa-check text-[#2451B8]"></i>
              <span>Creative Thinking</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="bg-[#F7F8FA] py-12 md:py-16 px-4 scroll-mt-20">
      <div class="max-w-5xl mx-auto">
        <div class="mb-8 md:mb-10" data-aos="fade-up">
          <p class="text-[#2451B8] font-semibold text-sm tracking-wide mb-2">Skills</p>
          <h3 class="text-2xl md:text-3xl font-['Sora'] font-bold">What I Work With</h3>
        </div>
        <div class="grid md:grid-cols-2 gap-8 md:gap-12">
          <!-- Technical Skills -->
          <div data-aos="fade-up" data-aos-delay="100">
            <h4 class="text-lg font-semibold mb-6 flex items-center gap-2 text-[#344054]">
              <i class="fas fa-laptop-code text-[#2451B8]"></i>
              Technical Skills
            </h4>
            <div class="space-y-5">
              <div v-for="skill in technicalSkills" :key="skill.name">
                <div class="flex items-center justify-between mb-1.5">
                  <div class="flex items-center gap-3">
                    <div class="w-6 h-6 flex items-center justify-center">
                      <img :src="skill.icon" :alt="skill.name + ' icon'" loading="lazy" class="w-5 h-5 object-contain">
                    </div>
                    <span class="font-medium text-sm">{{ skill.name }}</span>
                  </div>
                  <span class="text-[#667085] text-sm">{{ skill.percentage }}%</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress bg-[#2451B8]" :style="{ width: skill.percentage + '%' }"></div>
                </div>
              </div>
            </div>
          </div>

          <!-- Professional Skills -->
          <div data-aos="fade-up" data-aos-delay="200">
            <h4 class="text-lg font-semibold mb-6 flex items-center gap-2 text-[#344054]">
              <i class="fas fa-user-tie text-[#E76F51]"></i>
              Professional Skills
            </h4>
            <div class="space-y-5">
              <div v-for="skill in professionalSkills" :key="skill.name">
                <div class="flex justify-between mb-1.5">
                  <span class="font-medium text-sm">{{ skill.name }}</span>
                  <span class="text-[#667085] text-sm">{{ skill.percentage }}%</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress bg-[#E76F51]" :style="{ width: skill.percentage + '%' }"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="py-12 md:py-16 px-4 scroll-mt-20">
      <div class="max-w-5xl mx-auto">
        <div class="mb-8 md:mb-10" data-aos="fade-up">
          <h3 class="text-2xl md:text-3xl font-['Sora'] font-bold">Education</h3>
        </div>
        <div class="border border-[#E3E6EA] rounded-2xl p-6 hover:border-[#2451B8]/40 transition-all duration-300" data-aos="fade-up" data-aos-delay="100">
          <div class="flex flex-col md:flex-row items-center gap-6">
            <div class="flex-shrink-0 w-20 h-20 md:w-24 md:h-24 rounded-full bg-[#F7F8FA] flex items-center justify-center">
              <img src="/images/Logo-UNS.png" alt="UNS Logo" loading="lazy" class="w-16 h-16 md:w-20 md:h-20 object-contain">
            </div>
            <div class="flex-1 text-center md:text-left">
              <h4 class="text-xl md:text-2xl font-semibold mb-2">Sebelas Maret University</h4>
              <p class="text-[#667085] mb-4">Associate Degree - Informatic Engineering</p>
              <div class="flex flex-col sm:flex-row gap-3 justify-center md:justify-start items-center text-sm">
                <div class="flex items-center gap-2 bg-[#F7F8FA] px-4 py-2 rounded-lg">
                  <i class="fas fa-star text-[#E76F51]"></i>
                  <span>GPA: <span class="font-bold text-[#2451B8]">3.72 / 4.00</span></span>
                </div>
                <div class="flex items-center gap-2 bg-[#F7F8FA] px-4 py-2 rounded-lg">
                  <i class="fas fa-calendar-alt text-[#2451B8]"></i>
                  <span>2022 - 2025</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="bg-[#F7F8FA] py-12 md:py-16 px-4 scroll-mt-20">
      <div class="max-w-4xl mx-auto">
        <div class="mb-8 md:mb-12" data-aos="fade-up">
          <p class="text-[#2451B8] font-semibold text-sm tracking-wide mb-2">Experience</p>
          <h3 class="text-2xl md:text-3xl font-['Sora'] font-bold">Where I've Worked</h3>
        </div>

        <div class="relative pl-8">
          <div class="absolute left-[7px] top-2 bottom-2 w-px bg-[#D0D5DD]"></div>

          <div
            v-for="(exp, index) in experiences"
            :key="index"
            class="relative mb-10 last:mb-0"
            data-aos="fade-up"
            :data-aos-delay="index * 80"
          >
            <div class="absolute -left-8 top-1.5 w-4 h-4 rounded-full bg-white border-2 border-[#2451B8]"></div>

            <div class="bg-white border border-[#E3E6EA] rounded-xl p-5 sm:p-6 hover:border-[#2451B8]/40 transition-all duration-300">
              <div class="flex items-start sm:items-center gap-4 mb-4">
                <div class="w-12 h-12 rounded-full bg-[#F7F8FA] flex items-center justify-center overflow-hidden shrink-0">
                  <img v-if="exp.logo" :src="exp.logo" :alt="exp.company + ' logo'" loading="lazy" class="w-8 h-8 object-contain">
                  <i v-else :class="exp.icon || 'fas fa-briefcase'" class="text-[#2451B8] text-lg"></i>
                </div>
                <div class="min-w-0">
                  <h4 class="text-base sm:text-lg font-semibold leading-tight">{{ exp.title }}</h4>
                  <p class="text-[#2451B8] font-medium text-sm">{{ exp.company }}</p>
                </div>
              </div>

              <div class="flex items-center gap-2 mb-4 text-[#667085] text-sm">
                <i class="fas fa-calendar"></i>
                <span>{{ exp.period }}</span>
              </div>

              <p class="text-[#344054] mb-3 text-sm font-medium">{{ exp.description }}</p>

              <ul class="space-y-2">
                <li v-for="(achievement, i) in exp.achievements" :key="i" class="flex items-start gap-2 text-sm">
                  <i class="fas fa-check text-[#2451B8] mt-1 text-xs shrink-0"></i>
                  <span class="text-[#475467]">{{ achievement }}</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-12 md:py-16 px-4 scroll-mt-20">
      <div class="max-w-6xl mx-auto">
        <div class="mb-8 md:mb-10" data-aos="fade-up">
          <p class="text-[#2451B8] font-semibold text-sm tracking-wide mb-2">Projects</p>
          <h3 class="text-2xl md:text-3xl font-['Sora'] font-bold">Selected Work</h3>
        </div>

        <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-5 md:gap-6">
          <div
            v-for="(project, index) in projects"
            :key="index"
            class="bg-white border border-[#E3E6EA] rounded-2xl overflow-hidden hover:shadow-md hover:border-[#2451B8]/30 transition-all duration-300 group flex flex-col"
            data-aos="fade-up"
            :data-aos-delay="(index % 3) * 80"
          >
            <!-- Bagian Gambar / Gradient Placeholder -->
            <div class="aspect-video relative overflow-hidden border-b border-[#E3E6EA] bg-[#F7F8FA]">
              <img
                v-if="project.useImage"
                :src="project.image"
                :alt="project.title"
                loading="lazy"
                class="absolute inset-0 w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
              >
              <div v-else class="absolute inset-0 flex items-center justify-center" :class="project.gradient">
                <i :class="project.icon" class="text-white text-5xl opacity-90 group-hover:scale-110 transition-transform duration-300"></i>
              </div>
            </div>

            <!-- Bagian Konten Teks -->
            <div class="p-5 md:p-6 flex-1 flex flex-col">
              <h4 class="font-bold text-base md:text-lg mb-2">{{ project.title }}</h4>
              <p class="text-[#667085] mb-4 flex-1 text-sm leading-relaxed">{{ project.description }}</p>

              <!-- Tags Teknologi -->
              <div class="flex flex-wrap gap-2 mt-auto">
                <span v-for="(tech, techIndex) in project.technologies" :key="techIndex" class="px-2.5 py-1 text-xs rounded-full border" :class="tech.color">
                  {{ tech.name }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="bg-[#F7F8FA] py-12 md:py-16 px-4 scroll-mt-20">
      <div class="max-w-5xl mx-auto">
        <div class="mb-8 md:mb-10" data-aos="fade-up">
          <p class="text-[#2451B8] font-semibold text-sm tracking-wide mb-2">Contact</p>
          <h3 class="text-2xl md:text-3xl font-['Sora'] font-bold">Let's Work Together</h3>
        </div>
        <div class="grid md:grid-cols-2 gap-8 md:gap-12">
          <div data-aos="fade-up">
            <p class="text-[#667085] mb-6">
              Feel free to reach out if you're looking for a developer, have a question, or just want to connect.
            </p>
            <div class="space-y-3">
              <a
                :href="`mailto:${contactInfo.email}`"
                class="flex items-center gap-3 p-3 rounded-lg bg-white border border-[#E3E6EA] hover:border-[#2451B8] transition-all duration-300 cursor-pointer group"
              >
                <div class="w-10 h-10 rounded-full bg-[#EEF2FB] flex items-center justify-center shrink-0">
                  <i class="fas fa-envelope text-[#2451B8]"></i>
                </div>
                <div class="min-w-0">
                  <p class="font-medium text-sm">Email</p>
                  <p class="text-[#667085] group-hover:text-[#2451B8] transition-colors text-sm truncate">{{ contactInfo.email }}</p>
                </div>
              </a>

              <a
                :href="`https://wa.me/${contactInfo.phone.replace(/\D/g, '')}`"
                target="_blank"
                rel="noopener noreferrer"
                class="flex items-center gap-3 p-3 rounded-lg bg-white border border-[#E3E6EA] hover:border-[#22A06B] transition-all duration-300 cursor-pointer group"
              >
                <div class="w-10 h-10 rounded-full bg-[#E7F6EF] flex items-center justify-center shrink-0">
                  <i class="fab fa-whatsapp text-[#22A06B]"></i>
                </div>
                <div class="min-w-0">
                  <p class="font-medium text-sm">Phone / WhatsApp</p>
                  <p class="text-[#667085] group-hover:text-[#22A06B] transition-colors text-sm">{{ contactInfo.phone }}</p>
                </div>
              </a>

              <div class="flex items-center gap-3 p-3 rounded-lg bg-white border border-[#E3E6EA]">
                <div class="w-10 h-10 rounded-full bg-[#EEF2FB] flex items-center justify-center shrink-0">
                  <i class="fas fa-map-marker-alt text-[#2451B8]"></i>
                </div>
                <div class="min-w-0">
                  <p class="font-medium text-sm">Location</p>
                  <p class="text-[#667085] text-sm">{{ contactInfo.location }}</p>
                </div>
              </div>
            </div>
          </div>

          <form @submit.prevent="submitContactForm" class="grid gap-4" data-aos="fade-up" data-aos-delay="100">
            <input
              v-model="contactForm.name"
              type="text"
              placeholder="Your Name"
              class="bg-white border border-[#D0D5DD] p-3 rounded-lg w-full focus:ring-2 focus:ring-[#2451B8] focus:border-transparent transition-all min-h-[44px]"
              :disabled="isSending"
              required
            >
            <input
              v-model="contactForm.email"
              type="email"
              placeholder="Your Email"
              class="bg-white border border-[#D0D5DD] p-3 rounded-lg w-full focus:ring-2 focus:ring-[#2451B8] focus:border-transparent transition-all min-h-[44px]"
              :disabled="isSending"
              required
            >
            <textarea
              v-model="contactForm.message"
              placeholder="Your Message"
              rows="5"
              class="bg-white border border-[#D0D5DD] p-3 rounded-lg w-full focus:ring-2 focus:ring-[#2451B8] focus:border-transparent transition-all resize-none"
              :disabled="isSending"
              required
            ></textarea>

            <button
              type="submit"
              :disabled="isSending"
              class="min-h-[44px] px-6 py-3 bg-[#101828] text-white rounded-lg font-medium hover:bg-[#2451B8] transition-all flex items-center justify-center gap-2 disabled:bg-[#98A2B3] disabled:cursor-not-allowed"
            >
              <i v-if="isSending" class="fas fa-spinner fa-spin"></i>
              <i v-else class="fas fa-paper-plane"></i>
              {{ isSending ? 'Sending Message...' : 'Send Message' }}
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-[#101828] py-8 mt-auto">
      <div class="max-w-6xl mx-auto px-4">
        <div class="flex flex-col md:flex-row justify-between items-center gap-4 text-center md:text-left">
          <div class="flex items-baseline gap-2.5">
            <span class="font-['Sora'] text-lg font-bold tracking-tight text-white">
              Ariel<span class="text-[#E76F51]">.</span>
            </span>
            <span class="hidden sm:inline text-xs font-medium text-[#98A2B3] border-l border-[#344054] pl-2.5 tracking-wide">
              Fullstack Developer
            </span>
          </div>
          <div class="flex gap-6">
            <a v-for="(social, index) in socialLinks" :key="index" :href="social.url" class="text-[#98A2B3] hover:text-white transition-colors p-1" target="_blank" rel="noopener">
              <i :class="social.icon" class="text-xl"></i>
            </a>
          </div>
          <p class="text-sm text-[#98A2B3]">© {{ currentYear }} Ariel Fajar Herdanto</p>
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
      isSending: false,
      technicalSkills: [
        { name: 'HTML/CSS', percentage: 90, icon: '/images/html.png' },
        { name: 'JavaScript', percentage: 85, icon: '/images/javascript.png' },
        { name: 'Vue.js', percentage: 80, icon: '/images/vuejs.png' },
        { name: 'Laravel', percentage: 75, icon: '/images/laravel.png' },
        { name: 'React.js', percentage: 70, icon: '/images/react.png' },
        { name: 'PHP', percentage: 80, icon: '/images/php.png' },
        { name: 'Python', percentage: 75, icon: '/images/python.png' },
        { name: 'Java', percentage: 75, icon: '/images/java.png' },
        { name: 'MySQL', percentage: 85, icon: '/images/mysql.png' }
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
          title: 'Web Developer / IT Intern (Pemagangan Nasional)',
          company: 'PT. Boltz Indonesia',
          period: 'Oct 2025 - Apr 2026',
          description: 'During this national internship in the HRGA division, I successfully:',
          logo: '/images/maganghub_logo.png',
          icon: 'fas fa-industry',
          achievements: [
            'Built and maintained four internal Laravel web systems: Portal Website, Attendance System, Employee Self-Service (ESS), and Consumable Control System (CCS)',
            'Enhanced the Kaizen module with editable approval fields and role-based approval logic',
            'Integrated Laravel with SharePoint using Azure AD (OAuth) authentication',
            'Delivered a final project presentation and a system manual book to HRGA management'
          ]
        },
        {
          title: 'Kegiatan Magang Mahasiswa',
          company: 'PT Jababeka Tbk',
          period: 'Jan 2025 - Feb 2025',
          description: 'During this program, I successfully:',
          logo: '/images/logojbk.png',
          icon: null,
          achievements: [
            'Deploying and integrating the website to be publicly accessible',
            'Improving features for better usability',
            'Conducting testing with Jababeka HR Director and staff',
            'Coordinated with cross-divisional teams to ensure smooth system integration'
          ]
        },
        {
          title: 'MSIB Batch 7',
          company: 'PT Jababeka Tbk',
          period: 'Aug 2024 - Dec 2024',
          description: 'During this program, I successfully:',
          logo: '/images/msib.png',
          icon: null,
          achievements: [
            'Designing UI/UX and prototype for Jababeka Learning (LMS)',
            'Developing front-end using Vue.js',
            'Creating CDM and PDM',
            'Developing back-end using Laravel 11',
            'Coordinated with cross-divisional teams to ensure smooth system integration'
          ]
        },
        {
          title: 'MSIB Batch 6',
          company: 'PT Jababeka Tbk',
          period: 'Feb 2024 - Jun 2024',
          description: 'During this program, I successfully:',
          logo: '/images/msib.png',
          icon: null,
          achievements: [
            'Improved system performance with query optimization and database structure',
            'Developed new features on purchasing platform based on Laravel',
            'Fixing Purchasing System bugs and issues',
            'Fixing annual budget calculation as well as reimburse and PUM functions',
            'Improved user interface to be more intuitive and responsive',
            'Coordinated with cross-divisional teams to ensure smooth system integration'
          ]
        }
      ],
      projects: [
        {
          title: 'Portal Website Boltz',
          description: 'Official website of PT. Boltz Indonesia serving as a public information hub and gateway to internal applications.',
          gradient: 'bg-gradient-to-r from-teal-500 to-emerald-600',
          useImage: true,
          image: '/images/portalboltz.png',
          icon: 'fas fa-globe',
          technologies: [
            { name: 'Laravel', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'Tailwind CSS', color: 'bg-[#E7F6EF] text-[#22A06B] border-[#CDEEDD]' },
            { name: 'MySQL', color: 'bg-[#FBEEE9] text-[#E76F51] border-[#F5D9CC]' }
          ]
        },
        {
          title: 'Attendance System',
          description: 'A web-based employee attendance management system. Integrates data from tap in/out machines, manages monthly recaps, overtime, work calendars, and centralized attendance reporting.',
          gradient: 'bg-gradient-to-r from-blue-500 to-indigo-600',
          useImage: true,
          image: '/images/attendance-boltz.png',
          icon: 'fas fa-user-clock',
          technologies: [
            { name: 'Laravel', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'Chart.js', color: 'bg-[#FDF2FA] text-[#C11574] border-[#FCCEEE]' },
            { name: 'REST API', color: 'bg-[#F0F9FF] text-[#026AA2] border-[#B9E6FE]' }
          ]
        },
        {
          title: 'Employee Self Service (ESS)',
          description: 'A centralized digital employee data management system. Manages worker data, identity documents, medical benefits, family data, interns, as well as Kaizen management with a reward feature.',
          gradient: 'bg-gradient-to-r from-orange-400 to-rose-500',
          useImage: true,
          image: '/images/ess-boltz.png',
          icon: 'fas fa-users-cog',
          technologies: [
            { name: 'Laravel', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'Bootstrap 5', color: 'bg-[#F3E8FF] text-[#6941C6] border-[#E4D7FF]' },
            { name: 'REST API', color: 'bg-[#F0F9FF] text-[#026AA2] border-[#B9E6FE]' }
          ]
        },
        {
          title: 'Consumable Control System (CCS)',
          description: 'A digital consumable inventory management system. Manages stock, inbound/outbound transactions via QR Code, inter-section requests, and usage recaps.',
          gradient: 'bg-gradient-to-r from-pink-500 to-rose-600',
          useImage: true,
          image: '/images/ccs-boltz.png',
          icon: 'fas fa-qrcode',
          technologies: [
            { name: 'Laravel', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'QR Code API', color: 'bg-[#FDF2FA] text-[#C11574] border-[#FCCEEE]' },
            { name: 'PHPSpreadsheet', color: 'bg-[#E7F6EF] text-[#22A06B] border-[#CDEEDD]' }
          ]
        },
        {
          title: 'Jababeka Learning',
          description: 'Learning Management System (LMS) based on Laravel & Vue.js to manage training, certifications, and training recommendations at PT Jababeka Tbk.',
          gradient: 'bg-gradient-to-r from-blue-500 to-purple-600',
          useImage: true,
          image: '/images/lms.png',
          icon: 'fas fa-laptop-code',
          technologies: [
            { name: 'Laravel', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'Vue.js', color: 'bg-[#E7F6EF] text-[#22A06B] border-[#CDEEDD]' },
            { name: 'MySQL', color: 'bg-[#FBEEE9] text-[#E76F51] border-[#F5D9CC]' }
          ]
        },
        {
          title: 'JBPURC Jababeka',
          description: 'Jababeka Purchasing (JBPURC) web system for vendor management, purchase monitoring, and approval workflow optimization.',
          gradient: 'bg-gradient-to-r from-green-500 to-teal-600',
          useImage: true,
          image: '/images/purchasing.png',
          icon: 'fas fa-shopping-cart',
          technologies: [
            { name: 'Laravel', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'AJAX', color: 'bg-[#E7F6EF] text-[#22A06B] border-[#CDEEDD]' },
            { name: 'JavaScript', color: 'bg-[#FBEEE9] text-[#E76F51] border-[#F5D9CC]' }
          ]
        },
        {
          title: 'Budgetting Jababeka',
          description: 'Jababeka Budgeting System for efficient digital financial planning and analysis.',
          gradient: 'bg-gradient-to-r from-purple-500 to-pink-600',
          useImage: true,
          image: '/images/budget.png',
          icon: 'fas fa-chart-line',
          technologies: [
            { name: 'Java', color: 'bg-[#EEF2FB] text-[#2451B8] border-[#D6E0F5]' },
            { name: 'GUI', color: 'bg-[#FDECEC] text-[#D92D20] border-[#F9D5D5]' },
            { name: 'MySQL', color: 'bg-[#FBEEE9] text-[#E76F51] border-[#F5D9CC]' }
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
        { name: 'LinkedIn', icon: 'fab fa-linkedin', url: 'https://www.linkedin.com/in/arielfajarh' },
        { name: 'GitHub', icon: 'fab fa-github', url: 'https://github.com/arielfajar' },
        { name: 'Instagram', icon: 'fab fa-instagram', url: 'https://instagram.com/arielfajar' }
      ]
    }
  },
  mounted() {
    // Konfigurasi AOS yang lebih stabil untuk mobile
    AOS.init({
      duration: 600,
      easing: 'ease-out-cubic',
      once: true,           // animasi hanya sekali (tidak reset saat scroll balik)
      mirror: false,
      offset: 80,           // jarak trigger dari bawah viewport
      anchorPlacement: 'top-bottom',
      disable: () => window.matchMedia('(prefers-reduced-motion: reduce)').matches
    });

    // Refresh AOS setelah gambar & layout selesai dimuat (fix animasi tidak muncul di HP)
    window.addEventListener('load', () => AOS.refresh());
    // Refresh lagi jika ada resize/orientation change (misal rotate HP)
    let resizeTimer;
    window.addEventListener('resize', () => {
      clearTimeout(resizeTimer);
      resizeTimer = setTimeout(() => AOS.refresh(), 200);
    });

    window.addEventListener('scroll', this.handleScroll);
    this.animateSkillBars();
    emailjs.init("eTFDsabna1YryLWcv");

    // Refresh AOS setelah mount agar elemen dinamis (v-for) terdeteksi
    this.$nextTick(() => AOS.refresh());
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const sections = ['about', 'skills', 'education', 'experience', 'projects', 'contact'];
      const scrollPosition = window.scrollY + 120;

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
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.3 });

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

        await emailjs.send(
          'service_sa69l58',
          'template_ycyzcwy', // ⚠️ Ganti dengan template ID Anda yang benar!
          templateParams,
          'eTFDsabna1YryLWcv'
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
      const notification = document.createElement('div');
      notification.className = `fixed top-20 md:top-4 right-4 left-4 md:left-auto p-4 rounded-lg shadow-lg z-[100] transform transition-all duration-300 max-w-sm mx-auto md:mx-0 bg-white text-[#101828] ${
        type === 'success' ? 'border-l-4 border-[#22A06B]' : 'border-l-4 border-[#D92D20]'
      }`;

      notification.innerHTML = `
        <div class="flex items-center gap-3">
          <i class="fas ${type === 'success' ? 'fa-check-circle text-[#22A06B]' : 'fa-exclamation-circle text-[#D92D20]'}"></i>
          <span>${message}</span>
        </div>
      `;

      document.body.appendChild(notification);

      setTimeout(() => {
        notification.style.transform = 'translateX(0)';
      }, 100);

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
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@600;700;800&family=Inter:wght@400;500;600;700&display=swap');

:global(html) {
  scroll-behavior: smooth;
  -webkit-text-size-adjust: 100%;
}
:global(body) {
  overflow-x: hidden;
}
section[id] {
  scroll-margin-top: 5rem;
}

.skill-bar {
  height: 8px;
  background-color: #E4E7EC;
  border-radius: 4px;
  overflow: hidden;
}
.skill-progress {
  height: 100%;
  border-radius: 4px;
  transition: width 1s ease-in-out;
}
.nav-link.active {
  color: #2451B8;
  font-weight: 600;
}

/* Fallback: jika JS AOS gagal load, elemen tetap terlihat */
[data-aos] {
  pointer-events: auto;
}
[data-aos]:not(.aos-animate) {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}
[data-aos].aos-animate {
  opacity: 1;
  transform: translateY(0);
}
</style>