<template>
  <section class="contact">
    <h2><span class="red">Kontakt</span></h2>

    <div class="content">
      <div class="map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2550.057744391073!2d18.965248415950835!3d50.27218040807478!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4716cde612bfb1d7%3A0x1d20ca606e58bbab!2sKleofas%20Park!5e0!3m2!1sen!2spl!4v1575994824410!5m2!1sen!2spl"
          width="100%" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
      </div>
      <div class="contact-columns">
        <div class="adress">
          <h4><span class="pink">Adres</span></h4>

          <i class="fas fa-map-marker-alt fa-2x pink"></i>

          <div class="wauto">Kleofas park</div>
          <div class="wauto">Katowice</div>
          <div class="wauto">Gliwicka 275</div>
        </div>
        <div class="hours">
          <h4><span class="mustard">Godziny otwarcia</span></h4>

          <i class="far fa-clock fa-2x mustard"></i>

          <p class="wauto">10:00-19:00</p>
          <!-- <p class="wauto">sb-nd 10:00-19:00</p> -->
        </div>
        <div class="aboutUs">
          <h4><span class="red">Telefon</span></h4>

          <i class="fas fa-mobile-alt fa-2x red"></i>
          <p class="wauto">
            <a class="tel" href="tel:513-922-938">513 922 938</a>
          </p>

        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "kontakt"
}
</script>

<style scoped lang="scss">

</style>
