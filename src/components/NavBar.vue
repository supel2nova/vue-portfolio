<template lang="">
  <v-app-bar app color="black" darl flat class="px-12">
    <v-btn>
      <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon>
      Panupong
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text ref="homeBtn" @click="scroll('home') " class="text-yellow">Home</v-btn>
    <v-btn text ref="aboutBtn" @click="scroll('about')">About</v-btn>
    <v-btn text ref="projectBtn" @click="scroll('project')">Project</v-btn>
    <v-btn text ref="contactBtn" @click="scroll('contact')">Contact</v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
      this.$refs.homeBtn.classList.remove('text-yellow');
      if (refName === 'about') {
        this.$refs.aboutBtn.classList.add('text-yellow');
      }
    },
  },
};
</script>

<style lang=""></style>