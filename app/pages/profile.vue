<script setup>
const data = {
  info: {
    'Full Name': 'Junrie D. Murillo',
    Age: '23',
    Address: 'Butuan City, Philippines',
    Email: 'junriemurillo@gmail.com',
  },
  education: [
    { level: 'College', school: 'Caraga State University- Main Campus', detail: 'BS Information Technology' },
    { level: 'Senior High School', school: 'Butuan City Senior High School- Stand Alone', detail: 'STEM' },
  ],
  skills: ['HTML', 'CSS', 'JavaScript', 'Vue / Nuxt', 'Tailwind CSS', 'SQL'],
  interests: ['Web Development', 'Databases', 'System Design'],
  hobbies: ['Gaming', 'Listening to music', 'Watching movies'],
}
</script>

<template>
  <div class="space-y-6">
    <h1 class="text-3xl font-bold">My Profile</h1>

    <section class="bg-white rounded-2xl shadow p-6">
      <h2 class="text-xl font-semibold text-indigo-600 mb-3">Personal Information</h2>
      <ul class="space-y-1">
        <li v-for="(value, label) in data.info" :key="label">
          <span class="font-medium">{{ label }}:</span> {{ value }}
        </li>
      </ul>
    </section>

    <section class="bg-white rounded-2xl shadow p-6">
      <h2 class="text-xl font-semibold text-indigo-600 mb-3">Educational Background</h2>
      <ul class="space-y-2">
        <li v-for="e in data.education" :key="e.level">
          <p class="font-medium">{{ e.level }}</p>
          <p class="text-gray-600">{{ e.school }} - {{ e.detail }}</p>
        </li>
      </ul>
    </section>

    <section class="bg-white rounded-2xl shadow p-6">
      <h2 class="text-xl font-semibold text-indigo-600 mb-3">Skills and Interests</h2>
      <p class="font-medium mb-2">Skills</p>
      <div class="flex flex-wrap gap-2 mb-4">
        <span v-for="s in data.skills" :key="s"
          class="bg-indigo-100 text-indigo-700 px-3 py-1 rounded-full text-sm">{{ s }}</span>
      </div>
      <p class="font-medium mb-2">Interests</p>
      <div class="flex flex-wrap gap-2">
        <span v-for="i in data.interests" :key="i"
          class="bg-green-100 text-green-700 px-3 py-1 rounded-full text-sm">{{ i }}</span>
      </div>
    </section>

    <section class="bg-white rounded-2xl shadow p-6">
      <h2 class="text-xl font-semibold text-indigo-600 mb-3">Hobbies</h2>
      <ul class="list-disc list-inside">
        <li v-for="h in data.hobbies" :key="h">{{ h }}</li>
      </ul>
    </section>
  </div>
</template>
