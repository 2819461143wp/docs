<template>
  <div>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>随机壁纸</title>
    <button @click="ChangeBG()">切换背景</button>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'

const ChangeBG = () => {
            const urlList = [
                'https://b0.bdstatic.com/daaa0535d569ce15f5301068353cc9e1.jpg@h_1280',
                'https://b0.bdstatic.com/19fa4ab39078d78891031f43b5d13036.jpg@h_1280',
                'https://b0.bdstatic.com/e1b147b8e75495df728a3f4f69c0f2ff.jpg@h_1280',
                'https://b0.bdstatic.com/6d0437c07d8a5e1ccd60f22ba452c281.jpg@h_1280',
                'https://pic2.zhimg.com/v2-bef6f460b30747888fc62b6d28907305_r.jpg'];
            const num = Math.floor(Math.random() * urlList.length);
            document.body.style.backgroundImage = `url(${urlList[num]})`;
        }
</script>

<style scoped>

</style>
script