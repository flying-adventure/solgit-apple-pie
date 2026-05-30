# 무당이가 폭탄이라면? 🐞💣

사용자 사진에서 얼굴을 자동 인식해 게임 캐릭터로 만들고,  
하늘에서 떨어지는 폭탄(무당이)을 방향키로 피하는 Python 게임입니다.

---

## 기술 스택

| 분류 | 기술 |
|------|------|
| Language | Python 3 |
| 게임 엔진 | pygame |
| 컴퓨터 비전 | OpenCV (cv2), Haar Cascade 분류기 |
| 수치 연산 | numpy |

---

## 게임 규칙

| 항목 | 내용 |
|------|------|
| 조작 | 좌/우 방향키 |
| 성공 조건 | 폭탄 15개가 떨어지는 동안 충돌 없이 생존 |
| 실패 조건 | 폭탄(무당이)과 충돌 시 즉시 게임 오버 |
| 난이도 | 6점마다 폭탄 낙하 속도 증가 |

---

## 주요 기능

- **얼굴 인식 캐릭터** — `image/person.jpg`를 Haar Cascade로 분석해 얼굴 영역 자동 크롭
- **이미지 합성** — 크롭된 얼굴과 캐릭터 이미지(기본/경고/패배/승리)를 `cv2.addWeighted`로 합성
- **충돌 판정** — `pygame.sprite.spritecollideany`로 폭탄-플레이어 충돌 감지
- **레벨 시스템** — 점수 6점마다 폭탄 낙하 속도 증가
- **효과음** — BGM(`background_sound.mp3`) 및 폭발음(`boom.mp3`) 재생
- **게임 종료 화면** — 충돌 시 게임오버 / 15점 초과 시 승리 화면 표시

---

## 설치 및 실행

### 사전 요구사항
- Python 3 설치

### 패키지 설치

```bash
pip install pygame opencv-python numpy
```

### 사용자 사진 등록

`image/person.jpg` 파일을 본인 사진으로 교체합니다.  
(정면 얼굴이 잘 보이는 사진 권장)

### 실행

```bash
python game_source_code.py
```

---

## 디렉토리 구조

```
solgit-apple-pie/
├── game_source_code.py          # 메인 게임 코드
├── haarcascade_frontalface_default.xml  # 얼굴 인식 모델
├── haarcascade_eye.xml          # 눈 인식 모델
├── image/
│   ├── person.jpg               # 사용자 사진 (교체 필요)
│   ├── user_Base.png            # 캐릭터 기본 이미지
│   ├── user_Warning.png         # 캐릭터 경고 이미지
│   ├── user_Lose.png            # 캐릭터 패배 이미지
│   ├── user_Win.png             # 캐릭터 승리 이미지
│   ├── bomb_Base.png            # 폭탄 기본 이미지
│   ├── bomb_Warning.png         # 폭탄 충돌 이미지
│   └── back_ground.jpg          # 배경 이미지
└── Sound/
    ├── background_sound.mp3     # 배경 음악
    └── boom.mp3                 # 폭발 효과음
```

---

## 데모 화면

| 화면 | 링크 |
|------|------|
| 게임 실행 화면 | [Game Launch Screen](Game%20Launch%20Screen.png) |
| 폭탄 충돌 화면 | [Game Colliding Screen](Game%20colliding%20Screen.png) |
| 게임 오버 화면 | [Game Over Screen](Game%20Over%20Exit%20Screen.png) |
| 게임 성공 화면 | [Game Winning Screen](Game%20Winning%20Screen.png) |

---

## 참고 자료

- 낙하 오브젝트 & 캐릭터 이동 코드 참고: [ElenaLim/Pygame](https://github.com/ElenaLim/Pygame/blob/main/minigame.py)
- OpenCV 얼굴 인식 후 크롭 참고: [네이버 블로그](https://m.blog.naver.com/jcosmoss/220934659282)
