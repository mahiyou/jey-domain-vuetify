<template>
  <v-container class="toolbar-container" id="tb">
    <v-toolbar density="compact" color="white">
      <v-row>
        <v-col sm="2" cols="6">
          <div style="width: 110px">
            <v-img
              src="@/assets/pics/JeyDomain.svg"
              class="mt-4 mt-sm-2"
            ></v-img>
          </div>
        </v-col>
        <v-col sm="7" cols="1">
          <div class="visible">
            <v-row>
              <v-col cols="2">
                <v-btn class="toolbar-btn" href="#"> صفحه ی اصلی </v-btn></v-col
              >
              <v-col cols="2"
                ><v-btn class="toolbar-btn" href="#"> تعرفه ها </v-btn>
              </v-col>
              <v-col cols="2">
                <v-btn class="toolbar-btn" href="#">
                  سوالات متداول
                </v-btn></v-col
              >
              <v-col cols="2">
                <v-btn class="toolbar-btn" href="#"> درباره ی ما </v-btn></v-col
              >
              <v-col cols="2">
                <v-btn class="toolbar-btn" href="#"> بلاگ </v-btn></v-col
              >
            </v-row>
          </div>
        </v-col>
        <v-col sm="3" cols="5">
          <v-app-bar-nav-icon
            class="float-left nav-icon-visible"
            @click="$emit('clickOnNavBtn')"
          ></v-app-bar-nav-icon>

          <div class="float-left visible">
            <v-btn class="toolbar-btn" href="#"> ورود </v-btn>
            <v-btn class="toolbar-btn signup-btn" href="#"> ثبت نام </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-toolbar>
  </v-container>
</template>
<script>
import { defineComponent } from "vue"

  export default defineComponent({
    emits: ["clickOnNavBtn"]
  })
</script>
<style lang="scss">
#tb {
  max-width: 90%;
  padding-left: 0px;
  padding-right: 0px;
}
.toolbar-container {
  max-width: 90%;
  font-family: IRANSans;
  .toolbar-btn {
    letter-spacing: 0;
    font-size: 12px;
  }
  .signup-btn {
    background: #4f80ff;
    border-radius: 25px;
    color: white;
  }
  .visible {
    display: block;
    @media (max-width: 850px) {
      display: none;
    }
  }
  .nav-icon-visible {
    display: none;
    @media (max-width: 850px) {
      display: block;
    }
  }
}
</style>