<template >
  <v-locale-provider rtl>
    <Toolbar />
    <div style="background: #fafbff">
      <Header />
      <DomainRegistration />
      <Prices />
      <SuitableDomain />
      <PanelFeatures />
      <BuyDomain />
      <Questions />
      <NewArticle />
    </div>
    <Footer />
  </v-locale-provider>
</template>

<script lang="ts" setup>
import Toolbar from "@/components/Toolbar.vue";
import Header from "@/components/Header.vue";
import DomainRegistration from "@/components/DomainRegistration.vue";
import Prices from "@/components/Prices.vue";
import SuitableDomain from "@/components/SuitableDomain.vue";
import PanelFeatures from "@/components/PanelFeatures.vue";
import BuyDomain from "@/components/BuyDomain.vue";
import Questions from "@/components/Questions.vue";
import NewArticle from "@/components/NewArticle.vue";
import Footer from "@/components/Footer.vue";

</script>
