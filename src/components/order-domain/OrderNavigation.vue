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
            <v-card flat>
              <v-card-text>
                <p>
                  Morbi nec metus. Suspendisse faucibus, nunc et pellentesque
                  egestas, lacus ante convallis tellus, vitae iaculis lacus elit
                  id tortor. Sed mollis, eros et ultrices tempus, mauris ipsum
                  aliquam libero, non adipiscing dolor urna a orci. Curabitur
                  ligula sapien, tincidunt non, euismod vitae, posuere
                  imperdiet, leo. Nunc sed turpis.
                </p>

                <p>
                  Suspendisse feugiat. Suspendisse faucibus, nunc et
                  pellentesque egestas, lacus ante convallis tellus, vitae
                  iaculis lacus elit id tortor. Proin viverra, ligula sit amet
                  ultrices semper, ligula arcu tristique sapien, a accumsan nisi
                  mauris ac eros. In hac habitasse platea dictumst. Fusce ac
                  felis sit amet ligula pharetra condimentum.
                </p>

                <p>
                  Sed consequat, leo eget bibendum sodales, augue velit cursus
                  nunc, quis gravida magna mi a libero. Nam commodo suscipit
                  quam. In consectetuer turpis ut velit. Sed cursus turpis vitae
                  tortor. Aliquam eu nunc.
                </p>

                <p>
                  Etiam ut purus mattis mauris sodales aliquam. Ut varius
                  tincidunt libero. Aenean viverra rhoncus pede. Duis leo. Fusce
                  fermentum odio nec arcu.
                </p>

                <p class="mb-0">
                  Donec venenatis vulputate lorem. Aenean viverra rhoncus pede.
                  In dui magna, posuere eget, vestibulum et, tempor auctor,
                  justo. Fusce commodo aliquam arcu. Suspendisse enim turpis,
                  dictum sed, iaculis a, condimentum nec, nisi.
                </p>
              </v-card-text>
            </v-card>
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
    CheckDomain
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