<template>
  <div>
    <section id="about" class="hero is-medium is-dark" style="background-color: hsl(0, 0%, 8%)">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title is-spaced">Почему мы?</h1>
          <p class="subtitle">
            Основа нашей работы – это обеспечение согласованных профессиональных действий всех участников транспортного процесса при реализации задач любой степени сложности.

            Компания решает для своих клиентов практически любые задачи, связанные с международными грузоперевозками, внутренними доставками по стране, локальными перевозками по городу Бишкек, офисным и домашним переездам, таможенной очисткой и сертификацией товаров.

            Мы готовы предоставлять персональный сервис для каждого из наших клиентов и находить наилучшие решения для каждого конкретного груза.
          </p>
        </div>
      </div>
    </section>

    <div class="c-projects__showcase tile is-gapless is-ancestor">
      <div class="tile is-5 is-vertical is-parent">
        <a href="#contact" class="c-projects__thumbnail image tile is-child">
          <img src="~/assets/images/move.jpg" alt="move">
          <figcaption class="has-text-centered">
            <h2 class="title">Переезды</h2>
            <p class="subtitle">Экономия до 20% вашего времени  на поиске машины, грузчиков и мебельщиков.
              Переезд в Бишкеке с 100% гарантией сохранности ваших вещей</p>
            <p class="subtitle">Подробнее</p>
          </figcaption>
        </a>

        <a class="c-projects__thumbnail image tile is-child" href="#contact">
          <img src="~/assets/images/delivery.jpg" alt="delivery">
          <figcaption class="has-text-centered">
            <h2 class="title">Курьерская служба</h2>
            <p class="subtitle">Экспресс доставка документов и посылок по Бишкеку собственными курьерами в рамках одного дня. Экономьте до 20% ваших ресурсов</p>
            <p class="subtitle">Подробнее</p>
          </figcaption>
        </a>
      </div>

      <div class="tile is-parent">
        <a href="#contact" class="c-projects__thumbnail image tile is-child">
          <img src="~/assets/images/truck.jpg" alt="">
          <figcaption class="has-text-centered">
            <h2 class="title">Международные грузоперевозки</h2>
            <p class="subtitle">Организуем все этапы перевозки и доставим ваш груз в целости - сохранности.
              Проконтролируем все документы и выполним обещания по срокам</p>
            <p class="subtitle">Подробнее</p>
          </figcaption>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'projects-showcase',
    methods: {
      openUrl (url) {
        if (process.browser) {
          window.open(url)
        }

        return false
      }
    }
  }
</script>

<style lang="scss" scoped>
  .c-projects__showcase {
    background-color: black;
  }

  .c-projects__thumbnail {
    position: relative;
    overflow: hidden;
    cursor: pointer;

    img {
      object-fit: cover;
      height: 100%;
      transition: opacity 0.5s, transform 0.5s, filter 0.5s;
    }

    &:hover img {
      opacity: 0.4;
      filter: blur(2px);
    }

    figcaption {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      transition: opacity 0.5s;
      opacity: 0;
    }

    &:hover figcaption {
      opacity: 1;
    }

    .title {
      margin: 0 0 1em;
      background: rgba(0, 0, 0, 0.9);
      color: darkred;
      text-transform: uppercase;
      font-weight: 500;
      transition: margin 0.35s;
    }

    .subtitle {
      display: inline-block;
      margin: 0 0 0.25em;
      padding: 0.4em 1em;
      background: rgba(255, 255, 255, 0.9);
      color: black;
      font-weight: 500;
      margin: 0 20px;
    }

    .title, .subtitle {
      display: inline-block;
      padding: 0.4em 1em;
      box-shadow: 0 1px 10px rgba(0,0,0,0.2);
    }

    &:hover .title {
      margin: 0 0 0.25em;
    }
  }
</style>
