<template>
  <div id="navigationbar">
    <nav class="navbar navbar-default">
      <div class="container">
        <div class="navbar-header">
          <!-- <div class="container"> -->
          <button
            type="button"
            class="navbar-toggle collapsed"
            @click="showNavbar = !showNavbar"
          >
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <router-link
            to="/"
            class="navbar-brand"
            role="button"
            style="color: #777; background-color: transparent;font-size:15px;"
          >
            首页
          </router-link>
        </div>
        <collapse class="navbar-collapse text-align" v-model="showNavbar">
          <ul class="nav navbar-nav">
            <li>
              <router-link
                to="/goodscart"
                v-show="this.$store.state.user.isLogin"
                class="navbar-brand"
                role="button"
                style="color: #777; background-color: transparent;font-size:15px;"
                >个人中心</router-link
              >
            </li>
          </ul>
          <ul class="nav navbar-nav navbar-right">
            <transition name="fade">
              <li>
                <router-link
                  to=""
                  v-show="this.$store.state.user.isLogin"
                  style="padding-bottom:10px;color: #777; background-color: transparent;"
                  >{{ this.$store.state.user.email }}</router-link
                >
              </li>
            </transition>

            <transition name="fade">
              <li>
                <a @click="logout" v-show="this.$store.state.user.isLogin"
                  >注销 <span class="glyphicon glyphicon-log-out"></span
                ></a>
              </li>
            </transition>

            <transition name="fade">
              <li>
                <router-link
                  to="/login"
                  v-show="!this.$store.state.user.isLogin"
                  @click="dialogFormVisible = true"
                  ><span class="glyphicon glyphicon-log-in"></span>
                  登录</router-link
                >
              </li>
            </transition>
          </ul>
        </collapse>
      </div>
    </nav>
  </div>
</template>

<script>
// import './element';

export default {
  data() {
    return {
      showNavbar: false,
      dialogFormVisible: false
    };
  },
  methods: {
    logout() {
      this.$store.commit('userLogout');
    },

    getUserLoginState() {
      return this.$store.state.user.isLogin;
    },
    getUserInsertState() {
      return this.$store.state.user.isInsert;
    }
  }
};
</script>

<style >
.navbar {
  margin-bottom: 0 !important;
}
.iconstyle {
  padding-bottom: 10px;
  margin-right: 0px;
  color: #777;
}

.active-disable > .router-link-active {
  color: #777;
}

.router-link-active {
  color: #555;
  background-color: #e7e7e7;
}

.navbar-default .navbar-nav > li > a:focus,
.navbar-default .navbar-nav > li > a:hover {
  color: #555;
  background-color: #e7e7e7;
}
</style>
