<template>
  <v-container class="check-domain-container">
    <div>
      شما می توانید در زیر وضعیت دامنه مورد نظر خود و سایر پسوندها را مشاهده
      کنید:
    </div>
    <div class="search-domain">
      <div class="d-flex justify-center align-center margin-b">
        <form class="form-group search-input justify-center">
          <div class="input-group">
            <v-row>
              <v-col cols="9">
                <input
                  type="text"
                  class="input-style form-control ui-autocomplete-input"
                  placeholder="نام دامنه مورد نظر خود را وارد کنید"
                />
              </v-col>
              <v-col cols="3">
                <v-btn variant="text" type="submit" class="btn-confirm">
                  جستجو
                </v-btn>
              </v-col>
            </v-row>
          </div>
        </form>
      </div>
    </div>
    <div class="domain-search-resault">
      <P class="mb-5"> دامنه ی rion.com در دسترس است. </P>
      <w-row>
        <span class="price">۶۰۳,۰۰۰ تومان</span>

        <v-btn variant="text" class="buy-btn">خرید دامنه</v-btn>
      </w-row>
    </div>
    <div class="domain-sugestion">
      <div class="ds-title">دامنه های پیشنهادی</div>
      <div>
      <v-row class="sugestions" v-for="index in domains.length" :key="index">
        <v-col md="8" cols="6"><span style="font-weight: 100">rion</span>{{domains[index-1]}}</v-col>
        <v-col md="2" cpls="3">۴۸,۰۰۰</v-col>
        <v-col md="2" cols="3"
          ><v-btn variant="text" class="buy-btn-2">خرید دامنه</v-btn></v-col
        >
      </v-row>
      </div>
      <div class="ds-last">
        <a class="link" href="#">مشاهده ی دامنه های پیشنهادی دیگر</a>
      </div>
    </div>
  </v-container>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      domains:[".ir",".org",".net"]
    };
  },
});
</script>
<style lang="scss">
.check-domain-container {
  padding: 25px 20px;
  font-size: 14px;
  font-family: IRANSans;

  .search-domain {
    background-image: url("@/assets/pics/globe.svg");
    background-position: 98% -2%;
    background-size: 217px;
    border-radius: 5px;
    background-color: #f5f5f5;
    width: 100%;
    height: 110px;
    margin: 20px 0px;
    padding: 5px;

    .margin-b {
      margin-bottom: 30px;
    }
    .search-input {
      width: 70%;
      background-color: white;
      border-radius: 45px;
      min-height: 18px;
      margin-top: 30px;
    }
    .input-style {
      height: 50px;
      width: 100%;
      font-size: 14px;
      color: rgb(156, 156, 156);
      padding: 20px;
    }
    .btn-confirm {
      font-family: IRANSans;
      padding: 3px;
      letter-spacing: 0;
      border-radius: 40px;
      font-weight: 800;
      font-size: 14px;
      width: 120px;
      height: 38px;
      float: left;
      background-color: #4f80ff;
      color: white;
      margin: 7px 0px 0px 11px;
    }
  }

  .domain-search-resault {
    padding: 30px;
    text-align: center;
    margin: 40px 0px;
    border: 1px dashed #aeaeae;
    color: #5cb85c;
    font-size: 14px;
    font-weight: 800;
    .price {
      color: black;
      font-weight: 900;
      font-size: 16px;
    }
    .buy-btn {
      background: #5cb85c;
      color: white;
      letter-spacing: 0;
      font-family: IRANSans;
      border-radius: 50px;
      padding: 5px;
      width: 110px;
      margin-right: 20px;
    }
    @media(max-width: 400px){
      .price {
      font-weight: 700;
      font-size: 14px;}
      .buy-btn {

        width: 90px;
      }
    }
  }
  .domain-sugestion {
    .ds-title {
      background: #f5f5f5;
      padding: 14px;
      border-radius: 7px 7px 0px 0px;
      border-bottom: 1px solid #5cb85c;
      font-weight: 500;
      margin-bottom: 15px;
    }
    .ds-last {
      background: #f5f5f5;
      padding: 14px;
      font-weight: 500;
      text-align: center;
      margin-top: 10px;
      margin-bottom: 40px;
      .link {
        text-decoration: none;
        color: #4f80ff;
        font-weight: 600;
      }
    }
    .buy-btn-2 {
      background: #4f80ff;
      color: white;
      letter-spacing: 0;
      font-family: IRANSans;
      border-radius: 50px;
      padding: 3px;
      width: 90px;
      margin-top: -7px;
      font-size: 11px;
      font-weight: 600;
    }
    .sugestions {
      padding: 3px 14px 0px 14px;
      font-weight: 700;
      font-size: 15px;
      border-bottom: 1px dashed #aeaeae;
      &:last-child {
        border-bottom: 0;
      }
    }
  }
  @media (max-width: 600px) {
    .search-input {
      min-width: 100%;
    }
    .select-domain {
      width: 70px;
    }
    .input-style {
      width: 80%;
      padding-left: 10px;
      padding-right: 8px;
    }
  }
}
</style>