<template>
  <div class="hello">
    <h1>The Fantastic Art of G.G. Sundin</h1>
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

    <div class="imagez">
      <Portrait
        image="neptunus.jpg"
        text="Varlesen från Neptunus"
        class="portrait"
      />

      <Portrait image="terras_bane.jpg" text="Terras Bane" class="portrait" />
    </div>

    <div class="imagez">
      <Portrait image="revelation.jpg" text="The Revelation" class="portrait" />

      <Portrait image="the_beholder.jpg" text="The Beholder" class="portrait" />

      <Portrait image="gotcha.jpg" text="Gotcha!" class="portrait" />
    </div>
    <hr />
    <p>© G.G. Sundin 2022</p>
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

.hello {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.img-container {
  // max-width: 400px;
  position: relative;
  // width: 50%;
}
.imagez {
  max-width: 1200px;
  margin-left: 30px;
  margin-right: 30px;
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
