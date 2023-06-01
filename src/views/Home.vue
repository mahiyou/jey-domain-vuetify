<template >
  <v-locale-provider rtl>
    <Toolbar @clickOnNavBtn="navigation = true;"/>
    <Navigation v-model="navigation"/>
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

<script>
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
import Navigation from "@/components/Navigation.vue";


import { defineComponent } from "vue"

export default defineComponent({
  components:{
    Toolbar,
    Header,
    DomainRegistration,
    Prices,
    SuitableDomain,
    PanelFeatures,
    BuyDomain,
    Questions,
    NewArticle,
    Footer,
    Navigation
  },
  data(){
    return{
      navigation : false
    }
  }
})

</script>
