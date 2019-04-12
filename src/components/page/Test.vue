/*
这个页面作为登录页面的参考设计，其实是参考的boss直聘的，哈
 */
<template>
  <el-card class="box-card">
    <el-tabs v-model="activeName" @tab-click="handleClick" stretch="true">
      <el-tab-pane class="pane" label="密码登录" name="first">
        <!-- 密码登录 -->
        <el-form :model="ruleForm2" status-icon class="demo-ruleForm">
          <el-form-item prop="pass" class="pane-item">
            <el-input type="password" placeholder="手机/邮箱/用户名"></el-input>
          </el-form-item>
          <el-form-item prop="checkPass" class="pane-item">
            <el-input type="password"></el-input>
          </el-form-item>
          <el-form-item class="pane-item">
            <el-button type="primary" style="width: 100%">登录</el-button>
          </el-form-item>
        </el-form>
      </el-tab-pane>
      <el-tab-pane class="pane" label="短信登录" name="second">
        <!-- 短信登录 -->
        <el-form status-icon class="demo-ruleForm">
          <el-form-item prop="pass" class="pane-item">
            <!-- <el-input type="number" placeholder="手机"></el-input> -->
            <el-row :gutter="20">
              <el-col :span="16"><el-input placeholder="手机号码"></el-input></el-col>
              <el-col :span="8"><el-button style="width: 100%;">发送</el-button></el-col>
            </el-row>
          </el-form-item>
          <el-form-item prop="checkPass" class="pane-item">
            <el-input></el-input>
          </el-form-item>
          <el-form-item class="pane-item">
            <el-button type="primary" style="width: 100%">登录</el-button>
          </el-form-item>
        </el-form>
    
      </el-tab-pane>
    </el-tabs>
  </el-card>
</template>

<script>
export default {
  name: "test",
  data() {
    return {
      activeName: "second"
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
};
</script>
<style scoped>
.box-card {
  width: 480px;
}
.pane {
  height: 480px;
}
.pane-item {
  margin-left: 50px;
  margin-right: 50px;
}
.demo-ruleForm {
  margin-top: 25px;
}
</style>
