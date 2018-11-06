<template>
  <div class="container-fluid">
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";

export default {
  data: function() {
    return {
      quotes: [
        "It's only after we've lost everything that we're free to do anything."
      ],
      maxQuotes: 10
    };
  },
  components: {
    "app-quote-grid": QuoteGrid
  }
};
</script>

<style>
</style>
