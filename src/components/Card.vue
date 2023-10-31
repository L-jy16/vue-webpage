<template>
  <section id="cardType" :class="['card__wrap', element]">
    <h2 class="card__h2">{{ title }}</h2>
    <p class="card__p">
      웹디자이너, 웹 퍼블리셔, 프론트앤드 개발자를 목표로 공부하는 사이트입니다<br />
      NEXON Lv1 Gothic Light 22px 150% #6778A
    </p>
    <div class="card__inner container">
      <article class="card" v-for="(card, key) in cardInfo" :key="key">
        <figure class="card__header">
          <img class="img" :src="'/src/assets/img/' + card.img" :alt="card.title" />
        </figure>
        <div class="card__body">
          <h3 class="title">{{ card.title }}</h3>
          <p class="desc">{{ card.desc }}</p>
          <a href="/" class="btn">
            더자세히보기
            <span aria-hidden="true">
              <svg width="52" height="8" viewBox="0 0 52 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                  d="M51.3536 4.35355C51.5488 4.15829 51.5488 3.84171 51.3536 3.64645L48.1716 0.464466C47.9763 0.269204 47.6597 0.269204 47.4645 0.464466C47.2692 0.659728 47.2692 0.976311 47.4645 1.17157L50.2929 4L47.4645 6.82843C47.2692 7.02369 47.2692 7.34027 47.4645 7.53553C47.6597 7.7308 47.9763 7.7308 48.1716 7.53553L51.3536 4.35355ZM0 4.5H51V3.5H0V4.5Z"
                  fill="#5B5B5B" />
              </svg>
            </span>
          </a>
        </div>
      </article>

    </div>
  </section>
</template>

<script>
export default {
  props: {
    element: String,
    title: String
  },

  data: function () {
    return {
      cardInfo: [
        {
          img: "img05.jpg",
          title: "웹표준 사이트 만들기",
          desc: "사이트를 만들기 위한 기초 공부입니다. 기본 코딩에 대한 감각을 익히고, 웹 표준을 준수하면서 코딩하는 방법을 익힙니다. 다양한 예제를 통해서 사이트 만드는 기본을 익히도록 합니다."
        },
        {
          img: "img06.jpg",
          title: "반응형 사이트 만들기",
          desc: "웹표준 사이트를 완성하고, 반응형을 익히는 사이트입니다. 기본 코딩을 익히고, 반응형 감각을 키우면 모바일 및 반응형 사이트도 만들 수 있습니다."
        },
        {
          img: "img07.jpg",
          title: "페랠렉스 사이트 만들기",
          desc: "기업 사이트 중 50% 이상이 패랙렉스 스크로링 효과로 만들어져 있습니다. 웹 표준, 반응형 사이트를 완성하였다면, 이제는 인터랙티브한 패랠렉스 스크롤링 사이트를 완성할 수 있습니다."
        }
      ]
    }
  },


}
</script>

<style>
/* cardType */
.card__h2 {
  font-size: 50px;
  font-weight: 500;
  margin-bottom: 20px;
  line-height: 1;
  text-align: center;
}

.card__p {
  font-size: 22px;
  font-weight: 300;
  margin-bottom: 70px;
  line-height: 1.5;
  color: #777;
  text-align: center;
}

.card__inner {
  display: flex;
  justify-content: space-between;
}

.card {
  width: 32%;
  background: #f5f5f5;
}

.card__body {
  padding: 24px;
}

.card__body .title {
  font-size: 24px;
  margin-bottom: 10px;
}

.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}

.card__body .btn {
  font-size: 16px;
  color: #222;
}
</style>