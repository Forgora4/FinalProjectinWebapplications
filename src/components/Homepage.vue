<script setup>
import HeroSection from '../views/Hero.vue'
import ProgramsOfferedSection from '../views/Programsofferedsection.vue'
import FacultyAndStaff from '../views/Facultyandstaff.vue'
import PartnershipsAndMemberships from '../views/Partnershipsandmemberships.vue'
</script>

<template>
  <main class="page-shell">
    <HeroSection />
    <ProgramsOfferedSection />
    <FacultyAndStaff />
    <PartnershipsAndMemberships />
  </main>
</template>

<style scoped>
.page-shell {
  display: block;
}
</style>
