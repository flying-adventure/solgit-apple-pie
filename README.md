# solgit-apple-pie

---
## *프로젝트 개요* 
###  image 파일에 업로드 된 사용자의 사진에서 사용자의 얼굴을 인식하여 게임 캐릭터로 제작하고 제작된 캐릭터로 게임을 진행한다.
  
- 게임 이름 : 무당이가 폭탄이라면?
- 게임 규칙 : 하늘에서 떨어지는 폭탄 무당이를 방향키로 피해서 살아남기
- 성공 조건 : 15개의 무당이가 떨어지는 동안 게임이 종료되지 않는다면 성공! 
- 실패 조건:  무당이를 피하지 못했을 때 게임이 종료된다.
---
## *데모*

[게임 실행 화면](https://github.com/flying-adventure/solgit-apple-pie/blob/master/Game%20Launch%20Screen.png)

[무당이와 캐릭터의 충돌 시 화면](https://github.com/flying-adventure/solgit-apple-pie/blob/master/Game%20colliding%20Screen.png)

[충돌 이후 게임 종료 화면](https://github.com/flying-adventure/solgit-apple-pie/blob/master/Game%20Over%20Exit%20Screen.png)

[게임 성공시 종료 화면](https://github.com/flying-adventure/solgit-apple-pie/blob/master/Game%20Winning%20Screen.png)


---
## *사용한 패키지*

|패키지 |패키지 설명|이 프로젝트에서 사용된 곳|
|-------|-------|------|
| pygame | 비디오 게임 작성을 위해 사용된 python 모듈의 모음.| 게임 창 생성, 이벤트 처리 및 이미지 표시와 게임 관련 기능을 처리하는 데 사용됨. |
| cv2(OpenCV) | 오픈소스 컴퓨터 비전 및 머신 러닝 소프트웨어 라이브러리. | 얼굴 감지 및 이미지 조작에 사용됨. (이미지를 읽고, 사전 훈련된 Haar Cascade 분류기를 사용하여 얼굴을 감지하고, 감지된 얼굴을 자르며 다른 이미지와 결합함) |
| numpy | 파이썬 프로그래밍 언어를 위한 배열 및 행렬 지원을 제공하는 라이브러리|수치 연산에 사용됨. |    

설치가 필요한 패키지

```
$pip install pygame opencv-python numpy
```

---
## *실행방법*
- 전체 파일 다운로드 및 game_sorce_code.py 실행  
---
## *참고 자료*    
- 위에서 내려오는 개체 &캐릭터 이동 코드 [참고한 깃허브 링크](https://github.com/ElenaLim/Pygame/blob/main/minigame.py)
- 파이썬 OpenCV로 사진에서 얼굴인식 후 얼굴만 크로핑 하는 코드 [참고한 블로그 링크](https://m.blog.naver.com/jcosmoss/220934659282)
---
