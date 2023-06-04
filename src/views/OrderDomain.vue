<template>
  <v-locale-provider rtl>
    <Toolbar @clickOnNavBtn="navigation = true" />
    <Navigation v-model="navigation" />
    <Header :step="step"/>
    <div style="background: #fafbff">
      <OrderNavigation v-model="step"/>
    </div>
    <Footer />
  </v-locale-provider>
</template>
<script>
import Toolbar from "@/components/Toolbar.vue";
import Header from "@/components/order-domain/Header.vue";
import OrderNavigation from "@/components/order-domain/OrderNavigation.vue";
import Navigation from "@/components/Navigation.vue";
import Footer from "@/components/Footer.vue";

import { defineComponent } from "vue";

export default defineComponent({
  components: {
    Toolbar,
    Header,
    OrderNavigation,
    Navigation,
    Footer,
  },
  data() {
    return {
      navigation: false,
      step: "checkDomain",
    };
  },
});
</script>