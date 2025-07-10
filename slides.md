---
title: Sharing Session
titleTemplate: '%s - Aditya Nur Juang Rahmanda'
theme: ./
layout: full
author: Aditya Rahmanda
monaco: false
defaults:
  layout: default
  transition: slide-up | slide-down
htmlAttrs:
  dir: ltr
  lang: id
seoMeta:
  ogTitle: Sharing Session - Aditya Nur Juang Rahmanda
  ogDescription: Presentasi tentang Logika oleh Aditya Rahmanda untuk Sharing Session LZY - Kamis, 31 Juli 2025
  ogUrl: https://adityarahmanda.github.io/sharing-session
  twitterCard: summary_large_image
  twitterTitle: Sharing Session - Aditya Nur Juang Rahmanda
  twitterDescription: Presentasi tentang Logika oleh Aditya Rahmanda untuk Sharing Session LZY - Kamis, 31 Juli 2025
  twitterUrl: https://adityarahmanda.github.io/sharing-session
components:
  shuffled: './components/shuffled.vue'
  annotate: './components/annotate.vue'
  marquee: './components/marquee.vue'
  x: './components/x.vue'
class: bg-primary text-white flex flex-col items-center justify-center
annotateId: pembuka
---

# Pembuka

<script setup>
const annotateId = "pembuka";
</script>

<div class="w-full mt-8">
  <marquee direction="left" class="marquee font-bold text-4xl bg-secondary text-neutral-900" :duration=60>
  逻辑思维 | ꦩꦶꦏꦶꦂꦭꦺꦴꦒꦶꦱ꧀ | pensar lógicamente | 논리적 사고 | 論理的思考 | 𑼪𑼶𑼒𑼶𑼂𑼭𑼾𑼴𑼔𑼶𑼱𑽁 | التفكير المنطقي | ᮙᮤᮊᮤᮁ ᮜᮧᮌᮤᮞ᮪ | ᨅ ᨙᨑᨛᨄᨗᨀᨗᨑᨛ ᨒᨚᨁᨗᨔᨛ | 
  </marquee>
</div>

<div class="flex-grow" />

<shuffled class="anim-disabled text-9xl px-10 whitespace-nowrap" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :showAt=0 :sortAt=1 :id=annotateId v-click="1">Berpikir Logis</shuffled>
<shuffled class="text-4xl text-center px-10 whitespace-nowrap" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :id=annotateId>Aditya Nur Juang Rahmanda</shuffled>

<div class="flex-grow" />

<div class="w-full mb-8">
  <marquee direction="right" class="font-bold marquee text-4xl bg-secondary text-neutral-900" :duration=60>
  逻辑思维 | ꦩꦶꦏꦶꦂꦭꦺꦴꦒꦶꦱ꧀ | pensar lógicamente | 논리적 사고 | 論理的思考 | 𑼪𑼶𑼒𑼶𑼂𑼭𑼾𑼴𑼔𑼶𑼱𑽁 | التفكير المنطقي | ᮙᮤᮊᮤᮁ ᮜᮧᮌᮤᮞ᮪ | ᨅ ᨙᨑᨛᨄᨗᨀᨗᨑᨛ ᨒᨚᨁᨗᨔᨛ |
  </marquee>
</div>

<style>
.marquee {
  overflow: visible !important;
}
</style>

---
layout: default
class: bg-primary text-white
annotateId: kilas-balik
---

# Kilas Balik

<script setup>
const annotateId = "kilas-balik";
</script>

---
layout: default
class: bg-primary text-white
annotateId: definisi
---

# Definisi

<script setup>
const annotateId = "definisi";
</script>

<div class="relative flex flex-col justify-center align-center text-center px-10 h-full">
  <annotate 
    style="font-size: 14rem; line-height:1; margin-bottom: -2rem" 
    :mark="{ type: 'bracket', brackets: ['left', 'right'], color: '#bfee1d', strokeWidth: 8 }"
    :markAt=0
    :hideMarkAt=1
    :id=annotateId
  >
    /lo·gi·ka/
  </annotate>
  <div class="text-3xl">
    1. pengetahuan tentang kaidah <span class="slidev-vclick-true-hidden" v-click.hide>berpikir</span>
    <annotate tag="span" class="slidev-vclick-true-hidden" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :markAt=1 :id=annotateId v-after>berpikir</annotate>; 
    2. jalan pikiran yang <span class="slidev-vclick-true-hidden" v-after.hide>masuk akal</span>
    <annotate tag="span" class="slidev-vclick-true-hidden" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :markAt=1 :id=annotateId v-after>masuk akal</annotate>;
  </div>
