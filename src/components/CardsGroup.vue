<template>
  <div class="cards-group">
    <el-row :gutter="10">
      <el-col :xs="12" :sm="6" :md="6" :lg="6" v-for="(o, index) in 4" :key="o">
        <el-card :body-style="{ padding: '0px' }">
          <img src="../assets/images/hamburger.50e4091.png" class="image">
          <div style="padding: 14px;">
            <span>好吃的汉堡</span>
            <div class="bottom clearfix">
              <time class="time">{{ currentDate }}</time>
              <el-button type="text" class="button">操作按钮</el-button>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'cards-group',
  data () {
    return {
      currentDate: new Date()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
    display: table;
    content: "";
}

.clearfix:after {
    clear: both
}
.cards-group {
  overflow: hidden;
}
</style>
