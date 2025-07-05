---
title: Sharing Session
titleTemplate: '%s - Aditya Nur Juang Rahmanda'
theme: ./
layout: cover
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
  x: './components/x.vue'
---

# Logika

<shuffled style="font-size: 24rem; line-height:1; margin-bottom: -3rem;" :slide=1>Logika</shuffled>
<shuffled class="text-4xl" :slide=1>Aditya Nur Juang Rahmanda</shuffled>

---
layout: default
class: bg-primary text-white
---

# Definisi

<div class="relative flex flex-col justify-center align-center text-center px-10 h-full">
  <annotate 
    style="font-size: 14rem; line-height:1; margin-bottom: -2rem" 
    :mark="{ type: 'bracket', brackets: ['left', 'right'], color: '#bfee1d', strokeWidth: 8 }"
    :markAt=0
    :hideMarkAt=1
    :slide=2
  >
    /lo·gi·ka/
  </annotate>
  <div class="text-3xl">
    1. pengetahuan tentang kaidah <span class="slidev-vclick-true-hidden" v-click.hide>berpikir</span>
    <annotate tag="span" class="slidev-vclick-true-hidden" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :markAt=1 :slide=2 v-after>berpikir</annotate>; 
    2. jalan pikiran yang <span class="slidev-vclick-true-hidden" v-after.hide>masuk akal</span>
    <annotate tag="span" class="slidev-vclick-true-hidden" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :markAt=1 :slide=2 v-after>masuk akal</annotate>;
  </div>
</div> 

---
layout: default
class: bg-secondary text-primary flex flex-col justify-center
---

# Masuk Akal != Fakta

<shuffled 
  class="inline-grid text-9xl text-red-500"
  :mark="{ type: 'underline', brackets: ['left', 'right'], color: '#000', strokeWidth: 8 }"
  :markAt=0
  :slide=3
>
  Masuk Akal != Fakta
</shuffled>

---
layout: default
class: bg-secondary text-primary grid grid-cols-2 gap-4
---

# Masuk Akal != Fakta - 2

<div>
  <img src="/ronikerja.png" class="w-full h-auto rounded-3 mb-2" />
  <span class="font-bold text-3xl">Sosok pekerja LZY sedang giat berkreasi</span>
</div>
<x tweetId="1438695995970256897" :tweetMaxWidth=400 />

---
layout: default
---

# Kesesatan Logika

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
---

# Kesesatan Logika

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
---

# Kata-kata

<div class="relative w-full h-full" >
  <annotate 
    class="absolute h-full" 
    :mark="{ type: 'bracket', brackets: ['left', 'right'], color: '#bfee1d', strokeWidth: 10 }"
    :slide="7"
    style="width: 5rem"
  />
  <!-- <img 
    class="absolute right-0 bottom-0"
    src="/adit-outline.png"
    v-motion
    :initial="{ width: 500, x: 25, y: 2000 }"
    :enter="{ y: 700 }"
    :click-2="{ x: 125, y: 800 }"
  /> -->
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :slide=7 
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >K</shuffled>
    <!-- <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :slide=7 :sortAt=0 :showAt=0>???</shuffled> -->
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :slide=7 :sortAt=1 :showAt=1>eep</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :slide=7 :sortAt=2 :showAt=2>esederhanaan</shuffled>
  </div>
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :slide=7 
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >I</shuffled>
    <!-- <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :slide=7 :sortAt=0 :showAt=0>?</shuffled> -->
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :slide=7 :sortAt=1 :showAt=1>t</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :slide=7 :sortAt=2 :showAt=2>tu</shuffled>
  </div>
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :slide=7 
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >S</shuffled>
    <!-- <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :slide=7 :sortAt=0 :showAt=0>?????</shuffled> -->
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :slide=7 :sortAt=1 :showAt=1>imple</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :slide=7 :sortAt=2 :showAt=2>elalu</shuffled>
  </div>
  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :slide=7 
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >S</shuffled>
    <!-- <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :slide=7 :sortAt=0 :showAt=0>?????</shuffled> -->
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="2" :slide=7 :sortAt=1 :showAt=1>tup*d</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :slide=7 :sortAt=2 :showAt=2>olusinya</shuffled> 
  </div>
</div>

---
layout: default
class: bg-primary text-white  text-center flex justify-center items-center
---

# Penutup

<annotate 
  :mark="{ type: 'highlight', color: '#bfee1d', strokeWidth: 10 }"
  class="text-9xl text-neutral-900 px-10 py-4" 
  :slide=8 
  v-motion
  :initial="{ opacity: 0 }"
  :enter="{ opacity: 1 }"
  :leave="{ opacity: 0 }"
>
  Sekian dan <br />Terima Kasih
</annotate>

---