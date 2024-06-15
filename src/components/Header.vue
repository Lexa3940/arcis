<script setup>
defineProps({
  totalPrice: Number
})

const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="header-container flex justify-between items-center border-b border-slate-300 p-4">
    <router-link to="/">
      <div class="logo-container flex items-center">
        <img src="/logo.png" alt="logo" class="logo relative" />
      </div>
    </router-link>

    <div class="info-container flex flex-col gap-2 text-xl font-bold text-wrap pt-4">
      <h1 class="text-center">Режим работы:</h1>
      <p class="text-center">Ежедневно</p>
      <p class="text-center">С 8:00 до 18:00</p>
    </div>

    <div class="nav-container flex items-center gap-4 pt-4">
      <ul class="nav-list flex items-center gap-4">
        <li
          @click="() => emit('openDrawer')"
          class="nav-item flex items-center cursor-pointer text-grey-500 hover:text-black"
        >
          <img src="/cart.svg" alt="Cart" class="nav-icon pr-2" />
          <span class="text-xl">Корзина</span>
        </li>

        <router-link to="/favorites">
          <li class="nav-item flex items-center cursor-pointer text-grey-500 hover:text-black">
            <img src="/heart.svg" alt="Cart" class="nav-icon pr-1" />
            <span class="text-xl pl-0.5">Избранное</span>
          </li>
        </router-link>
      </ul>

      <ul class="nav-list flex items-center gap-4">
        <router-link to="/profile">
          <li class="nav-item flex items-center cursor-pointer text-grey-500 hover:text-black">
            <img src="/profile.svg" alt="Cart" class="nav-icon px-2" />
            <span class="text-xl">О нас</span>
          </li>
        </router-link>

        <router-link to="/conf">
          <li class="nav-item flex items-center cursor-pointer text-grey-500 hover:text-black">
            <img
              src="\public\product\password_protect_secure_security_privacy_lock_padlock_icon_219328.svg"
              alt="confi"
              class="nav-icon pr-1.5 text-xl"
            />
            <span class="text-xl">Конфиденциальность</span>
          </li>
        </router-link>
      </ul>
    </div>

    <div class="phone-container flex flex-col gap-2 text-xl font-bold text-wrap pt-4">
      <h1 class="text-center">Номера телефонов:</h1>
      <p class="text-center">+7-995-208-44-74</p>
      <p class="text-center">+7-861-205-00-91</p>
    </div>
  </header>
</template>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}

.logo-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  max-height: 70px;
}

.info-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}

.nav-container {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.nav-list {
  display: flex;
  justify-content: space-between;
  align-items: center;
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

.phone-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}

/* Медиа-запросы */

@media (max-width: 768px) {
  .header-container {
    flex-direction: column;
    align-items: flex-start;
  }

  .info-container {
    margin-bottom: 1rem;
  }

  .nav-container {
    flex-direction: column;
  }

  .nav-list {
    flex-direction: column;
    gap: 1rem;
  }

  .phone-container {
    margin-top: 1rem;
  }
}

@media (min-width: 768px) {
  .header-container {
    flex-direction: row;
    align-items: center;
  }

  .info-container {
    flex-direction: row;
    justify-content: space-around;
    margin-bottom: 0;
  }

  .nav-container {
    flex-direction: row;
    justify-content: flex-end;
  }

  .nav-list {
    flex-direction: row;
    gap: 2rem;
  }

  .phone-container {
    margin-top: 0;
  }
}
</style>
