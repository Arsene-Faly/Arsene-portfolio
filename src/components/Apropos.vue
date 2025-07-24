<template>
  <div id="apropos" class="py-16 px-6"></div>
  <section>
    <div class="container mx-auto w-full">
      <h2 class="text-4xl font-extrabold text-center mb-8 tracking-tight">À <span class="text-green-400">Propos</span></h2>
      <div class="flex flex-col items-center">
        <!-- Carte infos sans photo -->
        <div class="bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 border border-green-700 rounded-2xl p-4 lg:p-8 shadow-xl ml-2">
          <p class="text-gray-300 text-lg mb-6 text-center">
Passionné par le développement web, je m'appelle Arsène et j'ai 20 ans. J'aime concevoir des applications robustes côté backend, tout en veillant à leur accessibilité et à un design soigné côté frontend.          </p>
          <ul class="space-y-3 mb-8">
            <li><span class="font-bold text-green-400">Nom :</span> RATSIMBASON Faly Tiana Arsène</li>
            <li><span class="font-bold text-green-400">Âge :</span> 20 ans</li>
            <li><span class="font-bold text-green-400">Localisation :</span> Lot Ivk 19 D à Antanjombe</li>
            <li><span class="font-bold text-green-400">Spécialités :</span> Laravel, Django, Vue.js</li>
            <li><span class="font-bold text-green-400">Contact :</span> <a href="mailto:arsenefaly1@gmail.com" class="text-green-400 hover:underline">arsenefaly1@gmail.com</a></li>
          </ul>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <div>
              <h3 class="text-2xl font-bold text-green-400 mb-4">Mon parcours professionnel</h3>
              <div class="space-y-4">
                <div class="bg-gray-800 rounded-lg p-4 shadow transition-transform duration-300 hover:scale-105 hover:border-green-400 border border-transparent">
                  <h4 class="font-bold text-lg text-white mb-1">Stagiaire – Développeur d'applications de gestion budgétaire</h4>
                  <p class="text-gray-400 text-sm">2024</p>
                  <p class="text-gray-300">Création de dashboards de gestion financière avec Django, orientés suivi des dépenses et génération de rapports.</p>
                </div>
                <div class="bg-gray-800 rounded-lg p-4 shadow transition-transform duration-300 hover:scale-105 hover:border-green-400 border border-transparent">
                  <h4 class="font-bold text-lg text-white mb-1">Stagiaire – Développeur d’un logiciel de gestion de bibliothèque</h4>
                  <p class="text-gray-400 text-sm">2020 - 2022</p>
                  <p class="text-gray-300">Développement d’un logiciel de gestion de bibliothèque avec Python : enregistrement des livres, suivi des emprunts/retours, et gestion des utilisateurs.</p>
                </div>
                <div class="bg-gray-800 rounded-lg p-4 shadow transition-transform duration-300 hover:scale-105 hover:border-green-400 border border-transparent">
                  <h4 class="font-bold text-lg text-white mb-1">Stagiaire – Stage de découverte au EDUC PLUS</h4>
                  <p class="text-gray-400 text-sm">2019 - 2020</p>
                  <p class="text-gray-300">Observation et participation aux activités administratives et pédagogiques dans un établissement secondaire, dans le cadre d’un stage d’orientation scolaire.</p>
                </div>
              </div>
            </div>
            <div>
              <h3 class="text-2xl font-bold text-green-400 mb-4">Mes études</h3>
              <div class="space-y-4">
                <div class="bg-gray-800 rounded-lg p-4 shadow transition-transform duration-300 hover:scale-105 hover:border-green-400 border border-transparent">
                  <h4 class="font-bold text-lg text-white mb-1">Licence Informatique – ESMIA Mahamasina</h4>
                  <p class="text-gray-400 text-sm">2022 - 2024</p>
                  <p class="text-gray-300">Spécialisation en développement web et conception de bases de données, avec une orientation vers les risques et la prise de décision.</p>
                </div>
                <div class="bg-gray-800 rounded-lg p-4 shadow transition-transform duration-300 hover:scale-105 hover:border-green-400 border border-transparent">
                  <h4 class="font-bold text-lg text-white mb-1">Baccalauréat – Lycée Privé La Croyance, Andavamamba</h4>
                  <p class="text-gray-400 text-sm">2020 - 2021</p>
                  <p class="text-gray-300">Bases solides en programmation, algorithmique et conception d'applications.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Pas de logique JS nécessaire ici
</script>

<style scoped>
/* Responsive et design moderne */
</style>
