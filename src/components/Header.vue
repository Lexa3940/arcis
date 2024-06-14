<script setup>
defineProps({
  totalPrice: Number
})

const emit = defineEmits(['openDrawer'])
</script>

<style scoped>
.header-container {
  display: grid;
  grid-template-areas:
    "logo"
    "info"
    "nav";
  grid-template-rows: auto auto auto;
  grid-template-columns: 1fr;
  grid-gap: 1rem;
  border-bottom: 1px solid #cbd5e0;
  padding: 1rem;
  text-align: center;
}

@media (min-width: 768px) {
  .header-container {
    grid-template-areas:
      "logo info nav";
    grid-template-columns: auto 1fr auto;
    align-items: center;
    text-align: left;
    grid-gap: 1rem;
    padding: 1rem;
  }
}

.logo-container {
  grid-area: logo;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 1rem;
}

.logo {
  max-height: 70px;
}

@media (min-width: 768px) {
  .logo {
    max-height: 100px;
  }
}

.info-container {
  grid-area: info;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 0.5rem;
  margin-right: 1rem;
}

@media (min-width: 768px) {
  .info-container {
    flex-direction: row;
    justify-content: space-around;
    text-align: left;
    align-items: center;
    margin-top: 0;
  }
}

.working-hours,
.phone-numbers {
  margin: 0.5rem;
  text-align: center;
}

.nav-container {
  grid-area: nav;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 0.5rem;
}

@media (min-width: 768px) {
  .nav-container {
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    margin-top: 0;
  }
}

.nav-column {
  display: flex;
  flex-direction: column;
  list-style: none;
  padding: 0;
  margin: 0.5rem; /* увеличил отступ между колонками */
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
