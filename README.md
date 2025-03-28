# Couseplate Frontend

## 기술 스택

- **Expo SDK**: 52.0.40
- **React Native**: 0.76.7
- **React**: 18.3.1
- **Expo Router**: 4.0.19

## 프로젝트 디렉토리 구조
```
couseplate-frontend/
├── app/
│   ├── login/              ← 로그인 페이지
│   │   └── index.js
│   ├── signup/             ← 회원가입 페이지
│   │   └── index.js
│   └── _layout.js          ← 전역 레이아웃 및 헤더 설정
│
├── components/             ← 재사용 가능한 UI 컴포넌트
│   ├── CustomInput.js
│   └── PrimaryButton.js
│
├── styles/                 ← 공통 스타일
│   └── common.js
│
├── assets/
│   └── logo/
│       ├── logo.png
```
2025-03-25

✅ 구현된 주요 화면
🔐 회원가입 화면
이름, 전화번호, 비밀번호, 비밀번호 확인 입력

전화번호 인증 요청 버튼 (→ 서버 API 연동 예정)

입력값 유효성 검사 + 인증 완료 시에만 완료 버튼 활성화

입력 상태에 따라 완료 버튼이 회색으로 비활성화됨


🔑 로그인 화면
전화번호 + 비밀번호 입력

로그인 버튼 클릭 시 서버에 요청 예정

회원가입 링크 제공 (/signup으로 이동)


🧩 재사용 컴포넌트
CustomInput.js: 스타일이 통일된 입력 필드 컴포넌트

PrimaryButton.js: 버튼 기본 스타일 적용 및 disabled 상태 지원


🎨 공통 스타일 관리
모든 화면에서 사용하는 레이아웃, 입력, 버튼 스타일은 styles/common.js에 통합

flex, row, title, verifyButton 등도 여기에 정의하여 유지보수 효율화


⚙️ 개발 중 기능 (To-Do)
 전화번호 인증 API 연동 (/send-verification)

 로그인 API 연동 및 에러 처리

 자동 로그인 (토큰 저장)

 음식 취향 설문 페이지 구성

 홈화면 및 추천 결과 UI
 
### 실행
npx expo start

### 참고사항
공통 스타일은 styles/common.js에서 수정

입력 필드나 버튼은 CustomInput, PrimaryButton 컴포넌트를 사용하는 것이 원칙

새 페이지를 만들 때는 app/페이지이름/index.js로 만들고, router.push('/페이지이름')으로 이동
