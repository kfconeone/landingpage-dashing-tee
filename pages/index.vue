<script setup lang="ts">
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { MotionPathPlugin } from "gsap/MotionPathPlugin";

import videojs from "video.js";
import "video.js/dist/video-js.css";

const pos = { x: 0, y: 0 };

onMounted(async () => {
  console.log("begin");

  await waitForAllImagesLoaded();
  gsap.registerPlugin(MotionPathPlugin);
  gsap.registerPlugin(ScrollTrigger);

  rotateStar();

  loopImagesForPc();
  loopImagesForLaptop();
  loopImagesForTablet();
  loopImagesForMobile();

  moveDashingTee();

  showDashingTeeTextForTablet();

  floatingRect();

  showChairSectionText();

  changeTextAccordingToVideoCurrentTime();

  addListerCottonBirdImage();
  addListerFatguyImage();
  addListerBtsImage();
  addListerMoneyImage();

  moveClothInfo();
});

function moveDashingTee() {
  var pcDashingTl = gsap.timeline({
    scrollTrigger: {
      trigger: ".pc-dashing-tee-tri",
      start: "bottom bottom",
    },
  });
  pcDashingTl.to(".pc-dashing-tee", {
    width: "350px",
    duration: 2,
    ease: "Power2.easeOut",
    x: 0,
    y: 0,
  });
  pcDashingTl.to(".pc-dashing-tee", {
    ease: "Power4.easeOut",
    rotate: "-20deg",
  });
  var xlDashingTl = gsap.timeline({
    scrollTrigger: {
      trigger: ".xl-dashing-tee-tri",
      start: "bottom bottom",
    },
  });
  xlDashingTl.to(".xl-dashing-tee", {
    width: "350px",
    duration: 2,
    ease: "Power2.easeOut",
    x: 0,
    y: 0,
  });
  xlDashingTl.to(".xl-dashing-tee", {
    ease: "Power4.easeOut",
    rotate: "-20deg",
  });
  var mdDashingTl = gsap.timeline({
    scrollTrigger: {
      trigger: ".md-dashing-tee-tri",
      start: "bottom bottom",
    },
  });
  mdDashingTl.to(".md-dashing-tee", {
    width: "250px",
    duration: 2,
    ease: "Power2.easeOut",
    x: 0,
    y: 0,
  });
  mdDashingTl.to(".md-dashing-tee", {
    ease: "Power4.easeOut",
    rotate: "-20deg",
  });

  gsap.to(".sm-dashing-tee", {
    scrollTrigger: {
      trigger: ".sm-dashing-tee-tri",
      start: "bottom bottom",
    },
    width: "250px",
    duration: 2,
    ease: "Power2.easeOut",
    y: 0,
  });
}

function showDashingTeeTextForTablet() {
  gsap.from(".md-tee-text1", {
    scrollTrigger: {
      trigger: ".md-tee-text1-tri",
      start: "75% bottom",
    },
    opacity: 0,
    y: 50,
  });
  gsap.from(".md-tee-text2", {
    scrollTrigger: {
      trigger: ".md-tee-text2-tri",
      start: "75% bottom",
    },
    opacity: 0,
    y: 50,
  });

  gsap.from(".sm-tee-text1", {
    scrollTrigger: {
      trigger: ".sm-tee-text1-tri",
      start: "75% bottom",
    },
    opacity: 0,
    y: 50,
  });
  gsap.from(".sm-tee-text2", {
    scrollTrigger: {
      trigger: ".sm-tee-text2-tri",
      start: "75% bottom",
    },
    opacity: 0,
    y: 50,
  });
}

