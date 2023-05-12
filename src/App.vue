<template>
  <div class="bg-white py-24">
    <div class="bg-gray-100 mx-auto grid max-w-4xl gap-x-8 gap-y-20 p-6 lg:p-8 rounded-lg">
      <div class="bg-gray-300 mx-auto max-w-2xl p-4 rounded-xl">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">some profiles</h2>
        <p class="text-blue-500 font-bold">you can visit the profiles by clicking the Link button underneath each card</p>
      </div>
      <h3>Instructors</h3>
      <ul role="list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 items-center">
        <li v-for="instructor in instructors" :key="instructor.name">
          <div class="gap-x-20">
            <ProfileCard :data="instructor" />
          </div>
        </li>
      </ul>
      <h3>Students</h3>
      <ul role="list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 items-center">
        <li v-for="student in students" :key="student.name">
          <div class="gap-x-20">           
            <ProfileCard :data="student" />
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import ProfileCard from './components/ProfileCard.vue';

const instructors = [
  {
    name: 'Johan Sulaiman',
    role: 'Founder',
    link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
    imageUrl:
      'https://avatars.githubusercontent.com/u/3628963?v=4',
  },
  {
    name: 'Herry',
    role: 'CEO',
    link: 'https://www.linkedin.com/in/jon-lai-b8019b101/',
    imageUrl:
      'https://avatars.githubusercontent.com/u/832202?s=40&v=4',
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
  {
    name: "Mina Ali",
    role: "Cool CEO",
    imageUrl:
      "https://images.unsplash.com/photo-1683322001857-f4d932a40672?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=684&q=80",
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
