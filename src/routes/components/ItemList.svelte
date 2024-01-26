<script lang="ts">
  import catalog_img1 from '@/catalog_img1.svg';
  import catalog_img2 from '@/catalog_img2.svg';
  import catalog_img3 from '@/catalog_img3.svg';
  import catalog_img4 from '@/catalog_img4.svg';
  import Item from './Item.svelte';

  const ITEMS: ItemsProps[] = [
    { id: 1, img: catalog_img1, title: 'Печать для ТОО' },
    { id: 2, img: catalog_img2, title: 'Печать для КХ / ИП' },
    { id: 3, img: catalog_img3, title: 'Печать с гербом РК' },
    { id: 4, img: catalog_img4, title: 'Печать для ОЮЛ' },
  ];
</script>

<div class="catalog_item-list">
  {#each ITEMS as item}
    <Item img={item.img} title={item.title} id={item.id} />
  {/each}
</div>

<style lang="scss">
  .catalog_item-list {
    display: flex;
    flex-direction: row;
    gap: 17px;
    flex-wrap: wrap;
  }

  @media (max-width: 1400px) {
    .catalog_item-list {
      justify-content: center;
    }
  }

  @media (max-width: 768px) {
    .catalog_item-list {
      gap: 9px;
    }
  }
</style>
