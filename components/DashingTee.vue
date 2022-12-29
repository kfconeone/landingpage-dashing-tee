<script setup lang="ts">
onMounted(() => {
  console.log("DashingTee");
});
</script>
<template>
  <div class="hidden pc:block">
    <div class="bg-[#E8E4FF] pt-12">
      <div class="flex justify-center w-full">
        <div class="relative flex w-full max-w-[1550px] justify-between">
          <div style="font-family: dgo" class="text-[300px] text-[#C6CEFD] leading-[123.99%]">
            <p class="pc-dashing-tee-tri">DAS-</p>
            <p>01UT</p>
          </div>
        </div>
      </div>

      <div class="flex justify-center w-full mt-28 gap-12">
        <div class="relative w-[500px] flex justify-center items-center">
          <div class="absolute w-[698px] pc-dashing-tee translate-y-[-800px] translate-x-[850px]">
            <img class="w-full" src="/imgs/tee-698.png" />
          </div>
          <img class="w-full" src="/imgs/tee-bg.png" />
        </div>

        <div>
          <div class="ml-12 text-word-tri">
            <p class="text-black text-4xl font-bold text-word" style="font-family: jenhei">這是...</p>
          </div>

          <div class="w-[507px] mt-2">
            <img class="w-full" src="/imgs/dashing-first-tee.svg" />
          </div>

          <div class="ml-64 mt-[91px] bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[508px] text-xl flex justify-center py-4" style="font-family: taipei-black">
            <div>
              <div>
                <div class="flex items-center gap-1 w-full">
                  <p>首席設計師 Machi</p>
                  <img class="w-[23px] h-[20px]" src="/imgs/emoji-red-heart.png" />
                  <p>使用了街頭藝術、太空宇</p>
                </div>
                <div class="w-[433px]">
                  <p>宙、漫畫框架等元素手法，強調了達訊潮流、先</p>
                </div>
                <div class="w-[433px] flex items-center gap-1">
                  <p>進、活潑輕鬆的企業文化</p>
                  <img class="w-[23px] h-[20px]" src="/imgs/emoji-yellow-mark.png" />
                </div>
              </div>
              <div class="mt-5">
                <div class="flex items-center gap-1 w-full">
                  <p>DAS-01UT 設定一個程式碼宇宙，在這個宇宙，</p>
                </div>
                <div class="w-[433px] flex items-center gap-1">
                  <p>程式碼將成為決定這個宇宙命運的唯一定律</p>
                  <img class="w-[23px] h-[20px]" src="/imgs/emoji-blue-rect.png" />
                </div>
                <div class="w-[433px]">
                  <p>來看看更多在這個宇宙框架的故事吧!</p>
                </div>
              </div>
            </div>
          </div>
          <div class="pl-44 pt-[39px]">
            <div class="pc-rect-1 border-[1px] border-solid border-[#3f3f3f] bg-[#F9f8f3] w-[231px] h-[35px]"></div>
          </div>
          <div class="pl-32 pt-[29px]">
            <div class="pc-rect-2 border-[1px] border-solid border-[#3f3f3f] bg-[#F9f8f3] w-[146px] h-[25px]"></div>
          </div>
        </div>
      </div>

      <div class="flex justify-center border-y-[3px] border-solid border-[#3F3F3F] mt-16">
        <p class="text-[#4B5DC4] text-[150px]" style="font-family: dgo">UNIFORM STORY</p>
      </div>
    </div>
  </div>
  <div class="hidden xl:block pc:hidden">
    <div class="bg-[#E8E4FF] pt-12">
      <div class="flex justify-center w-full">
        <div class="relative flex w-full max-w-[1250px] justify-between">
          <div style="font-family: dgo" class="text-[250px] text-[#C6CEFD] leading-[123.99%]">
            <p class="xl-dashing-tee-tri">DAS-</p>
            <p>01UT</p>
          </div>
        </div>
      </div>

      <div class="flex justify-center w-full mt-28 gap-12">
        <div class="relative w-[500px] flex justify-center items-center">
          <div class="absolute w-[533px] translate-x-[650px] translate-y-[-700px] xl-dashing-tee">
            <img class="w-full" src="/imgs/tee-533.png" />
          </div>
          <img class="w-full" src="/imgs/tee-bg.png" />
        </div>

        <div>
          <div class="ml-12">
            <p class="text-black text-4xl font-bold" style="font-family: jenhei">這是...</p>
          </div>

          <div class="w-[507px] mt-2">
            <img class="w-full" src="/imgs/dashing-first-tee.svg" />
          </div>

          <div class="mt-24 ml-32 bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[416px] text-base flex justify-center py-4" style="font-family: taipei-black">
            <div>
              <div>
                <div class="flex justify-center items-center gap-1 w-full">
                  <p>首席設計師 Machi</p>
                  <img class="w-[23px] h-[20px]" src="/imgs/emoji-red-heart.png" />
                  <p>使用了街頭藝術、太空宇宙、</p>
                </div>
                <div class="w-[369px]">
                  <p>漫畫框架等元素手法，強調了達訊潮流、先進、活潑</p>
                </div>
                <div class="w-[369px] flex items-center gap-1">
                  <p>輕鬆的企業文化</p>
                  <img class="w-[23px] h-[20px]" src="/imgs/emoji-yellow-mark.png" />
                </div>
              </div>
              <div class="mt-5">
                <div class="flex items-center gap-1 w-full">
                  <p>DAS-01UT 設定一個程式碼宇宙，在這個宇宙，程式</p>
                </div>
                <div class="w-[369px] flex items-center gap-1">
                  <p>碼將成為決定這個宇宙命運的唯一定律</p>
                  <img class="w-[23px] h-[20px]" src="/imgs/emoji-blue-rect.png" />
                  <p>看更多在</p>
                </div>
                <div class="w-[369px]">
                  <p>這個宇宙框架的故事吧!</p>
                </div>
              </div>
            </div>
          </div>
          <div class="xl-rect-1 ml-24 mt-[45px] border-[1px] border-solid border-[#3f3f3f] bg-[#F9f8f3] w-[231px] h-[35px]"></div>
          <div class="xl-rect-2 ml-12 mt-[29px] border-[1px] border-solid border-[#3f3f3f] bg-[#F9f8f3] w-[146px] h-[25px]"></div>
        </div>
      </div>

      <div class="flex justify-center border-y-[3px] border-solid border-[#3F3F3F] mt-24">
        <p class="text-[#4B5DC4] text-[100px]" style="font-family: dgo">UNIFORM STORY</p>
      </div>
    </div>
  </div>
  <div class="hidden md:block xl:hidden">
    <div class="bg-[#E8E4FF] mt-40 rounded-t-[40px]">
      <div class="flex justify-center w-full">
        <div class="relative flex w-full max-w-[690px] justify-between">
          <div style="font-family: dgo" class="mt-36 text-[150px] text-[#C6CEFD] leading-[123.99%]">
            <p class="md-dashing-tee-tri">DAS-</p>
            <p>01UT</p>
          </div>
        </div>
      </div>
      <div class="flex w-full justify-center mt-8 md-tee-text1-tri">
        <p class="text-black text-2xl font-bold md-tee-text1" style="font-family: jenhei">這是...</p>
      </div>
      <div class="flex w-full justify-center mt-5 md-tee-text2-tri">
        <div class="w-[362px] md-tee-text2">
          <img class="w-full" src="/imgs/dashing-first-tee.svg" />
        </div>
      </div>
      <div class="flex gap-12 items-center justify-center">
        <div class="relative w-[300px] flex justify-center items-center">
          <div class="absolute w-[325px] translate-x-[380px] translate-y-[-525px] md-dashing-tee">
            <img class="w-full" src="/imgs/tee-533.png" />
          </div>
          <div class="absolute w-[98px] z-20 right-[-10%] top-[2%]">
            <svg viewBox="0 0 98 99" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M46.6005 5.03123C47.7126 2.84476 50.8362 2.84476 51.9484 5.03124L65.6384 31.9451C65.9225 32.5035 66.3743 32.9591 66.9305 33.2477L93.6438 47.1117C95.8012 48.2313 95.8012 51.3175 93.6438 52.4372L66.9305 66.3011C66.3743 66.5898 65.9225 67.0453 65.6384 67.6038L51.9484 94.5176C50.8362 96.7041 47.7126 96.7041 46.6005 94.5176L32.9104 67.6038C32.6263 67.0453 32.1745 66.5898 31.6184 66.3011L4.90503 52.4372C2.74762 51.3175 2.74763 48.2313 4.90504 47.1117L31.6184 33.2477C32.1745 32.9591 32.6263 32.5035 32.9104 31.9451L46.6005 5.03123Z"
                fill="#E8FF5A"
                stroke="#9EB41C"
                stroke-width="5"
              />
            </svg>
          </div>
          <div class="absolute w-[98px] z-20 left-[-15%] bottom-[-7.5%]">
            <svg viewBox="0 0 98 99" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M46.6005 5.03123C47.7126 2.84476 50.8362 2.84476 51.9484 5.03124L65.6384 31.9451C65.9225 32.5035 66.3743 32.9591 66.9305 33.2477L93.6438 47.1117C95.8012 48.2313 95.8012 51.3175 93.6438 52.4372L66.9305 66.3011C66.3743 66.5898 65.9225 67.0453 65.6384 67.6038L51.9484 94.5176C50.8362 96.7041 47.7126 96.7041 46.6005 94.5176L32.9104 67.6038C32.6263 67.0453 32.1745 66.5898 31.6184 66.3011L4.90503 52.4372C2.74762 51.3175 2.74763 48.2313 4.90504 47.1117L31.6184 33.2477C32.1745 32.9591 32.6263 32.5035 32.9104 31.9451L46.6005 5.03123Z"
                fill="#E8FF5A"
                stroke="#9EB41C"
                stroke-width="5"
              />
            </svg>
          </div>
          <div class="absolute w-[98px] z-20 left-[-15%] bottom-[-7.5%]">
            <svg viewBox="0 0 98 99" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M46.6005 5.03123C47.7126 2.84476 50.8362 2.84476 51.9484 5.03124L65.6384 31.9451C65.9225 32.5035 66.3743 32.9591 66.9305 33.2477L93.6438 47.1117C95.8012 48.2313 95.8012 51.3175 93.6438 52.4372L66.9305 66.3011C66.3743 66.5898 65.9225 67.0453 65.6384 67.6038L51.9484 94.5176C50.8362 96.7041 47.7126 96.7041 46.6005 94.5176L32.9104 67.6038C32.6263 67.0453 32.1745 66.5898 31.6184 66.3011L4.90503 52.4372C2.74762 51.3175 2.74763 48.2313 4.90504 47.1117L31.6184 33.2477C32.1745 32.9591 32.6263 32.5035 32.9104 31.9451L46.6005 5.03123Z"
                fill="#E8FF5A"
                stroke="#9EB41C"
                stroke-width="5"
              />
            </svg>
          </div>
          <img class="w-full" src="/imgs/tee-bg.png" />
        </div>
        <div class="pt-24">
          <div class="ml-12 bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[234px] h-[185px] text-xs flex justify-center py-4 px-2" style="font-family: taipei-black">
            <div>
              <div>
                <div class="flex items-center gap-1">
                  <p>首席設計師 Machi</p>
                  <img class="w-[17px] h-[15px]" src="/imgs/emoji-red-heart.png" />
                  <p>使用了街頭藝術</p>
                </div>
                <div class="flex">
                  <p>、太空宇宙、漫畫框架等元素手法，強</p>
                </div>
                <div class="flex items-center gap-1">
                  <p>調了達訊潮流、先進、活潑輕鬆的企業</p>
                </div>
                <div class="flex items-center gap-1">
                  <p>文化</p>
                  <img class="w-[17px] h-[15px]" src="/imgs/emoji-yellow-mark.png" />
                </div>
              </div>

              <div class="mt-5">
                <div class="flex items-center gap-1 w-full">
                  <p>DAS-01UT 設定一個程式碼宇宙，在這個宇宙，程式碼將成為決定這個宇宙命運的</p>
                </div>
                <div class="flex items-center gap-1">
                  <p>唯一定律</p>
                  <img class="w-[17px] h-[15px]" src="/imgs/emoji-blue-rect.png" />
                  <p>看更多在這個宇宙框架的</p>
                </div>

                <div class="flex items-center gap-1 w-full">
                  <p>事吧!</p>
                </div>
              </div>
            </div>
          </div>
          <div class="md-rect-1 mt-9 ml-8 bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[130px] h-6"></div>
          <div class="md-rect-2 mt-6 bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[82px] h-4"></div>
        </div>
      </div>
      <div class="flex justify-center border-y-[2px] border-solid border-[#3F3F3F] mt-12 py-6">
        <p class="text-[#4B5DC4] text-5xl" style="font-family: dgo">UNIFORM STORY</p>
      </div>
    </div>
  </div>
  <div class="block md:hidden">
    <div class="bg-[#E8E4FF] rounded-t-[40px]">
      <div class="flex justify-center w-full">
        <div class="relative flex w-full max-w-[690px] justify-center mt-64 text-[96px] text-[#C6CEFD] leading-[123.99%]" style="font-family: dgo">
          <div>
            <p class="sm-dashing-tee-tri">DAS-</p>
            <p>01UT</p>
          </div>
        </div>
      </div>
      <div class="flex w-full justify-center mt-8 sm-tee-text1-tri">
        <p class="text-black text-2xl font-bold sm-tee-text1" style="font-family: jenhei">這是...</p>
      </div>
      <div class="flex w-full justify-center mt-5 sm-tee-text2-tri">
        <div class="w-[362px] sm-tee-text2">
          <img class="w-full" src="/imgs/dashing-first-tee.svg" />
        </div>
      </div>
      <div class="flex gap-12 items-center justify-center mt-16">
        <div class="relative w-[300px] flex justify-center items-center">
          <div class="absolute w-[390px] z-10 translate-y-[-750px] sm-dashing-tee">
            <img class="w-full" src="/imgs/tee-left.png" />
          </div>
          <div class="absolute w-[84px] z-20 right-[-10%] top-[5%]">
            <svg viewBox="0 0 84 84" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M39.3316 4.19343C40.4476 2.02145 43.5524 2.02146 44.6684 4.19343L56.1543 26.5483C56.4407 27.1056 56.8944 27.5593 57.4517 27.8457L79.8066 39.3316C81.9785 40.4476 81.9785 43.5524 79.8066 44.6684L57.4517 56.1543C56.8944 56.4407 56.4407 56.8944 56.1543 57.4517L44.6684 79.8066C43.5524 81.9785 40.4476 81.9785 39.3316 79.8066L27.8457 57.4517C27.5593 56.8944 27.1056 56.4407 26.5483 56.1543L4.19343 44.6684C2.02145 43.5524 2.02146 40.4476 4.19343 39.3316L26.5483 27.8457C27.1056 27.5593 27.5593 27.1056 27.8457 26.5483L39.3316 4.19343Z"
                fill="#E8FF5A"
                stroke="#9EB41C"
                stroke-width="5"
              />
            </svg>
          </div>
          <div class="absolute w-[84px] z-20 left-[-15%] bottom-[-7.5%]">
            <svg viewBox="0 0 84 84" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M39.3316 4.19343C40.4476 2.02145 43.5524 2.02146 44.6684 4.19343L56.1543 26.5483C56.4407 27.1056 56.8944 27.5593 57.4517 27.8457L79.8066 39.3316C81.9785 40.4476 81.9785 43.5524 79.8066 44.6684L57.4517 56.1543C56.8944 56.4407 56.4407 56.8944 56.1543 57.4517L44.6684 79.8066C43.5524 81.9785 40.4476 81.9785 39.3316 79.8066L27.8457 57.4517C27.5593 56.8944 27.1056 56.4407 26.5483 56.1543L4.19343 44.6684C2.02145 43.5524 2.02146 40.4476 4.19343 39.3316L26.5483 27.8457C27.1056 27.5593 27.5593 27.1056 27.8457 26.5483L39.3316 4.19343Z"
                fill="#E8FF5A"
                stroke="#9EB41C"
                stroke-width="5"
              />
            </svg>
          </div>
          <img class="w-full" src="/imgs/tee-bg.png" />
        </div>
      </div>
      <div class="flex justify-center">
        <div class="w-full max-w-[390px] pl-4 pr-20">
          <div class="mt-12 bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[234px] h-[185px] text-xs flex justify-center py-4 px-2" style="font-family: taipei-black">
            <div>
              <div>
                <div class="flex items-center gap-1">
                  <p>首席設計師 Machi</p>
                  <img class="w-[17px] h-[15px]" src="/imgs/emoji-red-heart.png" />
                  <p>使用了街頭藝術</p>
                </div>
                <div class="flex">
                  <p>、太空宇宙、漫畫框架等元素手法，強</p>
                </div>
                <div class="flex items-center gap-1">
                  <p>調了達訊潮流、先進、活潑輕鬆的企業</p>
                </div>
                <div class="flex items-center gap-1">
                  <p>文化</p>
                  <img class="w-[17px] h-[15px]" src="/imgs/emoji-yellow-mark.png" />
                </div>
              </div>

              <div class="mt-5">
                <div class="flex items-center gap-1 w-full">
                  <p>DAS-01UT 設定一個程式碼宇宙，在這個宇宙，程式碼將成為決定這個宇宙命運的</p>
                </div>
                <div class="flex items-center gap-1">
                  <p>唯一定律</p>
                  <img class="w-[17px] h-[15px]" src="/imgs/emoji-blue-rect.png" />
                  <p>看更多在這個宇宙框架的</p>
                </div>

                <div class="flex items-center gap-1 w-full">
                  <p>事吧!</p>
                </div>
              </div>
            </div>
          </div>
          <div class="flex justify-end w-full pr-5">
            <div class="sm-rect-1 mt-3 bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[130px] h-6"></div>
          </div>
          <div class="flex justify-end w-full">
            <div class="sm-rect-2 mt-[14px] bg-[#F9F8F3] border-[1px] border-solid border-[#3F3F3F] w-[82px] h-4"></div>
          </div>
        </div>
      </div>

      <div class="flex justify-center border-y-[1px] border-solid border-[#3F3F3F] mt-5 py-3.5">
        <p class="text-[#4B5DC4] text-[32px]" style="font-family: dgo">UNIFORM STORY</p>
      </div>
    </div>
  </div>
</template>
