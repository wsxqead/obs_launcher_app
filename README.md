# 📺 OBS Launcher App

OBS Launcher App은 방송자가 **OBS를 직접 제어하지 않고도**  
플랫폼 전용 런처에서 **로그인 → 방송 시작/종료**를 손쉽게 할 수 있도록 만든 Electron 기반 앱입니다.  

OBS는 **백엔진**으로만 동작하며, 런처에서 모든 제어를 대신합니다.  

---

## 🚀 기능

- 아이콘 클릭으로 런처 실행  
- 방송 시작/종료 버튼 → OBS 자동 실행 및 제어  
- RTMP 서버 주소 & Stream Key 입력 → OBS 설정 자동 주입  
- **추후 기능 확장 예정**:
  - 플랫폼 로그인 + 스트림키 자동 발급
  - 후원 이벤트 발생 시 OBS에 효과 자동 삽입
  - UI/브랜드 커스터마이징

---

## 📦 설치 & 실행

### 개발 환경에서 실행
```bash

git clone https://your-repo-url/obs-launcher-app.git

cd obs-launcher-app

npm install

npm start
```

## 🚀 기능

아이콘 클릭으로 런처 실행

방송 시작/종료 버튼 → OBS 자동 실행 및 제어

RTMP 서버 주소 & Stream Key 입력 → OBS 설정 자동 주입

추후 기능 확장 예정:

플랫폼 로그인 + 스트림키 자동 발급

후원 이벤트 발생 시 OBS에 효과 자동 삽입

UI/브랜드 커스터마이징

📦 설치 & 실행

1. 개발 환경에서 실행

```bash

   git clone https://your-repo-url/obs-launcher-app.git

   cd obs-launcher-app

   npm install

   npm start
```

2. 빌드 (아이콘 더블클릭 실행 파일 만들기)
```bash
   npm run build
```

Windows: dist/OBS Launcher Setup.exe

Mac: dist/OBS Launcher.dmg

빌드된 실행 파일을 설치하면 바탕화면/시작 메뉴에 아이콘이 생기며, 아이콘 더블클릭으로 앱 실행이 가능합니다.

## ⚙️ OBS 설정

OBS 설치

OBS 공식 다운로드

OBS WebSocket 활성화

OBS 28 이상: 기본 포함 (Tools > WebSocket Server Settings)

포트: 4455

비밀번호: 설정 후 launcher 코드와 일치시켜야 함

런처 실행 후 연결 확인

OBS Connected! 로그가 나오면 정상 연결됨

## 🗂 프로젝트 구조
```bash
obs-launcher-app/
├── main.js # Electron 메인 프로세스
├── preload.js # Renderer <-> Node.js 브릿지
├── renderer/ # UI 관련 코드
│ ├── index.html # 로그인/방송 버튼 UI
│ └── index.js # UI 로직
└── services/
└── obsControl.js # OBS WebSocket 제어 모듈
```

## 📝 사용 방법

앱 실행 (아이콘 더블클릭)

RTMP 서버 주소 & Stream Key 입력

“방송 시작” 버튼 → OBS 자동 실행 및 송출 시작

“방송 종료” 버튼 → OBS 송출 종료

## 🛠 개발 예정 기능

플랫폼 계정 로그인 및 자동 스트림키 발급

후원 이벤트 → OBS Scene 자동 삽입

방송 상태 모니터링 UI (시청자 수, 후원 내역 등)

플랫폼 브랜드 전용 아이콘/스플래시 화면

## 📄 라이선스

이 프로젝트는 GPL v2
라이선스를 따르는 OBS 소스 코드와 연동됩니다.
런처 자체는 MIT 라이선스를 적용할 수 있습니다.
