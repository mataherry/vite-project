<!-- <ul role="list" class="grid gap-x-8 gap-y-12 sm:grid-cols-2 sm:gap-y-16 xl:col-span-2"> -->

<!--Huh, so by default, attributes apply to mobile. And sm applies to everything else?-->>
  <template>
    <div class="bg-white py-24 sm:py-32">
      <div class="mx-auto grid max-w-7xl gap-x-8 gap-y-20 px-6 lg:px-8">
        <div class="mx-auto max-w-2xl">
          <h2 class="mx-auto text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">some profiles</h2>
          <br>
          <p><span style="color: blue; font-weight: bold; margin: 0 1rem">you can visit the profiles by clicking the Link button underneath each card</span></p>
        </div>
        <ul role="list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 flex items-center">
          <li v-for="person in people" :key="person.name">
            <div class="gap-x-200 border border-purple-500">
              <ProfileCard :data="person" />
            </div>
          </li>
          <li v-for="person in students" :key="person.name">
            <div class="gap-x-200 border border-purple-500">
              <div class="mx-auto max-w-2xl grid gap-2 p-7 flex items-center margin-auto">
                <img class="rounded-full w-60" :src="person.imageUrl" alt="" />
              </div>
              <div class="mx-auto max-w-2xl p-6 border border-red-500 space-x-4">
                <a href="https://www.linkedin.com/in/jon-lai-b8019b101/"><h3 class="text-base font-semibold leading-7 tracking-tight text-gray-900">{{ person.name }}</h3></a>
                <p class="text-sm font-semibold leading-6 text-indigo-600">{{ person.role }}</p>
                <div class="mx-auto flex items-center space-x-4 px-40 md:px-20 lg:px-20 xl:px-20">
                <img class="h-10 w-10" src="https://png.pngitem.com/pimgs/s/32-326322_linkedin-logo-white-letters-png-download-transparent-png.png">
                <img class="h-10 w-10" src="https://png.pngitem.com/pimgs/s/25-256095_twitter-logo-png-2019-transparent-png.png">
                </div>
              </div>            
            </div>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <style scoped>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.vue:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
  }

  
  </style>
  
  <script setup>
  import HelloWorld from './components/HelloWorld.vue'
  import ProfileCard from './components/ProfileCard.vue'

  const people = [
    {
      name: 'Jonathan Lai',
      role: 'LinkedIn',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://media.licdn.com/dms/image/C5603AQEp8DNZ7K8uqw/profile-displayphoto-shrink_400_400/0/1613878440743?e=1688601600&v=beta&t=VkIAbUN2JXUlaRBB9L1zf4GyVCNtFgaEH4Vs0q9ZVuM',
    },
    // More people...
    {
      name: 'Jonathan Lai',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://avatars.githubusercontent.com/u/58882431?v=4',
    },
    {
      name: 'Eian Lai',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://avatars.githubusercontent.com/u/92978503?v=4',
    },
    {
      name: 'Johan Sulaiman',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://avatars.githubusercontent.com/u/3628963?v=4',
    },
    {
      name: 'John Doe',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'data:image/jpeg;base64,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',
    },
    {
      name: 'Budiyoga Nurhalim',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://avatars.githubusercontent.com/u/85048907?v=4',
    },
  ]

  const students = [
    {
      name: 'Jonathan Lai',
      role: 'LinkedIn',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://media.licdn.com/dms/image/C5603AQEp8DNZ7K8uqw/profile-displayphoto-shrink_400_400/0/1613878440743?e=1688601600&v=beta&t=VkIAbUN2JXUlaRBB9L1zf4GyVCNtFgaEH4Vs0q9ZVuM',
    },
    // More people...
    {
      name: 'Jonathan Lai',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://avatars.githubusercontent.com/u/58882431?v=4',
    },
    {
      name: 'Eian Lai',
      role: 'Github',
      link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
      imageUrl:
        'https://avatars.githubusercontent.com/u/92978503?v=4',
    }
  ]
  </script>