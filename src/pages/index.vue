<template>
  <div>
    <header>
      <div class="container d-flex">
        <a href="#" class="logo">
          <img src="../assets/icons/logo.svg" alt="logo" />
        </a>
        <ul class="menu d-flex d-lg-none align-items-center  gap-6">
          <li
            :class="{ 'menu-item': true }"
            v-for="item in menuItems"
            :key="item.id"
          >
            <a :href="item.link" class="menu-link">{{ item.displayName }}</a>
          </li>
        </ul>
      </div>
    </header>

    <section class="d-flex flex-row-reverse align-items-center pt-96">
      <div class="wrap-60">
        <img src="../assets/images/hero-lg.svg" alt="hero-lg" />
      </div>
      <div class="introduction">
        <h1 class="h1 mb-4 fc-7">Hi！我是 Noel</h1>
        <p class="fs-5 mb-2 fc-6">
          具有 10 年經驗的 
          <span class="mark">資深 UI 設計師</span> 
          兼
          <span class="mark">前端工程師</span>
        </p>
        <p class="fs-5 mb-3 fc-6">技術雙修並行，熱衷於優化使用者的網頁體驗</p>
        <p class="fs-6 fc-4">
          WEB DEVELOPMENT / BRANDING / UI / UX / APP DESIGN
        </p>
        <ul class="icon d-flex">
          <li class="icon-item" v-for="item in socialItems">
            <a :href="item.link" class="icon-link">
              <img :src="item.src" :alt="item.name" />
            </a>
          </li>
        </ul>
      </div>
    </section>

    <section class="pt-9">
      <SectionTitle class="pb-8" content="作品介紹" />
      <div class="bg bg-home-work-1 mask-dark-4">
        <div
          class="container d-flex justify-content-space-between align-items-center"
        >
          <div class="col-7 align-self-end">
            <img src="../assets/images/homepage-work1.svg" alt="work1" />
          </div>
          <div class="col-5 pl-55 px-200">
            <div class="work fc-white">
              <div class="work-header">
                <h3 class="h3 mb-2">星際旅行訂票平台</h3>
                <p class="fs-6 mb-4">悠遊宇宙的夢想，從這裡開始實現</p>
                <ul class="tags pb-6">
                  <li>
                    <a href="#" class="tag tag-white fs-6">網頁設計</a>
                  </li>
                  <li>
                    <a href="#" class="tag tag-white fs-6">響應式設計</a>
                  </li>
                  <li>
                    <a href="#" class="tag tag-white fs-6">Bootstrap</a>
                  </li>
                </ul>
              </div>
              <div class="work-footer">
                <a href="#" class="btn btn-dark btn-lg mt-6">
                  <span class="mr-2">完整介紹</span>
                  <span class="material-symbols-outlined">arrow_forward</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bg bg-home-work-2 mask-dark-4h">
        <div class="container">
          <div class="col-5 px-200">
            <div class="work fc-white">
              <div class="work-header">
                <h3 class="h3 mb-2">理財APP</h3>
                <p class="fs-6 mb-4">
                  連動帳戶與行動支付，讓 AI 提供您最好的理財建議
                </p>
                <ul class="tags pb-6">
                  <li>
                    <a href="#" class="tag tag-white fs-6">APP設計</a>
                  </li>
                  <li>
                    <a href="#" class="tag tag-white fs-6">iOS</a>
                  </li>
                  <li>
                    <a href="#" class="tag tag-white fs-6">React</a>
                  </li>
                </ul>
              </div>
              <div class="work-footer">
                <a href="#" class="btn btn-dark btn-lg mt-6">
                  <span class="mr-2">完整介紹</span>
                  <span class="material-symbols-outlined">arrow_forward</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bg bg-home-work-3 mask-dark-4">
        <div
          class="container d-flex justify-content-space-between align-items-center"
        >
          <div class="col-7">
            <img src="../assets/images/homepage-work3.svg" alt="work3" />
          </div>
          <div class="col-5 pl-55 px-200">
            <div class="work fc-white">
              <div class="work-header">
                <h3 class="h3 mb-2">醫美診所官網</h3>
                <p class="fs-6 mb-4">永保青春的秘密，從粹究開始</p>
                <ul class="tags pb-6">
                  <li>
                    <a href="#" class="tag tag-white fs-6">網頁設計</a>
                  </li>
                  <li>
                    <a href="#" class="tag tag-white fs-6">響應式設計</a>
                  </li>
                  <li>
                    <a href="#" class="tag tag-white fs-6">ＷordPress</a>
                  </li>
                </ul>
              </div>
              <div class="work-footer">
                <a href="#" class="btn btn-dark btn-lg mt-6">
                  <span class="mr-2">完整介紹</span>
                  <span class="material-symbols-outlined">arrow_forward</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="px-9">
      <SectionTitle class="pb-8" content="服務項目" />
      <div class="container">
        <div class="row mb-8 d-flex justify-content-space-between gap-4">
          <ServiceCard :services="services"/>
        </div>
        <div class="row text-center">
          <h4 class="h3 mb-6">想要合作或瞭解更多？</h4>
          <a href="#" class="btn btn-dark btn-lg">
            <span class="mr-2">詳細內容與合作流程</span>
            <span class="material-symbols-outlined">arrow_forward</span>
          </a>
        </div>
      </div>
    </section>

    <section class="px-9">
      <SectionTitle class="pb-8" content="精選文章" />
      <div class="container">
        <div class="row ">
          <ul class="articles d-flex justify-content-space-between gap-4 mb-6">
            <li class="col-4" v-for="(article, id) in articles" :key="id">
              <a href="#" class="article_header">
                <img :src="article.imgSrc" :alt="article.title" class="mb-3">
                <h4 class="h5b mb-3">{{ article.title }}</h4>
              </a>
              <div class="article_footer d-flex justify-content-space-between">
                <ul class="tags" v-for="tag in article.tags" :key="tag">
                  <li>
                    <a href="#" class="tag tag-gray fs-6">{{ tag }}</a>
                  </li>

                </ul>
                <span class="fs-6 fc-6">{{ article.date }}</span>
              </div>
            </li>
          </ul>
          <ul class="article-dots d-flex justify-content-center gap-3">
            <li v-for="(_, id) in articles" :key="id">
              <a href="#" class="dot"></a>
            </li>
          </ul>
        </div>
        
      </div>
    </section>

    <footer class="px-8 bg bg-footer-lg">
      <div class="container">
        <div class="row d-flex justify-content-space-between">
          <div class="col-4">
            <img src="../assets/icons/logo.svg" alt="logo" class="logo mb-4">
            <p class="fs-5">若有數位產品設計和開發相關問題</p>
            <p class="fs-5 mb-4">歡迎填寫表單，或直接與我聯絡！</p>
            <a href="mailto:service@hexschool.com" class="h5 fc-5">service@hexschool.com</a>
          </div>
          <div class="col-4">
            <div class="btn-group">
              <a href="#" class="btn btn-dark">
                <img src="../assets/icons/list.svg" alt="list" class="icon">
                <span class="text">填寫表單</span>
              </a>
              <a href="#" class="btn ">
                <img src="../assets/icons/instagram.svg" alt="instagram" class="icon">
                <span class="text">hexschool_demo</span>
              </a>
              <a href="#" class="btn ">
                <img src="../assets/icons/facebook.svg" alt="facebook" class="icon">
                <span class="text">hexschoolTW</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
  import InstagramIcon from '../assets/icons/instagram.svg';
  import FacebookIcon from '../assets/icons/facebook.svg';
  import YoutubeIcon from '../assets/icons/youtube.svg';
  import ServiceVisualIcon from '../assets/icons/service-item-visual.svg';
  import ServiceUIIcon from '../assets/icons/service-item-ui.svg';
  import ServiceHTMLCSSIcon from '../assets/icons/service-item-html&css.svg';
  import ServiceFrontEndIcon from '../assets/icons/service-item-front-end.svg';
  import Article1Image from '../assets/images/article-image1.svg';
  import Article2Image from '../assets/images/article-image2.svg';
  import Article3Image from '../assets/images/article-image3.svg';

  import SectionTitle from '../components/SectionTitle.vue';
  import ServiceCard from '../components/ServiceCard.vue';

  export default {
    name: 'Index',
    components: {
      SectionTitle,
      ServiceCard,
    },
    data() {
      return {
        menuItems: [
          {
            id: 1,
            displayName: '首頁',
            link: '#',
          },
          {
            id: 2,
            displayName: '作品集',
            link: '#',
          },
          {
            id: 3,
            displayName: '服務項目',
            link: '#',
          },
          {
            id: 4,
            displayName: '部落格',
            link: '#',
          },
          {
            id: 5,
            displayName: '聯絡我',
            link: '#',
          },
        ],
        socialItems: [
          {
            id: 1,
            src: InstagramIcon,
            name: 'instagram',
            link: '#',
          },
          {
            id: 2,
            src: FacebookIcon,
            name: 'facebook',
            link: '#',
          },
          {
            id: 3,
            src: YoutubeIcon,
            name: 'youtube',
            link: '#',
          },
        ],
        works: [
          {
            title: '星際旅行訂票平台',
            description: '悠遊宇宙的夢想，從這裡開始實現',
            tags: ['網頁設計', '響應式設計', 'Bootstrap'],
          },
        ],
        services: [
          {
            src: ServiceVisualIcon,
            title: '平面設計',
          },
          {
            src: ServiceUIIcon,
            title: 'UI 設計',
          },
          {
            src: ServiceHTMLCSSIcon,
            title: '切版服務',
          },
          {
            src: ServiceFrontEndIcon,
            title: '前端開發',
          },
        ],
        articles: [
          {
            imgSrc: Article1Image,
            title: 'Vision Pro 登場！Vision Pro UI/UX 設計重點大公開 (上)',
            date: '2024/02/10',
            tags: ['UI/UX 新知'],
          },
          {
            imgSrc: Article2Image,
            title: '給設計師和工程師的 Figma-Dev Mode 開發模式使用指南 (下)',
            date: '2023/11/20',
            tags: ['UI/UX 新知'],
          },
          {
            imgSrc: Article3Image,
            title: '給設計師和工程師的 Figma-Dev Mode 開發模式使用指南 (上)',
            date: '2023/10/18',
            tags: ['UI/UX 新知'],
          },
        ],
      };
    },
  };
