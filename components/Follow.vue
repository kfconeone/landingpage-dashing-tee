<script setup lang="ts">
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

onMounted(() => {});

function onSwiper() {}
function onSlideChange() {}

function onSlideNextClickedForPc() {
  console.log("onSlideNextClickedForPc");
  const swiper = (document.getElementById("pc-swiper") as any).swiper;

  swiper.slideNext();
}
function onSlideNextClickedForMobile() {
  console.log("onSlideNextClickedForMobile");
  const swiper = (document.getElementById("sm-swiper") as any).swiper;

  swiper.slideNext();
}
function onSlidePrevClickedForPc() {
  console.log("onSlidePrevClickedForPc");
  const swiper = (document.getElementById("pc-swiper") as any).swiper;

  swiper.slidePrev();
}
function onSlidePrevClickedForMobile() {
  console.log("onSlidePrevClickedForMobile");
  const swiper = (document.getElementById("sm-swiper") as any).swiper;

  swiper.slidePrev();
}
</script>
<template>
  <div class="hidden xl:block">
    <div class="w-full flex justify-center bg-[#F9F8F3] pt-20 pc:pt-[157px]">
      <div class="w-full max-w-[1050px] pc:max-w-[1502px]">
        <div class="py-4 justify-center text-[#F9F8F3] flex bg-[#3F3F3F] font-black text-[24px] pc:text-[36px]" style="font-family: Arial"><p>嗨嗨^^ 不可能看到最後了還不來追蹤我們吧?!</p></div>
        <div class="flex bg-[#F9F8F3] border-2 border-solid border-[#3f3f3f] justify-center items-center w-full p-8 pc:px-12 pc:py-12">
          <div class="w-full">
            <div class="w-full">
              <swiper id="pc-swiper" :slides-per-view="4" :space-between="10" @swiper="onSwiper" @slideChange="onSlideChange" :loop="true">
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-1.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-2.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-3.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-4.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-5.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-6.png" />
                  </div>
                </swiper-slide>
              </swiper>
            </div>
            <div class="flex justify-center gap-5 mt-8 pc:mt-12">
              <div class="w-8 pc:w-11 cursor-pointer" type="button" @click="onSlidePrevClickedForPc()">
                <svg viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="10" cy="10" r="10" fill="#B0A3FF" />
                  <path
                    d="M12.1191 13.165C12.041 13.165 11.9629 13.1504 11.8848 13.1211L6.04004 10.499C5.67871 10.3232 5.49805 10.0645 5.49805 9.72266V9.60547C5.49805 9.26367 5.67871 9.00488 6.04004 8.8291L11.8848 6.20703C11.9629 6.17773 12.041 6.16309 12.1191 6.16309C12.2852 6.16309 12.4268 6.22168 12.5439 6.33887C12.6611 6.45605 12.7197 6.59766 12.7197 6.76367C12.7197 6.88086 12.6807 6.99316 12.6025 7.10059C12.5244 7.20801 12.4268 7.28613 12.3096 7.33496L7.06543 9.66406L12.3096 11.9932C12.4268 12.042 12.5244 12.1201 12.6025 12.2275C12.6807 12.335 12.7197 12.4473 12.7197 12.5645C12.7197 12.7305 12.6611 12.8721 12.5439 12.9893C12.4268 13.1064 12.2852 13.165 12.1191 13.165Z"
                    fill="#F9F8F3"
                  />
                </svg>
              </div>
              <div class="w-8 pc:w-11 cursor-pointer" type="button" @click="onSlideNextClickedForPc()">
                <svg viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="10" cy="10" r="10" fill="#B0A3FF" />
                  <path
                    d="M7.37695 13.165C7.21094 13.165 7.06934 13.1064 6.95215 12.9893C6.83496 12.8721 6.77637 12.7305 6.77637 12.5645C6.77637 12.4473 6.81543 12.335 6.89355 12.2275C6.97168 12.1201 7.06934 12.042 7.18652 11.9932L12.416 9.66406L7.18652 7.33496C7.06934 7.28613 6.97168 7.20801 6.89355 7.10059C6.81543 6.99316 6.77637 6.88086 6.77637 6.76367C6.77637 6.59766 6.83496 6.45605 6.95215 6.33887C7.06934 6.22168 7.21094 6.16309 7.37695 6.16309C7.46484 6.16309 7.54297 6.17773 7.61133 6.20703L13.4561 8.8291C13.8174 9.00488 13.998 9.26367 13.998 9.60547V9.72266C13.998 10.0645 13.8174 10.3232 13.4561 10.499L7.61133 13.1211C7.54297 13.1504 7.46484 13.165 7.37695 13.165Z"
                    fill="#F9F8F3"
                  />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="block xl:hidden">
    <div class="w-full flex justify-center bg-[#F9F8F3] pt-40">
      <div class="w-full max-w-[345px] md:max-w-[627px]">
        <div class="py-4 justify-center text-[#F9F8F3] flex bg-[#3F3F3F] font-black text-xs md:text-base" style="font-family: Arial"><p>嗨嗨^^ 不可能看到最後了還不來追蹤我們吧?!</p></div>
        <div class="flex bg-[#F9F8F3] border-2 border-solid border-[#3f3f3f] justify-center items-center w-full p-6 md:px-11 md:py-8">
          <div class="w-full">
            <div class="w-full">
              <swiper id="sm-swiper" :slides-per-view="2" :space-between="5" @swiper="onSwiper" @slideChange="onSlideChange" :loop="true">
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-1.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-2.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-3.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-4.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-5.png" />
                  </div>
                </swiper-slide>
                <swiper-slide>
                  <div class="w-full">
                    <img src="imgs/sp-6.png" />
                  </div>
                </swiper-slide>
              </swiper>
            </div>
            <div class="flex justify-center gap-5 mt-2 md:mt-7">
              <div class="w-5 md:w-9" @click="onSlidePrevClickedForMobile()">
                <svg viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="10" cy="10" r="10" fill="#B0A3FF" />
                  <path
                    d="M12.1191 13.165C12.041 13.165 11.9629 13.1504 11.8848 13.1211L6.04004 10.499C5.67871 10.3232 5.49805 10.0645 5.49805 9.72266V9.60547C5.49805 9.26367 5.67871 9.00488 6.04004 8.8291L11.8848 6.20703C11.9629 6.17773 12.041 6.16309 12.1191 6.16309C12.2852 6.16309 12.4268 6.22168 12.5439 6.33887C12.6611 6.45605 12.7197 6.59766 12.7197 6.76367C12.7197 6.88086 12.6807 6.99316 12.6025 7.10059C12.5244 7.20801 12.4268 7.28613 12.3096 7.33496L7.06543 9.66406L12.3096 11.9932C12.4268 12.042 12.5244 12.1201 12.6025 12.2275C12.6807 12.335 12.7197 12.4473 12.7197 12.5645C12.7197 12.7305 12.6611 12.8721 12.5439 12.9893C12.4268 13.1064 12.2852 13.165 12.1191 13.165Z"
                    fill="#F9F8F3"
                  />
                </svg>
              </div>
              <div class="w-5 md:w-9" @click="onSlideNextClickedForMobile()">
                <svg viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="10" cy="10" r="10" fill="#B0A3FF" />
                  <path
                    d="M7.37695 13.165C7.21094 13.165 7.06934 13.1064 6.95215 12.9893C6.83496 12.8721 6.77637 12.7305 6.77637 12.5645C6.77637 12.4473 6.81543 12.335 6.89355 12.2275C6.97168 12.1201 7.06934 12.042 7.18652 11.9932L12.416 9.66406L7.18652 7.33496C7.06934 7.28613 6.97168 7.20801 6.89355 7.10059C6.81543 6.99316 6.77637 6.88086 6.77637 6.76367C6.77637 6.59766 6.83496 6.45605 6.95215 6.33887C7.06934 6.22168 7.21094 6.16309 7.37695 6.16309C7.46484 6.16309 7.54297 6.17773 7.61133 6.20703L13.4561 8.8291C13.8174 9.00488 13.998 9.26367 13.998 9.60547V9.72266C13.998 10.0645 13.8174 10.3232 13.4561 10.499L7.61133 13.1211C7.54297 13.1504 7.46484 13.165 7.37695 13.165Z"
                    fill="#F9F8F3"
                  />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
