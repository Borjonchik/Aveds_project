<template>
  <div class="home">
    <div class="container">
      <h1 class="main_title">
        Место для получения медицинской помощи
      </h1>
      <div class="main-page-buttons buttons">
        <router-link to="/login">
          <button>
            Войти
          </button>
        </router-link>
        <router-link to="/about">
          <button style="background: none; color: #FF685B; border: 1px solid #FF685B">
            Контакты
          </button>
        </router-link>
      </div>
      <ul>
        <li>
          <div class="list_info">
            <img class="list_logo" src="../assets/first.svg" alt="">
            <h2 class="flat">Онлайн-прием</h2>
            <div>
              <img src="../assets/fixed-width.svg" alt="">
            </div>
            <p>Рыба текст</p>
          </div>
        </li>
        <li>
          <div class="list_info">
            <img class="list_logo" src="../assets/second.svg" alt="">
            <h2 class="flat">Экстренный случай</h2>
            <div>
              <img src="../assets/fixed-width.svg" alt="">
            </div>
            <p>Рыба текст</p>
          </div>
        </li>
        <li>
          <div class="list_info">
            <img class="list_logo" src="../assets/third.svg" alt="">
            <h2 class="flat">Лечение рака</h2>
            <div>
              <img src="../assets/fixed-width.svg" alt="">
            </div>
            <p>Рыба текст</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style>
.container {
  padding: 97px 197px;
  display: flex;
  flex-flow: row wrap;
  max-width: 1046px;
}

h1 {
  font-family: Montserrat;
  margin: 0;
  margin-bottom: 32px;
  font-size: 58px;
  font-weight: 700;
  line-height: 80px;
  letter-spacing: 0.20000000298023224px;
  text-align: left;
}

.buttons {
  display: flex;
  gap: 10px;
}

button {
  padding: 15px 40px;
  font: Montserrat;
  background: #FF685B;
  border: none;
  color: #FFFFFF;
  border-radius: 5px;
}

.main-page-buttons button {
  margin-bottom: 96px;
  width: 100%;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 700;
  line-height: 22px;
  letter-spacing: 0.20000000298023224px;
  text-align: center;
}

.main-page-buttons button :last-child {
  background: none;
}

ul {
  padding: 0;
  margin: 0;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  gap: 30px;
  width: 100%;
}

li {
  display: flex;
  flex-flow: row wrap;
  padding: 35px 40px;
  list-style-type: none;
  width: 248px;
  box-shadow: 0px 13px 19px 0px #00000012;
}

.list_info {
  display: flex;
  flex-flow: column wrap;
  align-items: flex-start;
  max-width: 328px;
  width: 100%;
}

.list_info img {
  margin-bottom: 7px;
}

.list_info h2 {
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;
  letter-spacing: 0.10000000149011612px;
  text-align: left;
}

.list_info div {
  margin-bottom: 10px;
}

.list_info p {
  font-family: Montserrat;
  margin: 0;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
  letter-spacing: 0.20000000298023224px;
  text-align: left;
}

@media (max-width: 375px) {
  .container {
    padding: 10px;
    max-width: 375px;
  }

  h1 {
    font-family: Montserrat;
    font-size: 28px;
    font-weight: 700;
    line-height: 39px;
    letter-spacing: 0.20000000298023224px;
    text-align: left;
    margin-bottom: 45px;
  }

  .main-page-buttons button {
    margin-bottom: 30px;
  }

  li {
    padding: 35px 54px;
  }
}
</style>