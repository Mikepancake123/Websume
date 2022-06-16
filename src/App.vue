<template>
  <div class="lg:flex block h-full">
    <div class="lg:w-1/3 h-full bg-red-900">
      <ul class="h-screen text-3xl text-white">
        <li class="h-1/4">
          <button @click="homeToggleBtn" class="my-24 mx-auto">Home</button>
        </li>
        <li class="h-1/4">
          <button @click="aboutToggleBtn" class="my-24 mx-auto">Aboutme</button>
        </li>
        <li class="h-1/4">
          <button @click="educationToggleBtn" class="my-24 mx-auto">
            Education
          </button>
        </li>
        <li class="h-1/4">
          <button @click="hobbiesToggleBtn" class="my-24 mx-auto">
            Hobbies
          </button>
        </li>
      </ul>
    </div>
    <div class="lg:w-2/3 h-full">
      <!-- Home  -->
      <section class="home" v-show="homeToggle">
        <h1>Welcome!</h1>
        <p>
          I'm Joseph Maxen Manasan, and this is my simple Single Page
          Application (SPA).
        </p>
      </section>

      <!-- Aboutme  -->
      <section class="about" v-show="aboutToggle">
        <h1 class="heading">About Me</h1>
        <div class="info">
          <br />
          <h3>Name : Joseph Maxen D. Manasan</h3>
          <h3>Age : 22</h3>
          <h3>Birthday: January 31, 2000</h3>
          <h3>Weight : 80.90kg</h3>
          <h3>Course : Information Technology</h3>
          <h3>
            Address : Brgy. Malaubang, St. Stephanie, Blk. 11 Lot 16 &amp; 18,
            Purok - 6, Ozamiz City
          </h3>
        </div>
      </section>

      <!-- Education  -->
      <section class="education" v-show="educationToggle">
        <h1 class="heading">Education</h1>
        <div class="info">
          <br />
          <h3>Elementary : Misamis University</h3>
          <h3>Junior High : Ozamiz City School of Arts and Trades</h3>
          <h3>Senior High : La Salle University (Lyćee)</h3>
          <h3>College : La Salle University</h3>
        </div>
      </section>

      <!-- Hobbies  -->
      <section class="hobbies" v-show="hobbiesToggle">
        <h1 class="heading">My Hobbies</h1>
        <div class="lg:flex block justify-evenly">
          <div class=" my-3 w-96 h-64">
            <img src="@/assets/images/image1.jpg" alt="" class="w-96 h-64 border border-black"/>
          </div>

          <div class=" my-3 w-96 h-64">
            <img src="@/assets/images/image2.jpg" alt="" class="w-96 h-64"/>
          </div>

          <div class=" my-3 w-96 h-64">
            <img src="@/assets/images/image3.jpg" alt="" class="w-96 h-64"/>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import "@/assets/css/style.css";

export default {
  name: "App",
  data() {
    return {
      homeToggle: true,
      aboutToggle: false,
      educationToggle: false,
      hobbiesToggle: false,
    };
  },
  components: {},
  methods: {
    homeToggleBtn() {
      this.homeToggle = true;
      this.aboutToggle = false;
      this.educationToggle = false;
      this.hobbiesToggle = false;
    },
    aboutToggleBtn() {
      this.homeToggle = false;
      this.aboutToggle = true;
      this.educationToggle = false;
      this.hobbiesToggle = false;
    },
    educationToggleBtn() {
      this.homeToggle = false;
      this.aboutToggle = false;
      this.educationToggle = true;
      this.hobbiesToggle = false;
    },
    hobbiesToggleBtn() {
      this.homeToggle = false;
      this.aboutToggle = false;
      this.educationToggle = false;
      this.hobbiesToggle = true;
    },
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
