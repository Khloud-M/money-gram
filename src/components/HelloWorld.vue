<template>
  <section>
    <div class="logo">logo</div>
    <hr />
    <div class="cotnianer">
      <div class="process">
        <div class="col-lg-3">1</div>
        <div class="col-lg-3">2</div>
        <div class="col-lg-3">3</div>
      </div>
      <!-- end process -->
      <div class="steps">
        <h6>الخطوات التالية :</h6>
        <p>على المستلم إحضار بطاقة الهويةورقما مرجعيا لاستلام المال</p>
        <span> ابحث عن الموقع </span>
        <div class="details_proccess">
          table
        </div>
        <!-- end details_proccess -->
      </div>
      <!-- end steps -->
      <div class="notes">
        <p> ملاحظة الإيصالات عبر الإنترنت غير متوفرةلمعاملات التجارية في الموقع</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HelloWorld",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
.process {
  display: flex;
  flex-direction: row;
  justify-content: center;
  column-gap: 5px;
}
.process div {
  background-color: gray;
  border-radius: 20px 0 0 30px;
}
</style>
