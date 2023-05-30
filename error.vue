<template>
   <div class="prose">
    <div v-if="props.error.statusCode === 404">
       <h1>404</h1>
       <p>I guess this page doesn't exist</p>
    </div>
   </div>
</template>

<script setup>
   const props = defineProps({
      error: Object
   });
console.log(props.error);
const handleError = () => {
   clearError({ redirect: '/' })
}

definePageMeta({
   layout: 'default'
})
</script>