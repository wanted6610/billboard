<template>
  <div>
    <section class="section consultation-section">
      <IndexConsultation />
    </section>
    <div class="hr"></div>
    <section class="section offer-section">
      <IndexOffer />
    </section>
    <div class="hr"></div>
    <section class="section clients-section">
      <IndexClients />
    </section>
    <div class="hr"></div>
    <section class="section reviews-section">
      <IndexReviews />
    </section>
  </div>
</template>

<script>
import IndexConsultation from "~/components/pages/index/IndexConsultation";
import IndexOffer from "~/components/pages/index/IndexOffer";
import IndexClients from "~/components/pages/index/IndexClients";
import IndexReviews from "~/components/pages/index/IndexReviews";
export default {
  name: 'IndexPage',
  components: {IndexReviews, IndexClients, IndexOffer, IndexConsultation}
}
</script>

<style lang="scss" scoped>
.hr {
  height: 2px;
  background: $green;
  width: 100%;
}

.section {
  padding: 30px 0;
  @media screen and (min-width:768px) {
    padding: 50px 0;
  }
  @media screen and (min-width:1140px) {
    padding: 80px 0;
  }
}
</style>
