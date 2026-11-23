# AI 논문 리뷰 — GitHub Pages

논문 리뷰 사이트 모음
프로필 링크 하나로 리뷰한 논문들을 모아볼 수 있습니다.

---

## 🚀 배포 방법 (GitHub Pages)

1. GitHub에서 새 레포지토리를 만듭니다 (예: `paper-reviews`)
2. 이 세 파일을 레포지토리에 올립니다
3. **Settings → Pages → Source: Deploy from a branch → Branch: main / (root)** 선택
4. 약 1분 후 `https://아이디.github.io/paper-reviews` 로 접속 가능

인스타그램 프로필 편집 → **링크 추가** → 위 URL 입력

---

## 📊 Google Analytics 4 설정 (방문자 분석)

1. [analytics.google.com](https://analytics.google.com) 접속 → 계정 생성
2. 새 속성 → 웹 플랫폼 선택 → 측정 ID 발급 (`G-XXXXXXXXXX` 형태)
3. `index.html` 의 두 곳에 있는 `YOUR_GA4_ID` 를 발급받은 ID로 교체
4. GitHub에 푸시하면 24시간 내 데이터 수집 시작

관리자 페이지(`/admin.html`)에서 GA4 대시보드로 바로 연결됩니다.

---

## 📄 새 논문 추가 방법

`index.html` 파일을 열고 `PAPERS` 배열에 항목을 추가합니다:

```js
const PAPERS = [
  // 기존 논문들...
  {
    id: 'new-paper-id',          // 영문 소문자, 하이픈
    emoji: '✨',                  // 대표 이모지
    title: 'NewPaperTitle',      // 논문 제목
    subtitle: '한국어 부제',       // 한 줄 한국어 설명
    year: '2025',
    tags: ['Topic1', 'Topic2'],  // 태그 (최대 3개 권장)
    venue: 'arXiv',              // 학회/저널 이름
    desc: '논문에 대한 2-3문장 설명.',
    arxiv: 'https://arxiv.org/abs/XXXX.XXXXX',
    reels: 'https://www.instagram.com/reel/XXXXXXXXX'
  }
];
```

`admin.html` 의 `PAPERS` 배열도 동일하게 추가해 주세요 (클릭 통계용).

---

## 🔒 어드민 페이지

- 접속: `사이트주소/admin.html`
- 기본 비밀번호: **`miplab2024`** ← 반드시 변경하세요
- 변경 위치: `admin.html` 의 `const ADMIN_PASSWORD = 'miplab2024';`

어드민 페이지에서 확인할 수 있는 항목:
- 논문별 arXiv / 릴스 클릭 수 (현재 브라우저 기준)
- Google Analytics 4 대시보드 바로가기 (전체 방문자)

---

## 파일 구조

```
├── index.html   ← 메인 페이지 (논문 카드 목록)
├── admin.html   ← 관리자 분석 대시보드
└── README.md    ← 이 파일
```
