# ⚡ 고성능 OCR & 인페인팅 웹 에디터

<p align="left">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/Tesseract.js-v5.0-blue?style=for-the-badge" />
</p>

웹 브라우저에서 이미지 내 텍스트를 영역 지정하여 **OCR로 자동 인식**하고, 원본 배경을 **자동 인페인팅(Inpainting)**으로 깨끗하게 복원한 뒤 새로운 멀티라인 텍스트로 교체할 수 있는 Canvas 기반 이미지 편집 도구입니다.

---

## 📌 목차 (Table of Contents)
- [✨ 주요 기능](#-주요-기능-key-features)
- [🛠️ 기술 스택](#️-기술-스택-tech-stack)
- [🚀 시작하기](#-시작하기-getting-started)
- [⌨️ 단축키 안내](#️-단축키-안내-shortcuts)
- [📖 사용 방법](#-사용-방법-usage)

---

## ✨ 주요 기능 (Key Features)

- 🔄 **선택 영역 자동 저장 & 레이어화**
  - 영역 지정 및 수정 후 캔버스의 다른 곳을 클릭하면 작업 중이던 내용이 **자동으로 레이어로 확정/등록**되어 안전하게 보존됩니다.

- 🎨 **스마트 배경 복원 (Inpainting & Solid Fill)**
  - 선택 영역 외곽 픽셀 샘플링 기반의 **자동 배경 복원(Edge Sampling Inpaint)** 기능으로 원본 글씨 자국을 깨끗하게 지웁니다.
  - 단색(Solid Fill) 배경 채우기 모드도 자유롭게 전환할 수 있습니다.

- 📝 **멀티라인 텍스트 & 줄간격 조절**
  - OCR 인식 결과 및 직접 입력 시 `Enter` 키를 통한 **줄바꿈(Multiline)** 지원.
  - 폰트 크기, 색상, Bold, 정렬(왼쪽/중앙/오른쪽)과 더불어 **줄간격 배율(Line Height)**까지 세밀하게 조절 가능합니다.

- 🔍 **고정밀 OCR 엔진 탑재**
  - `Tesseract.js v5` 기반 한/영 동시 인식 및 워커(Worker) 사전 웜업을 통한 속도 최적화.

- 🔎 **캔버스 줌 & 팬 (Zoom & Pan)**
  - 마우스 휠을 통한 Smooth 줌 인/아웃.
  - `Space + Drag` 또는 마우스 휠 클릭을 통한 자유로운 화면 이동.

- ↩️ **히스토리 관리 (Undo / Redo)**
  - `Ctrl + Z` / `Ctrl + Y` 단축키를 통한 실시간 레이어 작업 취소 및 재실행 지원.

- 🔤 **Google Fonts 연동**
  - 12종의 다양한 한/영 구글 폰트 라이브러리 탑재.

---

## 🛠️ 기술 스택 (Tech Stack)

| 구분 | 기술 / 라이브러리 | 설명 |
| :--- | :--- | :--- |
| **Language** | `JavaScript (ES6+)` | 메인 인터랙션 및 레이어 로직 구현 |
| **Markup & Style** | `HTML5`, `CSS3` | 반응형 Split Workspace 레이아웃 |
| **Graphic Engine** | `HTML5 Canvas 2D API` | 레이어 렌더링, Matrix Transform, Inpainting |
| **AI / OCR** | `Tesseract.js (v5)` | 클라이언트 사이드 문자 인식 엔진 |
| **Typography** | `Google Fonts API` | 한/영 웹폰트 12종 동적 로딩 |

---

## 🚀 시작하기 (Getting Started)

단일 HTML 파일로 구성되어 있어 별도의 Node.js 환경 구축이나 빌드 과정 없이 **웹 브라우저에서 즉시 실행** 가능합니다.

### 1. 저장소 복사
```bash
git clone [https://github.com/사용자이름/저장소이름.git](https://github.com/사용자이름/저장소이름.git)
cd 저장소이름

2. 실행index.html 파일을 웹 브라우저(Chrome, Edge 등)로 열어 사용합니다.⌨️ 단축키 안내 (Shortcuts)단축키기능 설명Space + Drag캔버스 화면 이동 (Pan)Mouse Wheel캔버스 확대 / 축소 (Zoom)Ctrl + Z실행 취소 (Undo)Ctrl + Y / Ctrl + Shift + Z다시 실행 (Redo)Ctrl + 0화면 크기 100% 맞춤 (Reset Zoom)📖 사용 방법 (Usage)📂 이미지 로드: 상단 메뉴의 📂 이미지 로드 버튼으로 편집할 이미지를 불러옵니다.🖱️ 영역 선택: 수정할 텍스트 영역을 마우스로 드래그합니다.✏️ OCR 인식 & 편집: 자동 추출된 텍스트를 정정하고 폰트, 크기, 줄간격, 배경 복원 옵션을 설정합니다.➕ 자동 확정 & 추가 수정: 다른 위치를 클릭하면 현재 편집건이 레이어로 자동 확정되며 새로운 영역 선택이 가능합니다.💾 결과물 저장: 편집이 끝난 이미지를 💾 저장 버튼을 눌러 PNG 파일로 다운로드합니다.
