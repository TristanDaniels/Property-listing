<template>
  <div class="card shadow mb-4">
    <img
      v-bind:src="property.image"
      class="car-img mb-4 img-fluid"
      alt="Picture of Property"
    />
    <h5 class="text-black">{{ property.title }}</h5>
    <p class="text-secondary">
      {{ property.location }}
    </p>
    <p>{{ property.price }}</p>
    <div class="d-flex flex-row justify-content-center">
      <i class="fa-solid fa-bed me-2"></i>{{ property.bedrooms }}
      <i class="fa-solid fa-shower me-2 ms-2"></i>{{ property.bathrooms }}
      <i class="fa-solid fa-car me-2 ms-2"></i>{{ property.carspace }}
      <i class="fa-solid fa-person me-2 ms-2"></i>{{ property.population }}
    </div>
    <p class="mt-2">{{ property.type }}</p>
  </div>
</template>
<script>
export default {
  props: ["property"],
};
</script>
<style>
.card {
  border: 2px solid;
  width: 300px;
}
</style>
