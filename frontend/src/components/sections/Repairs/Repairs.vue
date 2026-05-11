<template>

  <section class="repairs">

    <div class="container">

      <!-- TOP -->

      <div class="repairs__top">

        <div class="repairs__heading">

          <span class="repairs__label">
            направления ремонта
          </span>

          <h2 class="repairs__title">
            ЧТО МЫ ЧИНИМ
          </h2>

        </div>

        <div class="repairs__info">

          <p class="repairs__description">
            Ремонтируем игровые приставки
            и контроллеры. Чистка, пайка HDMI,
            замена стиков и восстановление питания.
          </p>

          <div class="repairs__stats">

            <div class="repairs-stat">

              <strong>
                1–2 дня
              </strong>

              <span>
                средний срок ремонта
              </span>

            </div>

            <div class="repairs-stat">

              <strong>
                180 дней
              </strong>

              <span>
                гарантия на работы
              </span>

            </div>

          </div>

        </div>

      </div>

      <!-- GRID -->

      <div class="repairs__grid">

        <!-- PS5 -->

        <article class="repair-card">

          <div class="repair-card__image">

            <img
              src="/images/tab_1.webp"
              alt=""
            />

          </div>

          <div class="repair-card__overlay"></div>

          <div class="repair-card__content">

            <span class="repair-card__number">
              01
            </span>

            <h3 class="repair-card__title">
              PLAYSTATION 5
            </h3>

            <ul class="repair-card__list">

              <li>HDMI</li>

              <li>перегрев</li>

              <li>чистка</li>

              <li>охлаждение</li>

            </ul>

          </div>

        </article>

        <!-- DUALSENSE -->

        <article class="repair-card">

          <div class="repair-card__image">

            <img
              src="/images/tab_2.webp"
              alt=""
            />

          </div>

          <div class="repair-card__overlay"></div>

          <div class="repair-card__content">

            <span class="repair-card__number">
              02
            </span>

            <h3 class="repair-card__title">
              DUALSENSE
            </h3>

            <ul class="repair-card__list">

              <li>дрифт</li>

              <li>кнопки</li>

              <li>триггеры</li>

              <li>аккумуляторы</li>

            </ul>

          </div>

        </article>

        <!-- XBOX -->

        <article class="repair-card">

          <div class="repair-card__image">

            <img
              src="/images/tab_3.webp"
              alt=""
            />

          </div>

          <div class="repair-card__overlay"></div>

          <div class="repair-card__content">

            <span class="repair-card__number">
              03
            </span>

            <h3 class="repair-card__title">
              XBOX SERIES X
            </h3>

            <ul class="repair-card__list">

              <li>чистка</li>

              <li>питание</li>

              <li>охлаждение</li>

              <li>плата</li>

            </ul>

          </div>

        </article>

      </div>

    </div>

  </section>

</template>

<script setup>
import './Repairs.scss';
</script>