<script lang="ts">
  let count: number = $state(0);
  let squared: number = $state(0);

  const increment = () => {
    count += 1;
  };

  const square = (a: number) => {
    return a * a;
  };
</script>

<article class="card space-y-4 p-4">
  <button onclick={increment} class="btn preset-outlined-primary-500">
    count is {count}
  </button>

  <button
    onclick={() => (squared = square(count))}
    class="btn preset-outlined-primary-500"
  >
    squared is {squared}
  </button>
</article>
