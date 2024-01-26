<script>
  import logo from '@/logo.svg';
</script>

<footer class="footer">
  <div class="container">
    <div class="footer_flex">
      <div class="info_left">
        <div class="info_logo">
          <img src={logo} alt="logo" />
        </div>
        <div class="info_desc">
          «Алейрон» - известная алматинская типография полного цикла <br />, которая работает с 1992
          года, занимается полиграфией<br /> и сотрудничает<br /> с более чем тысячей компаний по всему
          Казахстану.
        </div>
      </div>

      <div class="info_right">
        <div class="info_text">Заказ по телефону</div>
        <div class="info_time">с 9:00 до 18:00</div>
        <div class="info_tel">
          <a href="tel:++77272506969">+7 727 250 69 69</a>
        </div>
      </div>
    </div>
  </div>
</footer>

<style lang="scss">
  .container {
    max-width: 1280px;
    margin: 0 auto;
  }

  .footer {
    background: #f0f0f4;
    padding: 80px 0 185px 80px;
    position: relative;
    &::after {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      bottom: 0;
      left: 0;
      display: block;
      height: 50px;
      background: #111;
    }
  }

  .footer_flex {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: start;
    gap: 140px;
    margin-right: 350px;
  }

  .info_left {
    display: flex;
    flex-direction: column;
    gap: 8px;

    .info_logo {
    }
    .info_desc {
      margin-top: -15px;
      width: 284px;
      height: 168px;
      color: #838d9e;

      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px;
    }
  }

  .info_right {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding-top: 13px;

    .info_text {
      color: #141317;
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px;
    }

    .info_time {
      color: #838d9e;
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px;
    }

    .info_tel > a {
      color: #141317;
      font-size: 24px;
      font-style: normal;
      font-weight: 500;
      line-height: 30px;
    }
  }

  @media (max-width: 1200px) {
    .footer_flex {
      margin-right: 200px;
    }
  }

  @media (max-width: 992px) {
    .footer {
      padding-left: 0;
      padding-right: 0;
      padding-top: 16px;
      padding-bottom: 165px;
    }

    .container {
      padding: 0 16px;
    }
    .footer_flex {
      margin-right: 0px;
      align-items: center;
      padding-top: 0;
    }
  }

  @media (max-width: 768px) {
    .footer_flex {
      flex-direction: column;
      gap: 40px;
      align-items: start;
    }
    .info_right {
      .info_text {
        font-weight: 500;
      }

      .info_time {
        line-height: 18px;
      }

      .info_tel > a {
        font-weight: 700;
        line-height: 28px;
      }
    }

    .info_desc {
      width: 100%;
    }
  }
</style>
