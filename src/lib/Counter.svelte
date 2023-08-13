<script lang="ts">
  let count: number = 0
  const increment = () => {
    count += 1
  }
</script>

<button class="btn-cnt" on:click={increment}>
  Count is {count}
</button>
<a href="/">Volver a Home</a>

<style>
  .btn-cnt {
    text-align: center;
    margin: auto;
    display: flex;
  }
</style>