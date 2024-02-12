<template>
  <div class="home-view">
    <div class="main">
      <div class="plate-1">
        <div class="banner">
          <svg
            class="bigBanner"
            xmlns="http://www.w3.org/2000/svg"
            width="500"
            height="300"
            style="font-style: no"
          >
            <text
              x="50%"
              y="50%"
              dominant-baseline="middle"
              text-anchor="middle"
              font-size="100px"
              fill="#fff"
            >
              🐟
            </text>
          </svg>
        </div>
        <div class="text-center">
          <button
            type="button"
            class="btn createNftBtn"
            data-bs-toggle="modal"
            data-bs-target="#staticBackdrop"
          >
            Create NFTs
          </button>
        </div>
        <div class="content">
          <small>
            我是教學案例，請同學們不要直接用該代碼作為自己項目，至少把樣式全部改一遍再用
          </small>
        </div>
        <p>1.做路由</p>
        <p>2.創建頁面</p>
        <p>3.js邏輯文件創建</p>
        <p>4.合約地址文件創建</p>
        <p>5.頁面變量創建</p>
        <p>6.頁面變量獲得的func創建 - 頁面需要的合約實例創建</p>
      </div>
    </div>

    <CreateNFTsPopup />
  </div>
</template>

<script>
const CreateNFTsPopup = () => import('@/components/Popups/CreateNFTsPopup');
import home from '@/mixins/home.js';
export default {
  mixins: [home],
  data() {
    return {};
  },
  name: 'Home',
  methods: {
    goOtherPage(url) {
      window.open(url);
    },
  },
  components: {
    CreateNFTsPopup,
  },
};
</script>

<style scoped lang="scss">
.createNftBtn {
  max-width: 500px;
  height: 60px;
  width: 90%;
  margin: 0 auto;
  color: #000 !important;
  border: 1px solid #000;
  font-size: 26px;
  // font-weight: bolder;
  &:disabled {
    opacity: 0.4;
  }

  &:hover {
    background-color: $clrYellow;
    border: 1px solid $clrYellow;
    color: #000 !important;
  }
}
</style>
