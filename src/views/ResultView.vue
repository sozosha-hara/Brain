<template>
  <div id="app">
    <div class="confetti"><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
		<span></span><span></span><span></span><span></span><span></span>
	</div>
    <h1>あなたの脳は今...</h1>
    <h1>{{ todaysBrainPower }}%</h1>
    <img class="text__bound" src="../assets/brain3.svg" alt="">
    <FooterComp></FooterComp>
  </div>
</template>
<script>
import FooterComp from '@/components/FooterComp.vue';

export default {
  data() {
    return {
      count: 0
    }
  },
  mounted() {
    const tf = this.$store.state.TodayFood
    let counter = 0
    tf.forEach(element => {
      if(element.isShow == true) {
        counter++
      }
    })
    this.count = Math.floor((counter / tf.length) * 100)
  },
  computed: {
    days() {
      return this.$store.state.clickDay
    },
    dailyFoodList() {
      return this.$store.state.dailyFoodList
    },
    todaysDailyFoodList() {
      return this.dailyFoodList.find((item) => {
        return item.date === this.days
      })
    },
    todaysBrainPower() {
      let counter = 0
      this.todaysDailyFoodList.foodList.forEach(item => {
        if(item.isShow) {
          counter++
        }
      })
      return counter / this.todaysDailyFoodList.foodList.length * 100
    }
  },
  components: {
    FooterComp,
  }
}
</script>
<style scoped>
h1 {
  font-size: 40px;
}
.confetti {
	position: absolute;
  top:0;
  left: 0;
	width: 100%;
	height: 100vh;
  overflow: hidden;
}
.confetti span {
	position: absolute;
	top: -30%;
	left: 0;
	width: 5vw;
	height: 5vw;
	background: #FFF;
}
.confetti span:nth-child(2n+1) {
	animation: confetti-anim-1 10s 0s linear infinite;
}
.confetti span:nth-child(2n+2) {
	animation: confetti-anim-2 10s 0s linear infinite;
}
.confetti span:nth-child(1) {
	left: 0%;
}
.confetti span:nth-child(2) {
	left: 2%;
}
.confetti span:nth-child(3) {
	left: 4%;
}
.confetti span:nth-child(4) {
	left: 6%;
}
.confetti span:nth-child(5) {
	left: 8%;
}
.confetti span:nth-child(6) {
	left: 10%;
}
.confetti span:nth-child(7) {
	left: 12%;
}
.confetti span:nth-child(8) {
	left: 14%;
}
.confetti span:nth-child(9) {
	left: 16%;
}
.confetti span:nth-child(10) {
	left: 18%;
}
.confetti span:nth-child(11) {
	left: 20%;
}
.confetti span:nth-child(12) {
	left: 22%;
}
.confetti span:nth-child(13) {
	left: 24%;
}
.confetti span:nth-child(14) {
	left: 26%;
}
.confetti span:nth-child(15) {
	left: 28%;
}
.confetti span:nth-child(16) {
	left: 30%;
}
.confetti span:nth-child(17) {
	left: 32%;
}

.confetti span:nth-child(18) {
	left: 34%;
}

.confetti span:nth-child(19) {
	left: 36%;
}

.confetti span:nth-child(20) {
	left: 38%;
}

.confetti span:nth-child(21) {
	left: 40%;
}

.confetti span:nth-child(22) {
	left: 42%;
}

.confetti span:nth-child(23) {
	left: 44%;
}

.confetti span:nth-child(24) {
	left: 46%;
}

.confetti span:nth-child(25) {
	left: 48%;
}

.confetti span:nth-child(26) {
	left: 50%;
}

.confetti span:nth-child(27) {
	left: 52%;
}

.confetti span:nth-child(28) {
	left: 54%;
}

.confetti span:nth-child(29) {
	left: 56%;
}

.confetti span:nth-child(30) {
	left: 58%;
}

.confetti span:nth-child(31) {
	left: 60%;
}

.confetti span:nth-child(32) {
	left: 62%;
}

.confetti span:nth-child(33) {
	left: 64%;
}

.confetti span:nth-child(34) {
	left: 66%;
}

.confetti span:nth-child(35) {
	left: 68%;
}

.confetti span:nth-child(36) {
	left: 70%;
}

.confetti span:nth-child(37) {
	left: 72%;
}

.confetti span:nth-child(38) {
	left: 74%;
}

.confetti span:nth-child(39) {
	left: 76%;
}

.confetti span:nth-child(40) {
	left: 78%;
}

.confetti span:nth-child(41) {
	left: 80%;
}

.confetti span:nth-child(42) {
	left: 82%;
}

.confetti span:nth-child(43) {
	left: 84%;
}

.confetti span:nth-child(44) {
	left: 86%;
}

.confetti span:nth-child(45) {
	left: 88%;
}

.confetti span:nth-child(46) {
	left: 90%;
}

.confetti span:nth-child(47) {
	left: 92%;
}

.confetti span:nth-child(48) {
	left: 94%;
}

.confetti span:nth-child(49) {
	left: 96%;
}

.confetti span:nth-child(50) {
	left: 98%;
}

/* colors */
.confetti span:nth-child(5n+1) {
	background: red;
}

.confetti span:nth-child(5n+2) {
	background: blue;
}

.confetti span:nth-child(5n+3) {
	background: green;
}

.confetti span:nth-child(5n+4) {
	background: pink;
}

.confetti span:nth-child(5n+5) {
	background: yellow;
}


/* animation-duration */
.confetti span:nth-child(4n+1) {
	animation-duration: 5s;
}

.confetti span:nth-child(4n+2) {
	animation-duration: 12s;
}

.confetti span:nth-child(4n+3) {
	animation-duration: 8s;
}

.confetti span:nth-child(4n+4) {
	animation-duration: 6s;
}


/* animation-delay */
.confetti span:nth-child(11n+1) {
	animation-delay: 0s;
}

.confetti span:nth-child(11n+2) {
	animation-delay: 9s;
}

.confetti span:nth-child(11n+3) {
	animation-delay: 2s;
}

.confetti span:nth-child(11n+4) {
	animation-delay: 5s;
}

.confetti span:nth-child(11n+5) {
	animation-delay: 6s;
}

.confetti span:nth-child(11n+6) {
	animation-delay: 7s;
}

.confetti span:nth-child(11n+7) {
	animation-delay: 3s;
}

.confetti span:nth-child(11n+8) {
	animation-delay: 1s;
}

.confetti span:nth-child(11n+9) {
	animation-delay: 2s;
}

.confetti span:nth-child(11n+10) {
	animation-delay: 11s;
}

.confetti span:nth-child(11n+11) {
	animation-delay: 10s;
}
@keyframes confetti-anim-1 {
	0% {
		top: -10%;
		transform: translateX(0) rotateX(0) rotateY(0);
	}
	100% {
		top: 100%;
		transform: translateX(20vw) rotateX(180deg) rotateY(360deg);
	}
}
@keyframes confetti-anim-2 {
	0% {
		top: -10%;
		transform: translateX(0) rotateX(0) rotateY(0);
	}
	100% {
		top: 100%;
		transform: translateX(-20vw) rotateX(180deg) rotateY(360deg);
	}
}
</style>