function moveClothInfo() {
  //for pc
  gsap.to(
    ".pc-cloth-info",

    {
      scrollTrigger: {
        trigger: ".pc-cloth-info-tri",
        start: "15% bottom",
      },
      duration: 1,
      ease: "Power2.easeOut",
      opacity: 1,
      motionPath: {
        path: [
          { x: -200, y: 150 },
          { x: -50, y: 100 },
          { x: 100, y: 50 },
          { x: 100, y: -100 },
        ],
        type: "cubic",
      },
    }
  );
  //for laptop
  gsap.to(
    ".xl-cloth-info",

    {
      scrollTrigger: {
        trigger: ".xl-cloth-info-tri",
        start: "15% bottom",
      },
      duration: 1,
      ease: "Power2.easeOut",
      opacity: 1,
      motionPath: {
        path: [
          { x: -100, y: 75 },
          { x: -25, y: 50 },
          { x: 50, y: 25 },
          { x: 50, y: -50 },
        ],
        type: "cubic",
      },
    }
  );
  //for tablet
  gsap.to(
    ".md-cloth-info",

    {
      scrollTrigger: {
        trigger: ".md-cloth-info-tri",
        start: "15% bottom",
      },
      duration: 1,
      ease: "Power2.easeOut",
      opacity: 1,
      motionPath: {
        path: [
          { x: -100, y: 100 },
          { x: -20, y: 60 },
          { x: -5, y: 15 },
          { x: 0, y: 0 },
        ],
        type: "cubic",
      },
    }
  );
  //for mobile
  gsap.to(
    ".sm-cloth-info",

    {
      scrollTrigger: {
        trigger: ".sm-cloth-info-tri",
        start: "15% bottom",
      },
      duration: 1,
      ease: "Power2.easeOut",
      opacity: 1,
      motionPath: {
        path: [
          { x: -100, y: 100 },
          { x: -20, y: 60 },
          { x: -5, y: 15 },
          { x: 0, y: 0 },
        ],
        type: "cubic",
      },
    }
  );
}

function rotateStar() {
  gsap.to(".pc-star", { duration: 6000, rotate: 50000, repeat: -1, ease: "none" });
  gsap.to(".laptop-star", { duration: 6000, rotate: 50000, repeat: -1, ease: "none" });
}

