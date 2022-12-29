<script setup lang="ts">
onMounted(() => {
  console.log("chair in");
});
</script>
<template>
  <div class="hidden pc:block">
    <div class="bg-[#F9F8F3] px-56 pt-20 pb-80">
      <div class="flex justify-center">
        <div class="w-full max-w-[1472px] border-[3px] border-solid border-[#3f3f3f]">
          <div class="relative">
            <div class="absolute rotate-[-3.74deg] left-[3.5%] bottom-[60%] z-10 pc-chair-text1-tri">
              <div class="pc-chair-text1 opacity-0">
                <div class="bg-[#D2EF20] my-3 px-7 py-2">
                  <p class="text-[#464F13] text-5xl font-bold" style="font-family: taipei-black">鐵椅噴飛愛旅鯊</p>
                </div>
                <div class="bg-[#D2EF20] my-3 px-7 py-2">
                  <p class="text-[#464F13] text-5xl font-bold" style="font-family: taipei-black">faQ響徹太空峽</p>
                </div>
              </div>
            </div>
            <div class="absolute left-[7.5%] bottom-[27.5%] text-2xl z-10 pc-chair-text2-tri">
              <div class="pc-chair-text2 opacity-0">
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>在這個程式碼的宇宙框架下，所有生物依</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>循而生，鐵椅與鯊鯊的定律尤其如此</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>鯊鯊一旦遇上鐵椅就啟動了命運的巨輪，</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>會讓鯊鯊伴隨著FxxK聲和太空船一起被鐵</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>在椅彈飛到遠方</p>
                </div>
              </div>
            </div>

            <div class="w-[300px] absolute left-[40%] bottom-[10%] z-10">
              <img src="imgs/code-film.gif" />
            </div>
            <img class="opacity-50" src="imgs/chair.jpg" />
          </div>
          <div class="flex">
            <div class="w-full flex justify-center border-r-[3px] border-t-[3px] border-solid border-[#3F3F3F]">
              <div class="border-x-[3px] border-solid border-[#3F3F3F]">
                <video class="video-js" preload="auto" ref="pcvideo" id="pcvideo" width="680" height="763" autoplay loop="true" muted>
                  <source src="imgs/dashing-concept.mp4" type="video/mp4" />
                </video>
              </div>
            </div>
            <div class="min-w-[563px] flex justify-center items-center border-t-[3px] border-solid border-[#3F3F3F] text-[#3F3F3F] font-bold text-xl">
              <div class="w-[283px] relative flex items-center">
                <p class="animate__animated animate__fadeOut pc-video-text1" style="font-family: taipei-black">今天是個百里無鐵椅的好天氣，鯊鯊駕駛著飛行船進到愛人 Dasiy 所在的第五維度宇宙</p>
                <p class="absolute animate__animated animate__fadeOut pc-video-text2" style="font-family: taipei-black">眼看著就快到愛人家門口，天敵鐵椅居然出現了!!!!</p>
                <p class="absolute animate__animated animate__fadeOut pc-video-text3" style="font-family: taipei-black">煞不住也停不了<br />在心裡默念Daisy I Love you 後</p>
                <p class="absolute animate__animated animate__fadeOut pc-video-text4" style="font-family: taipei-black">faQ~~~~~~~~~~~<br />太空船彈走了<br />鯊鯊也飛走了</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="hidden xl:block pc:hidden">
    <div class="bg-[#F9F8F3] py-[100px]">
      <div class="flex justify-center">
        <div class="w-full max-w-[1472px] border-[3px] border-solid border-[#3f3f3f]">
          <div class="relative">
            <div class="absolute rotate-[-3.74deg] left-[15%] bottom-[60%] z-10 xl-chair-text1-tri">
              <div class="xl-chair-text1">
                <div class="bg-[#D2EF20] my-3 px-7 py-2">
                  <p class="text-[#464F13] text-5xl font-bold" style="font-family: taipei-black">鐵椅噴飛愛旅鯊</p>
                </div>
                <div class="bg-[#D2EF20] my-3 px-7 py-2">
                  <p class="text-[#464F13] text-5xl font-bold" style="font-family: taipei-black">faQ響徹太空峽</p>
                </div>
              </div>
            </div>
            <div class="absolute left-[20%] bottom-[27.5%] text-xl z-10 xl-chair-text2-tri">
              <div class="xl-chair-text2">
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>在這個程式碼的宇宙框架下，所有生物依循</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>而生，鐵椅與鯊鯊的定律尤其如此</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>鯊鯊一旦遇上鐵椅就啟動了命運的巨輪，會</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>讓鯊鯊伴隨著FxxK聲和太空船一起被鐵椅彈</p>
                </div>
                <div class="bg-[#FFFFFF] w-fit px-1.5 pt-0.5 my-2">
                  <p>飛到遠方</p>
                </div>
              </div>
            </div>

            <div class="w-[350px] absolute right-[20%] bottom-[20%] z-10">
              <img src="imgs/code-film.gif" />
            </div>
            <img class="opacity-50" src="imgs/chair.jpg" />
          </div>
          <div class="flex">
            <div class="w-full flex justify-center border-r-[3px] border-t-[3px] border-solid border-[#3F3F3F]">
              <div class="border-x-[3px] border-solid border-[#3F3F3F]">
                <video class="video-js" preload="auto" id="xlvideo" width="680" height="763" autoplay loop="true" muted>
                  <source src="imgs/dashing-concept.mp4" type="video/mp4" />
                </video>
              </div>
            </div>

            <div class="min-w-[400px] flex justify-center items-center border-t-[3px] border-solid border-[#3F3F3F] text-[#3F3F3F] font-bold text-xl">
              <div class="w-[283px] flex items-center justify-center">
                <p class="animate__animated animate__fadeOut xl-video-text1" style="font-family: taipei-black">今天是個百里無鐵椅的好天氣，鯊鯊駕駛著飛行船進到愛人 Dasiy 所在的第五維度宇宙</p>
                <p class="absolute animate__animated animate__fadeOut xl-video-text2" style="font-family: taipei-black">眼看著就快到愛人家門口，天敵鐵椅居然出現了!!!!</p>
                <p class="absolute animate__animated animate__fadeOut xl-video-text3" style="font-family: taipei-black">煞不住也停不了<br />在心裡默念Daisy I Love you 後</p>
                <p class="absolute animate__animated animate__fadeOut xl-video-text4" style="font-family: taipei-black">faQ~~~~~~~~~~~<br />太空船彈走了<br />鯊鯊也飛走了</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="hidden md:block xl:hidden">
    <div class="bg-[#F9F8F3] py-[71px]">
      <div class="flex justify-center">
        <div class="w-[515px] border-[1px] border-solid border-[#3f3f3f] relative">
          <div class="absolute w-[200px] rotate-[-30deg] bottom-[20%] left-[-7.5%] z-10">
            <img src="imgs/code-film.gif" />
          </div>
          <img class="w-full opacity-50 z-0 relative" src="imgs/chair.jpg" />
        </div>
      </div>
      <div class="flex justify-center gap-9 mt-20 items-center">
        <div class="md-chair-text1-tri">
          <div class="md-chair-text1 rotate-[-3.74deg] text-[#3F3F3F] text-[32px] font-bold" style="font-family: taipei-black">
            <p>鐵椅噴飛愛旅鯊</p>
            <p>faQ響徹太空峽</p>
          </div>
        </div>
        <div class="w-[290px] md-chair-text2-tri">
          <div class="md-chair-text2">
            <p>在這個程式碼的宇宙框架下，所有生物依循而生，鐵椅與鯊鯊的定律尤其如此</p>
            <br />
            <p>鯊鯊一旦遇上鐵椅就啟動了命運的巨輪， 會讓鯊鯊伴隨著FxxK聲和太空船一起被鐵椅彈飛到遠方</p>
          </div>
        </div>
      </div>
      <div class="w-full flex justify-center border-r-[1px] border-y-[1px] border-solid border-[#3F3F3F] mt-[57px]">
        <div class="border-x-[1px] border-solid border-[#3F3F3F]">
          <video class="video-js" preload="auto" id="mdvideo" width="558" height="559" autoplay loop="true" muted>
            <source src="imgs/dashing-concept.mp4" type="video/mp4" />
          </video>
        </div>
      </div>

      <div class="flex justify-center py-16 border-solid border-black border-b-[1px]">
        <div class="w-[303px] text-xl flex justify-center items-center" style="font-family: taipei-black">
          <p class="animate__animated animate__fadeOut md-video-text1" style="font-family: taipei-black">今天是個百里無鐵椅的好天氣，鯊鯊駕駛著飛行船進到愛人 Dasiy 所在的第五維度宇宙</p>
          <p class="absolute animate__animated animate__fadeOut md-video-text2" style="font-family: taipei-black">眼看著就快到愛人家門口，天敵鐵椅居然出現了!!!!</p>
          <p class="absolute animate__animated animate__fadeOut md-video-text3" style="font-family: taipei-black">煞不住也停不了<br />在心裡默念Daisy I Love you 後</p>
          <p class="absolute animate__animated animate__fadeOut md-video-text4" style="font-family: taipei-black">faQ~~~~~~~~~~~<br />太空船彈走了<br />鯊鯊也飛走了</p>
        </div>
      </div>
    </div>
  </div>
  <div class="block md:hidden">
    <div class="bg-[#F9F8F3] py-[57px]">
      <div class="flex justify-center">
        <div class="w-[261px] border-[1px] border-solid border-[#3f3f3f] relative">
          <div class="absolute w-[100px] rotate-[-30deg] bottom-[20%] left-[-10%] z-10">
            <img src="imgs/code-film.gif" />
          </div>
          <img class="w-full opacity-50" src="imgs/chair.jpg" />
        </div>
      </div>
      <div class="flex justify-center gap-9 mt-[35px] items-center sm-chair-text1-tri">
        <div class="sm-chair-text1 rotate-[-3.74deg] text-[#3F3F3F] text-xl font-bold" style="font-family: taipei-black">
          <p>鐵椅噴飛愛旅鯊</p>
          <p>faQ響徹太空峽</p>
        </div>
        <div class="w-[190px] text-xs sm-chair-text2">
          <p>在這個程式碼的宇宙框架下，所有生物依循而生，鐵椅與鯊鯊的定律尤其如此</p>
          <br />
          <p>鯊鯊一旦遇上鐵椅就啟動了命運的巨輪， 會讓鯊鯊伴隨著FxxK聲和太空船一起被鐵椅彈飛到遠方</p>
        </div>
      </div>
      <div class="w-full flex justify-center border-r-[1px] border-y-[1px] border-solid border-[#3F3F3F] mt-11">
        <div class="border-x-[1px] border-solid border-[#3F3F3F]">
          <video id="smvideo" width="276" height="276" autoplay loop="true" muted>
            <source src="imgs/dashing-concept.mp4" type="video/mp4" />
          </video>
        </div>
      </div>
      <div class="flex justify-center border-b-[1px] border-solid border-[#3f3f3f] items-center">
        <div class="w-[303px] text-base py-5 flex justify-center items-center" style="font-family: taipei-black">
          <p class="animate__animated animate__fadeOut sm-video-text1" style="font-family: taipei-black">今天是個百里無鐵椅的好天氣，鯊鯊駕駛著飛行船進到愛人 Dasiy 所在的第五維度宇宙</p>
          <p class="absolute animate__animated animate__fadeOut sm-video-text2" style="font-family: taipei-black">眼看著就快到愛人家門口，天敵鐵椅居然出現了!!!!</p>
          <p class="absolute animate__animated animate__fadeOut sm-video-text3" style="font-family: taipei-black">煞不住也停不了<br />在心裡默念Daisy I Love you 後</p>
          <p class="absolute animate__animated animate__fadeOut sm-video-text4" style="font-family: taipei-black">faQ~~~~~~~~~~~<br />太空船彈走了<br />鯊鯊也飛走了</p>
        </div>
      </div>
    </div>
  </div>
</template>
