<template >
    <div class="activePublic " >
      <!-- 步骤组件 -->
      <el-steps :space="200" :active="step" class="step" style="margin:20px 0;">
        <el-step title="活动信息" description=""></el-step>
        <el-step title="报名签到" description=""></el-step>
        <el-step title="分享设置" description=""></el-step>
        <el-step title="个性设置" description=""></el-step>
      </el-steps>

        <!-- 视图 -->
      <router-view class="view"></router-view>

      <div class="but-group" >
        <el-button >预览</el-button>
        <el-button >上一步</el-button>
        <el-button  type="primary" @click="next">下一步</el-button>
        <el-button  type="primary">发布活动</el-button>
<!--         <router-link :to="{name:'bb'}">bb</router-link>
        <router-link to="/activePublic/aa">Go to Foo</router-link> -->
      </div>

      <!-- <a v-link="a">aa</a> -->
    </div>
</template>

<script>
  export default {
    data() {
      return {
        step: 0
      };
    },

    methods: {
      next() {
        this.step ++;
      }
    }
  }
</script>
