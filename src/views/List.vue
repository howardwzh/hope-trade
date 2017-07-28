<template>
  <div class="list">
    <el-row :gutter="16">
      <el-col :xs="24" :sm="24" :md="18" :lg="18">
        <el-input placeholder="请输入内容" v-model="input5">
          <el-select v-model="select" slot="prepend" placeholder="请选择">
            <el-option label="餐厅名" value="1"></el-option>
            <el-option label="订单号" value="2"></el-option>
            <el-option label="用户电话" value="3"></el-option>
          </el-select>
          <el-button slot="append" icon="search"></el-button>
        </el-input>
        <el-form ref="form" :model="form" label-width="80px">
          <el-form-item label="产品尺寸">
            <el-checkbox-group v-model="form.type">
              <el-checkbox label="10cm以下" name="type"></el-checkbox>
              <el-checkbox label="10cm - 20cm" name="type"></el-checkbox>
              <el-checkbox label="21cm - 30cm" name="type"></el-checkbox>
              <el-checkbox label="31cm - 50cm" name="type"></el-checkbox>
            </el-checkbox-group>
          </el-form-item>
          <el-form-item label="产品颜色">
            <el-checkbox-group v-model="form.type">
              <el-checkbox label="透明" name="type"></el-checkbox>
              <el-checkbox label="半透明" name="type"></el-checkbox>
              <el-checkbox label="红色" name="type"></el-checkbox>
              <el-checkbox label="蓝色" name="type"></el-checkbox>
            </el-checkbox-group>
          </el-form-item>
        </el-form>
        <el-form ref="form2" :model="form2" label-width="80px">
          <el-form-item label="排序方式">
            <el-select size="small" v-model="form.region" placeholder="排序方式">
              <el-option label="价格从低到高" value="shanghai"></el-option>
              <el-option label="价格从高到低" value="beijing"></el-option>
              <el-option label="销量从高到低" value="beijing"></el-option>
              <el-option label="销量从低到高" value="beijing"></el-option>
            </el-select>
          </el-form-item>
        </el-form>
        <el-row :gutter="16">
          <el-col :xs="8" :sm="6" :md="8" :lg="8" v-for="(o, index) in 4" :key="o">
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
      </el-col>
      <el-col :xs="24" :sm="24" :md="6" :lg="6">
        <h3 class="title-small">相似产品</h3>
        <el-row :gutter="16">
          <el-col :xs="8" :sm="6" :md="24" :lg="24" v-for="(o, index) in 4" :key="o">
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
			</el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'list',
  data () {
    return {
      form: {},
      currentDate: new Date()
    }
  },
  methods: {
    filter () {}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
  .el-form {
    margin: 16px 0;
    text-align: left;
    .el-form-item {
      margin-bottom: 0;
    }
  }
  .el-select-dropdown {
    li {
      display: list-item;
    }
  }
  .el-card {
    padding: 16px;
    margin-bottom: 16px;
    img {
      width: 100%;
    }
  }
  .title-small {
    text-align: left;
    margin: 0 0 16px;
  }
</style>
