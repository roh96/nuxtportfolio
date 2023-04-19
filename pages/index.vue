<template>
  <div class="bodybody">
    <Head>
      <link
        rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@40,400,1,0"
      />
      <link rel="preconnect" href="https://fonts.googleapis.com" />
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
      <link
        href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&family=Signika:wght@700&display=swap"
        rel="stylesheet"
      />
    </Head>
    <div class="headerBox">
      <h1>Roh's Portfolio</h1>
      <div>
        <p @click="goAbout()">ABOUT</p>
        <p @click="goSkill()">SKILL</p>
        <p @click="goProject()">PROJECT</p>
      </div>
    </div>
    <div class="visualMain">
      <canvas id="canvas"></canvas>
      <div>
        <p class="visualMaintxt1">밤하늘에 조용히 빛나는 별처럼</p>
        <p class="visualMaintxt2">작은 것들이 모였을 때</p>
        <p class="visualMaintxt3">하나의 작품이 완성됩니다.</p>
      </div>
    </div>
    <div class="about">
      <div>
        <h2 class="moveHide">ABOUT ME</h2>
        <div class="listBox moveHide">
          <ul>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined"> person </span>
                </div>
                <div class="rightBox">
                  <span>이&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;름</span>
                  <p>노준식</p>
                </div>
              </div>
            </li>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined">
                    calendar_month
                  </span>
                </div>
                <div class="rightBox">
                  <span>생년월일</span>
                  <p>&nbsp;96.06.25</p>
                </div>
              </div>
            </li>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined"> location_on </span>
                </div>
                <div class="rightBox">
                  <span>거&nbsp;&nbsp;주&nbsp;&nbsp;지</span>
                  <p>서울특별시 양천구</p>
                </div>
              </div>
            </li>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined"> call </span>
                </div>
                <div class="rightBox">
                  <span>연 &nbsp;락&nbsp; 처</span>
                  <p>010-3927-2915</p>
                </div>
              </div>
            </li>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined"> mail </span>
                </div>
                <div class="rightBox">
                  <span>이&nbsp; 메&nbsp; 일</span>
                  <p>shwnstlr1@gmail.com</p>
                </div>
              </div>
            </li>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined"> school </span>
                </div>
                <div class="rightBox">
                  <span>학&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 력</span>
                  <p>안양대학교 컴퓨터공학과</p>
                </div>
              </div>
            </li>
            <li>
              <div>
                <div class="leftBox">
                  <span class="material-symbols-outlined"> play_circle </span>
                </div>
                <div class="rightBox">
                  <span>취&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 미</span>
                  <p>준비중</p>
                </div>
              </div>
            </li>
          </ul>
        </div>
        <div class="aboutBox moveHide">
          사용자에 초점을 두고 이용에 불편함이 없도록 하는 것에 중점을 두는
          프론트엔드 개발자를 꿈꾸는 노준식 입니다. <br /><br />내가 불편해야
          이용자가 편하다는 것을 잊지 않고 배움의 자세로 임하겠습니다.
          <br />작은 것을 놓치지 않는 자가 큰 것 또한 챙길 수 있다는 생각으로
          작은 것 하나하나 살피는 개발자가 되겠습니다.
        </div>
      </div>
    </div>
    <div class="skill">
      <div>
        <h2 class="moveHide">SKILLS</h2>
        <div class="moveHide">
          <div class="firstBox card_large">
            <div>
              <h3>Frontend</h3>
              <div>
                <img src="@/assets/img/html_cs_js.webp" class="html" />
                <img src="@/assets/img/sass.png" class="sass" />
                <img src="@/assets/img/jquery.png" class="jquery" />
                <img src="@/assets/img/next.png" class="next" />
                <img src="@/assets/img/react.png" class="react" />
              </div>
            </div>
          </div>
          <div class="secondBox card_medium">
            <div>
              <h3>Version Control</h3>
              <div>
                <img src="@/assets/img/git.png" class="git" />
                <img src="@/assets/img/github.png" class="github" />
              </div>
            </div>
          </div>
          <div class="thirdBox card_small">
            <div>
              <h3>Deployment</h3>
              <div>
                <img src="@/assets/img/cloud.png" class="cloud" />
                <img src="@/assets/img/vercel.jpg" class="vercel" />
              </div>
            </div>
          </div>
          <div class="fourthBox card_medium">
            <div>
              <h3>Communication</h3>
              <div>
                <img src="@/assets/img/zeplin.jpg" class="zeplin" />
                <img src="@/assets/img/figma.jpg" class="figma" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="project">
      <div>
        <div class="proH">
          <h2 class="moveHide">PROJECTS</h2>
        </div>
        <div
          class="pro5 proContainer moveHide"
          v-for="item in data.data"
          :key="item.projcet_code"
        >
          <div>
            <h3>{{ item.project_name }}</h3>
            <div class="date">{{ item.project_date }}</div>
            <div class="pro">
              <div class="proLeft">
                <div class="proLeftImg">
                  <img :src="item.project_img" />
                </div>
                <div class="proLeftTxt">
                  <p v-html="item.project_leftTxt"></p>
                </div>
              </div>
              <div class="proRight">
                <div class="proRightT">
                  <div class="proRightHead">
                    {{ item.project_right[0].project_rightHead1 }}
                  </div>
                  <div class="proRightTxt">
                    {{ item.project_right[0].project_rightTxt1 }}
                  </div>
                  <div class="proRightHead">
                    {{ item.project_right[0].project_rightHead2 }}
                  </div>
                  <div class="proRightTxt">
                    <p v-html="item.project_right[0].project_rightTxt2"></p>
                  </div>
                  <div class="proRightHead">
                    {{ item.project_right[0].project_rightHead3 }}
                  </div>
                  <div class="proRightTxt">
                    <p v-html="item.project_right[0].project_rightTxt3"></p>
                  </div>
                </div>
                <div class="proRightBut">
                  <a
                    class="proRightBut1"
                    :href="item.project_url"
                    target="_blank"
                    >Site View</a
                  >
                  <a class="proRightBut2" :href="item.git_url" target="_blank"
                    >Git Hub</a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer">
      <div>© 2023. Roh JoonSik. All rights reserved.</div>
    </div>
  </div>
