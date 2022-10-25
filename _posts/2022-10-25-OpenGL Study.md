---
title: "Open GL Learning"
date: 2022-10-25 05:00:00
categories: opengl
---

Vertex를 그리기 위해서는 이해해야 될것이 있다

OpenGL API기준이다

<img src="https://user-images.githubusercontent.com/45751396/197693190-c6a997f0-7e0b-46b4-b190-83b605868b9c.png" width=250>

만약 내가 버텍스 정보 (Position, Color..)등을 갖고있다면,

이 버텍스 정보를 이용해 화면에 그리기 위해 이 정보들을 OpenGL에 전달해야되는데, 
OpenGl에 버텍스 데이터를 넣어줄 버퍼를 Vertex Buffer Object라고 부른다
줄여서 VBO라고하며, unstructured arrays of data를 받는다

VBO는 특별한거 없고 그냥 GPU가 접근할 수있는 a buffer of memory라고 볼 수 있다


이제,
VBO를 여러개 만들어서 GPU에 놓는다고 생각해보자

VBO는 그저 데이터 버퍼일 뿐이다. 지혼자 할 수 있는게 없는데
GPU가 이 데이터를 어떻게 이용할지 명령을 내려줘야하는데, 이때 VAO가
Vertex Array Object(VAO)가 GPU에서 VBO를 어떻게 처리할지 알려준다

>> In short words, VBO is an array of raw data, when VAO is an array of ATTRIBUTES - an instruction for shader program how to use the data.

Vertex Array Object와 Vertex Bind Object라는게 있다
VAO, VBO

VAO는 

glGenBuffers = Buffer Object Name을 만든다

Vertex Array Buffer를 만든다
glGenVertexArrays

Vertexs Shader 단계에서 GPU는 메모리에 남아있는 모든 Vertex Data를 처리하는데,
이 메모리를 관리하는 것이 Vertex Array Object(VAO)라고 한다
