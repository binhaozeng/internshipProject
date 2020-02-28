<template>
  <div class="backg">
    <el-row align="middle" justify="center" type="flex" class="row">
    <el-col :span="12" class="col-box">
      <div class="loginMain">
        <el-row align="middle" justify="center" type="flex" class="row-main">
          <el-col :span="11" class="col-main">
            <div class="left-img">
            </div>
          </el-col>
          <el-col :offset="1" :span="10" class="col-main">
            <div class="right-main">
            <p class="login-title">教师登录</p>
            <p>&nbsp;</p>
            <p>&nbsp;</p>
            <el-input v-model="account" placeholder="请输入用户名" prefix-icon="el-icon-user-solid" resize="both"></el-input>
            <p style="height: 1.9rem;">&nbsp;</p>
            <el-input v-model="password" placeholder="请输入密码" prefix-icon="el-icon-lock" resize="both"></el-input>
            <p>&nbsp;</p>
            <p>&nbsp;</p>
            <el-checkbox v-model="checked1" class="jizhuwo">记住我</el-checkbox>
            <p style="height: 1.9rem;">&nbsp;</p>
            <el-button type="primary" round>登录</el-button>
            <p style="height: 1rem;">&nbsp;</p>
            <el-checkbox v-model="checked2" class="jizhuwo">我已同意<a href="https://cdn.51bolema.com/html/agreement/index.html" style="color: #999;">《伯乐码用户服务协议》</a></el-checkbox>
            <p>&nbsp;</p>
            <p>
              推荐浏览器:
              <a class="guge" href="https://www.google.cn/chrome/"><i class="gugelogo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</i>谷歌</a>
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
              <a class="huohu" href="http://www.firefox.com.cn/"><i class="huohulogo">&nbsp;&nbsp;&nbsp; </i>火狐</a>
            </p>
            </div>
          </el-col>
        </el-row>
      </div>
    </el-col>
    </el-row>
    <p class="bottom-title">版权所有 © 2016-2020 上海践升信息科技有限公司&nbsp;&nbsp;沪ICP备19006290号-3</p>
  </div>
</template>

<script>
  export default {
    //数据存放
    data() {
      return {
        account: '',
        password: '',
        checked1: 1,
        checked2: 2
      }
    },
    //方法函数存放
    methods: {

    },
    //页面加载时
    mounted() {

    },
    //组件注册
    components: {

    },
    //自定义函数
    directives:{

    },
    //过滤器
    filters:{
    //时间戳转换
      formatDate(obj){
        return  new Date(obj).toLocaleString().replace(/:\d{1,2}$/,' ');
      }
    },
    //计算机属性对象
    computed:{

    },
    //侦听属性
    watch:{

    }
  }
</script>

<style lang="scss">
@import '@/assets/style/common.scss';
.backg{
  width: 100%;
  height: 100%;
  background: url(../assets/img/background.png) center no-repeat;
  overflow: hidden;
  background-size: cover;
  .bottom-title{
    font-size: .92rem;
    color: white;
    position: absolute;
    bottom: 0.8rem;
    left: 45rem;
    text-align: center;
  }
  .row{
    height: 100%;
    .col-box{
      height: 55%;
      .row-main{
        height: 100%;
        .col-main{
          height: 88%;
          .left-img{
            height: 100%;
            width: 100%;
            border-radius: 1.5rem;
            background: url(../assets/img/main_left.jpg);
            background-size: 100% 100%;
            box-shadow: 1px 1px 3px 0 rgba(0,0,0,.15);
          }
          .right-main{
            width: 100%;
            height: 100%;
            .guge{
              color: #2d8cf0;
              .gugelogo{
                background: url(../assets/img/guge.png);
                background-size: 100% 100%;
              }
            }
            .huohu{
              color: #2d8cf0;
              .huohulogo{
                background: url(../assets/img/huohu.png);
                background-size: 100% 100%;
              }
            }
            .el-button{
              background-color: #2d8cf0;
              padding-left: 11.3rem;
              padding-right: 11.3rem;
            }
            .jizhuwo{
              .el-checkbox__label{
                font-size: 1rem;
              }
            }
            .login-title{
              text-align: center;
              color: #2d8cf0;
              font-size: 2rem;
            }
            .el-input__inner{
              height: 3.4rem;
              font-size: 1rem;
              border-radius: 2.1875rem;
              padding-left: 3.1rem;
            }
            .el-input__prefix{
              font-size: 1.5rem;
              color: #2d8cf0;
              margin-left: 0.5rem;
            }
          }
        }
      }
    }
  }
  .loginMain{
    display: inline-block;
    width: 100%;
    height: 100%;
    background-color: white;
    border-radius: 1.5rem;
  }
}
</style>
