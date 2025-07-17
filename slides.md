---
title: Sharing Session
titleTemplate: '%s - Aditya Nur Juang Rahmanda'
theme: ./
layout: full
author: Aditya Rahmanda
monaco: false
mermaid: false
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
  inġeþanc rihtlīċ | 逻辑思维 | ꦩꦶꦏꦶꦂꦭꦺꦴꦒꦶꦱ꧀ | pensar lógicamente | 논리적 사고 | <ruby>論<rt>ろん</rt></ruby><ruby>理<rt>り</rt></ruby><ruby>的<rt>てき</rt></ruby><ruby>思<rt>し</rt></ruby><ruby>考<rt>こう</rt></ruby> | 𑼪𑼶𑼒𑼶𑼂𑼭𑼾𑼴𑼔𑼶𑼱𑽁 | التفكير المنطقي | ᮙᮤᮊᮤᮁ ᮜᮧᮌᮤᮞ᮪ | ᨅ ᨙᨑᨛᨄᨗᨀᨗᨑᨛ ᨒᨚᨁᨗᨔᨛ | 
  </marquee>
</div>

<div class="flex-grow" />

<shuffled class="anim-disabled text-9xl px-10 whitespace-nowrap" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :showAt=0 :sortAt=1 :id=annotateId v-click="1">Berpikir Logis</shuffled>
<shuffled class="text-4xl text-center px-10 whitespace-nowrap" :mark="{ type: 'highlight', color: '#000', strokeWidth: 8 }" :id=annotateId>Aditya Nur Juang Rahmanda</shuffled>

<div class="flex-grow" />

<div class="w-full mb-8">
  <marquee direction="right" class="font-bold marquee text-4xl bg-secondary text-neutral-900" :duration=60>
  inġeþanc rihtlīċ | 逻辑思维 | ꦩꦶꦏꦶꦂꦭꦺꦴꦒꦶꦱ꧀ | pensar lógicamente | 논리적 사고 | <ruby>論<rt>ろん</rt></ruby><ruby>理<rt>り</rt></ruby><ruby>的<rt>てき</rt></ruby><ruby>思<rt>し</rt></ruby><ruby>考<rt>こう</rt></ruby> | 𑼪𑼶𑼒𑼶𑼂𑼭𑼾𑼴𑼔𑼶𑼱𑽁 | التفكير المنطقي | ᮙᮤᮊᮤᮁ ᮜᮧᮌᮤᮞ᮪ | ᨅ ᨙᨑᨛᨄᨗᨀᨗᨑᨛ ᨒᨚᨁᨗᨔᨛ |
  </marquee>
</div>

<style>
.marquee {
  overflow: visible !important;
}
</style>

---
layout: default
class: bg-primary text-white flex flex-col justify-center
annotateId: kilas-balik
---

# Kilas Balik

<script setup>
const annotateId = "kilas-balik";
</script>

<div class="text-center text-6xl mb-4">Waktu Kecil, Kalian Pernah Nggak Sih...</div>

<div class="relative mx-auto w-auto h-400px">
  <img src="/kebongelap.jpg" class="h-full" v-click="1" />
  <img src="/blekcat.gif" 
    class="absolute h-100px" 
    style="left: 50px; top: 100px" 
    v-click="2"
  />
  <img src="/blekcat.gif" 
    class="absolute h-100px" 
    style="left: 280px; top: 150px" 
    v-click="2"
  />
  <img src="/blekcat.gif" 
    class="absolute h-100px" 
    style="right: 50px; bottom: 100px" 
    v-click="2"
  />
  <img src="/bananananacat.gif" 
    class="cat anim-disabled absolute left-0 bottom-0 w-150px h-150px" 
      :data-clicks="$slidev.nav.clicks"
      v-click="3"
  />
  <img src="/bananacat.gif" 
    class="cat-cry anim-disabled absolute left-0 bottom-0 w-100px h-100px" 
      :data-clicks="$slidev.nav.clicks"
      v-click="3"
  />
</div>

<style scoped>
.cat {
  transform: translate(-20px, 14px) scaleX(-1);
  filter: opacity(0%);
}

.cat[data-clicks="0"], .cat[data-clicks="1"] {
  filter: opacity(100%);
}

.cat-cry {
  transform: translate(0, 0px);
  filter: opacity(0%);
  transition: all .5 linear;
}

.cat-cry[data-clicks="2"] {
  filter: opacity(100%);
  animation: cat-1 .3s .5s linear;
}

.cat-cry[data-clicks="3"] {
  animation: cat-2 1s linear;
  filter: opacity(0%);
}

