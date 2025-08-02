<script setup>
import { ref } from "vue";

// === Imports d'images ===
// Backend
import django from "../assets/images/techno/django.svg";
import laravel from "../assets/images/techno/Laravel.svg.png";
import node from "../assets/images/techno/node.png";

// Frontend
import vueJs from "../assets/images/techno/vue.png";
import react from "../assets/images/techno/physics.png"; // Remplacer le nom si besoin

// CSS Frameworks
import Tailwind from "../assets/images/techno/Tailwind_CSS_Logo.svg.png";
import Bootstrap from "../assets/images/techno/bootstrap.png";

// Langages
import js from "../assets/images/techno/js.png";
import php from "../assets/images/techno/php.png";
import python from "../assets/images/techno/python.png";

// Bases de données
import mysql from "../assets/images/techno/mysql.png";
import sqlite from "../assets/images/techno/database.png";
import pgsql from "../assets/images/techno/Postgresql_elephant.svg";

import git from "../assets/images/techno/github.png";

const competences = ref({
  "Framework Backend": [
    {
      id: 1,
      img: laravel,
      name: "Laravel",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description:
        "Développement d’applications web robustes en architecture MVC avec gestion efficace des bases de données.",
      alt: "Logo Laravel",
    },
    {
      id: 2,
      img: django,
      name: "Django",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description:
        "Conception d’applications sécurisées et scalables avec intégration d’APIs RESTful.",
      alt: "Logo Django",
    },
    {
      id: 3,
      img: node,
      name: "Node Js",
      niveau: "Débutant",
      percent: 20,
      style: "width: 20%",
      description:
        "Compétences fondamentales en développement backend JavaScript avec Express.js.",
      alt: "Logo Node.js",
    },
  ],
  "Framework Frontend": [
    {
      id: 4,
      img: vueJs,
      name: "Vue.js",
      niveau: "Intermédiaire",
      percent: 50,
      style: "width: 50%",
      description:
        "Développement d’interfaces réactives, gestion de composants et intégration d’API REST.",
      alt: "Logo Vue.js",
    },
    {
      id: 5,
      img: react,
      name: "React",
      niveau: "Débutant",
      percent: 20,
      style: "width: 20%",
      description:
        "Création d’applications SPA avec gestion de composants et intégration d’API REST.",
      alt: "Logo React",
    },
  ],
  "Framework CSS": [
    {
      id: 6,
      img: Tailwind,
      name: "Tailwind CSS",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description: "Utilisation pour du design responsive et rapide",
      alt: "Logo Tailwind CSS",
    },
    {
      id: 7,
      img: Bootstrap,
      name: "Bootstrap",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description:
        "Création de maquettes rapides avec grilles et composants UI",
      alt: "Logo Bootstrap",
    },
  ],
  Programmation: [
    {
      id: 8,
      img: php,
      name: "PHP",
      niveau: "Intermédiaire",
      percent: 70,
      style: "width: 70%",
      description:
        "Développement d'APIs, sites dynamiques et gestion de bases de données",
      alt: "Logo PHP",
    },
    {
      id: 9,
      img: js,
      name: "JavaScript",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description:
        "Développement front-end et back-end, applications web dynamiques",
      alt: "Logo JavaScript",
    },
    {
      id: 10,
      img: python,
      name: "Python",
      niveau: "Intermédiaire",
      percent: 65,
      style: "width: 65%",
      description: "Scripts, automatisation, APIs et data science",
      alt: "Logo Python",
    },
  ],
  "Base de données": [
    {
      id: 11,
      img: mysql,
      name: "MySQL",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description:
        "Conception, optimisation et gestion de bases de données relationnelles",
      alt: "Logo MySQL",
    },
    {
      id: 12,
      img: sqlite,
      name: "SQLite",
      niveau: "Intermédiaire",
      percent: 70,
      style: "width: 70%",
      description: "Utilisation pour des applications légères et embarquées",
      alt: "Logo SQLite",
    },
    {
      id: 13,
      img: pgsql,
      name: "PostgreSQL",
      niveau: "Intermédiaire",
      percent: 60,
      style: "width: 60%",
      description:
        "Utilisation pour des applications robustes avec contraintes complexes",
      alt: "Logo PostgreSQL",
    },
  ],
  Outils: [
    {
      id: 14,
      img: git,
      name: "GitHub",
      niveau: "Intermédiaire",
      percent: 50,
      style: "width: 50%",
      description:
        "Gestion de code source, collaboration et versioning avec GitHub",
      alt: "Logo GitHub",
    },
  ],
});
</script>

