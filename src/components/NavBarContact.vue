<template>
  <v-bottom-navigation v-model="value" dark>
    <v-btn>
      <a href="https://github.com/supel2nova"
        ><v-icon color="yellow" height="50px">fab fa-github</v-icon> <br /><span
          class="text-black"
          >Github</span
        ></a
      >
    </v-btn>
    <v-btn>
      <a href="https://www.linkedin.com/in/panupong-yapradith-013391191/"
        ><v-icon color="yellow">fa-brands fa-linkedin-in</v-icon> <br /><span
          class="text-black"
          >Linkedin</span
        ></a
      >
    </v-btn>
    <v-btn>
      <a href="mailto: y.panupong.9125@gmail.com"
        ><v-icon color="yellow">fa-regular fa-envelope</v-icon> <br /><span
          class="text-black"
          >Email</span
        ></a
      >
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {};
</script>

<style>
a {
  text-decoration: none;
}
</style>
