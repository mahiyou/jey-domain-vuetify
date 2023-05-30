<template>
  <v-container class="sd-container">
    <div>
      <p class="sd-title">چه دامنه ای برای کسب و کار من مناسب تر است؟</p>
      <p class="sd-content">
        گر شما یک طراح هستین و یا با طراحی های گرافیکی سروکار دارید به متن های
        برخورده اید که با نام لورم ایپسوم شناخته می‌شوند.
      </p>
    </div>
    <v-row>
      <v-col md="7" cols="12" class="padding-top">
        <p class="sd-paragraph1">
          اگر شما یک طراح هستین و یا با طراحی های گرافیکی سروکار دارید به متن
          های برخورده اید که با نام لورم ایپسوم شناخته می‌شوند. لورم ایپسوم یا
          طرح‌نما  متنی ساختگی و بدون معنی است که برای
          امتحان فونت و یا پر کردن فضا در یک طراحی گرافیکی و یا صنعت چاپ استفاده
          میشود. طراحان وب و گرافیک از این متن برای پرکردن صفحه و ارائه شکل کلی
          طرح استفاده می‌کنند. طراحان سایت هنگام طراحی قالب سایت معمولا با این
          موضوع رو برو هستند که محتوای اصلی صفحات آماده نیست. در نتیجه طرح کلی
          دید درستی به کار فرما نمیدهد.
        </p>
        <p class="sd-paragraph2">
             اگر طراح بخواهد دنبال متن های مرتبط
          بگردد تمرکزش از روی کار اصلی برداشته میشود و اینکار زمان بر خواهد بود.
          همچنین طراح به دنبال این است که پس از ارایه کار نظر دیگران را در مورد
          طراحی جویا شود و نمی‌خواهد افراد روی متن های موجود تمرکز کنند.
        </p>
      </v-col>
      <v-col md="5" cols="12">
        <v-img class="man-img center" src="@/assets/pics/man1.svg" width="270px"> </v-img>
      </v-col>
    </v-row>
  </v-container>
</template>
<style lang="scss">
.sd-container {
  max-width: 90%;
  font-family: IRANSans;
  text-align: center;
  margin-bottom: 40px;
  .sd-title {
    font-weight: 900;
    font-size: 28px;
    margin-bottom: 15px;
  }
  .sd-content {
    font-size: 14px;
    margin-bottom: 40px;
  }
  .sd-paragraph1{
    font-size: 14px;
    text-align: right; 
    padding-top: 38px;
  }
  .sd-paragraph2{
    font-size: 14px;
    text-align: right; 
  }
  .man-img{
    margin-right: 80px;
  }
  .center{
    margin: auto;
  }
  @media(max-width: 960px) {
    .sd-paragraph1{
      padding-top:0px;
    }
  }
}
</style>