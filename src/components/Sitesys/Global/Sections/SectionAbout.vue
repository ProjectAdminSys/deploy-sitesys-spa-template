<template>
  <section id="about" class="about">
    <div class="container py-24 mx-auto px-4">
      <div class="anim1-scroll">
        <h2 class="trigger1-scroll text-7xl md:text-5xl mb-10 text-center">
          About
        </h2>
        <div
          class="lg:w-full mx-auto flex flex-wrap justify-center items-center"
        >
          <img
            alt="Image"
            class="w-[480px] h-[480px] max-w-auto lg:pl-10 lg:py-6 mt-6 lg:mt-0 object-cover object-center rounded"
            :src="imageUrl1"
          />
          <div class="lg:w-1/2 w-full lg:pl-10 lg:py-6 mt-6 lg:mt-0">
            <p class="text-base text-center lg:text-left">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas,
              quisquam optio! Sequi, amet veritatis culpa, hic explicabo eum
              voluptatem at officiis doloribus atque alias dignissimos ipsa enim
              suscipit impedit tempore? Lorem, ipsum dolor sit amet consectetur
              adipisicing elit. Cumque fugiat earum pariatur facere dolorum aut
              ex? Blanditiis in autem deleniti repellendus eveniet, dolor libero
              iusto non, dicta voluptates earum natus? Lorem ipsum dolor sit
              amet consectetur, adipisicing elit.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import imageUrl1 from '@/assets/images/sitesys/about/about-01.jpg'
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  gsap.from('.anim1-scroll', {
    y: 100,
    opacity: 0,
    duration: 0.5,
    ease: 'power3.inOut',
    scrollTrigger: {
      trigger: '.trigger1-scroll',
      start: 'top 80%',
      end: 'center 10%',
      toggleActions: 'play none resume complete',
      markers: false,
    },
  })
})
</script>