</div> 

---
layout: default
class: bg-secondary text-primary flex flex-col justify-center
annotateId: definisi-2
---

# Definisi - 2

<script setup>
const annotateId = "definisi-2";
</script>

<shuffled 
  class="inline-grid text-9xl text-red-500"
  :mark="{ type: 'underline', brackets: ['left', 'right'], color: '#000', strokeWidth: 8 }"
  :markAt=0
  :id=annotateId
>
  Masuk Akal != Fakta
</shuffled>

---
layout: default
class: bg-secondary text-primary grid grid-cols-2 gap-4
annotateId: definisi-3
---

# Definisi - 3

<script setup>
const annotateId = "definisi-3";
</script>

<div>
  <img src="/ronikerja.png" class="w-full h-auto rounded-3 mb-2" />
  <span class="font-bold text-3xl">Sosok pekerja LZY sedang giat berkreasi</span>
</div>
<x tweetId="1438695995970256897" :tweetMaxWidth=400 />

---
layout: default
annotateId: kesalahan-berpikir
---

# Kesalahan Berpikir

<script setup>
const annotateId = "kesalahan-berpikir";
</script>

<div class="w-full text-center">
  <p class="text-6xl">Asal Generalisir</p>
  <p class="text-center">Satu orang begitu, semua orang dianggap begitu juga</p>
</div>
<div class="flex gap-8 justify-center mt-6">
  <img src="/jawahama.jpeg" class="w-auto h-300px" v-click />
  <img src="/jawachillguy.png" class="w-auto h-300px" v-click />
</div>

---
layout: default
annotateId: kesalahan-berpikir
---

# Kesalahan Berpikir

<script setup>
const annotateId = "kesalahan-berpikir";
</script>

<div class="w-full text-center">
  <p class="text-6xl">Orang Ahli Itu Pasti Bener</p>
  <p class="text-center">
    <span v-mark.underline.orange>Pintar2</span> mencerna informasi dari ahli.
  </p>
</div>

<img src="/drtirtadepresi.png" class="mx-auto w-auto h-350px" v-click />

---
layout: default
class: bg-primary text-white text-9xl
annotateId: prinsip-kiss
---

# Prinsip Kiss

<script setup>
const annotateId = "prinsip-kiss";
</script>

<div class="relative w-full h-full" >
  <annotate 
    class="absolute h-full" 
    :mark="{ type: 'bracket', brackets: ['left', 'right'], color: '#bfee1d', strokeWidth: 10 }"
    :id="annotateId"
    style="width: 5rem"
  />
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :id="annotateId"
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >K</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :id="annotateId" :sortAt=1 :showAt=1>eep</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :id="annotateId" :sortAt=2 :showAt=2>esederhanaan</shuffled>
  </div>
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :id="annotateId"
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >I</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :id="annotateId" :sortAt=1 :showAt=1>t</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :id="annotateId" :sortAt=2 :showAt=2>tu</shuffled>
  </div>
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :id="annotateId"
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >S</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :id="annotateId" :sortAt=1 :showAt=1>imple</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :id="annotateId" :sortAt=2 :showAt=2>elalu</shuffled>
  </div>
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :id="annotateId"
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >S</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :id="annotateId" :sortAt=1 :showAt=1>tup*d</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :id="annotateId" :sortAt=2 :showAt=2>olusinya</shuffled> 
  </div>
</div>

---
layout: default
class: bg-primary text-white  text-center flex justify-center items-center
annotateId: Penutup
---

# Penutup

<script setup>
const annotateId = "penutup";
</script>

<annotate 
  :mark="{ type: 'highlight', color: '#bfee1d', strokeWidth: 10 }"
  class="text-9xl text-neutral-900 px-10 py-4" 
  :id="annotateId"
  v-motion
  :initial="{ opacity: 0 }"
  :enter="{ opacity: 1 }"
  :leave="{ opacity: 0 }"
>
  Sekian dan <br />Terima Kasih
</annotate>

---