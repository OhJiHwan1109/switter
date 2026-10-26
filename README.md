# 스위터 (Switter)

> **"가장 가볍고 직관적인 올인원 크로스 플랫폼 메모장"**  
> 생각과 아이디어가 떠오를 때 지체 없이 기록하고 안전하게 보관하세요.

---

## 📌 프로젝트 소개

**스위터(Switter)**는 Windows 10/11과 Android를 위한 모던 메모장 애플리케이션입니다.  
복잡하고 무거운 설정 없이, 더블클릭 한 번으로 즉시 실행되는 포터블(Portable) 무설치 환경을 제공하며, 오프라인 우선(Local-first) 설계로 작성된 모든 메모를 사용자 기기에만 안전하게 영구 저장합니다.

- **프로젝트 명칭**: 스위터 (Switter)
- **기본 언어**: 한국어 (한글 조합 및 긴 텍스트 입력 완벽 지원)
- **지원 플랫폼**: Windows 10 / 11 (x64 포터블 .exe), Android (8.0+ .apk)
- **라이선스**: MIT License

---

## ✨ 20가지 핵심 기능

1. **새 메모 즉시 작성**: `Ctrl+N` 또는 상단 툴바 버튼으로 빠른 메모 생성
2. **실시간 메모 열기 및 편집**: 사이드바 목록 선택 즉시 오른쪽 편집기에서 원활한 수정
3. **안전한 저장**: `Ctrl+S` 수동 저장 지원
4. **메모 삭제 및 확인**: 실수 방지를 위한 경고 확인 모달 지원
5. **다중 메모 목록 관리**: 생성된 모든 메모를 최근 수정순/오래된순/제목순으로 분류
6. **제목 및 본문 분리 편집**: 명확한 시각적 계층 구조의 입력창
7. **초고속 통합 검색**: 제목과 본문 내용 전체를 실시간 필터링
8. **3초 자동 저장**: 타이핑 중단 3초 후 데이터가 유실되지 않도록 자동 영구 보관
9. **최근 열었던 메모 유지**: 앱 재실행 시 작업 흐름 보존
10. **실행 취소 & 다시 실행**: `Ctrl+Z` / `Ctrl+Y` 및 툴바 서식 버튼 완벽 연동
11. **표준 클립보드 제어**: 복사(`Ctrl+C`), 잘라내기(`Ctrl+X`), 붙여넣기(`Ctrl+V`) 지원
12. **자유로운 글꼴 및 크기 선택**: 맑은 고딕, 나눔고딕, 코딩용 고정폭 폰트 및 12px~32px 크기 조절
13. **텍스트 서식 스타일링**: 굵게(Bold), 기울임(Italic), 밑줄(Underline), 취소선(Strikethrough)
14. **실시간 통계**: 공백 제외 글자 수 및 단어 수 상태 표시줄에 실시간 집계
15. **다양한 키보드 단축키**: 마우스 없이도 작업 가능한 단축키 환경
16. **눈이 편안한 다크 모드**: 고대비 다크 테마 및 깔끔한 라이트 테마 전환 (`Ctrl+D`)
17. **반응형 창 크기 조절**: 사이드바 드래그 리사이징 및 화면 크기에 따른 최적화 뷰포트
18. **재실행 시 데이터 보존**: 앱을 종료하고 다시 켜도 로컬 데이터베이스 완벽 유지
19. **TXT 파일 연동**: 외부 `.txt` 파일 일괄 가져오기(`Ctrl+O`) 및 내보내기(`Ctrl+Shift+S`)
20. **친절한 오류 안내**: 파일 입출력 및 처리 실패 시 직관적인 알림 토스트 표시

---

## 📂 폴더 구조

```
D:\프로젝트\스위터
├── app/                        # 앱 애플리케이션 소스코드
│   ├── assets/                 # 앱 아이콘 및 정적 자원
│   │   └── icons/              # icon.png, icon.svg
│   ├── src/                    # 메인 & 렌더러 소스
│   │   ├── main.js             # Electron 메인 프로세스 (IPC, 파일 I/O, 윈도우)
│   │   ├── preload.js          # 안전한 컨텍스트 브릿지 API
│   │   └── renderer/           # 웹 기반 반응형 UI (HTML/CSS/JS)
│   │       ├── index.html      # 앱 메인 뷰
│   │       ├── components/     # UI 로직 및 데이터 핸들러 (app.js)
│   │       └── styles/         # 메인 스타일 및 다크/라이트 테마 (main.css, themes.css)
│   └── package.json            # 앱 메타데이터 및 빌드 설정
├── website/                    # 스위터 공식 다운로드 사이트
│   ├── index.html              # 소개 및 다운로드 원페이지 웹
│   ├── assets/                 # 웹 전용 스타일(css) 및 스크립트(js)
│   └── README.md               # 사이트 배포 및 호스팅 가이드
├── scripts/                    # 빌드 및 패키징 자동화 스크립트
│   ├── build-windows.ps1       # Windows 포터블 EXE 빌드
│   ├── build-android.ps1       # Android APK 패키지 빌드
│   ├── build-all.ps1           # 전체 올인원 빌드 스크립트
│   └── create_apk.py           # Android APK 패키징 유틸리티
├── docs/                       # 상세 가이드 문서
│   ├── INSTALL.md              # 환경 설정 및 설치 안내
│   ├── BUILD.md                # 단계별 빌드 방법
│   └── RELEASE.md              # 배포 체크리스트 및 APK 서명 가이드
└── dist/                       # 최종 빌드 산출물
    ├── windows/
    │   └── Switter.exe         # [결과물] Windows 단일 포터블 실행 파일 (약 70MB)
    └── android/
        └── Switter.apk         # [결과물] Android 배포 패키지 파일
```

---

## 🛠️ 개발 환경 및 빌드 가이드

### 1. 개발 모드 실행
```bash
cd D:\프로젝트\스위터\app
npm install
npm start
```

### 2. 플랫폼별 빌드 스크립트 실행
PowerShell 콘솔에서 바로 실행할 수 있습니다:

- **Windows EXE 빌드**:
  ```powershell
  .\scripts\build-windows.ps1
  ```
  결과물: `D:\프로젝트\스위터\dist\windows\Switter.exe`

- **Android APK 빌드**:
  ```powershell
  .\scripts\build-android.ps1
  ```
  결과물: `D:\프로젝트\스위터\dist\android\Switter.apk`

- **통합 올인원 빌드**:
  ```powershell
  .\scripts\build-all.ps1
  ```

---

## 🌐 공식 웹사이트 미리보기

```bash
cd D:\프로젝트\스위터
python -m http.server 8080
```
브라우저에서 `http://localhost:8080/website/` 로 접속하여 다운로드 페이지와 실제 연결된 파일 배포 상태를 확인할 수 있습니다.
