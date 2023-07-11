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
    display: grid;
    grid-template-rows: subgrid;
    grid-row: 1/-1;

    align-content: start;
    padding: 1rem;
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
  }
</style>
