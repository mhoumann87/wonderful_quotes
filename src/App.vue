<template>
  <div class="container">
    <app-new-quote @quoteAdded="addQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";
import NewQuote from "./components/NewQuote";

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
    "app-quote-grid": QuoteGrid,
    "app-new-quote": NewQuote
  },
  methods: {
    addQuote(quote) {
      this.quotes.push(quote);
      console.log(quote);
    }
  }
};
</script>

<style>
</style>
