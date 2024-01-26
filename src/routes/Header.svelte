<script>
  import logo from '@/logo.svg';
  import search from '@/search.svg';
  import whatsapp from '@/whatsapp.svg';
  import mail from '@/mail.svg';
</script>

<header>
  <div class="header_container">
    <div class="container">
      <div class="header_flex">
        <div class="header-menu__icon"><span></span><span></span><span></span></div>

        <div class="header_logo">
          <a href="/">
            <img src={logo} alt="logo" />
          </a>
        </div>

        <div class="header_search">
          <div class="input_search">
            <input class="header_input" type="text" placeholder="Поиск" id="search" />
            <span class="icon_search"><img src={search} alt="search" /></span>
          </div>
        </div>

        <div class="header_whatsapp">
          <span class="icon_whatsapp">
            <img src={whatsapp} alt="whatsapp" />
          </span>
          <span class="text_whatsapp">WhatsApp</span>
        </div>

        <div class="header_mail">
          <span class="icon_mail">
            <img src={mail} alt="mail" />
          </span>
          <span class="mail_text">sales@aleyron.com</span>
        </div>
      </div>
    </div>
  </div>
</header>

<style lang="scss">
  .container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 80px;
  }

  .header_container {
    padding: 16px 0px;

    border-bottom: 1px solid #f0f0f4;
    background: #fff;
    box-shadow:
      0px 1px 3px 0px rgba(136, 141, 150, 0.05),
      0px 5px 5px 0px rgba(136, 141, 150, 0.04),
      0px 11px 7px 0px rgba(136, 141, 150, 0.03),
      1px 20px 8px 0px rgba(136, 141, 150, 0.01),
      1px 31px 9px 0px rgba(136, 141, 150, 0);
  }

  .header_flex {
    position: relative;
    max-width: 1360px;
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    justify-content: left;
    align-items: center;
    gap: 24px;
  }

  .input_search {
    position: relative;

    .header_input {
      display: flex;
      width: 613px;
      height: 26px;
      padding: 12px 20px;
      justify-content: space-between;
      align-items: center;
      flex-shrink: 0;
      border-radius: 8px;
      background: #f0f0f4;
      border: none;
    }

    .header_input::placeholder {
      color: #838d9e;
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px;
    }

    .icon_search {
      position: absolute;
      top: 12px;
      right: 20px;
    }
  }

  .header_mail {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .header_whatsapp {
    display: flex;
    justify-content: center;
    gap: 8px;
    height: 24px;
    padding: 13px 12px;
    border-radius: 8px;
    border: 0.5px solid #838d9e;

    .text_whatsapp {
      color: #141317;
      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px;
    }
  }

  .header_mail {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;
    .icon_mail {
      width: 24px;
      height: 24px;
      flex-shrink: 0;
    }
    .mail_text {
      color: #141317;
      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px;
    }
  }

  .header-menu__icon {
    display: none;
  }

  @media (max-width: 1200px) {
    .header_flex {
      .header_input {
        width: 350px;
      }
    }
  }

  @media (max-width: 992px) {
    .header_flex {
      .header_input {
        width: 150px;
      }
    }
  }

  @media (max-width: 768px) {
    .container {
      padding: 0 16px;
    }

    .header_search,
    .header_mail {
      display: none;
    }
    .header_logo {
      padding-left: 35px;
    }

    .header_flex {
      justify-content: space-between;
    }

    .header_whatsapp {
      padding: 0;
      height: auto;
      border: none;

      .icon_whatsapp {
        display: block;

        img {
          width: 48px;
          height: 48px;
        }
      }

      .text_whatsapp {
        display: none;
      }
    }

    .header-menu__icon {
      display: block;
      position: absolute;
      top: 16px;
      left: 0px;
      width: 20px;
      height: 18px;
      cursor: pointer;
      z-index: 5;
      span {
        border-radius: 10px;

        position: absolute;
        top: 8px;
        left: 0;
        width: 100%;
        height: 2.7px;
        background-color: #000;
        transition: all 0.3s ease 0s;
        &:first-child {
          top: 1px;
        }
        &:last-child {
          top: auto;
          bottom: 1px;
        }
      }
    }
  }
</style>
