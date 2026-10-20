# 🎮 Mobile Wedding Invitation Ver.3 (MapleStory Ludibrium Toy Factory Theme)

> **게임 감성 인터랙티브 맵, 오디오 사운드 시스템 및 서버리스 클라우드를 융합한 고도화 모바일 웹 애플리케이션**

[![Demo Page](https://img.shields.io/badge/Live_Demo-GitHub_Pages-2ea44f?style=for-the-badge&logo=github)](https://dbd01350-eng.github.io/mobilewedding3/demo.html)
[![Tech Stack](https://img.shields.io/badge/Stack-HTML5%20%7C%20CSS3%20%7C%20Web%20Audio%20%7C%20GAS-blue?style=for-the-badge)](#기술-스택-및-아키텍처)

---

## 📌 프로젝트 개요 (Overview)
- **프로젝트명**: 메이플스토리 루디브리엄 장난감공장 테마 모바일 청첩장 웹 애플리케이션
- **개발 형태**: Zero-Dependency 순수 정적 웹 + Web Audio API + 서버리스 클라우드 파이프라인
- **기획 및 디자인 의도**: 추억의 온라인 게임(메이플스토리 루디브리엄)의 독창적인 레고/도트 비주얼과 BGM, 게임 사운드를 모바일 웹 환경에 완벽 이식하여 하객에게 몰입감 넘치는 인터랙티브 경험 제공
- **핵심 목표**: Figma Node `109:1754` 100% 픽셀 일치, 게임 HUD 퀵메뉴, 3D 성탑 캐러셀, 실시간 초 단위 타이머 및 서버리스 연동을 총망라한 고난이도 인터랙티브 프론트엔드 구축

---

## 🛠 기술 스택 및 아키텍처 (Tech Stack & Architecture)
- **Frontend**: HTML5, CSS3 Custom Properties (Design Tokenization), Vanilla JavaScript (ES6+)
- **Audio & Media**: Web Audio / HTML5 Audio API (BGM & 상황별 효과음 4종 제어)
- **Serverless Backend**: Google Apps Script (GAS) Webhook
- **Database & Storage**: Google Sheets (RSVP 실시간 통계), Google Drive (하객 사진/영상 클라우드 백업)
- **Performance Optimization**: HTML5 Canvas API (인메모리 이미지 1600px 리사이징 & 압축)
- **Maps API**: Naver Maps Open API v3 (GitHub Secrets 자동 주입)
- **CI/CD & Deploy**: GitHub Actions, GitHub Pages
- **Quality Assurance**: Custom AST Token Linter (`check-hardcode.mjs`)

---

## ✨ 핵심 엔지니어링 역량 (Key Engineering Highlights)

### 1. 반응형 게임 HUD 퀵메뉴 바 (Fixed Game HUD Navigation)
- 모바일 100dvh 뷰포트 내에 완벽하게 안착하는 하단 6종 컬러 타일 HUD 시스템 구축.
- 예식정보, 오시는길, 참석여부, 마음전달, 갤러리, 사진올리기 6대 기능과 오버레이 모달이 즉각 반응.

### 2. 정밀한 인터랙티브 오디오 & 효과음 시스템 (Sound Architecture)
- 브라우저 자동재생 정책(Autoplay Policy)에 대응한 스마트 BGM 토글 시스템.
- 모달 열기(`open.mp3`), 닫기/취소(`close.mp3`), 퀘스트 수락(`quest.mp3`), 포탈 이동(`portal.mp3`) 등 사용자 행동마다 게임 원작의 생생한 피드백을 전달하는 오디오 믹싱.

### 3. 피그마 기반 레고 성탑 3D 캐러셀 및 풀스크린 뷰어
- CSS 3D Transform과 가상 요소(Pseudo-elements)를 조합하여 루디브리엄 레고 성탑과 무한 3D 회전 캐러셀 구현.
- 뷰포트 고정형 라이트박스 뷰어로 화면 스크롤 위치에 구애받지 않고 고화질 웨딩 사진 감상 가능.

### 4. 서버리스 파이프라인 (RSVP & 미디어 업로드)
- **퀘스트 전구 NPC 인터랙션**: 메이플 퀘스트 수락 UI를 차용한 재미있는 RSVP 설문 폼 및 Google Sheets 실시간 동기화.
- **하객 파파라치 기자단 미디어 백업**: 클라이언트 Canvas 인메모리 압축으로 하객 사진을 구글 드라이브에 다이렉트 전송.

### 5. 엄격한 품질 관리 & 안심 데모 모드 (`data-demo="true"`)
- `check-hardcode.mjs` 검사 결과 인라인 하드코딩 0 에러 달성.
- 포트폴리오 공개 시 실제 DB 오염을 방지하고 개인정보를 완벽 분리하는 안전한 샌드박스 환경 제공.

---

## 📂 디렉터리 구조 (Directory Structure)
```text
ver3/
├── assets/                  # 루디브리엄 도트/레고 에셋, WebP 이미지, 사운드(MP3)
├── css/
│   └── style.css            # 피그마 픽셀 일치 루디브리엄 디자인 시스템
├── hooks/
│   └── check-hardcode.mjs   # 디자인 하네스 토큰 준수 검증 린터
├── js/
│   └── main.js              # HUD 팝업, 사운드 제어, 지도, 갤러리, GAS 백엔드 연동
├── demo.html                # 포트폴리오/공개용 비식별화 안심 데모 페이지
├── index.html               # 프로덕션 배포 원본 파일
├── PRD.md                   # 제품 요구사항 정의서
└── README.md
```
