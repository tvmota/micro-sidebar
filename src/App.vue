<template>
  <div class="bg-green-300 shadow-lg h-full"> 
    <ul class="flex flex-col font-sans">
      <li class="p-1 pl-2 " v-for="(route, idx) in rotas" :key="idx">
        <router-link :to="route.path" active-class="underline text-gray-600">
          {{route.name}}
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'sidebar',
    data() {
      return {
        rotas: [
          {
            path: '/app1',
            name: 'App1',
          },
          {
            path: '/svelte',
            name: 'Svelte',
          },
          {
            path: '/angularjs',
            name: 'AngularJs',
          },
        ]
      };
    },
  };
</script>
