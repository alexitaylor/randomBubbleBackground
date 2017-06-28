<template>
  <div>
    <section>
      <div v-for="n  in 1000" :style="bubbleClass(n)" :class="zDepth()"></div>
    </section>
  </div>
</template>

<script>
import _ from 'lodash';

export default {
  name: 'hello',
  data() {
    return {
      bubbles: {
        left: 23,
        top: 23,
        width: 200,
        height: 200,
      },
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
    zDepth() {
      const z = _.random(1, 5);
      return `z-depth-${z}`;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

/*=====================
 Bubbles Styles
 =====================*/
section {
  position : relative ;
  left : 0px;
  top : 0px;
  width : 595px;
  height : 400px;
  background: #FFFFFE;
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

.z-depth-1 {
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
}

.z-depth-1-half {
  box-shadow: 0 5px 11px 0 rgba(0, 0, 0, 0.18), 0 4px 15px 0 rgba(0, 0, 0, 0.15);
}

.z-depth-2 {
  box-shadow: 0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.z-depth-3 {
  box-shadow: 0 12px 15px 0 rgba(0, 0, 0, 0.24), 0 17px 50px 0 rgba(0, 0, 0, 0.19);
}

.z-depth-4 {
  box-shadow: 0 16px 28px 0 rgba(0, 0, 0, 0.22), 0 25px 55px 0 rgba(0, 0, 0, 0.21);
}

.z-depth-5 {
  box-shadow: 0 27px 24px 0 rgba(0, 0, 0, 0.2), 0 40px 77px 0 rgba(0, 0, 0, 0.22);
}

</style>
