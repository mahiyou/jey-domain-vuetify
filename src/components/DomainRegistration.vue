<template>
  <v-container class="domain-container">
    <p class="sentence1">
      همین حالا <span style="color: #ffa200">دامنه</span> مورد نظرتان را ثبت
      کنید
    </p>
    <p class="margin-b">
      همین حالا دامنه ی مورد نظرتان را جستجو و در صورت آزاد بودن، اقدام به ثبت
      آن کنید.
    </p>
    <div class="d-flex justify-center align-center margin-b">
      <form class="form-group search-input justify-center">
        <div class="input-group">
          <v-row>
            <v-col cols="2">
              <select v-model="selected" class="form-control select-domain" dir="ltr">
                <option :value="domains[index - 1].value" v-for="index in 4" :key="index">
                  <v-btn>{{ domains[index - 1].tilte}}</v-btn>
                </option>
              </select>
            </v-col>
            <v-col cols="8">
              <input
                type="text"
                class="input-style form-control ui-autocomplete-input"
                placeholder="نام دامنه مورد نظر خود را وارد کنید"
              />
            </v-col>
            <v-col cols="2">
              <v-btn variant="text" type="submit" class="btn-confirm">
                جستجو
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </form>
    </div>
    <div class="featured-tlds">
      <div dir="ltr" class="prices">
        <div class="price">.com <span>۶۰۳,۰۰۰</span></div>
        <div class="price">.org <span>۵۰۳,۰۰۰</span></div>
        <div class="price">.net <span>۷۰۳,۰۰۰</span></div>
        <div class="price">.ir <span>۴۸,۰۰۰</span></div>
      </div>
    </div>
  </v-container>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      domains: [
        { tilte: ".com", value: "com" },
        { tilte: ".org", value: "org" },
        { tilte: ".net", value: "net" },
        { tilte: ".ir", value: "ir" },
      ],
      selected: "com",
    };
  },
});
</script>

<style lang="scss">
.domain-container {
  max-width: 90%;
  background: #4f80ff;
  border-radius: 15px;
  font-family: IRANSans;
  padding: 40px;
  color: white;
  text-align: center;
  margin-bottom: 50px;
  .sentence1 {
    font-weight: 900;
    font-size: 20px;
    margin-bottom: 15px;
  }
  .margin-b {
    margin-bottom: 30px;
  }
  .search-input {
    width: 77%;
    background-color: white;
    border-radius: 40px;
    min-height: 20px;

    input:focus {
      outline: none;
    }
  }
  .input-style {
    height: 50px;
    width: 100%;
    font-size: 14px;
    color: rgb(156, 156, 156);
    text-align: left;
  }
  .select-domain {
    background: rgb(235, 235, 235);
    padding: 14px;
    border-radius: 0px 40px 40px 0px;
    width: 110px;
    float: right;
    color: black;
    text-align: center;
  }
  .btn-confirm {
    font-family: IRANSans;
    padding: 10px;
    letter-spacing: 0;
    border-radius: 40px;
    background: #ffa200;
    font-weight: 800;
    font-size: 14px;
    width: 100px;
    height: 42px;
    margin-top: 5px;
    margin-left: 7px;
    float: left;
  }

  .featured-tlds {
    width: 100%;
    overflow: auto;
  }
  .prices {
    width: 480px;
    height: 3em;
    word-spacing: 12px;
    font-size: 15px;
    margin: auto;
  }
  .price {
    display: inline-block;
    border-right: 1px solid white;
    padding: 0 10px;
    &:last-child {
      border-right: 0;
      padding-right: 0;
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
  @media (max-width: 500px) {
    max-width: 100%;
    border-radius: 0px;
    padding: 30px 20px;
  }
}
</style>