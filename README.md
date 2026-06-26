# WINK SHOT — 윙크 사격 좀비 🧟

마우스 없이 **손가락 조준 + 윙크 사격**으로 즐기는 레트로 좀비 슈팅 웹게임.
웹캠만 있으면 됩니다. 단일 `index.html` 파일, 빌드 불필요.

> 📚 **본 프로젝트는 패스트캠퍼스(FastCampus) 강의 자료입니다.**

## 플레이 방법

- 🖐 **검지 끝**으로 조준점을 움직입니다 (손 움직임을 2.3배 증폭 — 작은 손짓으로 화면 전체 커버)
- 😉 **윙크(한쪽 눈 감기)** 로 사격합니다
- 메뉴 버튼도 같은 조준점으로 조작 — 버튼에 조준점을 올리고 윙크하면 클릭

## 좀비 3종

| 종류 | 체력 | 속도 | 점수 |
|------|------|------|------|
| 🟢 일반 | 1 | 보통 | 10 |
| 🟡 빠른 | 1 | 빠름 | 15 |
| 🟩 큰놈 | 3 | 느림 | 30 |

## 기술 스택

- **손 추적**: [MediaPipe HandLandmarker](https://developers.google.com/mediapipe) — 검지 끝(landmark 8) 추적
- **윙크 감지**: MediaPipe FaceLandmarker + blendshapes(`eyeBlinkLeft/Right`)
- 순수 Canvas 2D 렌더링, 외부 빌드 도구 없음
- 레트로 한글 픽셀폰트 [Galmuri](https://galmuri.quiple.dev/)

## 실행

```bash
# 로컬에서 바로 열기 (웹캠 권한 필요)
open index.html
```

> ⚠️ 카메라 접근은 `https` 또는 `localhost`/`file://` 환경에서 동작합니다.

## 키보드 폴백 (웹캠 없을 때 테스트용)

- 마우스 이동 = 조준
- 클릭 / 스페이스바 = 사격
