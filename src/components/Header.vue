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
      <!-- Колонка 1 -->
      <div class="nav-column">
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
      </div>
      <!-- Колонка 2 -->
      <div class="nav-column">
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
      </div>
    </div>
  </header>
</template>
