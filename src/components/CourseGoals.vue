<template>
  <ul>
    <li v-for="goal in goals" :key="goal">
      <slot :item="goal" another-prop="..."></slot>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      goals: ['Learn Vue', 'Finish the course', 'Get a job'],
    };
  },
};
</script>

<style></style>
