<template>
  <div>
    <div @click="onClick" :class="{menuActive}" class="menu">
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
    <nav :class="{navActive}" class="nav">
      <ul class="nav-links">
        <li><a href="#about" class="nav-link">bawialnia</a></li>
        <li><a href="#birthday" class="nav-link">urodziny</a></li>
        <li><a href="#activities" class="nav-link">warsztaty</a></li>
        <li><a href="#cafe" class="nav-link">kawiarnia</a></li>
        <li><a href="#gallery" class="nav-link">galeria</a></li>
        <li><a href="#contact" class="nav-link">kontakt</a></li>
        <li><a href="https://sklep.giligili.pl" class="nav-link ">sklep</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Menu",
  data() {
    return {
      menuActive: false,
      navActive: false,
    }
  },
  methods: {
    onClick() {
      this.navActive = !this.navActive;
      this.menuActive = !this.menuActive
    }
  }
}
</script>
