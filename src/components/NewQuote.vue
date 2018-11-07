<template>
  <div class="row">
   
      <div class="col-12 col-sm-8 offset-sm-2 col-md-6 offset-md-3 form-group">
    <form>
        <label>New Quote</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
        <button class="btn btn-primary mt-3" @click.prevent="createNew">Add Quote</button>
    </form>
      </div>

    
  </div>  
  
</template>

<script>
export default {
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  }
};
</script>

<style scoped>
</style>

