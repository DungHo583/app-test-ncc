<template>
  <div class="navbar-wrap">
    <ul class="navigation-list">
      <li
        class="navigation-item text-font-base"
        v-for="item in list"
        :key="item.key"
      >
        <span :class="item.key == 'home' ? 'navigation-active' : ''">{{
          item.name
        }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          key: "home",
          name: "Home",
        },
        {
          key: "services",
          name: "Services",
        },
        {
          key: "news",
          name: "News",
        },
        {
          key: "blog",
          name: "Blog",
        },
        {
          key: "contact",
          name: "Contact",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.navbar-wrap {
  background: #191718;
  width: 100%;
  height: 100%;
  .navigation-list {
    width: 100%;
    list-style: none;
    padding-inline-start: 0 !important;
    margin-block-start: 0 !important;
    margin-block-end: 0 !important;
    .navigation-item {
      font-weight: 700;
      padding: 14px 0 11px 16px;
      border-bottom: 1px solid #5c5c5c;
      text-align: left;
      transition: all 0.2s linear;
      cursor: pointer;
      span {
        color: #aaaaaa;
      }
      .navigation-active {
        color: #ffffff !important;
      }
    }
    .navigation-item:hover {
      background: #5c5c5c;
      span {
        color: #ffffff;
      }
    }
  }
}
</style>