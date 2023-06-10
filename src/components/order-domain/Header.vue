<template>
  <div class="contact-us-container">
    <p class="title">{{ title }}</p>
    <p>{{ subtitle }}</p>
  </div>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {
      texts: {
        checkDomain: {
          title: "بررسی دامنه",
          subtitle:
            "به متن های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند.",
        },
        configuration: {
          title: "پیکربندی دامنه",
          subtitle:
            "به متن های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند.",
        },
        confirmDomain: {
          title: "تایید دامنه",
          subtitle:
            "به متن های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند.",
        },
        completeOrder: {
          title: "تکمیل سفارش",
          subtitle:
            "به متن های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند.",
        },
      },
    };
  },
  props: {
    step: {
      type: String,
      required: true,
    },
  },
  computed: {
    title() {
      return this.texts[this.step].title;
    },
    subtitle() {
      return this.texts[this.step].subtitle;
    },
  },
});
</script>
<style lang="scss" scoped>
.contact-us-container {
  background: #4f80ff;
  text-align: center;
  padding: 50px 0px;
  color: white;
  font-size: 14px;
  line-height: 40px;
  .title {
    font-size: 30px;
    font-weight: 900;
  }
}
</style>