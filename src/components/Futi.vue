<template>
  <footer class="footer">
    <div class="footer__content">
      <div class="footer__left">
        <ul class="footer__list">
          <router-link to="/rabota">
            <li class="footer__list-item">Работа в фирме "1С"</li>
          </router-link>
          <router-link to="/vacansii">
            <li class="footer__list-item">Вакансии в фирме "1С"</li>
          </router-link>
          <p class="footer__copyright">ООО "АРКИС" © 2018 - 2024</p>
        </ul>
      </div>
      <div class="footer__logo">
        <img src="архив\vue-sait\public\trace.svg" alt="1C" class="footer__logo-img" />
      </div>
      <div class="footer__social">
        <a href="https://api.whatsapp.com/send?phone=89054012969" target="_blank" class="footer__social-link">
          <img src="архив\vue-sait\public\whatsapp-whats-app-svgrepo-com.svg" alt="whatsapp" class="footer__social-icon" />
        </a>
        <a href="https://t.me/JackP1888" target="_blank" rel="noopener noreferrer" class="footer__social-link">
          <img src="архив\vue-sait\public\telegram-svgrepo-com.svg" alt="Telegram" class="footer__social-icon" />
        </a>
        <a href="https://vk.com/prostoghora" target="_blank" rel="noopener noreferrer" class="footer__social-link">
          <img src="архив\vue-sait\public\vk-1-logo-svgrepo-com.svg" alt="ВКонтакте" class="footer__social-icon" />
        </a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #f2f2f2;
  padding: 20px;
}

.footer__content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

.footer__left {
  flex: 1;
  margin-right: 20px;
}

.footer__list {
  list-style: none;
  padding: 0;
}

.footer__list-item {
  font-size: 16px;
  margin-bottom: 10px;
  text-decoration: none;
  color: #333;
}

.footer__copyright {
  font-size: 14px;
  color: #666;
  margin-top: 10px;
}

.footer__logo {
  flex: 1;
  text-align: center;
  margin-right: 20px;
}

.footer__logo-img {
  max-width: 100%;
  height: auto;
}

.footer__social {
  flex: 1;
  display: flex;
  justify-content: flex-end;
}

.footer__social-link {
  margin-left: 10px;
}

.footer__social-icon {
  width: 40px;
  height: 40px;
}

@media (max-width: 768px) {
  .footer__content {
    flex-direction: column;
  }

  .footer__left,
  .footer__logo,
  .footer__social {
    margin-bottom: 20px;
  }
}
</style>

