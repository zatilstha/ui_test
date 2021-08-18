<template>
  <MobileMenu v-if="getMenuStatus"/>

  <div v-else>
    <TopSocial/>
    <Header/>

    <router-view></router-view>

    <Footer/>
  </div>
</template>

<script>
import TopSocial from '@/components/topSocial'
import Header from '@/components/header'
import Footer from '@/components/footer'
import MobileMenu from '@/components/mobileMenu'

import {mapGetters} from 'vuex'
export default {
  name: 'App',
  components: {
    TopSocial, Header, Footer, MobileMenu
  },

  computed: {
    ...mapGetters('siteSettings', {
      getMenuStatus: 'getMenuStatus'
    }),
  },


}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  /*color: #2c3e50;*/
  /*margin-top: 60px;*/
}

body {
  background: #F2EFEE;
}

.primaryColor {
  color: #003A92;
}

.secondaryColor {
  color: #3C3C3C;
}

.whiteColor {
  color: white;
}

.lightColor {
  color: #929292;
}

.bgWhite {
  background: white;
}

.bgMarron {
  background: #8C2531;
}

.bgBeige {
  background: #D7C3AE;
}

.bodyMarginLeft {
  margin-left: 60px;
}

.bodyMarginRight {
  margin-right: 60px;
}

.container-fluid {
  padding-right: 15vh;
  padding-left: 8vh;
}

a {
  color: #3C3C3C;
}

hr {
  border-top: 1px solid #929292;
}

hr.solid {
  border-top: 1px solid #003A92;
  float: left;
  width: 20%;
  margin-top: 9px;
}

hr.white {
  border-top: 1px solid white !important;
}

hr.date {
  border-top: 1px solid #C4C4C4;
  /*float: left;*/
  width: 32px;
  margin-top: 9px;
}

li > hr {
  border-top: 1px solid #c4c4c424;
}

.navbar-brand {
  font-size: 25px;
  font-weight: 600;
}

footer > div .navbar-brand {
  padding: 15px 0;
}

.navbar-brand > span > span {
  float: right;
  padding: 0 5px;
  font-size: 15px;
}

.navbar {
  margin-bottom: 0;
  border-radius: 0;
}

#socialNavbar {
  padding-right: 15px;
}

