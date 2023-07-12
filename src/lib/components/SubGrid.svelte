<script lang="ts">
  type CardData = {
    title: string;
    image?: {
      src: string;
      alt: string;
    };
    description: string;
  };

  export let data: CardData;
</script>

<div class="wrapper">
  <img
    src={data.image ? data.image.src : ''}
    alt={data.image ? data.image.alt : ''}
    class="image"
  />
  <h2 class="title">{data.title}</h2>
  <p class="description">{data.description}</p>
</div>

<style>
  .wrapper {
    grid-row: 1/4;
    align-content: start;
    display: grid;
    row-gap: 8px;
    /* grid-template-rows: subgrid; */
    padding: 16px;
    background-color: #ddd;
    border-radius: 8px;
  }
  .image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
    background-color: #aaa;
  }
  .title {
    font-size: 20px;
    font-weight: bold;
  }
</style>
