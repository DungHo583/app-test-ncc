<template>
  <div class="home-view">
    <div class="navigation-wrap">
      <navigation />
    </div>
    <div class="homeview-wrap">
      <div class="body-homeview-wrap">
        <div class="header-homeview-wrap">
          <img
            src="@/assets/images/logoNcc.png"
            width="310px"
            height="122px"
            alt=""
          />
        </div>
        <div class="info-homeview-wrap">
          <div class="info-homeview-card">
            <div class="title-info-card text-font-bold">
              Lorem ipsum dolor sit asmet?
            </div>
            <div class="content-info-card text-font-base">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed
              tristique consequat placerat. Vestibulum auctor pellentesque sem,
              eu posuere erat hendrerit quis. Maecenas vel consequat turpis. Nam
              facilisis, ligula in mattis sodales, augue justo tristique nulla,
              sed lacinia ante eros ut mi. Morbi vitae diam augue. Aliquam vel
              mauris a nibh auctor commodo. Praesent et nisi eu justo eleifend
              convallis. Quisque suscipit maximus vestibulum. Phasellus congue
              mollis orci, sit amet luctus augue tristique eu. Donec vulputate
              odio neque, sed semper turpis pellentesque a.
            </div>
          </div>
        </div>
        <div class="feature-homeview-wrap">
          <div class="row-content-custom flex-space-between">
            <div
              class="col-content-custom"
              v-for="items in list"
              :key="items._id"
            >
              <div class="content-col-custom">
                <div class="title-item-custom text-font-bold">
                  {{ items.name }}
                </div>
                <div class="content-item-custom">
                  <img
                    :src="require(`@/assets/images/${items.image}`)"
                    width="128px"
                    height="128px"
                    alt=""
                  />
                  <div class="text-font-base">
                    {{ items.content }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="footer-homeview-wrap">
        <div class="text-copyright text-font-base">Copyright © 2021</div>
      </div>
    </div>
  </div>
</template>

<script>
import navigation from "@/components/navigation.vue";
export default {
  components: {
    navigation,
  },
  data() {
    return {
      list: [
        {
          _id: "001",
          image: "css-image.png",
          name: "Lorem ipsum dolor sit amet",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices liquam egestas nunc at ullamcorper ultricies. Donec feugiat velit nulla, vel sodales est ullamcorper id. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices vestibulum mattis.",
        },
        {
          _id: "002",
          image: "html-image.png",
          name: "Lorem ipsum dolor sit amet",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices liquam egestas nunc at ullamcorper ultricies. Donec feugiat velit nulla, vel sodales est ullamcorper id. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices vestibulum mattis.",
        },
        {
          _id: "003",
          image: "url-image.png",
          name: "Lorem ipsum dolor sit amet",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices liquam egestas nunc at ullamcorper ultricies. Donec feugiat velit nulla, vel sodales est ullamcorper id. Aenean consequat condimentum velit ut tempor. Nam porta massa in metus bibendum congue. Pellentesque ultrices vestibulum mattis.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.home-view {
  display: flex;
  align-items: flex-start;
}
.navigation-wrap {
  width: 150px;
  height: 100%;
}
.homeview-wrap {
  width: calc(100% - 150px);
  height: 100%;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  .body-homeview-wrap {
    .header-homeview-wrap {
      padding: 20px 0;
      img {
        margin: 0 auto;
        max-width: 310px;
        max-height: 122px;
      }
    }
    .info-homeview-wrap {
      padding: 10px 0;
      width: 100%;
      .info-homeview-card {
        width: calc(100% - 258px - 76px);
        max-width: calc(1510px - 76px);
        margin: 0 auto;
        background: #efefef;
        padding: 38px;
        .title-info-card {
          margin-bottom: 18px;
          font-size: 18px;
          line-height: 21px;
        }
        .content-info-card {
          max-width: 972px;
          margin: 0 auto;
          text-align: center;
        }
      }
    }
    .feature-homeview-wrap {
      padding: 30px 0;
      width: 100%;
      .row-content-custom {
        max-width: 1510px;
        width: calc(100% - 258px);
        margin: 0 auto;
        .col-content-custom {
          width: calc(100% / 3 - 50px);
          .content-col-custom {
            max-width: 470px;
            text-align: left;
            .title-item-custom {
              margin-bottom: 18px;
            }
            .content-item-custom {
              width: 100%;
              img {
                float: left;
                margin-right: 16px;
              }
              // .text-font-base {
              //   span {
              //   }
              // }
            }
          }
        }
      }
    }
  }

  .footer-homeview-wrap {
    margin-top: auto;
    padding: 30px 129px;
    border-top: 1px solid #dedede;
    .text-copyright {
      color: #3e3e3e;
      text-align: left;
    }
  }
}
</style>