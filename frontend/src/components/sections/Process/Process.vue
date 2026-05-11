<template>

  <section
    class="process"
    style="background-image: url('/images/Process_bg.webp')"
  >

    <div class="process__overlay"></div>

    <div class="container">

      <!-- TOP -->

      <div class="process__top">

        <div class="process__heading">

          <span class="process__label">
            как мы работаем
          </span>

          <h2 class="process__title">
            ПРОЦЕСС
            РЕМОНТА
          </h2>

        </div>

        <p class="process__description">
          Проверяем устройство, согласовываем стоимость,
          выполняем ремонт и тестируем консоль
          перед выдачей.
        </p>

      </div>

      <!-- GRID -->

      <div class="process__grid">

        <!-- CARD -->

        <article class="process-card">

          <div class="process-card__image">

            <img
              src="/images/Process_1.webp"
              alt=""
            />

          </div>

          <div class="process-card__content">

            <span class="process-card__number">
              01
            </span>

            <h3 class="process-card__title">
              ДИАГНОСТИКА
            </h3>

            <p class="process-card__text">
              HDMI, питание,
              перегрев и плата.
            </p>

          </div>

        </article>

        <!-- CARD -->

        <article class="process-card process-card--reverse">

          <div class="process-card__image">

            <img
              src="/images/Process_2.webp"
              alt=""
            />

          </div>

          <div class="process-card__content">

            <span class="process-card__number">
              02
            </span>

            <h3 class="process-card__title">
              СОГЛАСОВАНИЕ
            </h3>

            <p class="process-card__text">
              Согласовываем стоимость
              ремонта заранее.
            </p>

          </div>

        </article>

        <!-- CARD -->

        <article class="process-card">

          <div class="process-card__image">

            <img
              src="/images/Process_3.webp"
              alt=""
            />

          </div>

          <div class="process-card__content">

            <span class="process-card__number">
              03
            </span>

            <h3 class="process-card__title">
              РЕМОНТ
            </h3>

            <p class="process-card__text">
              Пайка и замена
              компонентов.
            </p>

          </div>

        </article>

        <!-- CARD -->

        <article class="process-card process-card--reverse">

          <div class="process-card__image">

            <img
              src="/images/Process_4.webp"
              alt=""
            />

          </div>

          <div class="process-card__content">

            <span class="process-card__number">
              04
            </span>

            <h3 class="process-card__title">
              ВЫДАЧА
            </h3>

            <p class="process-card__text">
              Тестируем и выдаём
              консоль с гарантией.
            </p>

          </div>

        </article>

      </div>

    </div>

  </section>

</template>

<script setup>
import './Process.scss';
</script>