</template>

<script>
function Constellation(canvas) {
  var _this = this,
    context = canvas.getContext("2d"),
    config = {
      star: {
        color: "rgba(255, 255, 255, .5)",
        width: 3,
      },
      line: {
        color: "#3333CC",
        width: 0.2,
      },
      position: {
        x: 0,
        y: 0,
      },
      width: window.innerWidth,
      height: window.innerHeight,
      length:
        Math.sqrt(
          Math.pow(window.innerWidth, 2) + Math.pow(window.innerHeight, 2)
        ) / 10,
      distance: 120,
      radius: 150,
      stars: [],
    };

  function Star() {
    this.x = Math.random() * canvas.width;
    this.y = Math.random() * canvas.height;
    this.radius = Math.random() * config.star.width;

    this.vx = (0.5 - Math.random()) / 5;
    this.vy = (0.5 - Math.random()) / 5;

    this.create = function () {
      context.beginPath();
      context.arc(this.x, this.y, this.radius, 0, Math.PI * 2, false);
      context.fill();
    };
  }

  this.animate = function () {
    var i;
    for (i = 0; i < config.length; i++) {
      var star = config.stars[i];

      if (star.y < 0 || star.y > canvas.height) {
        star.vy = -star.vy;
      } else if (star.x < 0 || star.x > canvas.width) {
        star.vx = -star.vx;
      }

      star.x += star.vx;
      star.y += star.vy;
    }
  };

  this.line = function () {
    var length = config.length,
      iStar,
      jStar,
      i,
      j;

    for (i = 0; i < length; i++) {
      for (j = 0; j < length; j++) {
        iStar = config.stars[i];
        jStar = config.stars[j];

        if (
          iStar.x - jStar.x < config.distance &&
          iStar.y - jStar.y < config.distance &&
          iStar.x - jStar.x > -config.distance &&
          iStar.y - jStar.y > -config.distance
        ) {
          if (
            iStar.x - config.position.x < config.radius &&
            iStar.y - config.position.y < config.radius &&
            iStar.x - config.position.x > -config.radius &&
            iStar.y - config.position.y > -config.radius
          ) {
            context.beginPath();
            context.moveTo(iStar.x, iStar.y);
            context.lineTo(jStar.x, jStar.y);
            context.stroke();
            context.closePath();
          }
        }
      }
    }
  };

  this.createStars = function () {
    context.clearRect(0, 0, canvas.width, canvas.height);

    for (var i = 0; i < config.length; i++) {
      config.stars.push(new Star());
      config.stars[i].create();
    }

    _this.animate();
    _this.line();
  };

  this.setCanvas = function () {
    canvas.width = config.width;
    canvas.height = config.height;
  };

  this.setContext = function () {
    context.fillStyle = config.star.color;
    context.strokeStyle = config.line.color;
    context.lineWidth = config.line.width;
  };

  this.loop = function (callback) {
    callback();

    window.requestAnimationFrame(function () {
      _this.loop(callback);
    });
  };

  this.bind = function () {
    canvas.addEventListener("mousemove", function (e) {
      config.position.x = e.pageX - canvas.offsetLeft;
      config.position.y = e.pageY - canvas.offsetTop;
    });
  };

  this.init = function () {
    this.setCanvas();
    this.setContext();
    this.loop(this.createStars);
    this.bind();
  };
}

