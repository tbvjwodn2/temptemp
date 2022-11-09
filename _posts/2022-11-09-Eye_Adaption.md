---
title: "Eye Adaption"
date: 2022-11-04 13:40:00
categories: lumen, ue5
---

Auto Exposure
화면 전체의 기본 Luminance를 18% Gray 즉 Final Color로는 50% Gray(127)로 맞추기 위해 있는것

예) 어두운 곳에 가면, 화면의 전체 평균 Luminance밝기를 50% Gray로 맞추는것
화면 전체의 Luminance값을 평균내서 나온 값이 40% Gray라고 가정하면, 50%가 되기까지 10%가 부족하기에, 전체 화면에 10%를 더해줘 50%의 평균 Luminance값을 갖도록 한다

예2) 밝은 곳에 가면, 화면의 전체 평균 Luminance밝기를 50% Gray로 맞추는것
 

한번 따라해보자
Post Process에서
- Min Ev100을 -10으로 놓고
- Max Ev100을 -20으로 설정한다
그리고 Directional Light Intensity를 조절하여, 흐린날씨를 만들어보자

아마 거의 불가능할것이다
Directional Light의 Intensity를 0.1이나 10이나, 50이나 차이가 없기 똑같이 그려질것이다

이것이 바로 Min Ev100과 Max Ev100의 기능이다
어떠한 밝기에 상관없이 화면의 평균 Luminance값을 50%로 맞추려고 하는것..

이렇게 되면, 생각날것이
UE4, UE5에서 갑자기 밝은 것을 보게되면, 주변 모든것들이 어두워지는 현상
또는 어두운 것을 보면 모든것들이 밝아지는 현상





Auto Exposure를 계산할때, 태양, 그림자가 Auto Exposure 계산에 들어가지 못하도록 하는 것이

Low Percent와 High Percent이다


![image](https://user-images.githubusercontent.com/45751396/200765729-abae3aea-f88a-46f5-91d3-c753e7e47016.png)
