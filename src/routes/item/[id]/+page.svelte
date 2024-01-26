<script>
  import item from '@/item.png';
  import whatsapp from '@/whatsapp.svg';
</script>

<svelte:head>
  <title>Заказать печать для компании</title>
  <meta name="description" content="Заказать печать для компании" />
</svelte:head>

<section class="item">
  <div class="container">
    <div class="item_flex">
      <div class="item_image">
        <img src={item} alt="img" />
      </div>

      <div class="item_info">
        <div class="item_info-title">Печать с изображением герба РК</div>
        <div class="item_info-desc">
          <p>
            Заказ на изготовление печати с изображением герба оформляется при наличии свидетельства
            о государственной регистрации и документов, подтверждающих полномочия первого
            руководителя или ответственного доверенного лица
            <br />
            Минимальный диаметр печати: 25+1 мм;
            <br />
            Максимальный диаметр: 50+1 мм.
          </p>
        </div>
        <div class="item_info-btns">
          <div class="item_info-btn">Оставить заявку</div>
          <div class="item_info-whatsapp">
            <span class="icon_whatsapp">
              <img src={whatsapp} alt="whatsapp" />
            </span>
            <span class="item_info-whatsapp-text">WhatsApp</span>
          </div>
        </div>
      </div>
    </div>

    <div class="item_title">Описание</div>
    <div class="item_desc">
      <p>
        Печать с воспроизведением Государственного герба РК изготавливается по заявке
        государственных органов, государственных учреждений, государственных предприятий за подписью
        руководителя или ответственного доверенного лица. Заказ на изготовление печати с
        изображением герба оформляется при наличии свидетельства о государственной регистрации и
        документов, подтверждающих полномочия первого руководителя или ответственного доверенного
        лица.
      </p>

      <p>
        Тексты гербовых печатей государственных организаций должны содержать их наименование в
        соответствии с Законом Республики Казахстан «О языках в Республике Казахстан», а также
        должны быть выполнены по всем требованиям государственных стандартов РК. В тексте печати
        государственных учреждений, государственных органов и государственных предприятий
        обязательно указывается БИН этих организаций, название фирмы-изготовителя и дата
        изготовления печати.
      </p>

      <p>
        Изготовление клише печати производится на флексорезине, фотополимере и резине с
        обязательными элементами защиты от подделок. Наши рекомендации: с учетом большого объема
        информации о наименовании государственных органов, учреждений и предприятий мы советуем
        изготавливать печати диаметром не меньше 45 мм и использовать флексорезину в качестве
        материала для изготовления клише. Это позволит внести все данные и получить четкий оттиск
        элементов герба.
      </p>
    </div>
  </div>
</section>

<style lang="scss">
  .container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 80px;
  }

  .item {
    padding: 80px 0;
  }

  .item_flex {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 40px;
    margin-bottom: 40px;
  }

  .item_image {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    max-width: 610px;
    height: 380px;
    border-radius: 12px;
    background: #f0f0f4;
    box-shadow: 0px 2px 10px 0px rgba(0, 0, 0, 0.25);
  }

  .item_info {
    display: flex;
    flex-direction: column;
    gap: 20px;
    justify-content: center;
    align-items: left;
    width: 630px;

    &-title {
      color: #141317;
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 45px;
      letter-spacing: -0.6px;
    }

    &-desc > * {
      max-width: 468px;
      color: #141317;
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px;
    }

    &-btns {
      display: flex;
      flex-direction: row;
      justify-content: start;
      gap: 40px;
    }
  }

  .item_info-btn {
    max-width: 180px;
    display: inline-flex;
    padding: 12px 24px;
    justify-content: center;
    align-items: center;
    border-radius: 8px;
    background: #e82c2c;
    color: white;
    border: none;
    color: #fff;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 24px;
    width: 177px;
  }

  .item_info-whatsapp {
    display: flex;
    justify-content: center;
    gap: 8px;
    height: 24px;
    padding: 13px 12px;
    border-radius: 8px;
    border: 0.5px solid #838d9e;
    width: 213px;

    .item_info-whatsapp-text {
      color: #141317;
      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px;
    }
  }

  .item_title {
    color: #141317;

    font-size: 40px;
    font-style: normal;
    font-weight: 700;
    line-height: 45px;
    letter-spacing: -0.6px;
    margin-bottom: 24px;
  }

  .item_desc {
    width: 1118px;
    color: #141317;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px;
  }

  @media (max-width: 1100px) {
    .item_flex {
      flex-direction: column;
      align-items: start;
    }
    .item_info {
      width: 100%;
    }

    .item_desc {
      width: 100%;
    }
  }

  @media (max-width: 768px) {
    .container {
      padding: 0 16px;
    }

    .item {
      padding-bottom: 40px;
    }

    .item_flex {
      gap: 24px;
      margin-bottom: 24px;
    }

    .item_info {
      gap: 40px;
    }

    .item_info-title {
      font-size: 18px;
      font-weight: 700;
      line-height: 22px;
    }

    .item_info-desc {
      display: none;
    }

    .item_info-btns {
      flex-direction: column;
      gap: 16px;

      .item_info-btn {
        max-width: 100%;
        width: 100%;
        padding-left: 0;
        padding-right: 0;
      }
    }

    .item_info-whatsapp {
      width: 100%;
      padding: 13px 0px;
    }

    .item_title {
      font-size: 18px;
      font-weight: 700;
      line-height: 22px;
      margin-bottom: 16px;
    }

    .item_desc {
      font-size: 14px;
      font-weight: 400;
      line-height: 18px;
    }
  }

  @media (max-width: 576px) {
    .container {
      padding: 0 16px;
    }

    .item_image {
      height: auto;
      img {
        max-width: 343px;
        height: 232px;
      }
    }
  }
</style>
