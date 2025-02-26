<template>
  <button @click="handlePlay">123</button>
</template>

<script setup>
import TTSRecorder from '@/utils/onlineTTS'
import { onMounted, ref } from 'vue'
const title = ref('雷锋')
const content = ref(
  '我相信,人性的光芒无论被时光冲刷多少遍都不会褪却一点光彩。我相信,所以我坚持。我相信,所以我铭记。雷锋,雷锋......那个我脑海中不断呼唤的名字,那是我心中永恒的坚持。时钟在转动,科技在发展,世纪在变更。良知,良知....越来越多的现实岂能民灭良知?我怀念雷锋了。记起雷锋去世的经历,深深镇嵌在每个人心中;那是一个细雨的夏季,雷锋与他的助手乔安山驾车从工地返回驻地。他们的车子开进队里的车场后,雷锋看见车上滅了许多泥水。便不顾长途行车的疲急,立即叫他的助手乔安山发动车子去空地洗车;绕过一段比较窄的过道为了安全起见,雷锋下车为乔安山指挥倒转弯:“向左,向左……倒!倒因为地滑,突然倒到一根晒衣服的竹竿上,而竹竿却不偏不歪正好打到雷锋的太阳穴上,当场昏倒在地,昏死过去.....队员们急忙用担架护送雷锋到附近的医院。各级首长闻讯之后立即赶到医院,同时以最快的速度把医疗专家请到雷锋面前。因为顺骨的损伤,又耽搁了大量时间,雷锋同志因工牺牲了。他生的伟大,死的光荣。在雷锋的追悼会上有上万人为雷锋送行,他是人们心中永远的英雄。雷锋,那个为别人着想毫无怨言的人;雷锋,那个平凡而伟大的人;雷锋,那个心中永远的英雄。在以后的日子里回忆雷锋这个字眼都是想着他伟大的事迹,记得队曾对雷锋说的一句话:“雷锋出差一千里,好事做了一火车。”这就是雷锋。'
)
const isPlaying = ref(false)
const ttsRecorder = ref(null)
onMounted(() => {
  ttsRecorder.value = new TTSRecorder()
  ttsRecorder.value.setParams({
    voiceName: 'xiaoyan',
    tte: 'UTF8',
    text: title.value + ' ' + content.value,
  })
})
const handlePlay = (text) => {
  if (['init', 'endPlay', 'errorTTS'].indexOf(ttsRecorder.value.status) > -1) {
    ttsRecorder.value.start()
  } else {
    ttsRecorder.value.stop()
  }
}
</script>

<style  scoped>
</style>