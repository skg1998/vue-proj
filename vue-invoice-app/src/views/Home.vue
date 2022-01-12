<template>
  <div class="home container">
    <!-- Header -->
    <div class="header flex">
      <div class="left flex flex-column">
        <h1>Invoices</h1>
        <span>There are total 4 invoices</span>
      </div>
      <div class="right flex">
        <div @click="toggleFilterMenu" class="filter flex" ref="filter">
          <span>Filter by status</span>
          <img src="@/assets/icon-arrow-down.svg" alt="" />
          <ul v-show="filterMenu" class="filter-menu">
            <l1>Draft</l1>
            <l1>Pending</l1>
            <l1>Paid</l1>
            <l1>Clear Filter</l1>
          </ul>
        </div>
        <div @click="newInvoice" class="button flex">
          <div class="inner-button flex"><img src="@/assets/icon-plus.svg" alt=""><span></span>New Invoice</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
};
</script>

<style lang="scss" scoped>
.home{
  color: #fff;
  .header{
    margin-bottom: 65px;
    .left,.right{
      flex: 1;
    }

    .right{
      justify-content: flex-end;
      align-items: center;
      .button,.filter{
        align-items: center;
        span{
          font-size: 12px;
        }
      }
    }
  }
}
</style>