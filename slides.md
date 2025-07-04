---
theme: ./
layout: cover
components:
  jv: './components/jv.vue'
---

# Pembuka

<jv style="font-size: 24rem; line-height:1; margin-bottom: -3rem;" text="Logika" />
<jv class="text-4xl" text="Aditya Nur Juang Rahmanda"/>

---
layout: default
class: bg-primary text-white
---

# Pembuka

<div class="relative flex flex-col justify-center align-center text-center px-10 h-full">
  <jv style="font-size: 14rem; line-height:1; margin-bottom: -2rem" text="/lo·gi·ka/" v-mark="{ at: 0, color: '#bfee1d', type: 'circle', strokeWidth: 8 }"/>
  <p class="text-3xl">
    1. pengetahuan tentang kaidah berpikir; 2. jalan pikiran yang masuk akal;
  </p>
</div> 

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
layout: cover
---

# Penutup

<div class="text-9xl">
  <jv text="Sekian dan" />
  <jv text="Terima Kasih"/>
</div>