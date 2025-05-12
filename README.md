# O2 - 위치 기반 중고거래 플랫폼

## 프로젝트 개요
O2는 Flutter와 네이버 지도 API를 활용하여 개발된 **위치 기반 중고거래 플랫폼**입니다.  
사용자의 위치 정보를 기반으로, 근처에서 중고 물품을 거래할 수 있는 환경을 제공합니다.  
실시간 채팅, 푸시 알림, 다양한 소셜 로그인, 이미지 업로드 등 실제 서비스에 가까운 기능을 구현했으며,  
클린 아키텍처 패턴을 적용해 확장성과 유지보수성을 높였습니다.

- **프로젝트 기간:** 2025.01.23 ~ 2025.02.25
- **인원:** 4명
- **주요 역할:**  
  - 팀 개발 리드 및 일정 관리  
  - OAuth(구글, 페이스북, 카카오, 네이버) 로그인  
  - FCM 기반 푸시 알림  
  - 네이버 지도 기반 위치 서비스  

---

## 주요 기능
- **위치 기반 중고거래 서비스 (네이버 지도 API 활용)**
  - 내 주변 중고 물품 리스트 제공
  - 지도에서 거래 위치 확인 및 검색
  - 거래 희망 위치 저장 및 경로 안내
- **실시간 채팅**
  - 거래 상대와 1:1 채팅
  - 채팅 내 푸시 알림
- **소셜 로그인**
  - 구글, 페이스북, 카카오, 네이버 로그인 연동
  - 사용자 프로필 관리
- **알림 서비스**
  - Firebase Cloud Messaging을 활용한 푸시 알림
  - 거래 관련 알림 설정

---

## 기술 스택
- **Framework**: Flutter
- **상태관리**: flutter_riverpod
- **주요 패키지**:
  - go_router: 화면 간 라우팅 및 네비게이션 관리
  - flutter_naver_map: 네이버 지도 연동
  - firebase_auth, google_sign_in: Firebase 인증 (이메일, 소셜 로그인)
  - firebase_messaging, flutter_local_notifications: 푸시 알림
  - flutter_image_compress: 이미지 압축
  - shared_preferences: 로컬 데이터 저장

---

## 프로젝트 구조
```
lib/
├── core/           # 핵심 유틸리티 및 서비스
│   ├── constants/      # 앱 상수
│   ├── services/       # 핵심 서비스 (FCM, 권한 등)
│   ├── theme/          # 앱 테마 및 스타일 가이드
│   └── utils/          # 유틸리티 함수
├── data/           # 데이터 레이어
│   ├── models/         # 데이터 모델
│   ├── repositories/   # 데이터 저장소
│   └── datasources/    # 데이터 소스
├── domain/         # 비즈니스 로직
│   ├── entities/       # 비즈니스 엔티티
│   ├── repositories/   # 리포지토리 인터페이스
│   └── usecases/       # 유스케이스
└── presentation/   # UI 레이어
    ├── screens/        # 화면
    ├── widgets/        # 재사용 가능한 위젯
    └── providers/      # 상태 관리
```

---

## 아키텍처
이 프로젝트는 클린 아키텍처 패턴을 따릅니다:
- **Presentation Layer**: UI 컴포넌트와 상태 관리
- **Domain Layer**: 비즈니스 로직과 엔티티
- **Data Layer**: 데이터 처리와 저장소
- **Core**: 공통 유틸리티와 서비스

---

## 디자인 시스템
- **테마 시스템**: Material Design 3 기반의 커스텀 테마 적용
  - 앱 전체에 일관된 색상(Color) 팔레트 적용 (주색, 배경, 텍스트, 구분선 등)
  - 다양한 텍스트 스타일(타이포그래피) 계층 구조 제공 (제목, 본문, 라벨 등)
  - 버튼, 카드, 입력창 등 주요 컴포넌트의 스타일 일관성 유지
  - 라운드, 마진, 패딩 등 UI 요소의 공통 스타일(AppStyles)로 관리

---

## 주요 화면
- 로그인 화면: Firebase 인증 (이메일 및 소셜 로그인)
- 홈 화면: 내 주변 중고 물품 리스트 표시
- 검색 화면: 거래 위치 및 물품 검색
- 채팅 화면: 실시간 1:1 채팅
- 프로필 화면: 사용자 정보 및 설정, 물품 관리
- 알림 설정 화면: 푸시 알림 관리

---

## 트러블슈팅
- 로그인/인증 관련 문제는 별도 PPT로 케이스별 정리  
  (예: 네이버 OIDC 미지원, FCM 토큰 처리 등)

---

## 프로젝트 회고

- 1,2차 프로젝트 경험을 바탕으로 개발 효율 및 문제 해결 능력 향상
- 네이버 지도 API 등 다양한 외부 패키지 활용 경험
- 클린 아키텍처 적용으로 코드 관리 용이
- 팀원들과의 협업 및 일정 관리 경험
- 마지막 프로젝트로 팀원 모두가 익숙해져 높은 완성도 달성

---

## 프로젝트 캡쳐 이미지

<img src="https://github.com/user-attachments/assets/3f545ecd-1f68-4c66-8b76-c16538eac282" width="20%">
<img src="https://github.com/user-attachments/assets/d0b2b68d-b172-4c12-80ab-3a9fab48cca2" width="20%">
<img src="https://github.com/user-attachments/assets/62f6838a-27f7-4253-a595-31afb03c5c94" width="20%">
<img src="https://github.com/user-attachments/assets/6ccf36ed-0e04-428b-a2ad-86460dc2e0d7" width="20%">
<img src="https://github.com/user-attachments/assets/6dffb3f8-860c-49fa-b72e-66c0cd58e97a" width="20%">
<img src="https://github.com/user-attachments/assets/6f45891b-fcee-4678-bfe9-8631062b84eb" width="20%">
<img src="https://github.com/user-attachments/assets/2a9edf0a-11c8-4cc2-a9de-6825f8ce74b8" width="20%">
<img src="https://github.com/user-attachments/assets/29f3fcb8-4b05-44e1-b32a-8df75a859ad5" width="20%">

---

## 성과

<img src="https://github.com/user-attachments/assets/26f3c08f-289a-43ec-a300-37a7f8fffed1" width="30%">

