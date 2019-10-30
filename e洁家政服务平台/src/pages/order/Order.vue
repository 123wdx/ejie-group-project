<template>
    <div class="order">
        <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="所有订单" name="first">
                 <el-table :data="orders" style="width: 100%" :row-class-name="tableRowClassName">
            <el-table-column prop="id" label="订单编号"  width="180"></el-table-column>
            <el-table-column prop="name" label="下单时间" width="180"></el-table-column>
             <el-table-column prop="name" label="总价" width="180"></el-table-column>
              <el-table-column prop="name" label="状态" width="180"></el-table-column>
               <el-table-column prop="name" label="顾客id" width="180"></el-table-column>
        </el-table>
            </el-tab-pane>
            <el-tab-pane label="待派单" name="second">配置管理</el-tab-pane>
            <el-tab-pane label="待支付" name="third">角色管理</el-tab-pane>
            <el-tab-pane label="待服务" name="fourth">定时任务补偿</el-tab-pane>
            <el-tab-pane label="待接单" name="fifth">配置管理</el-tab-pane>
            <el-tab-pane label="待确认" name="sixth">角色管理</el-tab-pane>
            <el-tab-pane label="已完成" name="seventh">定时任务补偿</el-tab-pane>
        </el-tabs>
    </div>
</template>
<script>
  export default {
    data() {
      return {
        activeName: 'first'
      };
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>