<template >
    <v-locale-provider rtl>
      <Toolbar @clickOnNavBtn="navigation = true;"/>
      <Navigation v-model="navigation"/>
      <Header />
      <div style="background: #fafbff">
        <SendMessage />
    </div>
      <Footer />
  </v-locale-provider>
</template>

<script>
import Toolbar from "@/components/Toolbar.vue";
import Header from "@/components/contact-us/Header.vue";
import SendMessage from "@/components/contact-us/SendMessage.vue";
import Navigation from "@/components/Navigation.vue";
import Footer from "@/components/Footer.vue";



import { defineComponent } from "vue"

export default defineComponent({
  components:{
    Toolbar,
    Header,
    SendMessage,
    Navigation,
    Footer,
  },
  data(){
    return{
      navigation : false
    }
  }
})
</script>