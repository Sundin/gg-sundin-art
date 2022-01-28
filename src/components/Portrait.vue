<template>
  <div class="img-container">
    <ExpandableImage
      class="image"
      :src="require(`@/assets/images/${image}`)"
      :thumbnail="require(`@/assets/thumbnails/${image}`)"
      :alt="text"
      :title="text"
    ></ExpandableImage>
    <div class="middle">
      <div class="text">{{ text }}</div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import ExpandableImage from "@/components/ExpandableImage.vue";

@Options({
  props: {
    image: String,
    text: String,
  },
  components: {
    ExpandableImage,
  },
})
export default class Portrait extends Vue {
  image!: string;
  text!: string;
}
</script>

<style scoped lang="scss">
.image {
  opacity: 1;
  display: block;
  width: 100%;
  height: auto;
  transition: 0.5s ease;
  backface-visibility: hidden;
}

.middle {
  transition: 0.5s ease;
  opacity: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  text-align: center;
}

.img-container:hover .image {
  opacity: 0.3;
}

.img-container:hover .middle {
  opacity: 1;
}

.text {
  color: white;
  font-size: 16px;
  padding: 16px 32px;
}
</style>
