<script setup>
defineProps({
  totalPrice: Number
})

const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="header-container">
    <router-link to="/" class="logo-container">
      <img src="/logo.png" alt="logo" class="logo" />
    </router-link>

    <div class="info-container">
      <div class="working-hours">
        <h1>Режим работы:</h1>
        <p>Ежедневно</p>
        <p>С 8:00 до 18:00</p>
      </div>
      <div class="phone-numbers">
        <h1>Номера телефонов:</h1>
        <p>+7-995-208-44-74</p>
        <p>+7-861-205-00-91</p>
      </div>
    </div>

    <ul class="nav-container">
      <li @click="() => emit('openDrawer')" class="nav-item">
        <img src="/cart.svg" alt="Cart" class="nav-icon" />
        <span>Корзина</span>
      </li>

      <router-link to="/favorites">
        <li class="nav-item">
          <img src="/heart.svg" alt="Favorites" class="nav-icon" />
          <span>Избранное</span>
        </li>
      </router-link>

      <router-link to="/profile">
        <li class="nav-item">
          <img src="/profile.svg" alt="Profile" class="nav-icon" />
          <span>О нас</span>
        </li>
      </router-link>

      <router-link to="/conf">
        <li class="nav-item">
          <img src="/product/password_protect_secure_security_privacy_lock_padlock_icon_219328.svg" alt="Confidentiality" class="nav-icon" />
          <span>Конфиденциальность</span>
        </li>
      </router-link>
    </ul>
  </header>
</template>

<style scoped>
.header-container {
  display: grid;
  grid-template-areas: 
    "logo"
    "info"
    "nav";
  grid-gap: 1rem;
  border-bottom: 1px solid #cbd5e0;
  padding: 1rem;
}

@media(min-width: 768px) {
  .header-container {
    grid-template-areas: 
      "logo info nav";
    grid-template-columns: 1fr 2fr 1fr;
    align-items: center;
  }
}

.logo-container {
  grid-area: logo;
  display: flex;
  align-items: center;
}

.logo {
  max-height: 50px;
}

.info-container {
  grid-area: info;
  display: flex;
  justify-content: space-around;
  text-align: center;
}

.working-hours, .phone-numbers {
  text-align: left;
}

.nav-container {
  grid-area: nav;
  display: flex;
  justify-content: space-around;
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  display: flex;
  align-items: center;
  cursor: pointer;
  color: #718096;
  transition: color 0.3s ease;
}

.nav-item:hover {
  color: #000;
}

.nav-icon {
  margin-right: 0.5rem;
}
</style>
