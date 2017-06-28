<template>
  <div>
    <section>
      <div v-for="n  in 1500" :style="bubbleClass(n)"></div>
    </section>
  </div>
</template>

<script>
import _ from 'lodash';

export default {
  name: 'hello',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      bubbles: {
        left: 23,
        top: 23,
        width: 200,
        height: 200,
      },
      bubbleArrayClass: [],
    };
  },
  methods: {
    bubbleClass() {
      const left = _.random(0, 100);
      const top = _.random(0, 100);
      const widthHeight = _.random(5, 40);
      const animationDuration = _.random(0.8, 3.1);

      const bubble = {
        left: `${left}vw`,
        top: `${top}vh`,
        width: `${widthHeight}px`,
        height: `${widthHeight}px`,
        animationDuration: `${animationDuration}s`,
      };
      return bubble;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

/*=====================
 Bubbles Styles
 =====================*/
section {
  position : relative ;
  left : 0px;
  top : 0px;
  width : 595px;
  height : 400px;
  background: #fff;
}

@-webkit-keyframes scale-up {
  0% {
    -webkit-transform: scale(0.7);
    opacity: 0.6;
  }

  50% {
    -webkit-transform: scale(1.0);
    opacity: 1;
  }


  100% {
    -webkit-transform: scale(0.7);
    opacity: 0.6;
  }
}

@-moz-keyframes scale-up {
  0% {
    -moz-transform: scale(0.7);
    opacity: 0.6;
  }

  50% {
    -moz-transform: scale(1.0);
    opacity: 1;
  }


  100% {
    -moz-transform: scale(0.7);
    opacity: 0.6;
  }
}

@-moz-keyframes scale-up {
  0% {
    -moz-transform: scale(0.7);
    opacity: 0.6;
  }

  50% {
    -moz-transform: scale(1.0);
    opacity: 1;
  }


  100% {
    -moz-transform: scale(0.7);
    opacity: 0.6;
  }
}

@-ms-keyframes scale-up {
  0% {
    -ms-transform: scale(0.7);
    opacity: 0.6;
  }

  50% {
    -ms-transform: scale(1.0);
    opacity: 1;
  }


  100% {
    -ms-transform: scale(0.7);
    opacity: 0.6;
  }
}

@keyframes scale-up {
  0% {
    transform: scale(0.7);
    opacity: 0.6;
  }

  50% {
    transform: scale(1.0);
    opacity: 1;
  }


  100% {
    transform: scale(0.7);
    opacity: 0.6;
  }
}

div {
  background : #42b983;
  position: absolute;
  -webkit-animation: scale-up infinite ease-in-out;
  -moz-animation: scale-up infinite ease-in-out;
  -ms-animation: scale-up infinite ease-in-out;
  animation: scale-up infinite ease-in-out;
  border-radius: 50%;
}

</style>
