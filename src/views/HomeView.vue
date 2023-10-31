<script setup>
import Header from "@/components/Header.vue"
import Footer from "@/components/Footer.vue"
import Slider from "@/components/Slider.vue"
import Image from "@/components/Image.vue"
import ImgText from "@/components/ImgText.vue"
import Card from "@/components/Card.vue"
import Banner from "@/components/Banner.vue"
import Text from "@/components/Text.vue"
</script>

<template>
  <Header element="nexon" />
  <main>
    <Slider element="nexon" />
    <Image element="nexon section" title="포트폴리오가 실력이다." />
    <ImgText element="nexon section" title="이미지 텍스트 유형" />
    <Card element="nexon section" title="포토폴리오 공부" />
    <Banner element="nexon" title="배너영역" />
    <Text element="nexon section" title="텍스트 유형" />
  </main>
  <Footer element="nexon section" />
</template>