<template>
  <section>
    <div class="logo">logo</div>
    <hr />
    <div class="container">
      <div class="process">
        <div class="col-lg-3">1</div>
        <div class="col-lg-3">2</div>
        <div class="col-lg-3">3</div>
      </div>
      <!-- end process -->
      <div class="steps">
        <h5>الخطوات التالية :</h5>
        <p>على المستلم إحضار بطاقة الهويةورقما مرجعيا لاستلام المال</p>
        <span> ابحث عن الموقع </span>
        
        <div class="details_proccess">
          <h5>تفاصيل العملية :</h5>
          <table class="table">
          <tbody>
            <tr v-for="(item, index) in tableData" :key="index">
              <td v-html="item.column1"></td>
              <td>{{ item.column2 }}</td>
              <td>{{ item.column3 }}</td>
            </tr>
          </tbody>
        </table>
          <div class="notes">
            <p>
              ملاحظة الإيصالات عبر الإنترنت غير متوفرةلمعاملات التجارية في
              الموقع
            </p>
          </div>
        </div>
        <!-- end details_proccess -->
      </div>
      <!-- end steps -->
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      currentDate: "",
      showIcon: true,
      tableData: [
        { column1: "", column2: "تحويل", column3: "نوع العملية" },
        { column1: "", column2: "", column3: "تاريخ البدء" },
        { column1: "", column2: "", column3: "جاهز للاستلام" },
        {
          column1:
            '<svg fill="#000000" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 32 32" xml:space="preserve" width="30px" height="30px"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path id="time_1_" d="M16,31.36C7.53,31.36,0.64,24.47,0.64,16S7.53,0.64,16,0.64S31.36,7.53,31.36,16S24.47,31.36,16,31.36z M15.64,28h0.72v2.636c7.788-0.188,14.087-6.488,14.276-14.276H28v-0.72h2.636C30.447,7.853,24.147,1.553,16.36,1.364V4h-0.72V1.364C7.853,1.553,1.553,7.853,1.364,15.64H4v0.72H1.364c0.189,7.788,6.488,14.087,14.276,14.276V28z M22.748,20.312l-7.108-4.104V6h0.72v9.792l6.748,3.896L22.748,20.312z"></path><rect id="_Transparent_Rectangle" style="fill: none" width="15" height="15"></rect></g></svg>',
          column2: "123456789",
          column3: "الرقم المرجعي",
        },
      ],
    };
  },
  mounted() {
    this.updateColumn2();
  },
  methods: {
    getCurrentDate() {
      const date = new Date();
      return date.toLocaleDateString();
    },
    updateColumn2() {
      const currentDate = this.getCurrentDate();
      this.tableData[1].column2 = currentDate;
      this.tableData[2].column2 = currentDate;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" >
.table {
  border-collapse: collapse;
}

.table th,
.table td {
  padding: 8px;
}
.process {
  display: flex;
  flex-direction: row;
  justify-content: center;
  column-gap: 5px;
  // &:nth-child(1){
  //   // clip-path: polygon(75% 0%, 100% 50%, 75% 100%, 0% 100%, 0 51%, 0% 0%);
  //   // width: 280px;
  //   // height: 280px;
  // }
  div {
    background-color: gray;
    // border-radius: 20px 0 0 30px;
  }
}
.details_proccess {
  background-color: #f6f6f6;
  padding: 30px;
  div {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    border-bottom: 1px solid #c1c4c3;
    padding: 3px;
    align-items: center;
    color: #969a98;
  }
}
.notes {
  color: #565f5c;
}
</style>
