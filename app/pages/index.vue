<template>
  <section class="bg-white rounded-2xl shadow p-8 text-center">
    <img
      src="/avatar.png"
      alt="Profile picture"
      class="w-40 h-40 rounded-full mx-auto object-cover border-4 border-indigo-500"
    />

    <h1 class="text-3xl font-bold mt-6">Junrie D. Murillo</h1>
    <p class="text-indigo-600 font-medium">IT Student</p>

    <p class="mt-4 text-gray-600 max-w-xl mx-auto">
      Hi! I am an IT student who loves building websites and learning
      new technologies. This is my first Nuxt application.
    </p>

    <h2 class="text-xl font-semibold mt-6">Welcome to my website!</h2>

    <NuxtLink
      to="/profile"
      class="inline-block mt-6 bg-indigo-600 text-white px-6 py-2 rounded-lg hover:bg-indigo-700"
    >
      View My Profile
    </NuxtLink>
  </section>
</template>
