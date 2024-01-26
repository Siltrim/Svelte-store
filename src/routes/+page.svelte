<script>
  import banner from '@/banner.png';
  import arrow_left from '@/arrow_left.svg';
  import arrow_right from '@/arrow_right.svg';
  import ItemList from './components/ItemList.svelte';
</script>

<svelte:head>
  <title>Алейрон</title>
  <meta name="description" content="Алейрон" />
</svelte:head>

<section class="main">
  <div class="container">
    <div class="banner">
      <div class="image_wrapper">
        <img class={'banner_img'} src={banner} alt="banner" />
      </div>

      <div class="banner_info">
        <div class="banner_title">Заказать печать для компании</div>
        <div class="banner_desc">
          Вы можете заказать у нас практически любой товар с доставкой прямо до двери
        </div>
        <button class="banner_btn">Оставить заявку</button>
      </div>

      <div class="banner_arrow">
        <span class="arrow_left">
          <img src={arrow_left} alt="arrow_left" />
        </span>
        <span class="arrow_right">
          <img src={arrow_right} alt="arrow_right" />
        </span>
      </div>
    </div>

    <div class="catalog">
      <div class="catalog_title">Каталог товаров</div>
      <ItemList />
    </div>
  </div>
</section>

<style lang="scss">
  .container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 80px;
  }

  .main {
    margin-top: 40px;
  }

  .banner {
    position: relative;

    .image_wrapper {
      max-width: 1280px;
      width: 100%;
      img {
        width: 100%;
        height: auto;
      }
    }

    .banner_info {
      margin-left: 40px;
      margin-top: 80px;

      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      display: flex;
      flex-direction: column;

      .banner_title {
        margin-bottom: 12px;

        color: #141317;
        font-size: 40px;
        font-style: normal;
        font-weight: 700;
        line-height: 45px;
      }

      .banner_desc {
        margin-bottom: 90px;
        width: 428px;
        color: #141317;
        font-size: 16px;
        font-style: normal;
        font-weight: 500;
        line-height: 24px;
      }

      .banner_btn {
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
      }
    }

    .banner_arrow {
      display: flex;
      flex-direction: row;
      gap: 8px;
      position: absolute;
      width: 100%;
      // height: 100%;
      bottom: 45px;
      left: 48%;
      .arrow_left,
      .arrow_right {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 48px;
        height: 48px;
        border-radius: 88px;
        background: #fff;
        box-shadow: 0px 1px 5px 0px #f0f0f4;
      }
    }
  }

  .catalog {
    margin: 40px 0;
    width: 100%;
    // display: flex;

    .catalog_title {
      margin-bottom: 40px;
      color: #141317;
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 45px;
      letter-spacing: -0.6px;
    }
  }

  @media (max-width: 1200px) {
    .banner {
      .banner_info {
        position: static;
        margin-top: 12px;
        margin-left: 0;

        .banner_desc {
          margin-bottom: 12px;
        }
      }

      .banner_arrow {
        display: none;
      }
    }
  }

  @media (max-width: 768px) {
    .container {
      padding: 0 16px;
    }

    .banner {
      .banner_info {
        .banner_title {
          font-size: 24px;
          line-height: 28px;
        }
        .banner_desc {
          width: 100%;
          font-size: 14px;
          line-height: 18px;
        }
      }
    }

    .catalog {
      .catalog_title {
        font-size: 24px;
        line-height: 28px;
      }
    }
  }
</style>
