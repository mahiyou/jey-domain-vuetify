<template>
  <v-container class="toolbar-container" id="tb">
    <v-toolbar density="compact" color="white">
      <v-row>
        <v-col md="9" cols="6">
          <v-row>
            <v-col md="2" cols="12">
              <v-img
                src="@/assets/pics/JeyDomain.svg"
                width="110px"
                class="mt-2"
              >
              </v-img>
            </v-col>
            <v-col cols="2" class="p-0">
              <v-btn class="toolbar-btn px-0 btn-display" style="padding: 0px;" href="#">
                صفحه ی اصلی
              </v-btn></v-col
            >
            <v-col cols="2"
              ><v-btn class="toolbar-btn px-0 btn-display" style="padding: 0px;" href="#"> تعرفه ها </v-btn>
            </v-col>
            <v-col cols="2">
              <v-btn class="toolbar-btn px-0 btn-display" style="padding: 0px;" href="#">
                سوالات متداول
              </v-btn></v-col
            >
            <v-col cols="2">
              <v-btn class="toolbar-btn px-0 btn-display" style="padding: 0px;" href="#">
                درباره ی ما
              </v-btn></v-col
            >
            <v-col cols="2">
              <v-btn class="toolbar-btn px-0 btn-display" style="padding: 0px;" href="#"> بلاگ </v-btn></v-col
            >
          </v-row>
        </v-col>
        <v-col md="3" cols="6">
          <div class="float-left">
          <v-btn class="toolbar-btn " href="#"> ورود </v-btn>
          <v-btn class="toolbar-btn signup-btn " href="#"> ثبت نام </v-btn></div>
        </v-col>
      </v-row>
    </v-toolbar>
  </v-container>
</template>
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
    font-size: 14px;
    @media (max-width: 960px) {
      font-size: 12px;
    }
  }
  .signup-btn {
    background: #4f80ff;
    border-radius: 25px;
    color: white;
  }
  .btn-display{
      padding-bottom: 0px;
    }
  @media(max-width: 960px) {
    .btn-display{
      display: none;
      padding: 0px;
    }
  }
}
</style>