.combineBtn {
  margin-left: -10px;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

.btn-default:focus, .btn-default.active.focus, .btn-default.active:focus, .btn-default:hover, .btn-default:active.focus, .btn-default:active:focus, .btn-default:active:hover, .open > .dropdown-toggle.btn-default.focus, .open > .dropdown-toggle.btn-default:focus, .open > .dropdown-toggle.btn-default:hover {
  background-color: white;
  border-color: #ccc;
}

.btn.active.focus, .btn.active:focus, .btn.focus, .btn:active.focus, .btn:active:focus, .btn:focus {
  outline: 0;
}

.sidenav {
  padding-top: 20px;
  background-color: #f1f1f1;
  height: 100%;
}

.homeBigText {
  padding: 25px 0 40px;
  display: flex
}

.homeBigText .col-md-3 {
  align-self: flex-end;
  text-align: center;
}

.homeBigText > div > h1 {
  font-size: 60px;
}

.homeBigImg {
  /*margin-top: -250px;*/
  /*height: 500px;*/

  margin-top: -45vh;
  height: 75vh;
}

.borderWhitePadding {
  border: 1px solid white;
  padding: 25px;
}

.borderGrayPadding {
  border: 1px solid #f2efee;
  padding: 25px;
}


.divTopMargin {
  margin-top: 60px;
}

.btnWithBorderButton {
  font-size: 18px;
  font-weight: 700;
  background: transparent;
  border: 0;
  border-bottom: 2px solid #C4C4C4;
}

.cursor {
  cursor: pointer;
}

.borderWhitePadding > img {
  padding-bottom: 15px;
}

.borderWhitePadding > span {
  display: flex;
  float: left;
}

.borderWhitePadding > h2, .borderWhitePadding > h3, .borderWhitePadding > p {
  display: inline-flex;
}

.newsBox {
  height: 400px;
}

.pl-0 {
  padding-left: 0;
}

.pb-5 {
  padding-bottom: 50px;
}

.pr-0 {
  padding-right: 0;
}

.pb-forImg {
  /*padding-bottom: 250px;*/
  padding-bottom: 25%
}

.mt-5 {
  margin-top: 50px;
}

.missionText {
  color: white;
  padding: 25px 0;
}

.benefContainer {
  overflow-x: auto;
  display: flex;
  /*margin-left: -15px;*/
  margin-top: 20px;
}

footer {
  background-color: #3C3C3C;
  color: white;
  padding: 30px 15px;
}

.founderText {
  margin-top: -170px;
  color: white;
}

.nav > li > a:focus, .nav > li > a:hover {
  background-color: transparent;
}

footer > div .nav > li > a {
  padding: 10px 30px 0 0;
}

footer > div .navbar-right > li > a {
  padding: 10px 15px !important;
}

.navbar-toggle .icon-bar {
  background: #3C3C3C;
}

.navbar-collapse.in {
  padding: 20px 35px;
  background: #003A92;
}

.navbar-collapse.in > div > img {
  float: right;
  width: 30px;
  margin-top: -35px;
}

.navbar-collapse.in > ul > li > a {
  color: white;
}

.navbar-collapse.in > ul > li > a {
  color: white;
  padding: 0;
}

.navbar-collapse.in > ul {
  padding-left: 15px;
  padding-top: 25px;
}

.navbar-nav > li > ul {
  padding-left: 5vh;
}

.navbar-nav > li > ul > li > a {
  padding: 0;
  color: white;
}

.imgFullWidth {
  width: 100%;
}

.founderContainer {
  /*background-image: url(founder.jpg);*/
  background-size: cover;
  padding: 350px 50px 100px;
  background-position: center;
  margin: -45vh -30px 0 20px;
  color: white;
}

.latestNews > div > div > h4 {
  font-weight: bold;
  padding: 100px 0 30px 0;
}

.gallery > div > div > h4 {
  font-weight: bold;
  padding: 100px 0 30px 0;
}


.founderContainer > hr {
  border-top: 1px solid #e8e8e838;
  width: 100%;
}

.missionImg {
  margin-left: -15vh
}

.homeBigImgRow {
  margin-right: -15vh
}

.mobFooter, .mobFooterSocial {
  display: none;
}

/*################*/
::-webkit-scrollbar {
  height: 3px;
  width: 4px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #888;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}

/*################*/

@media screen and (max-width: 767px) {
  .container-fluid {
    padding-left: 15px;
    padding-right: 15px;
  }

  .bodyMarginLeft {
    margin-left: 0;
  }

  #socialNavbar > li {
    float: left;
  }

  .homeBigText > div > h1 {
    font-size: 32px;
  }

  .navbar-right {
    float: right !important;
    margin-right: -15px;
  }

  .homeBigText {
    display: block;
  }

  .homeBigText .col-md-3 {
    align-self: flex-end;
    text-align: left;
  }

  .homeBigImg {
    margin-top: -13vh;
    height: 25vh;
  }

  .missionImg > div {
    margin-right: 15px;
  }

  .founderContainer {
    padding: 150px 29px 50px;
    margin: -180px 0 0 0;
  }

  .ptc > li {
    float: left;
  }

  footer > div > ul .navbar-right {
    float: left;

  }

  .latestNews > div > div > h4 {
    padding: 0 0 30px 0;
  }

  .gallery > div > div > h4 {
    padding: 0 0 30px 0;
  }

  .mobFooter {
    display: flex;
  }

  .webFooter {
    display: none;
  }

  footer > div > .mbLeft {
    float: left !important;
  }

  .mobFooter > ul {
    width: 50%;
    margin: 7.5px 0;
  }

  .mobFooter > ul > li {
    text-align: left;
  }

  .mobFooterSocial {
    display: block;
  }

  .mobFooterSocial > ul > li {
    float: left;
  }

  .mobFooterSocial > ul {
    float: right !important;
    margin-right: 0;
    margin-top: -40px;
  }
}

@media screen and (max-width: 540px) {
  .founderContainer {
    padding: 50px 25px 20px;
    margin: -100px 0 0 0;
  }

  .borderGrayPadding {
    padding: 15px;
  }

  .newsBox {
    display: none;
  }

  .homeBigImgRow {
    margin-right: -15px;
  }

  .hideMe {
    display: none;
  }

  .ptc {
    margin: 7.5px 0;
  }

  .gallery > div > div .col-sm-4 {
    width: 75%;
  }
}
</style>
