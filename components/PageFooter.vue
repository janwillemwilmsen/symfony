<template>
  <footer class="outer">
    <div>
      <NuxtLink to="/" class="logo">
        <img src="/logo-shop2.png" alt="" width="69"  />
      </NuxtLink>
    </div>


  <div>
    <img src="/harts.png" style="width:150px;" alt="Symfony">
  </div>

    <footer class="navlist">
      <h5>Menu</h5>
      <ul>
      <li v-for="child of navItems" :key="child.path" class="nav-list-item">
        <NuxtLink :to="child.path">
          {{ child.name }}
        </NuxtLink>
      </li>
      </ul>
    </footer>
    <div class="powered">
      <p>eCommerce by</p>
      <a href="https://crystallize.com" aria-label="crystallize.com">
        <img src="/logo-crystallize.svg" alt="" width="120" height="54" />
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  props: {
    navItems: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.outer {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  max-width: 1600px;
  margin: 50px auto;
  border-top: 2px solid var(--color-box-background);
  padding: 50px 50px;
  justify-content: space-between;
}

.logo img {
  width: 70px;
}

.powered {
  width: 100%;
  display: block;
  display: flex;
  align-items: center;
  font-size: 12px;
  font-weight: 600;
}

.powered p {
  margin: 0;
}

.powered img {
  width: 120px;
}

.navlist {
  list-style: none;
  font-weight: 500;
  font-size: 1rem;
  display: block;
  margin: 0 0 0 auto;
}

.navlist li {
  line-height: 2.5rem;
}

.navlist h5 {
  font-size: 0.7rem;
  font-weight: 400;
  margin-bottom: 10px;
}
</style>
