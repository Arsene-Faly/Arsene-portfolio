<script setup>
import { ref } from "vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/solid";
import { EnvelopeIcon } from "@heroicons/vue/24/outline";

const isMobileMenuOpen = ref(false);
const currentYear = new Date().getFullYear();
const menuLinks = [
  { id: "accueil", label: "Accueil" },
  { id: "apropos", label: "À propos" },
  { id: "projets", label: "Projets" },
  { id: "competences", label: "Compétences" },
  { id: "contact", label: "Contact" },
];

function handleNavClick(id, isMobile = false) {
  const el = document.getElementById(id);
  if (el) el.scrollIntoView({ behavior: "smooth" });
  if (isMobile) isMobileMenuOpen.value = false;
}
</script>

<template>
  <div id="accueil" class="py-1 px-1"></div>
  <div class="bg-[#020617] text-white font-sans">
    <!-- NAVBAR -->
    <nav
      class="bg-[#080f2c] py-4 px-6 shadow-xl fixed top-0 z-50 rounded-3xl w-[98%] max-w-7xl left-1/2 -translate-x-1/2 mt-5">
      <div class="flex justify-between items-center">
        <a href="#accueil"
          class="logo text-3xl font-extrabold tracking-wide text-green-700 hover:text-green-300 transition">Arsène</a>

        <!-- Menu desktop -->
        <div class="hidden md:flex space-x-8">
          <template v-for="link in menuLinks" :key="link.id">
            <a :href="`#${link.id}`" @click.prevent="handleNavClick(link.id)"
              class="font-medium text-lg hover:text-green-400 transition">{{ link.label }}</a>
          </template>
        </div>

        <!-- Bouton toggle mobile -->
        <button @click="isMobileMenuOpen = !isMobileMenuOpen"
          class="md:hidden text-green-400 focus:outline-none cursor-pointer">
          <Bars3Icon v-if="!isMobileMenuOpen" class="h-8 w-8 transition-transform duration-200" />
          <XMarkIcon v-else class="h-8 w-8 transition-transform duration-200" />
        </button>
      </div>

      <!-- Menu mobile -->
      <div v-if="isMobileMenuOpen" class="fixed inset-0 z-50 bg-black/40 backdrop-blur-sm md:hidden"
        aria-label="Menu mobile" @click.self="isMobileMenuOpen = false">
        <div class="absolute left-1/2 -translate-x-1/2 top-8 w-[92%] max-w-[320px] animate-slide-down">
          <div class="relative flex flex-col items-center space-y-4 bg-slate-800/80 rounded-2xl shadow-xl p-4">
            <button @click="isMobileMenuOpen = false"
              class="absolute top-3 right-3 text-green-400 hover:text-green-300 p-2 rounded-full focus:outline-none cursor-pointer"
              style="width:60px;height:60px;display:flex;align-items:center;justify-content:center;z-index:10;">
              <XMarkIcon class="h-12 w-12" />
            </button>
            <template v-for="link in menuLinks" :key="link.id">
              <a :href="`#${link.id}`" @click.prevent="handleNavClick(link.id, true)"
                class="block w-full text-center font-semibold text-base py-3 px-4 rounded-xl bg-slate-700/70 hover:bg-green-400 hover:text-slate-900 transition-all duration-200 shadow">{{
                link.label }}</a>
            </template>
          </div>
        </div>
      </div>
    </nav>


    <!-- CONTENU -->
    <main class="w-[90%] mt-10 mx-auto max-w-7xl">
      <slot />
    </main>

    <!-- FOOTER -->
    <footer class="gradientsection rounded-3xl mx-auto mt-10 w-[90%] mb-5 border border-slate-800 shadow-xl">
      <div class="flex flex-col md:flex-row justify-between items-center gap-4 py-6 px-4">
        <div>
          <a href="#accueil"
            class="text-2xl font-extrabold logo text-green-400 hover:text-green-300 transition">Arsène</a>
          <p class="text-gray-200 mt-1 text-sm">© {{ currentYear }} Tous droits réservés</p>
        </div>
        <div class="flex flex-col sm:flex-row sm:space-x-6 items-start sm:items-center space-y-2 sm:space-y-0">
          <a href="#" class="text-gray-50 hover:text-green-400 transition text-sm">Mentions légales</a>
          <a href="#" class="text-gray-50 hover:text-green-400 transition text-sm">Politique de confidentialité</a>
        </div>
        <div class="flex space-x-4 mt-4 md:mt-0">
          <a href="https://linkedin.com" target="_blank" rel="noopener" class="hover:text-green-400 transition"
            title="LinkedIn">
            <!-- Icon LinkedIn -->
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="..." />
            </svg>
          </a>
          <a href="https://github.com" target="_blank" rel="noopener" class="hover:text-green-400 transition"
            title="GitHub">
            <!-- Icon GitHub -->
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="..." />
            </svg>
          </a>
          <a href="mailto:arsenefaly1@email.com" class="hover:text-green-400 transition" title="Email">
            <EnvelopeIcon class="h-6 w-6" />
          </a>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
/* @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');

.animate-fade-in {
  animation: fadeIn 0.4s ease;
}

.animate-slide-down {
  animation: slideDown 0.4s cubic-bezier(.4,0,.2,1);
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideDown {
  from {
    opacity: 0;
    transform: translateY(-40px) scale(0.98);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
} */
</style>
