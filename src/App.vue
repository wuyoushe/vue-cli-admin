<template>
  <div id="app">
    <div class="layout">
      <Layout>
        <Header>
          <Menu mode="horizontal" theme="dark" active-name="1">
            <div class="layout-logo"><img src="./assets/logo_new.png" style="width: 100px;height: 60px;"></div>
            <div class="layout-nav">
              <MenuItem name="1">
                <Icon type="ios-paper"  />
                管理首页
              </MenuItem>
              <MenuItem name="2">
                <Icon type="ios-people" />
                用户管理
              </MenuItem>
              <Submenu name="3">
                <template slot="title">
                  <Icon type="ios-stats" />
                  统计分析
                </template>
                <MenuGroup title="使用">
                  <MenuItem name="3-1">新增和启动</MenuItem>
                  <MenuItem name="3-2">活跃分析</MenuItem>
                  <MenuItem name="3-3">时段分析</MenuItem>
                </MenuGroup>
                <MenuGroup title="留存">
                  <MenuItem name="3-4">用户留存</MenuItem>
                  <MenuItem name="3-5">流失用户</MenuItem>
                </MenuGroup>
              </Submenu>
              <MenuItem name="4">
                <Icon type="ios-construct" />
                综合设置
              </MenuItem>
            </div>
          </Menu>
        </Header>
        <Layout>
          <Sider hide-trigger :style="{background: '#fff'}">
            <Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
              <Submenu name="1">
                <template slot="title">
                  <Icon type="ios-paper" />
                  管理首页
                </template>
                <MenuItem name="1-1">文章管理</MenuItem>
                <MenuItem name="1-2">评论管理</MenuItem>
                <MenuItem name="1-3">举报管理</MenuItem>
              </Submenu>
              <Submenu name="2">
                <template slot="title">
                  <Icon type="ios-people" />
                  用户管理
                </template>
                <MenuItem name="2-1">新增用户</MenuItem>
                <MenuItem name="2-2">活跃用户</MenuItem>
              </Submenu>
              <Submenu name="3">
                <template slot="title">
                  <Icon type="ios-stats" />
                  统计分析
                </template>
                <MenuGroup title="使用">
                  <MenuItem name="3-1">新增和启动</MenuItem>
                  <MenuItem name="3-2">活跃分析</MenuItem>
                  <MenuItem name="3-3">时段分析</MenuItem>
                </MenuGroup>
                <MenuGroup title="留存">
                  <MenuItem name="3-4">用户留存</MenuItem>
                  <MenuItem name="3-5">流失用户</MenuItem>
                </MenuGroup>
              </Submenu>
            </Menu>
          </Sider>
          <Layout :style="{padding: '0 24px 24px'}">
            <Breadcrumb :style="{margin: '24px 0'}">
              <BreadcrumbItem>Home</BreadcrumbItem>
              <BreadcrumbItem>Components</BreadcrumbItem>
              <BreadcrumbItem>Layout</BreadcrumbItem>
            </Breadcrumb>
            <Content :style="{padding: '24px', minHeight: '280px', background: '#fff'}">
              <Row :gutter="16">
                <i-col span="3">
                  <div><a href=""><img src="./assets/logo.png">CRM管理</a></div>
                </i-col>
                <i-col span="3">
                  <div><img src="./assets/logo.png"><a href="">问题咨询库</a></div>
                </i-col>
                <i-col span="3">
                  <div> <img src="./assets/logo.png"><a href="">人事管理</a></div>
                </i-col>
                <i-col span="3">
                  <div><img src="./assets/logo.png"><a href="">热点问题</a></div>
                </i-col>
              </Row>
            </Content>
          </Layout>
        </Layout>
      </Layout>
    </div>
    <router-view/>
  </div>
</template>

<script>
    export default {
    data () {
        return {
            theme2: 'light'
        }
    }
}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>

<style scoped>
  .layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
  }
  .layout-logo{
    width: 100px;
    height: 30px;
    background: #5b6270;
    border-radius: 3px;
    float: left;
    position: relative;
    top: 0px;
    left: 5px;
  }
  .layout-nav{
    width: 420px;
    margin: 0 auto;
    margin-right: 40px;
  }
</style>


