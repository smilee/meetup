<template>
  <div class="speaker">
    <h1 id="speaker">세션</h1>
    <p>
      발표자 모집 중 입니다.
      <a href="https://goo.gl/XkRCuZ" target="_blank" class="enter-button">모집 링크</a>
    </p>
    <!-- <div class="speaker-list">
      <div class="speaker-item">
        <div class="profile-image">
          <img src="~@/assets/second/sunhyoup.png">
        </div>
        <div class="content">
          <div class="title">Vue.js와 Reactive Programming</div><br>
          <div class="profile-name">이선협</div>
        </div>
      </div>
    </div> -->
  </div>
</template>

<script>
  export default {
    name: 'speaker'
  }
</script>

<style lang="scss" scoped>
  @import '~@/assets/media_query';

  .speaker {
    width: 800px;
    margin: 0 auto;
    padding-top: 150px;

    @include mobile-only {
      width: 90%;
    }

    @include tablet-only {
      width: 600px;
    }

    p {
      text-align: center;
    }

    h1 {
      margin-bottom: 50px;
      text-align: center;
      font-weight: 200;

      @include mobile-only {
        font-size: 30px;
      }
    }

    .speaker-list {
      .speaker-item {
        width: calc(100% - 20px);
        min-height: 120px;
        margin: 20px auto;
        border-radius: 10px;
        background-color: white;
        box-shadow: 0 15px 35px rgba(50,50,93,.03), 0 5px 15px rgba(0,0,0,.06);
        cursor: pointer;
        overflow: hidden;

        @include mobile-only {
          width: 100%;
          font-size: 15px;
          text-align: center;
          word-break: keep-all;
          padding: 10px 0;
        }

        &:hover {
          box-shadow: 0 15px 35px rgba(50,50,93,.07), 0 5px 15px rgba(0,0,0,.1);
        }

        .profile-image {
          float: left;
          width: 120px;
          height: 120px;
          overflow: hidden;

          img {
            width: 120px;
            border-right: 1px solid #EEE;
          }

          @include mobile-only {
            float: none;
            display: block;
            margin: 0 auto;
            text-align: center;
            border-radius: 50%;
            box-shadow: 0 15px 35px rgba(50,50,93,.2), 0 5px 15px rgba(0,0,0,.2);

            img {
              border-right: none;
            }
          }
        }

        .content {
          @include mobile-only {
            float: none;
            padding-left: 0;
          }

          float: left;
          padding-left: 10px;
          .title {
            display: inline-block;
            margin-top: 10px;
            vertical-align: top;
            font-weight: bold;
          }

          .profile-name {
            display: inline-block;
            margin-top: 5px;
            vertical-align: top;

            @include mobile-only {
              margin-top: -2px;
            }
          }
        }

        &:after {
          content: '';
          display: block;
          clear: both;
        }
      }
    }
    .enter-button {
      display: block;
      width: 200px;
      height: 40px;
      margin: 20px auto;
      margin-top: 40px;
      text-align: center;
      line-height: 40px;
      font-weight: bold;
      font-size: 15px;
      text-decoration: none;  
      color: white;
      border-radius: 30px;
      background-color: #3AB982;
      border: none;
      transition-duration: 0.4s;

      &:active, &:hover {
        background-color: #319267
      }
    }
  }
</style>