import data from "@/assets/json/data.json";

function contents() {
  const elMove = document.querySelectorAll(".moveHide");
  window.addEventListener("scroll", contents);
  elMove.forEach(function (cont, key) {
    if (
      // $(".moveHide").eq(key).offset().top - window.innerHeight * 0.8 <
      elMove[key].offsetTop - window.innerHeight * 0.8 <
      window.pageYOffset
    ) {
      // console.log(elMove[key].offsetTop);
      cont.classList.add("moveUp");
    }
  });
}

export default {
  data() {
    return {
      data: data,
      scrollTop: 0,
      target: null,
    };
  },
  beforeUnmount: function () {
    window.removeEventListener("scroll", this.handleScroll);
  },
  mounted() {
    // var result = bodybody.replace( /(\n)/g, "<br>");
    var c = new Constellation(document.getElementById("canvas"));
    c.init();

    contents();

    // headColor();

    console.log(window.innerHeight);
    window.addEventListener("scroll", this.handleScroll);
    // console.log(data.data);
    // console.log(data.data[0].project_right[0].project_rightHead1);
  },
  // computed: {
  //   content() {
  //     return (this.data.data[0].project_right[0].project_rightTxt2 =
  //       this.data.data[0].project_right[0].project_rightTxt2.replaceAll(
  //         "\\n",
  //         "<br/>"
  //       ));
  //     // return (this.data.data[0].project_right[0].project_rightTxt2 =
  //     //   this.data.data[0].project_right[0].project_rightTxt2.replaceAll(
  //     //     "\\n",
  //     //     "<br/>"
  //     //   ));
  //   },
  // },
  methods: {
    goAbout() {
      window.scrollTo({
        top: document.querySelector(".about").offsetTop,
        behavior: "smooth",
      });
    },
    goSkill() {
      window.scrollTo({
        top: document.querySelector(".skill").offsetTop,
        behavior: "smooth",
      });
    },
    goProject() {
      window.scrollTo({
        top: document.querySelector(".project").offsetTop,
        behavior: "smooth",
      });
    },
    handleScroll() {
      const scrollColor = document.querySelector(".headerBox");

      // if (window.pageYOffset > 900) {
      if (window.pageYOffset > (window.innerHeight * 3) / 5) {
        scrollColor.classList.add("black");
      } else {
        scrollColor.classList.remove("black");
      }
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/css/index.scss";
</style>
