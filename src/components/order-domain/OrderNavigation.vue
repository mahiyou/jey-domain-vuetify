<template>
  <v-container class="order-nav-con">
    <v-row>
      <v-col sm="4" cols="12">
        <v-tabs   center-active :align-tabs="alignTabs" :model-value="modelValue" @update:model-value="onTabChanged"  :direction="tabsDirection" hide-slider color="primary">
          <v-tab
            value="checkDomain"
            class="order-tabs-handler"
            :border="false"
            rounded="lg"
            variant="flat"
          >
            <span class="num-border">۱</span>
            بررسی دامنه
          </v-tab>
          <v-tab
            value="configuration"
            class="order-tabs-handler"
            :border="false"
            rounded="lg"
            variant="flat"
          >
            <span class="num-border">۲</span>
            پیکربندی
          </v-tab>
          <v-tab
            value="confirmDomain"
            class="order-tabs-handler"
            :border="false"
            rounded="lg"
            variant="flat"
          >
            <span class="num-border">۳</span>
            تایید دامنه
          </v-tab>
          <v-tab
            value="completeOrder"
            class="order-tabs-handler"
            :border="false"
            rounded="lg"
            variant="flat"
          >
            <span class="num-border">۴</span>
            تکمیل سفارش
          </v-tab>
        </v-tabs>
      </v-col>
      <v-col sm="8" cols="12">
        <v-window :model-value="modelValue" @update:model-value="onTabChanged">
          <v-window-item value="checkDomain">
            <CheckDomain />
          </v-window-item>
          <v-window-item value="configuration">
            <ConfigurationDomain />
          </v-window-item>
          <v-window-item value="confirmDomain">
            <v-card flat>
              <v-card-text>
                <p>
                  Fusce a quam. Phasellus nec sem in justo pellentesque
                  facilisis. Nam eget dui. Proin viverra, ligula sit amet
                  ultrices semper, ligula arcu tristique sapien, a accumsan nisi
                  mauris ac eros. In dui magna, posuere eget, vestibulum et,
                  tempor auctor, justo.
                </p>

                <p class="mb-0">
                  Cras sagittis. Phasellus nec sem in justo pellentesque
                  facilisis. Proin sapien ipsum, porta a, auctor quis, euismod
                  ut, mi. Donec quam felis, ultricies nec, pellentesque eu,
                  pretium quis, sem. Nam at tortor in tellus interdum sagittis.
                </p>
              </v-card-text>
            </v-card>
          </v-window-item>
          <v-window-item value="completeOrder">
            <v-card flat>
              <v-card-text>
                <p>
                  Fusce a quam. Phasellus nec sem in justo pellentesque
                  facilisis. Nam eget dui. Proin viverra, ligula sit amet
                  ultrices semper, ligula arcu tristique sapien, a accumsan nisi
                  mauris ac eros. In dui magna, posuere eget, vestibulum et,
                  tempor auctor, justo.
                </p>

                <p class="mb-0">
                  Cras sagittis. Phasellus nec sem in justo pellentesque
                  facilisis. Proin sapien ipsum, porta a, auctor quis, euismod
                  ut, mi. Donec quam felis, ultricies nec, pellentesque eu,
                  pretium quis, sem. Nam at tortor in tellus interdum sagittis.
                </p>
              </v-card-text>
            </v-card>
          </v-window-item>
        </v-window>
      </v-col>
    </v-row>
  </v-container>
</template>

<style lang="scss">
.order-nav-con {
  min-width: 90%;
  font-family: IRANSans;
  padding-top: 50px;

  .order-tabs-handler {
    margin-bottom: 1em;
    letter-spacing: 0px;
  }
  .num-border {
    border-left: 1px solid;
    margin-left: 10px;
    padding-left: 10px;
  }
}
</style>
<script>
import CheckDomain from "@/components/order-domain/CheckDomain.vue";
import ConfigurationDomain from "@/components/order-domain/ConfigurationDomain.vue";


import { defineComponent } from "vue";
import { useDisplay } from 'vuetify'

export default defineComponent({
  setup(){
    const display = useDisplay();
    return{
      display
    };
  },
  components:{
    CheckDomain,
    ConfigurationDomain
  },
  props: {
    modelValue: {
      type: String,
      required: true,
    },
  },
  methods: {
    onTabChanged(newTab) {
      this.$emit("update:modelValue", newTab);
    }
  },
  computed:{
    tabsDirection(){
      return this.display.name.value == "xs" ? "horizontal" : "vertical";
    },
    alignTabs(){
      return this.display.name.value == 'xs' ? 'center' : 'undefined'
    }
  }
});
</script>