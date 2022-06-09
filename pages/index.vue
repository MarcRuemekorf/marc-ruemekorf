<template>
  <div>
    <!-- Header -->
    <div class="relative overflow-hidden flex flex-col lg:block">
      <div class="z-10 pb-8 bg-white sm:pb-16 md:pb-20 lg:max-w-7xl mx-auto w-full lg:pb-28 xl:pb-32 order-2">
        <div class="mt-10 mx-auto max-w-7xl px-4 sm:mt-12 sm:px-6 md:mt-16 lg:mt-20 lg:px-8 xl:mt-28">
          <div class="text-left md:text-center lg:text-left">
            <h1 class="text-4xl tracking-tight font-bold text-gray-900 sm:text-5xl md:text-6xl">
              Marc Ruemekorf
            </h1>
          </div>
        </div>
      </div>
      <div class="order-1 hidden lg:block lg:absolute lg:bottom-0 lg:right-0 lg:w-1/2">
        <img class="h-auto w-full sm:h-auto md:h-auto lg:w-full lg:h-auto" src="~/assets/images/hero-logos.png" alt="" />
      </div>
    </div>

    <!-- About -->
    <div class="max-w-7xl mx-auto mx-auto px-4 sm:px-6 lg:px-8 lg:max-w-7xl pb-16 md:pb-0">
      <div class="md:grid md:grid-cols-5 md:grid-flow-col md:gap-6">
        <div class="col-span-2">
          <p class="text-2xl mb-12">Front-end ontwikkelaar met een grafisch ontwerp achtergrond en een leergierige mentaliteit.</p>
          <dl>
            <dt class="sr-only">Geboorte datum</dt>
            <dd>Geboorte datum: <span class="font-bold">24-06-1991</span></dd>
            <dt class="sr-only">Woonplaats</dt>
            <dd>Woonplaats: <span class="font-bold">Weesp</span></dd>
            <dt class="sr-only">Nationaliteit</dt>
            <dd>Nationaliteit: <span class="font-bold">Nederlands/Amerikaans</span></dd>
            <dt class="sr-only">Talen</dt>
            <dd>Talen: <span class="font-bold">Nederlands, Engels</span></dd>
            <dt class="sr-only">Telefoonnummer</dt>
            <dd>Telefoonnummer: <span class="font-bold">+31 (0)6 52 61 43 23</span></dd>
            <dt class="sr-only">E-mail</dt>
            <dd>E-mail: <span class="font-bold">hallo@marcruemekorf.nl</span></dd>
          </dl>

          <div class="flex space-x-2 items-center mt-6">
            <a href="/downloads/CV_marcruemekorf.pdf" target="_blank" class="inline-flex items-center px-3 py-2 border border-transparent shadow-sm text-sm leading-4 font-medium rounded-md text-white bg-black hover:bg-black focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-black">
              Download CV
            </a>
            <a href="https://www.linkedin.com/in/marcruemekorf" target="_blank" class="inline-flex items-center p-1.5 border border-transparent rounded-md shadow text-black bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-black">
              <svg class="w-5 h-5" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:2;">
                <path d="M19,0L5,0C2.239,0 0,2.239 0,5L0,19C0,21.761 2.239,24 5,24L19,24C21.762,24 24,21.761 24,19L24,5C24,2.239 21.762,0 19,0ZM8,19L5,19L5,8L8,8L8,19ZM6.5,6.732C5.534,6.732 4.75,5.942 4.75,4.968C4.75,3.994 5.534,3.204 6.5,3.204C7.466,3.204 8.25,3.994 8.25,4.968C8.25,5.942 7.467,6.732 6.5,6.732ZM20,19L17,19L17,13.396C17,10.028 13,10.283 13,13.396L13,19L10,19L10,8L13,8L13,9.765C14.396,7.179 20,6.988 20,12.241L20,19Z" style="fill-rule:nonzero;"/>
              </svg>
            </a>
          </div>
        </div>
        <div class="col-span-3 content-start mt-12 md:mt-0 lg:mt-24">
          <h3 class="text-xl font-bold">Over mij</h3>
          <p class="mt-3">
            Na mijn studie in media vormgeving op het Koning Willem I College ben ik aan de slag gegaan als webdesigner bij een jong en ambitieus webbureau in Breda. Hier werd mijn interesse in het ontwikkelen van websites en applicaties opgewekt. Ik heb altijd de wens gehad om mijn ontwerpen leven in te blazen en heb zo een passie gekweekt voor front-end technieken. Sindsdien ben ik aan de slag gegaan als ZZP’er en heb ik mijzelf verdiept in de nodige technieken om de meest efficiënte en gebruiksvriendelijke websites en applicaties te ontwikkelen.
          </p>
          <p class="mt-3">
            Tijdens mijn periode als freelancer heb ik met een klein team ook veel tijd besteed aan het oprichten van 3 IT bedrijfjes dat gespecialiseerde software ontwikkelde. Hierbij was ik verantwoordelijk voor het design en de front-end.
          </p>
          <p class="mt-3">
            Ook in mijn vrije tijd houd ik mij bezig met het ontwikkelen van nieuwe applicaties/websites en het uitproberen van verschillende technieken en frameworks. Mijn focus ligt momenteel op het beheersen van Javascript en frameworks zoals React en Vue.
          </p>
        </div>
      </div>
    </div>

    <!-- Experience -->
    <div class="max-w-7xl mx-auto mx-auto px-4 sm:px-6 lg:px-8 lg:max-w-7xl">
      <h2 class="text-2xl font-bold mb-6">Werkervaring</h2>
      <div class="md:grid md:grid-cols-12 md:grid-rows-auto md:grid-flow-col md:gap-y-6 z-10 relative">
        <div v-for="(block, index) in experience" :key="index" :class="['mt-6 md:mt-0', ...block.size]">
          <div :class="['bg-white border-b-2 h-full w-full p-3 rounded shadow-md', block.borderColor]">
            <h3 class="font-semibold">{{ block.company }}</h3>
            <p class="text-sm text-gray-500">{{ block.period }}</p>
            <p class="mt-2">{{ block.position }}</p>
            <div class="flex flex-wrap">
              <img v-for="(skill, index) in block.skills" :key="index" :src="require(`~/assets/images/logos/${skill.filename}.png`)" alt="" class="h-5 w-5 mr-2 mt-3" v-tooltip="skill.name" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Projects -->
    <div class="bg-gradient-to-b from-gray-100 via-gray-50 -mt-12">
      <div class="max-w-4xl mx-auto px-4 pt-24 md:pt-16 pb-16 sm:px-6 sm:pb-24 lg:max-w-7xl lg:pt-24 lg:px-8">
        <h2 class="text-2xl font-bold mb-6">Projecten</h2>
        <p class="sr-only mt-4 max-w-3xl text-lg">
          Projecten waar ik met trots aan heb mogen werken.
        </p>
        <div class="mt-12 grid grid-cols-1 gap-x-6 gap-y-6 lg:gap-y-12 sm:grid-cols-2 lg:mt-6 lg:grid-cols-3 lg:gap-x-8 lg:gap-y-16">
          <div v-for="project in projects" :key="project.name">
            <div>
              <h3 class="text-lg font-semibold">{{ project.name }}</h3>
              <p class="mt-2 text-base">
                {{ project.description }}
              </p>
              <p class="mt-3 text-sm text-gray-400">
                {{ project.responsibilities.join(', ') }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Opleidingen -->
    <div>
      <div class="max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:py-20 lg:px-8">
        <div class="lg:grid lg:grid-cols-3 lg:gap-12">
          <div>
            <h2 class="text-2xl font-bold mb-6">Opleidingen en relevante kennis</h2>
            <p class="mt-4 text-lg text-gray-500">Ik probeer bij te blijven door online cursussen te volgen. Zo ben ik regelmatig actief op FreeCodeCamp en Udemy.</p>
          </div>
          <div class="mt-12 lg:mt-0 lg:col-span-2">
            <dl class="space-y-12">
              <div>
                <dt>
                  <span class="block text-lg leading-6 font-semibold text-gray-900">FreeCodeCamp, online - <span class="italic">Full Stack Web Development</span></span>
                  <span class="block text-sm text-gray-400">2016 - 2017</span>
                </dt>
                <dd class="mt-2 text-base text-gray-500">FreeCodeCamp heeft mij de basis geleerd mijn designs om te zetten in code en helpt mij nog altijd mijzelf te verbeteren.</dd>
              </div>
              <div>
                <dt>
                  <span class="block text-lg leading-6 font-semibold text-gray-900">Koning Willen I College, 's-Hertogenbosch - <span class="italic">Mediavormgeving (MBO niveau 4)</span></span>
                  <span class="block text-sm text-gray-400">2009 - 2013</span>
                </dt>
                <dd class="mt-2 text-base text-gray-500">Tijdens mijn opleiding heb ik onder andere geleerd wat een design sterk maakt en hoe ik dit in de praktijk toe kan passen.</dd>
              </div>
            </dl>
          </div>
        </div>
      </div>
    </div>

    <div class="bg-white">
      <div class="max-w-7xl mx-auto py-16 px-4 sm:py-20 sm:px-6 lg:px-8">
        <h2 class="text-2xl font-bold mb-6">Vaardigheden</h2>
        <div class="-mt-6 -ml-6 flex flex-wrap lg:-ml-6">
          <div v-for="(skill, index) in skills" :key="index" class="mt-6 ml-6 flex flex-shrink-0 lg:flex-grow-0 lg:ml-6" v-tooltip="skill.name">
            <img class="max-h-12" :src="require(`~/assets/images/logos/${skill.filename}.png`)" :alt="skill.name">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import { ref } from '@nuxtjs/composition-api'

export default {
  name: 'IndexPage',
  setup() {
    const skills = {
      'illustrator': {
        name: 'Illustrator',
        filename: 'illustrator'
      },
      'photoshop': {
        name: 'Photoshop',
        filename: 'photoshop'
      },
      'adobe-xd': {
        name: 'Adobe XD',
        filename: 'adobe-xd'
      },
      'sketch': {
        name: 'Sketch',
        filename: 'sketch'
      },
      'figma': {
        name: 'Figma',
        filename: 'figma'
      },
      'google-web-designer': {
        name: 'Google Web Designer',
        filename: 'google-web-designer'
      },
      'affinity-designer': {
        name: 'Affinity Designer',
        filename: 'affinity-designer'
      },
      'affinity-photo': {
        name: 'Affinity Photo',
        filename: 'affinity-photo'
      },
      'affinity-publisher': {
        name: 'Affinity Publisher',
        filename: 'affinity-publisher'
      },
      'jetbrains': {
        name: 'PHP Storm',
        filename: 'jetbrains'
      },
      'vscode': {
        name: 'Visual Studio Code',
        filename: 'vscode'
      },
      'html': {
        name: 'HTML',
        filename: 'html'
      },
      'css': {
        name: 'CSS',
        filename: 'css'
      },
      'sass': {
        name: 'Sass',
        filename: 'sass'
      },
      'tailwindcss': {
        name: 'Tailwind CSS',
        filename: 'tailwindcss'
      },
      'php': {
        name: 'PHP',
        filename: 'php'
      },
      'javascript': {
        name: 'Javascript',
        filename: 'javascript'
      },
      'vuejs': {
        name: 'Vue JS',
        filename: 'vuejs'
      },
      'nuxtjs': {
        name: 'Nuxt JS',
        filename: 'nuxtjs'
      },
      'react': {
        name: 'React',
        filename: 'react'
      },
      'nextjs': {
        name: 'Next JS',
        filename: 'nextjs'
      },
      'wordpress': {
        name: 'WordPress',
        filename: 'wordpress'
      },

    }
    const experience = [
      {
        company: "Celebrate Media",
        position: "Webdesigner",
        period: "2013",
        size: ['row-start-1 col-start-1 col-span-3'],
        borderColor: "border-green-500",
        skills: [
          skills['illustrator'],
          skills['photoshop'],
          skills['sketch']
        ]
      },
      {
        company: "Freelance",
        position: "Grafisch & UI/UX designer, Front-end ontwikkelaar",
        period: "2013 - heden",
        size: ['row-start-2 col-start-3 col-span-11'],
        borderColor: "border-black",
        skills: [
          skills['affinity-designer'],
          skills['affinity-photo'],
          skills['affinity-publisher'],
          skills['sketch'],
          skills['google-web-designer'],
          skills['html'],
          skills['css'],
          skills['php'],
          skills['javascript'],
          skills['wordpress'],
          skills['react'],
          skills['vuejs'],
          skills['nuxtjs']
        ]
      },
      {
        company: "Launchtin",
        position: "Medeoprichter, Grafisch & UI/UX designer, Front-end ontwikkelaar",
        period: "2015 - 2018",
        size: ['row-start-3 col-start-4 col-span-5'],
        borderColor: "border-pink-600",
        skills: [
          skills['photoshop'],
          skills['illustrator'],
          skills['affinity-designer'],
          skills['affinity-photo'],
          skills['affinity-publisher'],
          skills['sketch'],
          skills['html'],
          skills['css'],
          skills['php'],
          skills['javascript'],
          skills['wordpress']
        ]
      },
      {
        company: "Doen IT",
        position: "Medeoprichter, UI/UX designer, Front-end ontwikkelaar",
        period: "2018 - 2020",
        size: ['row-start-4 col-start-7 col-span-3'],
        borderColor: "border-teal-500",
        skills: [
          skills['affinity-designer'],
          skills['affinity-photo'],
          skills['sketch'],
          skills['html'],
          skills['css'],
          skills['php'],
          skills['javascript'],
          skills['wordpress'],
          skills['vuejs']
        ]
      },
      {
        company: "Digital Forge",
        position: "Medeoprichter, UI/UX designer, Front-end ontwikkelaar",
        period: "2020 - heden",
        size: ['row-start-5 col-start-10 col-span-3'],
        borderColor: "border-violet-900",
        skills: [
          skills['affinity-designer'],
          skills['affinity-photo'],
          skills['sketch'],
          skills['html'],
          skills['css'],
          skills['php'],
          skills['javascript'],
          skills['vuejs'],
          skills['nuxtjs']
        ]
      }
    ]
    const projects = [
      {
        name: "Groenergras Hoveniers",
        description: "GroenerGras Hoveniers had een platform nodig om aangesloten hoveniers een plek te geven op het web. Ik heb het hele proces mogen bijstaan van ontwerp tot ontwikkeling en onderhoud.",
        responsibilities: ["Webdesign", "Ontwikkeling", "SEO"]
      },
      {
        name: "Dé OnderhoudsHovenier",
        description: "Een initiatief om eenvoudig en snel vakhoveniers te vinden in de buurt. Hierbij heb ik het ontwerp proces bijgestaan en de website vervolgens op het Wordpress CMS online gezet.",
        responsibilities: ["Webdesign", "Ontwikkeling", "SEO"]
      },
      {
        name: "Fitland",
        description: "Ik heb Fitland IT mogen ondersteunen met het ontwerpen en ontwikkelen van een compleet nieuwe website en online advertenties via Google Adwords.",
        responsibilities: ["Webdesign", "Grafisch design"]
      },
      {
        name: "Smart City Plaza",
        description: "Een onafhankelijk platform voor overheden, adviseurs en installateurs met Smart City oplossingen voor de openbare ruimte. Ik ben verantwoordelijk geweest voor de branding, webdesign en ontwikkeling.",
        responsibilities: ["Grafisch design", "Webdesign", "Ontwikkeling"]
      },
      {
        name: "City Resort Hotels",
        description: "Ik was verantwoordelijk voor zowel het ontwerpen van de website als de ontwikkeling. De site werd ontwikkeld met behulp van het Wordpress CMS. Hiervoor is een op-maat thema ontwikkeld.",
        responsibilities: ["Webdesign", "Ontwikkeling"]
      },
      {
        name: "PayIBAN",
        description: "PayIBAN maakt het makkelijk om iDeal, iDIN en incassomachtigen te implementeren in een website of webshop. Deze diensten kunnen online aangevraagd worden. Ik heb de website mogen ontwerpen en ontwikkelen waar dit in mogelijk wordt gemaakt.",
        responsibilities: ["Webdesign", "Ontwikkeling"]
      },
      {
        name: "Bedankjevrijwilliger",
        description: "Het is hartstikke belangrijk dat je je vrijwilligers in het zonnetje zet. Het platform van bedankjevrijwilliger bied de kans om de vrijwilliger eens te bedanken voor zijn of haar inzet door middel van een filmpje",
        responsibilities: ["Grafisch design", "Webdesign", "Ontwikkeling"]
      },
      {
        name: "Vrijwilligersprijzen.tv",
        description: "Elk jaar maken vrijwilligersorganisaties kans een prijs te winnen enkel door hun eigen inzet. Vrijwilligersprijzen.tv heeft de prijsuitreiking van 2021 live uitgezonden.",
        responsibilities: ["Webdesign", "Ontwikkeling"]
      },
      {
        name: "Vrijwilligersprijzen.nl",
        description: "Door middel van een presentatie in de vorm van een filmpje of presentatie worden vrijwilligers in het zonnetje gezet en maken zij automatisch kans op een prijs.",
        responsibilities: ["Webdesign", "Ontwikkeling"]
      },
    ]
    return {
      experience,
      projects,
      skills
    }
  }
}
</script>
