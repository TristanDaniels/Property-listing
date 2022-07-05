<template>
  <div class="card shadow mb-4">
    <Properties v-for="property in Properties" :key="property.id" />
  </div>
</template>
<script>
import PropertyCard from "../components/PropertyCard";
export default {
  components: PropertyCard,
  data() {
    return {
      Properties: [],
    };
  },
  mounted() {
    fetch("http://localhost:8080/Properties")
      .then((res) => res.json())
      .then((data) => (this.Properties = data))
      .catch((err) => console.log(err.message));
  },
};
</script>
<style></style>
