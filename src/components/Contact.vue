<template>
  <!-- Section Contact -->
  <div id="contact" class="py-16 px-6"></div>
  <section>
    <div class="container mx-auto max-w-4xl">
      <h2 class="text-4xl font-bold text-center mb-4">
        Contactez-<span class="text-green-400">moi</span>
      </h2>
      <p class="text-gray-400 text-center max-w-2xl mx-auto mb-12">
        Disponible pour des opportunités de collaboration. Réponse garantie sous
        24h.
      </p>

      <div class="flex flex-col md:flex-row gap-12">
        <div class="md:w-1/2">
          <form
            class="space-y-6"
            @submit.prevent="handleSubmit"
            aria-label="Formulaire de contact"
          >
            <div>
              <label for="name" class="block mb-2 text-sm font-medium"
                >Votre nom</label
              >
              <input
                type="text"
                id="name"
                v-model="name"
                required
                aria-required="true"
                aria-label="Nom"
                class="w-full bg-[#080f2c] border border-gray-600 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-green-500"
              />
            </div>
            <div>
              <label for="email" class="block mb-2 text-sm font-medium"
                >Votre email</label
              >
              <input
                type="email"
                id="email"
                v-model="email"
                required
                aria-required="true"
                aria-label="Email"
                class="w-full bg-[#080f2c] border border-gray-600 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-green-500"
              />
            </div>
            <div>
              <label for="message" class="block mb-2 text-sm font-medium"
                >Votre message</label
              >
              <textarea
                id="message"
                rows="4"
                v-model="message"
                required
                aria-required="true"
                aria-label="Message"
                class="w-full bg-[#080f2c] border border-gray-600 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-green-500"
              ></textarea>
            </div>
            <button
              type="submit"
              class="w-full bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-lg transition"
            >
              Envoyer le message
            </button>
            <p v-if="error" class="text-red-500 mt-2">{{ error }}</p>
            <p v-if="success" class="text-green-400 mt-2">Message envoyé !</p>
          </form>
        </div>
        <div class="md:w-1/2">
          <div class="bg-[#080f2c] p-8 rounded-2xl h-full ml-2 space-y-8">
            <!-- Titre Coordonnées -->
            <h3 class="text-xl font-bold mb-4">Coordonnées</h3>

            <!-- Liste coordonnées -->
            <div class="space-y-6">
              <!-- Email -->
              <div class="flex items-start gap-4">
                <span class="mt-1">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6 text-green-400"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M16 12l-4-4-4 4m8 0v6a2 2 0 01-2 2H6a2 2 0 01-2-2v-6"
                    />
                  </svg>
                </span>
                <div>
                  <h4 class="font-bold">Email</h4>
                  <p class="text-gray-400">arsenefaly1@email.com</p>
                </div>
              </div>

              <!-- Téléphone -->
              <div class="flex items-start gap-4">
                <span class="mt-1">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6 text-green-400"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M3 5a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H5a2 2 0 01-2-2V5zm0 10a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H5a2 2 0 01-2-2v-2zm10-10a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V5zm0 10a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                    />
                  </svg>
                </span>
                <div>
                  <h4 class="font-bold">Téléphone</h4>
                  <p class="text-gray-400">+261 34 54 292 33</p>
                </div>
              </div>

              <!-- Localisation -->
              <div class="flex items-start gap-4">
                <span class="mt-1">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6 text-green-400"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M12 11c1.104 0 2-.896 2-2s-.896-2-2-2-2 .896-2 2 .896 2 2 2zm0 0c-3.314 0-6 2.686-6 6v1a1 1 0 001 1h10a1 1 0 001-1v-1c0-3.314-2.686-6-6-6z"
                    />
                  </svg>
                </span>
                <div>
                  <h4 class="font-bold">Localisation</h4>
                  <p class="text-gray-400">Antananarivo, Ambohimanarina</p>
                </div>
              </div>
            </div>

            <!-- Réseaux sociaux -->
            <div class="pt-6 border-t border-gray-700">
              <h3 class="text-xl font-bold mb-4">Réseaux sociaux</h3>
              <div class="flex gap-4">
                <!-- LinkedIn -->
                <a
                  href="https://www.linkedin.com/in/ratsimbason-faly-ars%C3%A8ne-7918a7375/"
                  target="_blank"
                  rel="noopener"
                  aria-label="LinkedIn"
                  class="w-10 h-10 bg-gray-600 rounded-full flex items-center justify-center hover:bg-blue-600 transition transform hover:scale-110"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6 text-blue-400"
                    fill="currentColor"
                    viewBox="0 0 24 24"
                  >
                    <path
                      d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.761 0 5-2.239 5-5v-14c0-2.761-2.239-5-5-5zm-11 19h-3v-10h3v10zm-1.5-11.268c-.966 0-1.75-.784-1.75-1.75s.784-1.75 1.75-1.75 1.75.784 1.75 1.75-.784 1.75-1.75 1.75zm13.5 11.268h-3v-5.604c0-1.337-.026-3.063-1.867-3.063-1.868 0-2.154 1.459-2.154 2.967v5.7h-3v-10h2.881v1.367h.041c.401-.761 1.379-1.563 2.838-1.563 3.036 0 3.6 2.001 3.6 4.601v5.595z"
                    />
                  </svg>
                </a>

                <!-- GitHub -->
                <a
                  href="https://github.com/Arsene-Faly"
                  target="_blank"
                  rel="noopener"
                  aria-label="GitHub"
                  class="w-10 h-10 bg-gray-600 rounded-full flex items-center justify-center hover:bg-purple-600 transition transform hover:scale-110"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6 text-purple-400"
                    fill="currentColor"
                    viewBox="0 0 24 24"
                  >
                    <path
                      d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.483 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.342-3.369-1.342-.454-1.154-1.11-1.461-1.11-1.461-.908-.62.069-.608.069-.608 1.004.07 1.532 1.032 1.532 1.032.892 1.529 2.341 1.088 2.91.833.091-.646.35-1.088.636-1.34-2.221-.253-4.555-1.112-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.338 1.909-1.294 2.748-1.025 2.748-1.025.546 1.378.202 2.397.099 2.65.64.7 1.028 1.595 1.028 2.688 0 3.847-2.337 4.695-4.566 4.944.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.744 0 .268.18.579.688.481C19.135 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"
                    />
                  </svg>
                </a>

                <!-- Dribbble -->
                <a
                  href="https://dribbble.com/arsene"
                  target="_blank"
                  rel="noopener"
                  aria-label="Dribbble"
                  class="w-10 h-10 bg-gray-600 rounded-full flex items-center justify-center hover:bg-pink-600 transition transform hover:scale-110"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6 text-pink-400"
                    fill="currentColor"
                    viewBox="0 0 24 24"
                  >
                    <path
                      d="M12 2C6.477 2 2 6.477 2 12c0 5.523 4.477 10 10 10s10-4.477 10-10c0-5.523-4.477-10-10-10zm7.938 7.001c-3.282-.527-6.453-.57-7.047-.577-.021-.031-.041-.062-.062-.093-.271-.406-.553-.801-.846-1.184 3.309-1.293 5.309-3.13 5.309-3.13A8.004 8.004 0 0120 12c0 .232-.012.461-.031.687-.627-.131-2.021-.393-3.031-.393-.146 0-.287.004-.426.011-.021-.047-.041-.094-.062-.141-.271-.594-.563-1.172-.875-1.734 2.563-.188 4.563-.812 4.563-.812A7.963 7.963 0 0021.938 9.001zM12 4c1.563 0 3.021.406 4.281 1.125-.021.016-1.938 1.771-5.063 2.984-1.563-2.938-3.188-5.031-3.188-5.031A7.97 7.97 0 0112 4zm-7.938 7.001c.188-.406.396-.801.625-1.188.021.016 2.063 2.031 5.438 3.219-.188.375-.365.75-.531 1.125-4.438-.125-7.188.812-7.188.812A7.963 7.963 0 004.062 11.001zm-.031 1.312c.75-.219 3.063-.812 7.188-.75-.188.406-.365.813-.531 1.219-4.188.531-6.938 2.219-7.031 2.281A7.963 7.963 0 003.969 12.313zm8.031 8.687c-1.563 0-3.021-.406-4.281-1.125.021-.016 1.938-1.771 5.063-2.984 1.563 2.938 3.188 5.031 3.188 5.031A7.97 7.97 0 0112 21zm2.219-1.844c-.406-.594-1.563-2.219-2.938-4.719 1.188-.344 2.438-.594 3.75-.75.406.594 1.563 2.219 2.938 4.719-1.188.344-2.438.594-3.75.75zm-4.219-5.25c.188-.406.365-.813.531-1.219 1.219.016 2.406.062 3.594.156.312.563.604 1.141.875 1.734-1.219-.016-2.406-.062-3.594-.156zm4.219-5.25c-.188.406-.365.75-.531 1.125-1.219-.016-2.406-.062-3.594-.156-.312-.563-.604-1.141-.875-1.734 1.219.016 2.406.062 3.594.156z"
                    />
                  </svg>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
const name = ref("");
const email = ref("");
const message = ref("");
const error = ref("");
const success = ref(false);

function handleSubmit() {
  error.value = "";
  success.value = false;
  if (!name.value || !email.value || !message.value) {
    error.value = "Tous les champs sont obligatoires.";
    return;
  }
  // Simule l'envoi du message
  setTimeout(() => {
    success.value = true;
    name.value = "";
    email.value = "";
    message.value = "";
  }, 1000);
}
</script>
