---
title: "jsp"
date: 2021-07-15 16:41:28 -0400
categories: study
---
1. URL 유효성 검사
function goEventPage(url){
  //url 유효성 검사
  let regex = /(http|https):\/\/(\w+:{0,1}\w*@)?(\S+)(:[0-9]+)?(\/|\/([\w#!:.?+=&%@!\-\/]))?/;
  
  //올바른 url이 맞다면 해당 url로 이동
  if(regex.test(url)){
  	location.href = url;
  }
}
위와 같이 함수 생성 후 유효성 검사를 통과하면 location.href = url을 통한 url 이동

2. Image 유효성 검사
// 태그에서 data-width / data-height의 value 가져오기
tempMaxWidth = parseInt($(this).next().attr('data-width'));
tempMaxHeight = parseInt($(this).next().attr('data-height'));


let file = this.files[0];
let _URL = window.URL || window.webkitURL;
let img = new Image();
img.src = _URL.createObjectURL(file);
img.onload = function() {
  //Image File과 기존 Tag에 정의한 width, Height 비교
  if(img.width !== tempMaxWidth || img.height !== tempMaxHeight) {
    alert(`이미지 가로 \${tempMaxWidth}px, 세로 \${tempMaxHeight}px로 맞춰서 올려주세요.`);
    //사용 후 공백으로 초기화
    tempMaxWidth = "";
    tempMaxHeight = "";
  }else{
    // 이미지 사이즈가 맞다면 Ajax, Image Append 등 원하는 로직 전개
  }
}
