<template>
  <div class="container mt-3">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="addQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to Delete it</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";
import NewQuote from "./components/NewQuote";
import Header from "./components/Header";

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
    "app-new-quote": NewQuote,
    "app-header": Header
  },
  methods: {
    addQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("Please Delete Quotes First!");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
