<template>
  <NuxtLayout>
   <div class="prose">
    <div>
       <h1>Aw, Snap</h1>
       <p>It looks like something broke</p>
      <p>
        <strong>{{ error.message }}</strong>
      </p>
      <p>
        Go to the
        <a class="hover:cursor-pointer" @click="handleError">First lesson</a>
      </p>
    </div>
   </div>
  </NuxtLayout>
</template>

<script setup>
   const props = defineProps({
      error: Object
   });
console.log(props.error);
const handleError = () => {
   clearError({ redirect: '/course/chapter/1-chapter-1/lesson/2-typescript-in-vue-components' })
}
</script>