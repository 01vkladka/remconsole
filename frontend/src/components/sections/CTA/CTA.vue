<template>

  <section class="cta">

    <!-- BG -->

    <div class="cta__background">

      <img
        src="/images/cta_bg.webp"
        alt=""
      />

    </div>

    <div class="cta__overlay"></div>

    <div class="container">

      <div class="cta__layout">

        <!-- LEFT -->

        <div class="cta__content">

          <span class="cta__label">
            готово к игре
          </span>

          <h2 class="cta__title">
            ВАША КОНСОЛЬ
            <br />
            <span>
              КАК НОВАЯ
            </span>
          </h2>

          <p class="cta__description">
            Проверяем устройство,
            тестируем после ремонта
            и выдаём с гарантией.
          </p>

          <div class="cta__stats">

            <div class="cta-stat">

              <strong>
                180 дней
              </strong>

              <span>
                гарантия на ремонт
              </span>

            </div>

            <div class="cta-stat">

              <strong>
                1–2 дня
              </strong>

              <span>
                средний срок ремонта
              </span>

            </div>

            <div class="cta-stat">

              <strong>
                PS5 / Xbox
              </strong>

              <span>
                современные консоли
              </span>

            </div>

          </div>

         <div class="cta__actions">

  <div class="cta__button">

    <AppButton
      text="оставить заявку"
    />

  </div>

  <div class="cta__meta">
    Ответим быстро
    и поможем с проблемой
  </div>

</div> 

        </div>

      </div>

    </div>

  </section>

</template>

<script setup>
import AppButton from '@components/ui/button/button.vue';

import './CTA.scss';
</script>