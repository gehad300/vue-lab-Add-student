<template>
  <div class="container my-1">
    <div class="row">
      <div class="col-12 py-2 bg-warning">
        <headercomponent>
  
        </headercomponent>
      </div>
    </div>

    <div class="row">
      <div class="col-4">
        <linkscomponent />
      </div>

      <div class="col-8">
        <bodycomponent />
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <!-- <h3 class="text-center">Footer</h3> -->
        <div class="col-12 text-light p-2 bg-info">
          <footercomponent />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import headercomponent from "./components/headercomponent.vue";
import linkscomponent from "./components/linkscomponent.vue";
import bodycomponent from "./components/bodycomponent.vue";
import Footercomponent from "./components/footercomponent.vue";

export default {
  components: {
    headercomponent,
    linkscomponent,
    bodycomponent,
    Footercomponent,
  },
};
</script>
<style scoped>
h5 {
  color: red;
  font-weight: bold;
}
</style>
