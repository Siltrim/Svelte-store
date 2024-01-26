<script lang="ts">
  export let img: string;
  export let title: string;
  export let id: number;
</script>

<a href="item/{id}">
  <div class="catalog_item">
    <div class="item_img">
      <img src={img} alt={img} />
    </div>
    <div class="item_desc">{title}</div>
    <button class="item_btn">Заказать</button>
  </div>
</a>

<style lang="scss">
  .catalog_item {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 16px;

    padding: 16px;
    border-radius: 12px;
    border: 1px solid #f0f0f4;
    background: #fff;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);

    .item_img > img {
      width: 271px;
      height: 208px;
    }

    .item_desc {
      color: #141317;
      text-align: center;
      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px;
    }
    .item_btn {
      display: flex;
      width: 273px;
      padding: 12px 24px;
      justify-content: center;
      align-items: center;
      border-radius: 8px;
      border: 1px solid #f0f0f4;
      background: #f0f0f4;
    }
  }

  @media (max-width: 768px) {
    .catalog_item {
      margin-bottom: 8px;
      gap: 12px;
      padding: 16px;
      .item_img > img {
        width: 152px;
        height: 114px;
      }

      .item_desc {
        font-size: 14px;
        font-weight: 400;
        line-height: 18px;
      }
      .item_btn {
        width: 143px;
        padding: 4px 12px;
      }
    }
  }
</style>
