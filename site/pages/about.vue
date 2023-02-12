<template>
  <section class="main">
    <div class="container">
      <div class="widget">
        <div class="widget-header">关于</div>
        <div class="widget-content content">
          <h2>简介</h2>
          <p>这里是Freedom动漫社论坛。</p>

          <p>
            本站基于bbs-go项目开发，基于GPL-3.0协议开源。
            <br />
            欢迎加入开发者团队
            <a href="https://github.com/FreedomACGdev/bbs">项目地址</a>
          </p>

          <h2>项目贡献者</h2>
          <p>
            <a
              href="https://github.com/mlogclub/bbs-go/graphs/contributors"
              target="_blank"
              >Contributors</a
            >
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  head() {
    return {
      title: this.$siteTitle('关于'),
    }
  },
}
</script>

<style lang="scss" scoped></style>
