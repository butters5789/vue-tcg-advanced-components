<template>
  <div>
    <the-header></the-header>
    <badge-list></badge-list>
    <user-info
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></user-info>
    <course-goals #default="passedProps">
      <h2>{{ passedProps.item }}</h2>
      <p>{{ passedProps.anotherProp }}</p>
    </course-goals>
  </div>
</template>

<script>
import BadgeList from './components/BadgeList.vue';
import CourseGoals from './components/CourseGoals.vue';
import TheHeader from './components/TheHeader.vue';
import UserInfo from './components/UserInfo.vue';

export default {
  components: {
    BadgeList,
    CourseGoals,
    TheHeader,
    UserInfo,
  },
  data() {
    return {
      activeUser: {
        name: 'Maximilian Schwarzmüller',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>