</script>

<style scoped lang="scss">
  .pl-55 {
    padding-left: 55px;
  }

  .pt-96 {
    padding-top: 96px;
  }

  .px-200 {
    padding-top: 200px;
    padding-bottom: 200px;
  }

  .wrap-40 {
    width: 40%;
  }

  .wrap-60 {
    width: 60%;
  }

  header {
    padding-top: 28px;
    padding-bottom: 28px;
    background: #fff;
    border-bottom: 1px solid #f1f1f1;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 2;
  }

  .logo {
    margin-right: 25%;
  }

  .menu {

    &-link {
      padding: 4px 8px;
      line-height: 24px;

      &:hover,
      &:active {
        font-weight: 600;

        &::before,
        &::after {
          display: inline-block;
        }
      }

      &:active {
        transform: scale(0.9);
      }

      &::before,
      &::after {
        content: '';
        display: none;
        width: 8px;
        height: 8px;
        border-top: 1px solid #000;
        position: absolute;
        top: 0;
        -webkit-box-reflect: below 16px;
      }

      &::before {
        border-left: 1px solid #000;
        left: 0;
      }

      &::after {
        border-right: 1px solid #000;
        right: 0;
      }
    }
  }

  .introduction {
    width: 430px;
    margin-right: 24px;
    margin-left: 12px;

    .mark {
      &::before {
        content: '';
        height: 100%;
        width: 112.12%;
        position: absolute;
        left: -6.06%;
        background-image: url('../assets/icons/mark.svg');
        background-repeat: no-repeat;
        background-position: 0 bottom;
        z-index: -1;
      }
    }

    .icon {
      margin-top: 60px;
      gap: 16px;

      &-item {
        &:hover {
          transform: scale(1.1);
        }
        &:active {
          transform: scale(1);
        }
      }
    }
  }

  .work {
    padding: 80px 40px 56px 40px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 24px;

    &-header {
      border-bottom: 1px solid rgba(241, 241, 241, 1);
    }

    &-footer {
      text-align: center;
    }
  }

  .tags {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;

    .tag {
      padding: 4px 12px;
      border-radius: 16px;

      &-white {
        background: #fff;
        color: #3b3b3b;

        &:hover {
          color: #fff;
          background: #000;
        }
      }

      &-gray {
        color: #3b3b3b;
        background: #f1f1f1;
      }
    }
  }

  .btn {
    border-radius: 5px;

    &-lg {
      padding: 16px;
      font-weight: 700;
      font-size: 20px;
      line-height: 30px;
    }

    &-dark {
      color: #fff;
      background: #000;
      border: 1px solid #000;

      &:hover {
        color: #3b3b3b;
        background: #fff;
        border-color: #c1c1c1;
      }
    }
  }

  .dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: #e9e9e9;
  }

  footer {
    .logo {
      width: 120px;
    }

    .btn {
      max-width: 306px;
      margin-left: auto;
      padding: 8px 24px;
      border-radius: 8px;
      line-height: 72px;
      display: flex;
      font-size: 20px;
      color: #3b3b3b;
      background: #fff;
      border: 1px solid #c1c1c1;

      &:hover {
        transform: scale(0.95);
      }

      &:active {
        transform: scale(1.0);
      }

      &:not(:last-child) {
        margin-bottom: 24px;
      }
      
      &-dark {
        font-weight: 700;
        color: #fff;
        background: #000;
        border-color:#000;

        &:hover {
          color: #fff;
          background: #000;
          background-color: #000;
        }
      }

      .icon {
        margin-right: 8px;
      }
    }
  }

</style>
