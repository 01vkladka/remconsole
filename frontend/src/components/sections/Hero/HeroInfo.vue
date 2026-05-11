<template>

  <div class="hero-info">

    <article class="hero-card">

      <span class="hero-card__label">
        состояние устройства
      </span>

      <div class="hero-card__rows">

        <div class="hero-card__row">
          <span>стики</span>
          <strong>износ 12%</strong>
        </div>

        <div class="hero-card__row">
          <span>кнопки</span>
          <strong class="green">
            ok
          </strong>
        </div>

        <div class="hero-card__row">
          <span>триггеры</span>
          <strong>износ 45%</strong>
        </div>

      </div>

    </article>

    <article class="hero-card">

      <span class="hero-card__label">
        причины обращений
      </span>

      <div class="hero-bars">

        <div class="hero-bars__item">

          <span>
            дрифт стиков
          </span>

          <div class="hero-bars__line">
            <i style="width: 72%"></i>
          </div>

        </div>

        <div class="hero-bars__item">

          <span>
            не заряжается
          </span>

          <div class="hero-bars__line">
            <i style="width: 34%"></i>
          </div>

        </div>

        <div class="hero-bars__item">

          <span>
            перегрев
          </span>

          <div class="hero-bars__line">
            <i style="width: 58%"></i>
          </div>

        </div>

      </div>

    </article>

  </div>

</template>

<script setup>
import './hero-info.scss';
</script>