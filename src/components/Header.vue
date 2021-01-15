<template>
    <div id="firstview">
      <header id="top-header">
        <div class="flex">
          <h1 class="header-logo">estra inc.</h1>
          <nav class="header-nav">
            <ul>
              <li><a href="#">home</a></li>
              <li><a href="#">about</a></li>
              <li><a href="#">service</a></li>
              <li><a href="#">works</a></li>
              <li><a href="#">price</a></li>
              <li><a href="#">contact</a></li>
            </ul>
          </nav>
        </div>
      </header>
      <p class="catchcopy">機械ではできない仕事を</p>
      <div class="news flex">
        <div class="news-content">
          <p class="news_date">2019/01/01</p>
          <p class="news_title">
            ニュースタイトルがここには入ります。3月の決算報告書
          </p>
        </div>
        <div class="news-icon">news</div>
      </div>
        <div id="hamburger" @click="hamburger" :class="{'active':isClass}">
          <span></span>
          <span></span>
          <span></span>
        </div>
        <nav class="menu-content" :class="{'open':isClass}">
          <p class="menu-title">estra inc.</p>
          <ul class="menu-content_inner">
            <li>
              <a href="#">home</a>
            </li>
            <li>
              <a href="#">about</a>
            </li>
            <li>
              <a href="#">service</a>
            </li>
            <li>
              <a href="#">works</a>
            </li>
            <li>
              <a href="#">price</a>
            </li>
            <li>
              <a href="#">contact</a>
            </li>
          </ul>
        </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isClass: false
    };
  },
  methods: {
    hamuburger() {
      this.isClass = !this.isClass;
    }
  }
};
</script>

<style scoped>
/*------------------------*/
/*         header         */
/*------------------------*/
#hamburger {
  display: none;
}

#top-header {
  height: 70px;
  line-height: 70px;
  background: rgba(0, 0, 0, 1);
}

.header-logo {
  font-size: 20px;
  font-weight: bold;
  margin-left: 35px;
  color: #fff;
  line-height: 70px;
}

.header-nav li {
  display: inline-block;
  margin-right: 35px;
  font-size: 16px;
}

.header-nav a {
  color: #fff;
}

#firstview {
  height: 100%;
  background: url(./assets/eyecatch.jpg) no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
}

.catchcopy {
  position: absolute;
  top: 60%;
  left: 10%;
  font-size: 60px;
  font-style: italic;
  font-weight: bold;
  color: #fff;
  line-height: 1;
}


</style>