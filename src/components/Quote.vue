<template>
    <div class="col-sm-6 col-md-4 col-lg-3 kort">
    <div class="quote">
      <slot></slot>
      </div>
    </div>
</template>

<script>
export default {};
</script>

<style scoped>
.kort {
  box-sizing: border-box;
  font-family: "Caveat", cursive;
  font-size: 1.6rem;
  color: #6e6e6e;
  margin-bottom: 1rem;
}

.quote {
  cursor: pointer;
  border: 1px solid rgba(40, 40, 40, 0.1);
  padding: 10px;
}

.quote:hover {
  background-color: #ffe2e2;
}
</style>


