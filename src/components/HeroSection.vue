<script setup>
import { ArrowDownCircleIcon } from "@heroicons/vue/24/outline";
import profil from "../assets/images/profil/sariko1.png";
import django from "../assets/images/techno/django.svg";
import laravel from "../assets/images/techno/Laravel.svg.png";
import vueJs from "../assets/images/techno/physics.png";

import pdf from "../assets/cv_arsene.pdf"
</script>

<template>
  <section id="hero" class="min-h-screen flex items-center py-10 px-2 sm:py-20 sm:px-6 pt-30">
    <div class="container mx-auto">
      <div class="flex flex-col-reverse sm:flex-col lg:flex-row items-center gap-8 sm:gap-12 lg:gap-16">
        <div class="w-full sm:w-3/4 lg:w-2/5 flex flex-col items-center mx-auto">
          <div class="photo-container mb-8 sm:mb-12">
            <div
              class="relative w-40 h-40 sm:w-64 sm:h-64 md:w-80 md:h-80 rounded-full overflow-hidden border-4 border-green-400 shadow-lg">
              <img :src="profil" alt="Photo de profil Arsène"
                class="w-full h-full object-cover transition-transform duration-500 hover:scale-105 hover:rotate-2 bg-[#080f2c]"
                aria-label="Photo de profil" />
            </div>
            <div class="text-white space-y-2 sm:space-y-4 mt-2 sm:mt-4 w-full">
              <div class="flex flex-col gap-2 sm:gap-3 items-start text-xs sm:text-base">
                <div class="flex items-center gap-2 sm:gap-3">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-400" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M5.121 17.804A13.937 13.937 0 0112 15c2.5 0 4.847.657 6.879 1.804M15 10a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                  <span class="font-bold text-sm md:text-xl">RATSIMBASON Faly Tiana Arsène</span>
                </div>
                <div class="flex items-center gap-2 sm:gap-3">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-400" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                  </svg>
                  <span class="font-semibold">20 ans</span>
                </div>
                <div class="flex items-center gap-2 sm:gap-3">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-400" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M17.657 16.657L13.414 12.414a4 4 0 10-5.657 5.657l4.243 4.243a8 8 0 1011.314-11.314z" />
                  </svg>
                  <span class="font-semibold">Lot Ivk 19 D à Antanjombe</span>
                </div>
                <a href="https://github.com/Arsene-Faly" target="_blank"
                  class="flex items-center gap-2 sm:gap-3 text-green-400 hover:underline">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-green-400" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.483 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.342-3.369-1.342-.454-1.154-1.11-1.461-1.11-1.461-.908-.62.069-.608.069-.608 1.004.07 1.532 1.032 1.532 1.032.892 1.529 2.341 1.088 2.91.833.091-.646.35-1.088.636-1.34-2.221-.253-4.555-1.112-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.338 1.909-1.294 2.748-1.025 2.748-1.025.546 1.378.202 2.397.099 2.65.64.7 1.028 1.595 1.028 2.688 0 3.847-2.337 4.695-4.566 4.944.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.744 0 .268.18.579.688.481C19.135 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z" />
                  </svg>
                  <span class="font-semibold">github.com/Arsene-Faly</span>
                </a>
              </div>
            </div>
          </div>

          <h3 class="text-base sm:text-xl font-semibold mb-2 text-center underline underline-offset-8">
            Compétences techniques
          </h3>
          <div class="flex justify-center gap-4 sm:gap-8 flex-wrap">
            <!-- Laravel Heroicon SVG -->
            <div class="tech-logo group flex flex-col items-center w-1/3 sm:w-auto">
              <div
                class="w-14 h-14 sm:w-20 sm:h-20 border border-gray-700 rounded-full flex items-center justify-center mb-2 shadow-lg group-hover:scale-110 transition-transform duration-300">
                <img :src="laravel" alt="Laravel" class="h-8 w-8 sm:h-12 sm:w-12 object-contain" />
              </div>
              <span class="text-xs sm:text-base font-bold text-white">Laravel</span>
            </div>

            <!-- Django Heroicon SVG -->
            <div class="tech-logo group flex flex-col items-center w-1/3 sm:w-auto">
              <div
                class="w-14 h-14 sm:w-20 sm:h-20 border border-gray-700 rounded-full flex items-center justify-center mb-2 shadow-lg group-hover:scale-110 transition-transform duration-300">
                <img :src="django" alt="Django" class="h-8 w-8 sm:h-12 sm:w-12 object-contain" />
              </div>
              <span class="text-xs sm:text-base font-bold text-white">Django</span>
            </div>

            <!-- Vue.js Heroicon SVG -->
            <div class="tech-logo group flex flex-col items-center w-1/3 sm:w-auto">
              <div
                class="w-14 h-14 sm:w-20 sm:h-20 border border-gray-700 rounded-full flex items-center justify-center mb-2 shadow-lg group-hover:scale-110 transition-transform duration-300">
                <img :src="vueJs" alt="Vue.js" class="h-8 w-8 sm:h-12 sm:w-12 object-contain" />
              </div>
              <span class="text-xs sm:text-base font-bold text-white">React Js</span>
            </div>
          </div>
        </div>

        <!-- Texte de présentation -->
        <div class="w-full sm:w-11/12 lg:w-3/5 mx-auto">
          <h1 class="text-2xl sm:text-4xl md:text-5xl lg:text-6xl font-bold mb-4 sm:mb-6 text-center sm:text-left">
            <span
              class="bg-gradient-to-l from-green-100 to-green-400 bg-clip-text text-transparent text_shadow text-shine">
              Développeur Full Stack <br />
              Spécialisé en
            </span>
            <span
              class="bg-gradient-to-r from-green-600 via-green-400 to-green-300 bg-clip-text text-transparent text_shadow text-shine">
              Laravel,
            </span>
            <span
              class="bg-gradient-to-r from-green-700 via-green-500 to-green-300 bg-clip-text text-transparent text_shadow text-shine">
              Django &
            </span>
            <span
              class="bg-gradient-to-r from-green-400 via-green-300 to-green-200 bg-clip-text text-transparent text_shadow text-shine">
              React js
            </span>
          </h1>

          <p
            class="text-sm sm:text-lg md:text-xl text-white drop-shadow-[0_2px_6px_rgba(0,0,0,0.5)] mb-4 sm:mb-8 max-w-full sm:max-w-2xl text-center sm:text-left">
            Je crée des applications web performantes avec les frameworks
            backend et frontend les plus modernes.
          </p>

          <div class="flex flex-wrap gap-2 sm:gap-4 mb-6 sm:mb-10 justify-center sm:justify-start">
            <div class="flex items-center bg-dark-800 px-2 sm:px-4 py-1 sm:py-2 rounded-full text-xs sm:text-base">
              <div class="w-3 h-3 rounded-full mr-2 bg-gradient-to-l from-green-500 to-green-300 animate-bounce"></div>
              <span>Disponible pour missions</span>
            </div>
            <div class="flex items-center bg-dark-800 px-2 sm:px-4 py-1 sm:py-2 rounded-full text-xs sm:text-base">
              <div
                class="w-3 h-3 rounded-full mr-2 bg-gradient-to-r from-green-400 via-green-300 to-green-200 animate-pulse">
              </div>
              <span>1+ ans d'expérience</span>
            </div>
          </div>

          <div class="flex flex-col sm:flex-row gap-2 sm:gap-4">
            <a :href="pdf" download
              class="bg-gradient-to-r from-green-500 to-green-700 hover:bg-green-800 text-white text-base sm:text-lg font-bold px-4 sm:px-8 py-2 sm:py-4 rounded-lg transition flex-1 text-center flex items-center justify-center gap-2">
              Télécharger mon CV
            </a>
            <a href="#projets"
              class="border border-green-600 text-green-400 hover:bg-green-900 text-base sm:text-lg font-bold px-4 sm:px-8 py-2 sm:py-4 rounded-lg transition flex-1 text-center">
              Voir mes réalisations
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.text-shine {
  background-size: 200% 100%;
  animation: shine 5s linear infinite;
}

@keyframes shine {
  0% {
    background-position: -200% center;
  }

  100% {
    background-position: 200% center;
  }
}

/* Mobile styles (inférieur à sm) */
@media (max-width: 639px) {
  #hero {
    min-height: 100vh;
    padding: 70px 2px 10px 2px;
    /* 70px pour navbar fixé */
  }

  .photo-container {
    margin-bottom: 2rem;
  }

  .photo-container .relative {
    width: 160px;
    height: 160px;
    margin: auto;
  }

  .tech-logo span {
    font-size: 0.75rem;
  }

  h1 {
    font-size: 1.6rem;
    text-align: center;
    margin-bottom: 1rem;
  }

  p {
    font-size: 0.95rem;
    text-align: center;
    margin-bottom: 1rem;
  }

  .flex-wrap {
    gap: 0.5rem;
    margin-bottom: 1.5rem;
    justify-content: center;
  }

  .flex-col {
    gap: 0.5rem;
  }

  .rounded-lg {
    padding: 0.5rem 1rem;
    font-size: 1rem;
  }
}
</style>