@keyframes cat-1 {
  0% {
    transform: translate(0, 0px);
  }
  30% {
    transform: translate(0, -10px);
  }
  100% {
    transform: translate(0, 0px);
  }
}

@keyframes cat-2 {
  0% {
    transform: translateX(0);
    filter: opacity(100%);
  }
  80% {
    filter: opacity(100%);
  }
  100% {
    filter: opacity(0%);
    transform: translateX(520px);
  }
}
</style>

---
layout: default
class: bg-primary text-white
annotateId: memahami
---

# Memahami

<script setup>
const annotateId = "memahami";
</script>

<div class="text-center text-6xl mb-4">Namun Berbekal dengan Pemikiran Logis</div>

<div class="relative w-full h-400px">
  <img src="/adittaktakutlagidengankebongelap.png" class="absolute h-full top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2" v-click.hide="1" />
  <img src="/evolusi.png" class="absolute h-full top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2" v-click="[1, 2]" />
  <img src="/evolusiadit.png" class="absolute h-full top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2" v-click="[2, 3]" />
  <img src="/ummi.jpeg" class="absolute h-full top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2" v-click="3" />
</div> 

---
layout: default
class: bg-secondary h-full text-primary flex flex-col justify-center
annotateId: bagaimana
---

# Bagaimana

<script setup>
const annotateId = "bagaimana";
</script>

<shuffled 
  class="inline-grid mx-auto text-9xl text-red-500 whitespace-nowrap"
  :id=annotateId
>
  Berpikir Logis Itu
</shuffled>
<shuffled 
  class="inline-grid mx-auto text-9xl text-red-500 whitespace-nowrap"
  :markAt=0
  :id=annotateId
>
  Bagaimana?
</shuffled>

---
layout: default
class: bg-secondary text-neutral-900
annotateId: definisi
---

# Definisi

<script setup>
const annotateId = "definisi";
</script>

<div class="relative flex flex-col justify-center align-center text-center px-10 h-full">
  <annotate 
    style="font-size: 14rem; line-height:1; margin-bottom: -2rem" 
    :mark="{ type: 'bracket', brackets: ['left', 'right'], color: '#ef4444', strokeWidth: 8 }"
    :markAt=0
    :hideMarkAt=1
    :id=annotateId
  >
    /lo·gi·ka/
  </annotate>
  <div class="text-3xl">
    1. pengetahuan tentang <span class="slidev-vclick-true-hidden" v-click.hide>kaidah berpikir</span>
    <annotate tag="span" class="slidev-vclick-true-hidden" :mark="{ type: 'highlight', color: '#9ed0ff', strokeWidth: 8 }" :markAt=1 :id=annotateId v-after>kaidah berpikir</annotate>; 
    2. jalan pikiran yang <span class="slidev-vclick-true-hidden" v-after.hide>masuk akal</span>
    <annotate tag="span" class="slidev-vclick-true-hidden" :mark="{ type: 'highlight', color: '#9ed0ff', strokeWidth: 8 }" :markAt=1 :id=annotateId v-after>masuk akal</annotate>;
  </div>
</div>

---
layout: default
class: bg-secondary text-neutral-900 flex flex-col justify-center align-center
annotateId: sistematis
---

# Sistematis

<script setup>
const annotateId = "sistematis";
</script>

<div class="relative flex justify-center mb-8">
  <annotate class="grid-inline whitespace-nowrap text-6xl" :mark="{ type: 'highlight', color: '#9ed0ff', strokeWidth: 8 }" :id=annotateId >Berpikir Secara Sistematis</annotate>
  
  <img src="/nerd.gif" class="absolute top-1/2 transform -translate-y-1/2 left-0 w-120px" />

  <img src="/nerd.gif" class="absolute top-1/2 transform -translate-y-1/2 right-0 w-120px" />
</div>

<div class="relative w-full mb-8">
  <div class="text-3xl text-center mb-2">Runtutan Ngopi (Alternatif 1)</div>
  <img src="/kopi-1.svg" />
</div>

<div class="relative w-full">
  <div class="text-3xl text-center mb-2">Runtutan Ngopi (Alternatif 2)</div>
  <img src="/kopi-2.svg" />
</div>

---
layout: default
class: bg-secondary text-neutral-900 flex flex-col justify-center align-center
annotateId: masuk-akal
---

# Masuk Akal

<script setup>
const annotateId = "masuk-akal";
</script>

<div class="relative flex justify-center mb-8">
  <annotate class="grid-inline whitespace-nowrap text-6xl" :mark="{ type: 'highlight', color: '#9ed0ff', strokeWidth: 8 }" :id=annotateId >Berpikir Yang Masuk Akal</annotate>
  
  <img src="/thinkthinkbukanpermen.gif" class="absolute top-1/2 transform -translate-y-1/2 left-0 w-120px" />

  <img src="/thinkthinkbukanpermen.gif" class="absolute top-1/2 transform -translate-y-1/2 right-0 w-120px" />
