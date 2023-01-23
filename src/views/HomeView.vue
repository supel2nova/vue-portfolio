<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-yellow">Hello!</h1>
              <h1 class="text-gray">I'm Panupong Yapradith</h1>
              <span class="text-gray">Full-Stack Developer</span><br />
              <v-btn
                tile
                dark
                class="text-yellow mt-5"
                variant="outlined"
                @click="scroll('contact')"
                >Contact Me</v-btn
              >
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
            >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="i211.gif" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img class="imgEgg" src="i122.png" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h3 class="mt-16">About Me</h3>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="yellow"> </v-slider>
              </div>
              <p class="text-black">
                I have a degree in engineering, but I am not from the computer
                science field, I like things related to computers, like
                overclocking the CPU, so I got interested in programming and
                enjoy it. Even though it can be difficult sometimes, I will
                develop myself to make it.
              </p>
              <br />
              <p class="text-black">
                With my current programming skills and knowledge, I am looking
                for growth opportunities to start a new career as a successful
                Junior Web Developer where I can apply my in-depth knowledge of
                web programming languages, tools, and testing methods.
              </p>
              <a
                href="https://www.canva.com/design/DAFGOF4PZVA/x_V7a38PQ0VpCqps_4R_6g/view?utm_content=DAFGOF4PZVA&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton"
                target="_blank"
                ><v-btn tile dark color="yellow" class="mt-4"
                  >My Resume</v-btn
                ></a
              >
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What we Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow"></v-slider>
        </div>
      </div>
      
      <v-col cols="12" sm="12" id="project">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">Projects</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover mb-16">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <a :href="item.url" target="_blank"
                    ><v-img :src="item.img" height="225px" cover=""></v-img
                  ></a>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
    </v-container>
    <NavBarContact id="contact" />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import NavBar from "@/components/NavBar.vue";
import NavBarContact from "@/components/NavBarContact.vue";

export default defineComponent({
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
  name: "HomeView",
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "project01.png",
          url: "https://supel2nova.github.io/bmi-calculator.github.io/",
        },
        {
          img: "project02.png",
          url: "http://jammming-pyco2.surge.sh/",
        },
        {
          img: "project03.png",
          url: "https://replit.com/@PanupongYapradi/Find-Your-Hat#index.js",
        },
        {
          img: "project04.png",
          url: "https://landing-page-tailwind-py.surge.sh/",
        },
        {
          img: "project05.png",
          url: "https://blog-panu.vercel.app/",
        },
      ],
    };
  },

  components: {
    NavBar,
    NavBarContact,
  },
});
</script>
<style scoped>
.v-container {
  padding: 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.imgEgg {
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
</style>
