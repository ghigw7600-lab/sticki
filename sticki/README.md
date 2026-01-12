# Sticki - 스마트 메모보드

> 책상 위 포스트잇을 주머니 속으로. 디지털 업무 관리 앱

## 📌 프로젝트 개요

| 항목 | 내용 |
|------|------|
| **앱 이름** | Sticki (스티키) |
| **컨셉** | 모니터 옆 포스트잇 → 디지털화 |
| **타겟** | 영업직, 사무직, 1인샵 사장님, 프리랜서 |
| **기술 스택** | HTML/CSS/JS, Firebase Realtime DB, PWA |
| **메인 컬러** | #20C997 (민트) |

## 🎯 핵심 기능

1. **스마트 파싱** - 카톡 복붙하면 자동으로 회사명/연락처/담당자 분리
2. **드래그앤드롭** - 포스트잇을 단계별로 이동
3. **자동 이월** - 자정에 미완료 건 → 다음날로
4. **실시간 동기화** - Firebase로 PC/모바일 동기화
5. **프리셋** - 영업용/사무직용/사장님용/단순관리/프리랜서용

## 📁 파일 구조

```
sticki/
├── index.html      # 메인 앱
├── manifest.json   # PWA 설정
├── sw.js           # 서비스 워커
├── icon-192.png    # 앱 아이콘
├── icon-512.png    # 앱 아이콘 (고해상도)
└── README.md       # 이 파일
```

## 🎨 컬러 팔레트

```
메인:     #20C997 (민트)
서브:     #E6FCF5 (연한 민트)
다크:     #1A1A2E (네이비)
텍스트:   #212529
서브텍스트: #868E96
배경:     #F8F9FA
```

## ✅ 완료된 작업

- [x] PWA 기본 구조
- [x] Firebase 연동
- [x] 스마트 파싱 로직 (연락처/이름/회사명 자동 인식)
- [x] 드래그앤드롭 단계 이동
- [x] 상태메모 도장 스타일 (우측하단)
- [x] 프리셋 시스템 (5종)
- [x] 단계 커스터마이징
- [x] 오늘 콜백 패널
- [x] 메인보드 (날짜별 뷰)
- [x] 로그 검색
- [x] 반응형 디자인 (PC/모바일)

## 📋 다음 할일 (TODO)

- [ ] **아이콘/이모티콘 적용** - Copilot에서 생성 후 적용
  - 앱 아이콘 (3가지 컬러 옵션 중 선택)
  - 내부 UI 아이콘 (카톡 스타일 심플 아이콘)
- [ ] **전화걸기 버튼** - 카드 팝업에서 바로 전화 연결
- [ ] **디자인 최종 개선**
- [ ] **테스트 & 피드백**
- [ ] **앱스토어 출시 준비** (Capacitor)

## 🖼️ 아이콘 생성 프롬프트 (Copilot용)

### 앱 아이콘 (민트)
```
Minimal flat app icon design.
A simple sticky note with folded corner.
Colors: mint green (#20C997) note on dark navy (#1A1A2E) background.
Clean, modern, no text, no shadows, geometric style.
Similar to iOS app icon style.
```

### 내부 아이콘
```
Simple solid fill icon set for mobile app UI.
Style: KakaoTalk-like minimal icons, single color filled, no outlines.
Color: gray (#868E96)
Icons: home, calendar, search, settings (gear), plus, bell, checkmark, trash, pencil, X close, hamburger menu, user profile.
Each icon very simple geometric shape, no details.
```

## 🔧 설정 방법

1. Firebase 프로젝트 생성
2. Realtime Database 활성화 (테스트 모드)
3. 웹 앱 추가 → firebaseConfig 복사
4. 앱에서 config 붙여넣기

## 📝 스마트 파싱 지원 패턴

| 입력 예시 | 인식 결과 |
|----------|----------|
| `테이크엠 김사장 010-1234-5678` | 회사: 테이크엠, 대표: 김사장, 연락처 |
| `02-555-1234 홍길동대표` | 연락처, 대표: 홍길동 |
| `(주)세넷코리아 내일 2시 통화` | 회사명, 콜백: 내일 2시 |
| `네일샵 예약 오후 3시` | 회사: 네일샵, 콜백: 오후 3시 |

## 🗂️ 프리셋 종류

| 프리셋 | 단계 |
|--------|------|
| 영업용 | 접수 → 1차콜 → 2차콜 → 계약 → 완료 |
| 사무직용 | 접수 → 처리중 → 처리완료 |
| 사장님용 | 예약접수 → 방문예정 → 완료 |
| 단순관리 | 할일 → 완료 |
| 프리랜서 | 문의 → 진행 → 완료 |

---

## 📅 작업 로그

### 2025-01-13
- Sticki v1.0 베이스캠프 생성
- 스마트 파싱 로직 구현
- 민트 컬러 테마 적용
- 드래그앤드롭 + 상태메모 도장 스타일

### 이전 (콜보드 시절)
- 날짜 기반 구조 설계
- 프리셋 시스템 설계
- 포스트잇 컨셉 UI

---

**Made with Claude AI** 🤖
