# 대담쌤 포트폴리오 웹사이트

AI & 코딩 교육 전문가 문수희 강사의 포트폴리오 웹사이트입니다.

---

## 📁 파일 구조

```
website/
├── index.html          # 메인 페이지
├── 404.html            # 404 에러 페이지
├── favicon.svg         # 파비콘 (SVG)
├── manifest.json       # PWA 매니페스트
├── robots.txt          # 검색엔진 크롤러 설정
├── sitemap.xml         # 사이트맵
├── .htaccess           # Apache 서버 설정
├── netlify.toml        # Netlify 배포 설정
├── vercel.json         # Vercel 배포 설정
└── README.md           # 이 파일
```

---

## 🚀 배포 방법

### 방법 1: Netlify (추천 - 무료)

1. [Netlify](https://www.netlify.com) 회원가입
2. "Add new site" → "Deploy manually"
3. website 폴더를 드래그 앤 드롭
4. 자동 배포 완료!
5. 커스텀 도메인 연결: Site settings → Domain management

### 방법 2: Vercel (무료)

1. [Vercel](https://vercel.com) 회원가입
2. "Add New" → "Project"
3. website 폴더 업로드
4. 자동 배포 완료!
5. 커스텀 도메인: Settings → Domains

### 방법 3: GitHub Pages (무료)

1. GitHub 저장소 생성
2. website 폴더 내용을 저장소에 업로드
3. Settings → Pages → Source: main branch
4. 커스텀 도메인: Settings → Pages → Custom domain

### 방법 4: 일반 웹호스팅 (카페24, 가비아 등)

1. FTP 클라이언트 (FileZilla 등) 설치
2. 호스팅 FTP 정보로 접속
3. public_html 또는 www 폴더에 모든 파일 업로드
4. 도메인 연결 완료

---

## 🔧 커스텀 도메인 연결

### DNS 설정 (도메인 관리 페이지에서)

**A 레코드 (Netlify 예시)**
```
Type: A
Name: @
Value: 75.2.60.5
```

**CNAME 레코드 (www 서브도메인)**
```
Type: CNAME
Name: www
Value: your-site.netlify.app
```

### SSL 인증서
- Netlify, Vercel: 자동으로 Let's Encrypt SSL 제공
- 일반 호스팅: Let's Encrypt 무료 SSL 또는 유료 SSL 구매

---

## ⚙️ 설정 변경

### 1. 도메인 변경 시

`robots.txt`와 `sitemap.xml`에서 `yourdomain.com`을 실제 도메인으로 변경:

```
Sitemap: https://실제도메인.com/sitemap.xml
```

```xml
<loc>https://실제도메인.com/</loc>
```

### 2. 관리자 비밀번호 변경

`index.html` 파일에서 아래 부분을 찾아 변경:

```javascript
var ADMIN_PASSWORD = 'aive2025'; // 원하는 비밀번호로 변경
```

### 3. 연락처 정보 변경

`index.html` 파일에서 이메일, 전화번호, 주소 등을 검색하여 수정

---

## 📱 기능 안내

### 메인 기능
- ✅ 반응형 디자인 (모바일/태블릿/데스크탑)
- ✅ 부드러운 스크롤 애니메이션
- ✅ 포트폴리오 필터링
- ✅ 문의 폼 제출

### 관리자 기능
- ✅ 비밀번호 로그인
- ✅ 문의 내역 조회
- ✅ 읽음/미읽음 상태 관리
- ✅ 문의 삭제
- ✅ CSV 내보내기
- ✅ 필터링 (전체/미확인/학교/기업/개인)

### 데이터 저장
- 문의 데이터는 브라우저의 localStorage에 저장됩니다
- 서버 데이터베이스가 필요한 경우 백엔드 개발이 필요합니다

---

## 🔍 SEO 최적화

이미 적용된 항목:
- ✅ 시맨틱 HTML 구조
- ✅ 메타 태그 (title, description)
- ✅ Open Graph 태그 추가 권장
- ✅ robots.txt
- ✅ sitemap.xml

### 추가 권장 사항

`index.html`의 `<head>` 섹션에 추가:

```html
<meta name="description" content="15년 IT 전문가가 가르치는 실전 AI & 코딩 교육. 야놀자, NHN 출신 DBA의 맞춤형 교육 프로그램.">
<meta name="keywords" content="AI교육, 코딩교육, ChatGPT, 로봇교육, FLL, 기업교육">
<meta name="author" content="대담쌤 문수희">

<!-- Open Graph -->
<meta property="og:title" content="대담쌤 문수희 | AI & 코딩 교육 전문가">
<meta property="og:description" content="15년 IT 전문가가 가르치는 실전 AI & 코딩 교육">
<meta property="og:type" content="website">
<meta property="og:url" content="https://yourdomain.com">
<meta property="og:image" content="https://yourdomain.com/og-image.png">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="대담쌤 문수희 | AI & 코딩 교육 전문가">
<meta name="twitter:description" content="15년 IT 전문가가 가르치는 실전 AI & 코딩 교육">
```

---

## 📞 문의

- 이메일: aive.msh@gmail.com
- 전화: 010-2164-2076

---

© 2025 대담쌤 문수희 | AI & 코딩 교육 전문가
