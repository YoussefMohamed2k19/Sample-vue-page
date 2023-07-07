<template>
  <div class="card-block">
    <div class="row">
      <div class="col-md-8">
        <h3 class="h3-large">Interested working<br />with me?</h3>
      </div>
      <div
        class="col-md-4 justify-content-sm-center justify-content-md-end justify-content-lg-end pt-4"
      >
        <a href="#" class="button-large w-inline-block"
          ><div class="mail-icon"></div>
          <div class="text-block">Email Us</div></a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SendUS",
};
</script>

<style>
/* Add any custom styles here */
.card-block {
  width: 100%;
  margin-top: 50px;
  margin-bottom: 50px;
  padding: 50px 75px;
  -webkit-box-pack: justify;
  -webkit-justify-content: space-between;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  border-radius: 25px;
  background-color: #eebf63;
}
.h3-large {
  margin-top: 0px;
  margin-bottom: 0px;
  color: #fff;
  font-size: 48px;
  line-height: 62px;
  font-weight: 600;
}
.button-large {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  padding: 23px 50px;
  -webkit-box-pack: center;
  -webkit-justify-content: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  border-radius: 10px;
  background-color: #fff;
  color: #2f2f2f;
  font-size: 24px;
  line-height: 24px;
  font-weight: 600;
  text-decoration: none;
}
.mail-icon {
  width: 26px;
  height: 21px;
  margin-right: 17px;
  background-image: url("../icons/mail-icon.svg");
  background-position: 50% 50%;
  background-size: contain;
  background-repeat: no-repeat;
}
</style>
