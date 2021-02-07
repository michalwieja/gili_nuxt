<template>
  <section class="gallery">
    <h2>
      <span class="red">Nasza</span>
      <span class="mustard">galeria</span>
    </h2>


      <CoolLightBox
        :items="items"
        :index="index"
        @close="index = null">
      </CoolLightBox>

      <div class="images-wrapper">
        <div
          class="image"
          v-for="(image, imageIndex) in items"
          :key="imageIndex"
          @click="index = imageIndex"
          :style="{ backgroundImage: 'url(' + image.src + ')' }"
        ></div>
      </div>



    <p>
      zobacz też nasz
      <a class="pink" href="https://www.facebook.com/giligilibawialnia/" target="_blank" rel="noreferrer noopener">facebook</a>
      i
      <a class="pink" href="https://www.instagram.com/giligili_bawialnia/" target="_blank"
         rel="noreferrer noopener">instagram</a>
    </p>
    <p>
      zdjęcia: elladium FOTOGRAFIA
      <a class="pink" href="http://www.elladium.pl" rel="noreferrer noopener" target="_blank">www.elladium.pl</a>
    </p>
  </section>
</template>

<script>
import CoolLightBox from 'vue-cool-lightbox'
import 'vue-cool-lightbox/dist/vue-cool-lightbox.min.css'
export default {
  data(){
    return{
      items: [
        {
          title: 'In nature, nothing is perfect and everything is perfect',
          description: "Photo by Lucas",
          src: '~/assets/img/bawialnia.jpg',
        },
        {
          title: 'A beautiful mountain view',
          description: "Photo by Facundo",
          src: 'https://upload.wikimedia.org/wikipedia/commons/4/42/Shaqi_jrvej.jpg',
        },
      ],
      index: null
    }
  },
  name: "galeria",
  components: {
    CoolLightBox,
  },
}
</script>

<style lang="scss" scoped>

.images-wrapper{
  width: 100%;
  height: auto;
  .image{
    width: 100px;
    height: 100px;
    margin: 10px;
    background-size: cover;
  }
}

section{
  flex-direction: column;
}

.gridContainer {
  display: grid;
  grid-gap: 10px;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  grid-auto-rows: 120px;
  grid-auto-flow: dense;

  a {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2em;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: 0.5s;

      &:hover {
        transform: scale(1.05);
      }
    }
  }

  .horizontal {
    grid-column: span 2;
  }

  .vertical {
    grid-row: span 2;
  }

  .big {
    grid-column: span 2;
    grid-row: span 2;
  }
}
</style>
