<script setup lang="ts">
import LandingCard from "./components/LandingCard.vue";
import FAQ from "./components/FAQ.vue";

const cards = [
  {
    title: 'Soutien & bien-être',
    description: 'Une communauté bienveillante où partager vos questions, vos doutes et vos victoires, sans jugement.',
    image: `${import.meta.env.BASE_URL}frame2.jpg`
  },
  {
    title: 'Le parcours',
    description: 'Guides, étapes, retours d’expérience… Tout pour vous aider à comprendre si le tatouage thérapeutique est fait pour vous.',
    image: `${import.meta.env.BASE_URL}frame3.jpg`
  },
  {
    title: 'Histoires vraies',
    description: 'Explorez les résultats, les témoignages et l’impact réel du tatouage thérapeutique.',
    image: `${import.meta.env.BASE_URL}frame4.jpg`
  },
]

const frame2 = `${import.meta.env.BASE_URL}frame2.jpg`
</script>

<template>
  <nav class="flex justify-around item-center mx-40 mt-5 h-20 bg-red-100 rounded-4xl">
    <img width="200" src="/logo_horizontal_bloomInk_blanc.svg"/>
    <ul class="h-full flex justify-center items-center gap-10">
      <li class="cursor-pointer">
        Tatouages
      </li>
      <li class="cursor-pointer">
        Conseils & Accompagnement
      </li>
      <li class="cursor-pointer">
        Témoignages
      </li>
      <li class="cursor-pointer">
        Notre mission
      </li>
    </ul>
    <div class="flex items-center gap-4">
      <div class="cursor-pointer flex justify-between gap-5 bg-white py-4 px-7 rounded-4xl text-black">
        <p>Télécharger l'application</p>
        <img src="/arrow-right.svg"/>
      </div>
    </div>
  </nav>
  <div class="flex justify-around items-center gap-15 m-25">
    <div class="w-220 flex flex-col gap-5">
      <h2 class="text-6xl font-semibold">On transforme les marques du passé en force pour l’avenir.</h2>
      <p>Grâce à BloomInk, trouvez un tatoueur spécialisé en tatouage thérapeutique, découvrez des parcours inspirants et avancez à votre rythme vers une nouvelle relation à votre corps. Un espace bienveillant, pensé pour celles et ceux qui méritent enfin de se retrouver.</p>
    </div>
    <img src="/pexels-eduardordone-2928342%201.jpg" alt="" class="rounded-3xl">
  </div>
  <div class="bg-white h-60">
    <div class="h-20 w-full bg-[url(/banner1.svg)] bg-cover bg-no-repeat"/>

    <div class="flex w-full justify-around items-center h-full pb-15">
      <img class="w-20" src="/marques/img1.png" alt="">
      <img class="w-50" src="/marques/img2.png" alt="">
      <img class="w-20" src="/marques/img3.png" alt="">
      <img class="w-20" src="/marques/img4.png" alt="">
      <img class="w-20" src="/marques/img5.png" alt="">
      <img class="w-20" src="/marques/img6.png" alt="">
    </div>
  </div>

  <div class="bg-beige pb-15">
    <div class="h-20 w-full bg-[url(/banner2.svg)] bg-cover bg-no-repeat"/>

    <div class="flex justify-center gap-10 flex-wrap">

      <div class="flex justify-center gap-10 w-full">
        <div class="w-200 rounded-4xl overflow-hidden glass">
          <div class="flex flex-col justify-center h-full gap-10 px-10 py-7">
            <h3 class="text-4xl font-bold w-150 leading-13">Chaque tatouage est unique. Le vôtre aussi.</h3>
            <div class="flex items-center gap-4 cursor-pointer border-1 rounded-4xl px-7 py-4 bg-white text-black w-fit hover:opacity-70">
              <p>BloomInk vous accompagne avec douceur et expertise</p>
              <img src="/arrow-oriented.svg" alt="">
            </div>
          </div>
        </div>

        <LandingCard
            class="w-95"
            title="Tatoueurs spécialisés"
            description="Chaque tatoueur est vérifié et expérimenté dans le tatouage thérapeutique. Vous choisissez un artiste de confiance, vraiment adapté à votre parcours."
            :image="frame2"
        />
      </div>

      <LandingCard
          v-for="card in cards"
          class="w-95"
          :title="card.title"
          :description="card.description"
          :image="card.image"
      />
    </div>
  </div>

  <div class="bg-light-beige text-black pb-10">
    <div class="h-20 w-full bg-[url(/banner3.svg)] bg-cover bg-no-repeat"/>

    <div class="flex flex-col gap-7 w-200 mt-10 ml-50">
      <h1 class="text-4xl">
        Chaque tatouage thérapeutique change une vie. Parfois même deux.
      </h1>
      <p>
        Quand une personne retrouve son reflet, ce sont souvent ses proches, sa famille, sa confiance et son quotidien qui changent aussi. BLOOMINK vous accompagne dès la première question jusqu’à la dernière retouche.
      </p>

      <div class="cursor-pointer bg-light-beige-button py-4 px-7 rounded-4xl w-fit font-bold hover:opacity-50 border-1">
        Je veux découvrir mon parcours
      </div>
    </div>

    <div class="flex w-full h-100 justify-end mt-10">
      <div class="relative w-170 h-100 bg-red-100 rounded-3xl border-black border-3 mr-60 overflow-hidden">
        <img class="absolute -top-50 -right-45" width="260" src="/img5.png" alt="">
        <img class="object-cover w-full h-full" src="/9490e6f1cb1d9965a20629243a10141006d16e7e.jpg" alt="">
      </div>
    </div>
  </div>

  <div class="bg-beige pb-20">
    <div class="h-20 w-full bg-[url(/banner2.svg)] bg-cover bg-no-repeat"/>

    <h1 class="ml-25 text-gray-800 text-4xl font-bold">Manon, son histoire...</h1>

    <div class="flex flex-col gap-10">
      <div class="flex justify-around items-center">
        <div class="flex flex-col gap-5 glass rounded-4xl w-200 p-10">
          <div class="flex gap-2">
            <img v-for="_ in 5" src="/star-icon.svg" alt="">
          </div>

          <p class="text-xl font-light">
            “Après mon opération, j’avais l’impression que mon corps ne m’appartenait plus. Le tatouage thérapeutique n’a pas effacé ce que j’ai vécu, mais il m’a donné une nouvelle force. Grâce à ArtSkin, j’ai trouvé une artiste à l’écoute, qui m’a redonné une relation apaisée avec mon image.”
          </p>

          <div class="flex flex-col">
            <p class="font-bold">Manon</p>
          </div>
        </div>

        <div class="glass rounded-4xl overflow-hidden">
          <img src="/img1.jpg" alt="">
        </div>
      </div>

      <div class="flex gap-10 justify-center">
        <div class="glass rounded-4xl overflow-hidden w-100 h-100 bg-red-100">
          <img class="object-cover w-full h-full bg-no-repeat" src="/img2.jpg" alt="">
        </div>

        <div class="glass rounded-4xl overflow-hidden w-200 h-100 bg-red-200">
          <img class="object-cover w-full h-full bg-no-repeat" src="/img3.jpg" alt="">
        </div>
      </div>

      <div class="mt-10 flex flex-col items-center justify-center gap-10">
        <div class="flex flex-col gap-6 w-170 text-center">
          <h1 class="text-4xl">Faite comme Manon, soyez-vous aussi son héros.</h1>
          <p>Avancez avec une communauté qui vous comprend.</p>
        </div>

        <div class="relative text-black py-4 px-7 bg-white rounded-4xl w-fit">
          <div class="relative top-0 -left-20">
            <img class="absolute -top-40 -left-85" src="/1.svg" alt="">
            <img class="absolute -top-3 -left-45" src="/arrow.svg" alt="">
          </div>

          Je télécharge l'application
        </div>
      </div>
    </div>
  </div>

  <div class="bg-gray-light pb-15">
    <div class="h-20 w-full bg-[url(/banner4.svg)] bg-cover bg-no-repeat"/>

    <div class="flex justify-center">
      <div class="w-340 glass flex justify-center gap-10 flex-wrap rounded-4xl p-10">
        <div class="flex justify-around items-center">
          <div class="flex flex-col gap-10 mx-20">
            <h1 class="text-3xl font-bold">Une mission guidée par la confiance</h1>

            <div class="flex flex-col gap-10">
              <p>
                Bloomink est né d’un constat simple : personne ne devrait traverser seul la reconstruction de son corps.
                Nous avons réuni : des artistes spécialisés et certifiés, des témoignages authentiques, des ressources fiables et des outils pour vous accompagner étape par étape.
              </p>
              <p>
                Notre engagement : vous offrir un espace qui respecte votre histoire et célèbre votre courage.
              </p>
              <p>
                Chaque adoption, chaque soin, chaque intervention repose sur un engagement clair : assurer le bien-être, la sécurité et la dignité de tous les animaux que nous accueillons.
              </p>
            </div>

            <div class="flex items-center gap-4 text-xl font-bold cursor-pointer">
              <img src="/plus.svg"/>
              <p class="font-bold">En savoir plus</p>
            </div>
          </div>

          <div class="relative rounded-4xl overflow-visible">
            <div class="absolute inset-0 rounded-4xl bg-orange-500 blur-3xl opacity-30"></div>
            <img src="/img4.jpg" class="object-cover relative rounded-4xl w-250 h-100" />
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="flex justify-around bg-white pb-40 text-black">
    <div class="mt-40 flex flex-wrap justify-around items-center w-full">
      <div class="flex flex-col gap-5 w-120">
        <h1 class="text-5xl font-bold">Questions Fréquemment Posées</h1>
        <p>Vous avez encore des questions ? Consultez nos réponses aux demandes les plus fréquentes et contactez-nous pour un échange avec un expert.</p>
      </div>

      <div class="flex flex-col gap-5">
        <FAQ title="Est-ce que le tatouage thérapeutique fait mal ?" description="Cela dépend de la zone, de la cicatrisation et de votre sensibilité. Les artistes vous expliquent le processus et adaptent leur technique."/>
        <FAQ title="Puis-je parler avec un artiste avant de prendre une décision ?" description="Cela dépend de la zone, de la cicatrisation et de votre sensibilité. Les artistes vous expliquent le processus et adaptent leur technique."/>
        <FAQ title="Combien coûte un tatouage thérapeutique ?" description="Les prix varient selon la complexité et la taille. Certains projets peuvent être partiellement pris en charge, nous vous guidons selon votre cas."/>
        <FAQ title="Comment savoir si un tatoueur est réellement spécialisé ?" description="Les tatoueurs Bloomink sont constament évalués par la communauté, pour garantir une experience fiable et transparente."/>
      </div>
    </div>
  </div>

  <div class="mt-10 py-10 flex flex-col items-center justify-around pb-40 gap-15">
    <h1 class="relative text-5xl font-bold w-150 text-center">
      Prêt(e) à transformer votre cicatrice en œuvre d’art thérapeutique ?
      <img class="absolute -left-40 -top-5" src="/abstract1.png" alt="">
    </h1>
    
    <div class="flex gap-8">
      <div class="text-center leading-13 w-100 h-30 text-3xl px-10 py-8 rounded-4xl border-3 hover:opacity-50 cursor-pointer">
        APP STORE
      </div>
      <div class="relative text-center leading-13 w-100 h-30 text-3xl px-10 py-8 rounded-4xl border-3 hover:opacity-50 cursor-pointer">
        PLAYSTORE STORE
        <img class="absolute -right-20 -top-20" src="/abstract2.png" alt="">
      </div>
    </div>
  </div>

  <div class="p-5 text-center">
    <h1>©2025, BloomInk. Tous droits réservés</h1>
  </div>
</template>

<style scoped>
nav {
  background: rgba(255, 255, 255, 0.2);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
}

.bg-beige {
  background-color: #A37968;
}

.bg-light-beige {
  background-color: #FDFDF2;
}

.bg-light-beige-button {
  background-color: #FFF6EE;
}

.bg-gray-light {
  background-color: #655D5A;
}
</style>