</div>

<div class="relative w-full mb-8">
  <div class="text-3xl text-center mb-2">Ngopi Nggak Masuk Akal</div>
  <img src="/kopi-error-1.svg" />
</div>

<div class="relative w-full">
  <div class="text-3xl text-center mb-2">Ngopi Nggak Masuk Akal Banget</div>
  <img src="/kopi-error-2.svg" />
</div>

---
layout: default
class: bg-secondary text-neutral-900 text-9xl
annotateId: prinsip-kiss
---

# Prinsip Kiss

<script setup>
const annotateId = "prinsip-kiss";
</script>

<div class="relative w-full h-full" >
  <annotate 
    class="absolute h-full" 
    :mark="{ type: 'bracket', brackets: ['left', 'right'], color: '#ef4444', strokeWidth: 10 }"
    :id="annotateId"
    style="width: 5rem"
  />
  
  <img src="/catcium.gif" class="absolute h-400px top-1/2 left-1/2 transform  -translate-y-1/2" />

  <div class="flex">
    <shuffled 
      class="grid-inline slidev-vclick-true-hidden text-center px-4 mr-6"
      :id="annotateId"
      :sortAt=0 
      :showAt=0
      style="width: 5rem"
    >K</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :id="annotateId">???</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="[1, 2]" :id="annotateId" :sortAt=1 :showAt=1>eep</shuffled>
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
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :id="annotateId">?</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="[1, 2]" :id="annotateId" :sortAt=1 :showAt=1>t</shuffled>
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
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :id="annotateId">?????</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="[1, 2]" :id="annotateId" :sortAt=1 :showAt=1>imple</shuffled>
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
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click.hide="1" :id="annotateId">?????</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="[1, 2]" :id="annotateId" :sortAt=1 :showAt=1>tup*d</shuffled>
    <shuffled class="grid-inline slidev-vclick-true-hidden" v-click="2" :id="annotateId" :sortAt=2 :showAt=2>olusinya</shuffled> 
  </div>
</div>

---
layout: default
class: bg-secondary text-neutral-900 flex flex-col justify-center align-center
annotateId: efisien
---

# Efisien

<script setup>
const annotateId = "efisien";
</script>

<div class="relative flex justify-center mb-8">
  <annotate class="grid-inline whitespace-nowrap text-6xl" :mark="{ type: 'highlight', color: '#9ed0ff', strokeWidth: 8 }" :id=annotateId >Berpikir Secara Efisien</annotate>
</div>

<img src="/elmodenganlatarbelakangyangsangatberapiapi.gif" class="absolute top-1/2 transform -translate-y-1/2 left-30px w-150px" />

<img src="/elmodenganlatarbelakangyangsangatberapiapi.gif" class="absolute top-1/2 transform -translate-y-1/2 right-30px w-150px" />

<div class="relative w-full">
  <div class="text-3xl text-center mb-2">Ngopi Efisien</div>
  <img src="/kopi-efisien.svg" class="w-500px mx-auto" />
</div>

---
layout: default
class: bg-secondary h-full text-primary
annotateId: mengapa
---

# Mengapa

<script setup>
const annotateId = "mengapa";
</script>

<div class="absolute w-full h-full top-0 left-0 flex flex-col justify-center" v-click.hide="1">
  <shuffled 
    class="inline-grid mx-auto text-9xl text-red-500 whitespace-nowrap"
    :id=annotateId
  >
    Mengapa kita perlu
  </shuffled>
  <shuffled 
    class="inline-grid mx-auto text-9xl text-red-500 whitespace-nowrap"
    :id=annotateId
  >
    Berpikir logis?
  </shuffled>
</div>

<div class="absolute w-full h-full top-0 left-0 flex flex-col justify-center" v-click="1">
  <img src="/spongebobintuisi.png" class="mx-auto h-400px" />
</div>

---
layout: default
class: bg-primary text-white text-center flex justify-center items-center
annotateId: penutup
---

# Penutup

<script setup>
const annotateId = "penutup";
</script>

<annotate 
  class="text-9xl text-neutral-900 px-10 py-4" 
  :mark="{ type: 'highlight', color: '#bfee1d', strokeWidth: 10 }"
  :id="annotateId"
  v-motion
  :initial="{ opacity: 0 }"
  :enter="{ opacity: 1 }"
  :leave="{ opacity: 0 }"
>
  Sekian dan <br />Terima Kasih
</annotate>
