<template>
  <div>
    <div class="test">{{text}}</div>
    <div id="entry-wrapper">
      <div class="chat-entry">
        <div class="entry-logo">
          <div class="entry-text">在线客服</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from 'jquery'
import jQueryBridget from 'jquery-bridget'
import Draggabilly from 'draggabilly'

export default {
  data () {
    return {
      text: 'absdaaawwww',
    }
  },
  mounted () {
    jQueryBridget( 'draggabilly', Draggabilly, $ );
    var draggie = $('.chat-entry').draggabilly({
      axis: 'y'
    })
  },
  methods: {
  }
}
</script>

<style>
.test {
  color: red;
  font-size: 20px;
}
#entry-wrapper {
  right: 10px;
  bottom: -100px;
  z-index: 900;
  position: fixed;
  width: 100px;
  height: 100px;
  cursor: move;
}
#entry-wrapper .chat-entry {
  bottom: 200px;
  position: relative;
}
#entry-wrapper .entry-logo {
  background: url(^) no-repeat 0 0;
  width: 100px;
  height: 100px;
  margin: 0 auto;
  background-size: 60px;
  background-position: 50%;
  position: relative;
}
#entry-wrapper .entry-logo .entry-text {
  font-weight: 700;
  width: 100%;
  text-align: center;
  position: absolute;
  bottom: 12px;
  font-size: 12px;
  color: #464c5b;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
</style>
