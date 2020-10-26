<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div>
          <colorPicker style="width: 100px;" v-model="color" @change="handleChangeColor"></colorPicker>
<!--        <el-color-picker style="width: 100%;" v-model="color"></el-color-picker>-->
    </div>
    <div>

      <template>
        <section>
<!--          <el-button :style="{background:color}" type="test" @click="handleShowColor"></el-button>-->
<!--          <div class="color_con" :style="{background:color}" ></div>-->
          <div v-show="colorShow" style="text-align: center">
            <sketch-picker v-model="color" @input="updateValue"></sketch-picker>
          </div>
        </section>
      </template>
    </div>
  </div>
</template>
<script>
import { Sketch } from 'vue-color'
export default {
  name: 'system',
  components: {
    'sketch-picker': Sketch
  },
  data () {
    return {
      color: '#FFFFFF',
      // 颜色选择器
      colorShow: true
      // colors: {
      //   hex: '#194d33',
      //   hsl: { h: 150, s: 0.5, l: 0.2, a: 1 },
      //   hsv: { h: 150, s: 0.66, v: 0.30, a: 1 },
      //   rgba: { r: 25, g: 77, b: 51, a: 1 },
      //   a: 1
      // }
    }
  },
  methods: {
    handleChangeColor (val) {
      console.log('输出颜色值', val) // 颜色 #6c8198
      console.log(this.color)
    },
    // 颜色选择器
    handleShowColor () {
      if (this.colorShow) {
        this.colorShow = false
      } else {
        this.colorShow = true
      }
    },
    updateValue (val) {
      console.log('颜色选择', val) // 输出参数如下图1-1
      this.color = val.hex
      // this.colorShow = false
      console.log(this.color)
    }
  }
}
</script>
