<template>
  <div>
    <main class="container" v-show="!inputHidden">
      <h1 class="page-header">登录</h1>
      <p>输入您的邮箱地址，用于登录的验证邮件将发送到您的邮箱。</p>
      <div class="row">
        <div class="form-group col-xs-9">
          <div class="input-group">
            <span class="input-group-addon">用户名</span>
            <input
              placeholder="您的邮箱地址"
              :class="{
                input: true,
                'is-danger': errors.has('email'),
                'input-lg': true,
                'form-control': true
              }"
              v-validate="'required|email'"
              type="text"
              name="email"
              v-model="email"
            />
          </div>
        </div>
        <button
          type="submit"
          value="Login"
          @click="next"
          class="btn btn-primary btn-lg col-xs-2"
        >
          登录
        </button>
      </div>
    </main>
  </div>
</template>

<script>
import router from '@/router';

export default {
  data() {
    return {
      inputHidden: false,
      email: ''
    };
  },
  methods: {
    next() {
      if (this.email.length <= 0) {
        this.$message({
          showClose: true,
          message: '请输入邮箱',
          type: 'error'
        });
      } else {
        if (this.$validator.errorBag.has('email') === false) {
          this.inputHidden = true;
          this.$store.commit('userLogin', {
            email: this.email,
            isLogin: true
          });
          router.push('/');
        } else {
          this.$message({
            showClose: true,
            message: '请输入正确格式的邮箱地址',
            type: 'error'
          });
        }
      }
    }
  }
};
</script>

<style>
</style>
