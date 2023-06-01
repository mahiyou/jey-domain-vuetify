<template>
  <v-container class="header-container">
    <v-row>
      <v-col md="6" cols="12">
        <p class="header-title">
          بزرگترین مرکز ثبت <span style="color: #4f80ff">دامنه</span> در ایران
        </p>
        <p class="header-content">
          اگر شما یک طراح هستین و یا با طراحی های گرافیکی سروکار دارید به متن
          های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند. لورم ایپسوم یا
          طرح‌نما متنی ساختگی و بدون معنی است که برای امتحان فونت و یا پر کردن
          فضا در یک طراحی گرافیکی و یا صنعت چاپ استفاده میشود. طراحان وب و
          گرافیک از این متن برای پرکردن صفحه و ارائه شکل کلی طرح استفاده
          می‌کنند.
        </p>
        <div class="center-btn">
            <v-btn class="header-btn">مشاهده ی تعرفه ها</v-btn>
        </div>
        
      </v-col>
      <v-col md="6" cols="12">
        <v-img src="@/assets/pics/girl1.gif" width="430px" class="center">
        </v-img>
      </v-col>
    </v-row>
  </v-container>
</template>
<style lang="scss">
.header-container {
  max-width: 90%;
  font-family: IRANSans;

  .header-title {
    font-size: 30px;
    font-weight: 900;
    margin-bottom: 20px;
    padding-top: 95px;
  }
  .header-content {
    font-size: 14px;
    line-height: 30px;
  }
  .header-btn {
    background: #4f80ff;
    border-radius: 25px;
    color: white;
    letter-spacing: 0;
    margin-top: 20px;
  }
  .center {
    margin: auto;
  }
  .center-btn{
      text-align: right;
    }
  @media (max-width: 600px) {
    .header-title {
      text-align: center;
      padding-top: 20px;
    }
    .center-btn{
      text-align: center;
    }
  }
  @media (max-width: 960px) {
    .header-title {
      padding-top: 20px;
    }
  }
  @media (max-width: 500px) {
    max-width: 100%;
    padding: 20px;
  }
}
</style>