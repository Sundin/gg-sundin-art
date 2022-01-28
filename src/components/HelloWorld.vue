<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="imagez">
      <Portrait image="babylon.jpg" text="Babylons Skräck" class="portrait" />

      <Portrait
        image="space_pirate.jpg"
        text="Space Smuggler"
        class="portrait"
      />

      <Portrait
        image="ringed_planet.jpg"
        text="Ringed Planet I"
        class="portrait"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Portrait from "@/components/Portrait.vue";

@Options({
  props: {
    msg: String,
  },
  components: {
    Portrait,
  },
})
export default class HelloWorld extends Vue {
  msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
a {
  color: #42b983;
}
img {
  // max-width: 400px;
  height: auto;
}
.img-container {
  // max-width: 400px;
  position: relative;
  // width: 50%;
}
.imagez {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.portrait {
  margin: 30px;
}

@media screen and (max-width: 960px) {
  .imagez {
    flex-direction: column;
  }
}
</style>
