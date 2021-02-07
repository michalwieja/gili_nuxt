<template>
  <div>
    <div @click="onClick" :class="{menuActive}" class="menu">
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
    <nav :class="{navActive}" class="nav">
      <ul class="nav-links">
        <li v-for="(link,index) in links" :key="index"@click="onLinkClick">
          <NuxtLink  :to="link" class="nav-link">{{ link }}</NuxtLink>
        <li>
        <a rel="noreferrer noopener" target="_blank" href="https://sklep.giligili.pl" class="nav-link ">sklep</a>
        </li>
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
      links: ['bawialnia', 'urodziny', 'warsztaty', 'kawiarnia', 'galeria', 'kontakt']
    }
  },
  methods: {
    onClick() {
      this.navActive = !this.navActive;
      this.menuActive = !this.menuActive
    },
    onLinkClick() {
      console.log('ok')
      this.navActive = !this.navActive;
      this.menuActive = !this.menuActive
    }
  }
}
</script>
