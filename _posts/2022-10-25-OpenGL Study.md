---
title: "Open GL Learning"
date: 2022-10-25 05:00:00
categories: opengl
---

Vertex를 그리기 위해서는 이해해야 될것이 있다

OpenGL API기준이다

<img src="https://user-images.githubusercontent.com/45751396/197693190-c6a997f0-7e0b-46b4-b190-83b605868b9c.png" width=100>

만약 내가 버텍스 정보 (Position, Color..)등을 갖고있다면,

이 버텍스 정보를 이용해 화면에 그리기 위해 이 정보를 OpenGL에 전달해야되는데, 
OpenGl에 버텍스 데이터를 넣어줄 버퍼를 Vertex Buffer Object라고 부른다
VBO라고 줄여부르는, 이것은 unstructured arrays of data라고 Array형태의 데이터를 받는다

unstructured arrays라고 float, int, double 등등의 타입이 정해지지 않은 array로 타입을 정하면 넣어줄 수 있다

GPU에 해당 ARRAYㄷ


Vertex Array Object와 Vertex Bind Object라는게 있다
VAO, VBO

VAO는 

glGenBuffers = Buffer Object Name을 만든다

Vertex Array Buffer를 만든다
glGenVertexArrays
