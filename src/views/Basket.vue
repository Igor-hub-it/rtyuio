<template>
  <div class="main">
    <div class="content">
      <div class="content__title">
        <h3>Ваши покупки</h3>
        <h4>Совместимость компонентов: {{ "есть" }}</h4>
      </div>
      <div class="content__purchases">
        <div class="content__component component">
            <img class="component__img-cmpnt" src="/images/Без названия.jpg" alt="">
            <div class="component__description">Lorem ipsum dolor, sit amet consectetur adipisicing.</div>
            <div class="component__info">
              <div class="component__cost">Цена: {{ '1р' }}</div>
              <button class="component__delete">&#10006;</button>
            </div>
        </div>
      </div>
      <div class="content__end">
        <div class="content__finalPrise"><h4>Итоговая цена: {{  }}</h4></div>
        <button class="content__buybtn">Купить</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      
    }
  },
}
</script>

<style lang="scss" scoped>
  .main {
    height: 100vh;
    width: 100%;
    padding: 30px;
    background-color: #f6f6f6;
  }
  .content {
    width: 80%;
    margin: auto;
    padding: 20px;
    border-radius: 5px;
    background-color: white;
    &__title {
      margin-bottom: 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    &__end {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    &__buybtn {
      height: 30px;
      width: 100px;
      padding: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #1c3062;
      border-radius: 3px;
      color: #fff;
    }
    &__buybtn:hover {
      background-color: #183a8f;
    }
  }
  .component {
    border: 0.5px solid #eee;
    border-radius: 5px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    align-items: center;
    margin-bottom: 20px;

    &__buying, &__info {
      display: flex;
      gap: 15px;
      justify-content: space-between;
      align-items: center;
    }

    img {
      height: 120px;
      width: 120px;
      border-radius: 5px;
    }
    &__description {
      padding-right: 15px;
    }
    &__delete {
      height: 50px;
      width: 50px;
      border: 1px solid #eee;
      margin-right: 20px;
      border-radius: 3px;
      background-color: #fff;
      font-size: 20px;
      @media screen and (max-width: 400px) {
        // : 20px;
        margin-bottom: 10px;
      }
    }
    &__delete:hover {
      border-radius: 3px;
      background-color: #eee;
    }

    &:hover {
      border: 0.1px solid #717bff;
    }
  }

  @media screen and (max-width: 900px) {
    .component {
      &__description {
        padding: 2em 16px;
        flex: 100%;
        text-align: center;
        order: 1000;
      }
    }
  }
</style>