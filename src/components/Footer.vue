<template>
  <footer class="footer" :class="{ 'footer-ru': locale === 'ru' }" id="footer">
    <div class="footer__container">
      <div class="footer__social">
        <p>Мы в соц. сетях:</p>
        <ul class="social-links">
          <li>
            <a href="#" target="_blank" rel="noopener noreferrer">
              <img src="/icons/vk.svg" alt="ВКонтакте" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank" rel="noopener noreferrer">
              <img src="/icons/instagram.svg" alt="Instagram" />
            </a>
          </li>
          <li>
            <a href="#" target="_blank" rel="noopener noreferrer">
              <img src="/icons/youtube.svg" alt="YouTube" />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #f0f0f0;
  padding: 20px 0;
  text-align: center;
}

.footer__container {
  max-width: 1200px;
  margin: 0 auto;
}

.footer__social {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.social-links {
  display: flex;
  list-style: none;
  padding: 0;
  margin-top: 10px;
}

.social-links li {
  margin: 0 10px;
}

.social-links img {
  width: 30px;
  height: 30px;
}

@media (min-width: 768px) {
  .footer {
    text-align: left;
  }

  .footer__social {
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
