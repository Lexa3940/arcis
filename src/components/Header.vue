<script setup>
defineProps({
  totalPrice: Number
})

const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="header-container">
    <router-link to="/" class="logo-container">
      <img src="/logo(1).svg" alt="logo" class="logo" />
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

    <div class="nav-container">
      <ul class="nav-column">
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
      </ul>

      <ul class="nav-column">
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
    </div>
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
  text-align: center;
}

@media(min-width: 768px) {
  .header-container {
    grid-template-areas: 
      "logo info nav";
    grid-template-columns: auto 1fr auto;
    align-items: center;
    text-align: left;
  }
}

.logo-container {
  grid-area: logo;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  max-height: 70px;
}

@media(min-width: 768px) {
  .logo {
    max-height: 100px;
  }
}

.info-container {
  grid-area: info;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 0.5rem; /* Уменьшен отступ сверху */
}

@media(min-width: 768px) {
  .info-container {
    flex-direction: row;
    justify-content: space-around;
    text-align: left;
    margin-top: 0; /* Убираем отступ для больших экранов */
  }
}

.working-hours, .phone-numbers {
  margin: 0 0.5rem; /* Уменьшен отступ между колонками */
  text-align: left;
}

.nav-container {
  grid-area: nav;
  display: flex;
  flex-direction: column;
  margin-top: 0.5rem; /* Уменьшен отступ сверху */
}

@media(min-width: 768px) {
  .nav-container {
    flex-direction: row;
    justify-content: space-around;
    margin-top: 0; /* Убираем отступ для больших экранов */
  }
}

.nav-column {
  display: flex;
  flex-direction: column;
  list-style: none;
  padding: 0;
  margin: 0 0.5rem; /* Уменьшен отступ между колонками */
}

.nav-item {
  display: flex;
  align-items: center;
  cursor: pointer;
  color: #718096;
  transition: color 0.3s ease;
  margin-bottom: 0.5rem;
  white-space: nowrap;
}

.nav-item:hover {
  color: #000;
}

.nav-icon {
  margin-right: 0.5rem;
}
</style>