<template>
  <div id="competences" class="py-20 px-6"></div>
  <section class="xl:ml-10">
    <div class="container mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold text-center mb-4">
          Mes <span class="text-green-400">Expertises</span>
        </h2>
        <p class="text-gray-400 max-w-2xl mx-auto">
          Survolez chaque technologie pour voir mon niveau de maîtrise
        </p>
      </div>

      <!-- Séparation par catégorie -->
      <div v-for="(items, type) in competences" :key="type" class="mb-16 cursor-pointer">
        <h3
          class="text-4xl font-extrabold text-green-400 mb-8 text-left border-l-4 border-green-400 pl-4 bg-[#080f2c]"
        >
          {{ type }}
        </h3>
        <div
          class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-10 px-2 ml-2"
        >
          <div
            v-for="data in items"
            :key="data.id"
            class="skill-card bg-[#080f2c] rounded-3xl p-8 flex flex-col items-center h-72 relative group"
          >
            <div
              v-if="data.img"
              class="w-20 h-20 mb-4 flex items-center justify-center"
            >
              <img :src="data.img" alt="Image" class="h-16 skill-logo" />
            </div>
            <div v-else class="w-20 h-20 mb-4 flex items-center justify-center">
              <span class="text-4xl text-green-400 font-bold">{{
                data.name.charAt(0)
              }}</span>
            </div>
            <span
              class="text-xl font-bold mb-1 text-green-300 tracking-wide flex justify-center items-center gap-2"
            >
              {{ data.name }}
            </span>
            <span class="badge-niveau mb-2">{{ data.niveau }}</span>
            <div class="skill-info">
              <div class="text-xs font-bold text-green-400 mb-2 text-center">
                {{ data.niveau }}
              </div>
              <div class="flex justify-end">
                <span class="text-xs">{{ data.percent }} %</span>
              </div>
              <div
                class="skill-level mb-3"
                title="Maîtrise : {{ data.percent }}%"
              >
                <div class="skill-level-bar" :style="data.style"></div>
              </div>

              <p class="text-xs text-gray-300 text-center">
                {{ data.description }}
              </p>
            </div>
            <div class="glow-border"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skill-card {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.18);
  border-radius: 1.5rem;
}
.skill-card .glow-border {
  pointer-events: none;
  position: absolute;
  inset: 0;
  border-radius: 1.5rem;
  border: 2px solid transparent;
  background: linear-gradient(
    120deg,
    rgba(34, 197, 94, 0.3),
    rgba(16, 185, 129, 0.2),
    rgba(59, 130, 246, 0.15)
  );
  opacity: 0;
  transition: opacity 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  z-index: 1;
}
.skill-card:hover .glow-border {
  opacity: 1;
}
.badge-niveau {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  font-size: 0.85rem;
  font-weight: 700;
  color: #fff;
  background: linear-gradient(90deg, #22c55e, #0ea5e9);
  border-radius: 999px;
  box-shadow: 0 2px 8px rgba(34, 197, 94, 0.15);
  letter-spacing: 0.03em;
}
.skill-info {
  position: absolute;
  bottom: -100%;
  left: 0;
  right: 0;
  background: rgba(15, 23, 42, 0.97);
  padding: 1.2rem;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  backdrop-filter: blur(7px);
  z-index: 2;
}
.skill-card:hover .skill-info {
  bottom: 0;
}
.skill-card:hover {
  transform: translateY(-10px) scale(1.04);
  box-shadow: 0 20px 48px rgba(34, 197, 94, 0.18),
    0 16px 40px rgba(0, 0, 0, 0.35);
}
.skill-logo {
  filter: grayscale(30%) brightness(1.2);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
.skill-card:hover .skill-logo {
  filter: grayscale(0%) brightness(1.5);
  transform: scale(1.15);
}
.skill-level {
  height: 8px;
  background: #334155;
  border-radius: 4px;
  overflow: hidden;
}
.skill-level-bar {
  height: 100%;
  background: linear-gradient(90deg, #22c55e, #0ea5e9);
}
</style>