function loopImagesForPc() {
  let pa1 = gsap.to(".pc-hero-section1", {
    duration: 5,
    ease: "none",
    objectPosition: "-25px center",
    paused: true,
    onComplete: () => {
      let t1 = gsap.timeline({
        onComplete: () => {
          pa2.restart();
        },
      });
      t1.set(".pc-hero-section2", { opacity: 1, objectPosition: "0px center" });
      t1.to(".pc-hero-section1", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let pa2 = gsap.to(".pc-hero-section2", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-25px center",
    onComplete: () => {
      let t2 = gsap.timeline({
        onComplete: () => {
          pa3.restart();
        },
      });
      t2.set(".pc-hero-section3", { opacity: 1, objectPosition: "0px center" });
      t2.to(".pc-hero-section2", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let pa3 = gsap.to(".pc-hero-section3", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-25px center",
    onComplete: () => {
      let t3 = gsap.timeline({
        onComplete: () => {
          gsap.set(".pc-hero-section1", { zIndex: 20 });
          pa1.restart();
        },
      });
      t3.set(".pc-hero-section1", { opacity: 1, objectPosition: "0px center", zIndex: 0 });
      t3.to(".pc-hero-section3", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });
  pa1.play();
}
function loopImagesForLaptop() {
  let laptop1 = gsap.to(".laptop-hero-section1", {
    duration: 5,
    ease: "none",
    objectPosition: "-25px center",
    paused: true,
    onComplete: () => {
      let t1 = gsap.timeline({
        onComplete: () => {
          laptop2.restart();
        },
      });
      t1.set(".laptop-hero-section2", { opacity: 1, objectPosition: "0px center" });
      t1.to(".laptop-hero-section1", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let laptop2 = gsap.to(".laptop-hero-section2", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-25px center",
    onComplete: () => {
      let t2 = gsap.timeline({
        onComplete: () => {
          laptop3.restart();
        },
      });
      t2.set(".laptop-hero-section3", { opacity: 1, objectPosition: "0px center" });
      t2.to(".laptop-hero-section2", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let laptop3 = gsap.to(".laptop-hero-section3", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-25px center",
    onComplete: () => {
      let t3 = gsap.timeline({
        onComplete: () => {
          gsap.set(".laptop-hero-section1", { zIndex: 20 });
          laptop1.restart();
        },
      });
      t3.set(".laptop-hero-section1", { opacity: 1, objectPosition: "0px center", zIndex: 0 });
      t3.to(".laptop-hero-section3", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });
  laptop1.play();
}
function loopImagesForTablet() {
  let md1 = gsap.to(".md-hero-section1", {
    duration: 5,
    ease: "none",
    objectPosition: "-25px center",
    paused: true,
    onComplete: () => {
      let t1 = gsap.timeline({
        onComplete: () => {
          md2.restart();
        },
      });
      t1.set(".md-hero-section2", { opacity: 1, objectPosition: "0px center" });
      t1.to(".md-hero-section1", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let md2 = gsap.to(".md-hero-section2", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-25px center",
    onComplete: () => {
      let t2 = gsap.timeline({
        onComplete: () => {
          md3.restart();
        },
      });
      t2.set(".md-hero-section3", { opacity: 1, objectPosition: "0px center" });
      t2.to(".md-hero-section2", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let md3 = gsap.to(".md-hero-section3", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-25px center",
    onComplete: () => {
      let t3 = gsap.timeline({
        onComplete: () => {
          gsap.set(".md-hero-section1", { zIndex: 20 });
          md1.restart();
        },
      });
      t3.set(".md-hero-section1", { opacity: 1, objectPosition: "0px center", zIndex: 0 });
      t3.to(".md-hero-section3", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });
  md1.play();
}
function loopImagesForMobile() {
  let sm1 = gsap.to(".sm-hero-section1", {
    duration: 5,
    ease: "none",
    objectPosition: "-15px center",
    paused: true,
    onComplete: () => {
      let t1 = gsap.timeline({
        onComplete: () => {
          sm2.restart();
        },
      });
      t1.set(".sm-hero-section2", { opacity: 1, objectPosition: "0px center" });
      t1.to(".sm-hero-section1", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let sm2 = gsap.to(".sm-hero-section2", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-15px center",
    onComplete: () => {
      let t2 = gsap.timeline({
        onComplete: () => {
          sm3.restart();
        },
      });
      t2.set(".sm-hero-section3", { opacity: 1, objectPosition: "0px center" });
      t2.to(".sm-hero-section2", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });

  let sm3 = gsap.to(".sm-hero-section3", {
    duration: 5,
    ease: "none",
    paused: true,
    objectPosition: "-15px center",
    onComplete: () => {
      let t3 = gsap.timeline({
        onComplete: () => {
          gsap.set(".sm-hero-section1", { zIndex: 20 });
          sm1.restart();
        },
      });
      t3.set(".sm-hero-section1", { opacity: 1, objectPosition: "0px center", zIndex: 0 });
      t3.to(".sm-hero-section3", { ease: "none", opacity: 0, duration: 0.5 });
    },
  });
  sm1.play();
}

function floatingRect() {
  //for laptop
  gsap.fromTo(
    ".xl-rect-1",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  gsap.fromTo(
    ".xl-rect-2",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  //for tablet
  gsap.fromTo(
    ".md-rect-1",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  gsap.fromTo(
    ".md-rect-2",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  //for mobile
  gsap.fromTo(
    ".sm-rect-1",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  gsap.fromTo(
    ".sm-rect-2",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  //for pc
  gsap.fromTo(
    ".pc-rect-1",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );

  gsap.fromTo(
    ".pc-rect-2",
    {
      y: "random(-5, -3,1)",
    },
    {
      duration: 2,
      repeat: -1,
      yoyo: true,
      y: "random(3, 5,1)",
    }
  );
}

function addListerCottonBirdImage() {
  var cc: any = document.querySelector(".pc-combed-cotten");
  var setOpacity = gsap.quickSetter(".pc-cottonbird", "opacity");
  cc?.addEventListener("mousemove", function (event: any) {
    var rect = cc.getBoundingClientRect();
    var x = event.clientX - rect.left;
    var y = event.clientY - rect.top;
    cc.style.cursor = "none";
    pos.x = x - 150;
    pos.y = y - 75;
  });
  cc?.addEventListener("mouseleave", function (event: any) {
    gsap.ticker.remove(setCottonBirdImagePosition);
    setOpacity(0);
  });
  cc?.addEventListener("mouseenter", function (event: any) {
    gsap.ticker.add(setCottonBirdImagePosition);
    setOpacity(1);
  });
}

function addListerFatguyImage() {
  var cc: any = document.querySelector(".pc-exciting-story");
  var setOpacity = gsap.quickSetter(".pc-fatguy", "opacity");
  cc?.addEventListener("mousemove", function (event: any) {
    var rect = cc.getBoundingClientRect();
    var x = event.clientX - rect.left;
    var y = event.clientY - rect.top;
    cc.style.cursor = "none";
    pos.x = x - 150;
    pos.y = y - 75;
  });
  cc?.addEventListener("mouseleave", function (event: any) {
    gsap.ticker.remove(setFatguyImagePosition);
    setOpacity(0);
  });
  cc?.addEventListener("mouseenter", function (event: any) {
    gsap.ticker.add(setFatguyImagePosition);
    setOpacity(1);
  });
}
function addListerMoneyImage() {
  var cc: any = document.querySelector(".pc-money-zone");
  var setOpacity = gsap.quickSetter(".pc-money", "opacity");
  cc?.addEventListener("mousemove", function (event: any) {
    console.log("mousemove");
    var rect = cc.getBoundingClientRect();
    var x = event.clientX - rect.left;
    var y = event.clientY - rect.top;
    console.log(x, y);
    cc.style.cursor = "none";
    pos.x = x - 150;
    pos.y = y - 75;
  });
  cc?.addEventListener("mouseleave", function (event: any) {
    console.log("mouseleave");
    gsap.ticker.remove(setMoneyImagePosition);
    setOpacity(0);
  });
  cc?.addEventListener("mouseenter", function (event: any) {
    console.log("mouseenter");
    gsap.ticker.add(setMoneyImagePosition);
    setOpacity(1);
  });
}
function addListerBtsImage() {
  var cc: any = document.querySelector(".pc-bts-zone");
  var setOpacity = gsap.quickSetter(".pc-bts", "opacity");
  cc?.addEventListener("mousemove", function (event: any) {
    console.log("mousemove");
    var rect = cc.getBoundingClientRect();
    var x = event.clientX - rect.left;
    var y = event.clientY - rect.top;
    console.log(x, y);
    cc.style.cursor = "none";
    pos.x = x - 150;
    pos.y = y - 75;
  });
  cc?.addEventListener("mouseleave", function (event: any) {
    console.log("mouseleave");
    gsap.ticker.remove(setBtsImagePosition);
    setOpacity(0);
  });
  cc?.addEventListener("mouseenter", function (event: any) {
    console.log("mouseenter");
    gsap.ticker.add(setBtsImagePosition);
    setOpacity(1);
  });
}

function showChairSectionText() {
  //for pc
  gsap.fromTo(
    ".pc-chair-text1",
    { y: 50 },
    {
      ease: "Power4.easeOut",
      y: 0,
      opacity: 1,
      duration: 1,
      scrollTrigger: {
        trigger: ".pc-chair-text1-tri",
        start: "15% bottom",
      },
    }
  );
  gsap.fromTo(
    ".pc-chair-text2",
    { y: 50 },
    {
      ease: "Power4.easeOut",
      y: 0,
      opacity: 1,
      duration: 1,
      scrollTrigger: {
        trigger: ".pc-chair-text2-tri",
        start: "15% bottom",
      },
    }
  );

  //for laptop
  gsap.fromTo(
    ".xl-chair-text1",
    { y: 50 },
    {
      ease: "Power4.easeOut",
      y: 0,
      opacity: 1,
      duration: 1,
      scrollTrigger: {
        trigger: ".xl-chair-text1-tri",
        start: "15% bottom",
      },
    }
  );
  gsap.fromTo(
    ".xl-chair-text2",
    { y: 50 },
    {
      ease: "Power4.easeOut",
      y: 0,
      opacity: 1,
      duration: 1,
      scrollTrigger: {
        trigger: ".xl-chair-text2-tri",
        start: "15% bottom",
      },
    }
  );

  //for Tablet
  var tabletTl = gsap.timeline({
    scrollTrigger: {
      trigger: ".md-chair-text1-tri",
      start: "15% bottom",
    },
  });
  tabletTl.from(".md-chair-text1", {
    ease: "Power4.easeOut",
    y: 50,
    opacity: 0,
    duration: 0.5,
  });

  tabletTl.from(".md-chair-text2", {
    ease: "Power4.easeOut",
    y: 50,
    opacity: 0,
    duration: 0.5,
  });

  //for Mobile
  var mobileTl = gsap.timeline({
    scrollTrigger: {
      trigger: ".sm-chair-text1-tri",
      start: "15% bottom",
    },
  });
  mobileTl.from(".sm-chair-text1", {
    ease: "Power4.easeOut",
    y: 15,
    opacity: 0,
    duration: 0.5,
  });

  mobileTl.from(".sm-chair-text2", {
    ease: "Power4.easeOut",
    y: 15,
    opacity: 0,
    duration: 0.5,
  });
}

function changeTextAccordingToVideoCurrentTime() {
  const player = videojs("pcvideo");
  player.on("timeupdate", function () {
    var text1 = document.querySelector(".pc-video-text1");
    var text2 = document.querySelector(".pc-video-text2");
    var text3 = document.querySelector(".pc-video-text3");
    var text4 = document.querySelector(".pc-video-text4");
    if (player.currentTime() > 0 && player.currentTime() < 7) {
      text4?.classList.add("animate__fadeOut");
      text4?.classList.remove("animate__fadeIn");
      text1?.classList.add("animate__fadeIn");
      text1?.classList.remove("animate__fadeOut");
    } else if (player.currentTime() > 7 && player.currentTime() < 12) {
      text1?.classList.add("animate__fadeOut");
      text1?.classList.remove("animate__fadeIn");
      text2?.classList.remove("animate__fadeOut");
      text2?.classList.add("animate__fadeIn");
    } else if (player.currentTime() > 12 && player.currentTime() < 17) {
      text2?.classList.add("animate__fadeOut");
      text2?.classList.remove("animate__fadeIn");
      text3?.classList.remove("animate__fadeOut");
      text3?.classList.add("animate__fadeIn");
    } else if (player.currentTime() > 17 && player.currentTime() < 20) {
      text3?.classList.add("animate__fadeOut");
      text3?.classList.remove("animate__fadeIn");
      text4?.classList.remove("animate__fadeOut");
      text4?.classList.add("animate__fadeIn");
    }
  });
  const xlPlayer = videojs("xlvideo");
  xlPlayer.on("timeupdate", function () {
    console.log("xlplayer on");
    var xltext1 = document.querySelector(".xl-video-text1");
    var xltext2 = document.querySelector(".xl-video-text2");
    var xltext3 = document.querySelector(".xl-video-text3");
    var xltext4 = document.querySelector(".xl-video-text4");
    if (xlPlayer.currentTime() > 0 && xlPlayer.currentTime() < 7) {
      xltext4?.classList.add("animate__fadeOut");
      xltext4?.classList.remove("animate__fadeIn");
      xltext1?.classList.add("animate__fadeIn");
      xltext1?.classList.remove("animate__fadeOut");
    } else if (xlPlayer.currentTime() > 7 && xlPlayer.currentTime() < 12) {
      xltext1?.classList.add("animate__fadeOut");
      xltext1?.classList.remove("animate__fadeIn");
      xltext2?.classList.remove("animate__fadeOut");
      xltext2?.classList.add("animate__fadeIn");
    } else if (xlPlayer.currentTime() > 12 && xlPlayer.currentTime() < 17) {
      xltext2?.classList.add("animate__fadeOut");
      xltext2?.classList.remove("animate__fadeIn");
      xltext3?.classList.remove("animate__fadeOut");
      xltext3?.classList.add("animate__fadeIn");
    } else if (xlPlayer.currentTime() > 17 && xlPlayer.currentTime() < 20) {
      xltext3?.classList.add("animate__fadeOut");
      xltext3?.classList.remove("animate__fadeIn");
      xltext4?.classList.remove("animate__fadeOut");
      xltext4?.classList.add("animate__fadeIn");
    }
  });
  const mdPlayer = videojs("mdvideo");
  mdPlayer.on("timeupdate", function () {
    console.log("xlplayer on");
    var mdtext1 = document.querySelector(".md-video-text1");
    var mdtext2 = document.querySelector(".md-video-text2");
    var mdtext3 = document.querySelector(".md-video-text3");
    var mdtext4 = document.querySelector(".md-video-text4");
    if (mdPlayer.currentTime() > 0 && mdPlayer.currentTime() < 7) {
      mdtext4?.classList.add("animate__fadeOut");
      mdtext4?.classList.remove("animate__fadeIn");
      mdtext1?.classList.add("animate__fadeIn");
      mdtext1?.classList.remove("animate__fadeOut");
    } else if (mdPlayer.currentTime() > 7 && mdPlayer.currentTime() < 12) {
      mdtext1?.classList.add("animate__fadeOut");
      mdtext1?.classList.remove("animate__fadeIn");
      mdtext2?.classList.remove("animate__fadeOut");
      mdtext2?.classList.add("animate__fadeIn");
    } else if (mdPlayer.currentTime() > 12 && mdPlayer.currentTime() < 17) {
      mdtext2?.classList.add("animate__fadeOut");
      mdtext2?.classList.remove("animate__fadeIn");
      mdtext3?.classList.remove("animate__fadeOut");
      mdtext3?.classList.add("animate__fadeIn");
    } else if (mdPlayer.currentTime() > 17 && mdPlayer.currentTime() < 20) {
      mdtext3?.classList.add("animate__fadeOut");
      mdtext3?.classList.remove("animate__fadeIn");
      mdtext4?.classList.remove("animate__fadeOut");
      mdtext4?.classList.add("animate__fadeIn");
    }
  });
  const smPlayer = videojs("smvideo");
  smPlayer.on("timeupdate", function () {
    console.log("xlplayer on");
    var smtext1 = document.querySelector(".sm-video-text1");
    var smtext2 = document.querySelector(".sm-video-text2");
    var smtext3 = document.querySelector(".sm-video-text3");
    var smtext4 = document.querySelector(".sm-video-text4");
    if (smPlayer.currentTime() > 0 && smPlayer.currentTime() < 7) {
      smtext4?.classList.add("animate__fadeOut");
      smtext4?.classList.remove("animate__fadeIn");
      smtext1?.classList.add("animate__fadeIn");
      smtext1?.classList.remove("animate__fadeOut");
    } else if (smPlayer.currentTime() > 7 && smPlayer.currentTime() < 12) {
      smtext1?.classList.add("animate__fadeOut");
      smtext1?.classList.remove("animate__fadeIn");
      smtext2?.classList.remove("animate__fadeOut");
      smtext2?.classList.add("animate__fadeIn");
    } else if (smPlayer.currentTime() > 12 && smPlayer.currentTime() < 17) {
      smtext2?.classList.add("animate__fadeOut");
      smtext2?.classList.remove("animate__fadeIn");
      smtext3?.classList.remove("animate__fadeOut");
      smtext3?.classList.add("animate__fadeIn");
    } else if (smPlayer.currentTime() > 17 && smPlayer.currentTime() < 20) {
      smtext3?.classList.add("animate__fadeOut");
      smtext3?.classList.remove("animate__fadeIn");
      smtext4?.classList.remove("animate__fadeOut");
      smtext4?.classList.add("animate__fadeIn");
    }
  });
}

function setCottonBirdImagePosition() {
  var setX = gsap.quickSetter(".pc-cottonbird", "x", "px");
  var setY = gsap.quickSetter(".pc-cottonbird", "y", "px");
  // adjust speed for higher refresh monitors
  if (pos.x + 150 > 0 || pos.y + 75 > 0) {
    setX(pos.x);
    setY(pos.y);
  }
}
function setBtsImagePosition() {
  var setX = gsap.quickSetter(".pc-bts", "x", "px");
  var setY = gsap.quickSetter(".pc-bts", "y", "px");
  // adjust speed for higher refresh monitors
  if (pos.x + 150 > 0 || pos.y + 75 > 0) {
    setX(pos.x);
    setY(pos.y);
  }
}
function setMoneyImagePosition() {
  var setX = gsap.quickSetter(".pc-money", "x", "px");
  var setY = gsap.quickSetter(".pc-money", "y", "px");
  // adjust speed for higher refresh monitors
  if (pos.x + 150 > 0 || pos.y + 75 > 0) {
    setX(pos.x);
    setY(pos.y);
  }
}

function setFatguyImagePosition() {
  var setX = gsap.quickSetter(".pc-fatguy", "x", "px");
  var setY = gsap.quickSetter(".pc-fatguy", "y", "px");
  // adjust speed for higher refresh monitors
  if (pos.x + 150 > 0 || pos.y + 75 > 0) {
    setX(pos.x);
    setY(pos.y);
  }
}

async function waitForAllImagesLoaded() {
  let allImgs = document.querySelectorAll("img");
  const imagePromises: any[] = [];
  allImgs.forEach((img) => {
    if (!img.complete) {
      const promise = new Promise((resolve) => {
        img.addEventListener("load", resolve);
      });
      imagePromises.push(promise);
    }
  });

  console.log("start:", new Date().getTime());
  await Promise.all(imagePromises);
  console.log("end:", new Date().getTime());
  console.log("all images loaded");
}
</script>

<template>
  <div class="overflow-hidden">
    <HeroSection />
    <DashingTee />
    <Chair />
    <Contains />
    <Follow />
    <Footer />
  </div>
</template>
