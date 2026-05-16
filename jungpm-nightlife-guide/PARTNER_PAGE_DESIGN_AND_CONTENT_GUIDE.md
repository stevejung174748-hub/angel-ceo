# 신규 업체(파트너) 페이지 — 디자인 패턴 & 콘텐츠 가이드

차후 업체가 추가될 때 이 문서를 기준으로 페이지를 만들면 **JungPM 허브 사이트의 아이덴티티·링크 구조·SEO 규칙**을 그대로 유지할 수 있습니다.

**프로덕션 도메인:** `https://joungsy.ivyro.net/`  
**제휴·광고 문의 (텔레그램):** [`https://t.me/Jungpm`](https://t.me/Jungpm) — **홈 `index.html` CTA에만** 사용 (업소 상세·지역 허브에는 넣지 않음)  
**공통 스타일:** `assets/css/style.css` (디자인 토큰 및 컴포넌트는 여기만 확장)

### 외부 링크 2종 (혼동 금지)

| 용도 | URL | 앵커(키워드) | 위치 |
|------|-----|--------------|------|
| 업체 공식 사이트(백링크) | 페이지별 1개 | 아래 표 참고 | 상세 페이지 본문 1곳 |
| 허브 제휴 문의 | `https://t.me/Jungpm` | 버튼 문구(키워드 아님) | **홈 CTA만** |

| 상세 경로 | 공식 URL | 앵커 텍스트 |
|-----------|----------|-------------|
| `jeju/room-salon/` | https://jeju-room.com/ | 제주도 룸싸롱 |
| `jeju/nightlife/` | https://jejuroom.io.kr/ | 제주도 유흥 |
| `busan/haeundae-hoppa/` | https://busanhoppa.kr/ | 해운대 호빠 |
| `songpa/karaoke/` | https://송파노래방.com/ | 송파 노래방 |
| `gangnam/hoppa/` | https://gangnamhoppa.com/ | 강남 호빠 |

---

## 1. 브랜드 & 톤 (사이트 아이덴티티)

| 요소 | 규칙 |
|------|------|
| 허브 이름 | 상단 로고·카피에서 **「JungPM이 추천하는 유흥」** 유지 |
| 포지셔닝 | **정보형 가이드** — 예약 대행·중개가 아님을 명시 |
| 문체 | 과장·단정적 보장 표현 지양. 「기준 정리」「방문 전 확인」「공식 안내와 대조」 중심 |
| 푸터 브랜드 | **BLINDUP** 워드마크 + 면책 + `© 2026 blindup. All rights reserved.` (전 페이지 동일 블록) |
| 접근성 | `lang="ko"`, 버튼 `aria-*`, 의미 있는 `alt`, 섹션 제목 계층(`h1` → `h2`) 유지 |

새 업체 페이지도 **헤더·푸터 HTML 구조**는 기존 상세 페이지와 동일하게 복제한 뒤 경로·문구만 바꿉니다.

---

## 2. 페이지 유형 3가지

### A. 홈 (`index.html`)

- 히어로 + JungPM 소개 + **내부 링크만** 연결된 파트너 배너 그리드
- `canonical`: `https://joungsy.ivyro.net/`
- Google Search Console **HTML 태그 검증**이 있으면 이 파일 `<head>`에만 유지

### B. 지역 허브 (`area/index.html`)

- 지역별로 `partner-banner` 카드 그룹
- 배너 `href`는 **항상 사이트 내부 상세 URL** (외부 도메인 직링크 금지)
- 동일 배너 이미지·카피는 홈과 맞출 것 (일관성)

### C. 업소 소개 상세 (예: `jeju/room-salon/index.html`)

- 메인 배너에서 들어오는 **단일 허브 내 랜딩**
- 구조는 아래 「상세 페이지 표준 블록」 순서를 따름
- **외부 공식 사이트 링크는 페이지당 1개**만 (보통 「가격 및 예약 기준」 근처의 키워드 앵커)

---

## 3. 디자인 시스템 요약 (`:root` 토큰)

색·타이포·반경은 `style.css` 상단 변수와 통일합니다.

- 배경: `--color-bg`, `--color-bg-soft`, 카드 `--color-bg-card`
- 텍스트: `--color-text`, 보조 `--color-muted`, `--color-muted-2`
- 악센트(골드): `--color-gold`, `--color-gold-soft`, `--color-line-gold`
- 최대 폭: `--container` (1180px), 본문 좁은 폭: `.narrow`
- 본문 폰트: `--font-body` (Pretendard 등 시스템 스택)
- 새 컴포넌트가 필요하면 **기존 클래스 패턴**(카드 그리드, `section-sm`, `page-hero`)을 재사용

---

## 4. 상세 페이지 표준 블록 (순서 고정)

`main`에 `class="article venue-page"` 사용. 아래 순서를 유지합니다.

1. **`page-hero venue-hero`**  
   - `partner-hero-badge`: 「업소 소개 페이지」  
   - `eyebrow`: `지역 · 업종 · 업체별 구분`(짧은 라벨)  
   - `h1`: 페이지 제목  
   - `lead`: JungPM 관점 한 줄 + **내부 페이지**임 + 공식 링크는 아래 섹션에서만 연다는 안내

2. **`venue-intro section-sm`**  
   - `eyebrow`: `Venue Introduction`  
   - `h2` + 여러 `p`: 업체·카테고리 맥락, 이용자가 알아야 할 판단 기준 (정보형)

3. **`article-figure venue-figure`**  
   - 배너와 동일 계열 이미지 권장 (시각 일관성)  
   - 권장 비율 참고: `width="820" height="460"`, `loading="lazy"`  
   - `figcaption`으로 이미지 설명

4. **`venue-info section-sm`**  
   - `venue-info-grid` 안에 `venue-info-card` 9칸 패턴 유지 가능:  
     업체명, 지역, 업종, 주소, 영업·상담, 연락처, 가격 기준, 주요 테마, 대표 키워드  
   - 공개 가능한 범위만 기입; 미공개 시 「상세 주소 미공개 · ○○ 기준 안내」처럼 정직하게  
   - `venue-note-box`: 예약 전 한 줄 체크리스트

5. **`article section-sm` → `article-body`**  
   - 소제목 예시(업종에 맞게 조정):  
     공간·서비스 선택 기준, 가격 및 예약 기준(여기에 **외부 링크 1개**), 위치·동선, 예약 전 준비 정보, JungPM 추천 기준  
   - **FAQ 블록은 상세 페이지에 넣지 않음** (기존 사이트 정책)

6. **`related-links`**  
   - 같은 지역 다른 파트너, `지역별 업소 추천`, `홈` 등 **상대 경로 내부 링크**만

각 섹션은 기존 `jeju/room-salon/index.html` 를 **마스터 템플릿**으로 삼습니다.

---

## 5. 링크 & SEO 규칙

| 구분 | 규칙 |
|------|------|
| 사이트 내부 | **상대 경로만** (`./` `../` `../../` 등). 도메인 하드코딩 금지 |
| 상세 → 공식 사이트 | **1페이지 1링크**, 앵커는 자연스러운 키워드 문구, `target="_blank" rel="noopener"` |
| `rel="nofollow"` | 외부 백링크에 **사용하지 않음** (현행 정책) |
| `canonical` | 절대 URL: `https://joungsy.ivyro.net/` + 경로 슬래시까지 일치 |
| `meta robots` | 일반 페이지: `index, follow` |
| `title` / `description` | 업체명 + 가격·위치·예약 등 사용자 검색 의도 반영, 중복 최소화 |

**신규 상세 페이지 추가 시 필수 후속 작업**

- `sitemap.xml`에 `<loc>` 항목 추가  
- 홈·`area/`에 **배너 카드** 추가 (동일 상대 경로로 상세 진입)  
- `related-links`를 다른 페이지들과 상호 참조 가능하면 1~2개 추가

---

## 6. 에셋 규칙

- 배너 이미지: `assets/images/`  
  - 파일명 규칙 예: `banner-{지역}-{슬러그}.png` (기존 5종과 패턴 맞춤)  
  - 홈·area 배너 권장: `1200 × 380` 전후  
- 상세 본문 figure: 배너와 같은 이미지 재사용 가능 (파일 하나로 통일하면 유지보수 쉬움)  
- `alt`: 장식이 아니라 **콘텐츠 설명**(브랜드·분위기·용도)

---

## 7. URL·폴더 네이밍

- 권장: `{지역}/{서비스-슬러그}/index.html`  
  예: `busan/haeundae-hoppa/index.html`  
- 슬러그는 영문·하이픈, 짧고 안정적으로 (이후 URL 변경은 SEO에 불리)

---

## 8. 신규 업체 추가 체크리스트

- [ ] 폴더·`index.html` 생성 (기존 상세 1개 복제 후 교체)
- [ ] `title`, `description`, `canonical`, `h1` 일치 검토
- [ ] 헤더 네비·로고 링크 깊이에 맞는 `../../` 경로 수정
- [ ] 배너 이미지 추가 및 `partner-banner`(홈·area) 연결
- [ ] 「가격 및 예약 기준」에 외부 링크 **1개만**
- [ ] `venue-info` 카드·`venue-note-box`·본문 소제목 업데이트
- [ ] `related-links` 내부 링크 정리
- [ ] 푸터 블록 그대로 유지 (BLINDUP / blindup 카피라이트)
- [ ] `sitemap.xml` 반영
- [ ] 로컬에서 모바일 메뉴·이미지 깨짐 확인 후 FTP 반영

---

## 9. 참고: 최소 HTML 골격 (상세 페이지)

아래는 **구조만** 요약한 것입니다. 실제 클래스·마크업은 `jeju/room-salon/index.html` 전체를 복사하는 것을 권장합니다.

```html
<!doctype html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="robots" content="index, follow">
  <title><!-- 업체명·검색 의도 --></title>
  <meta name="description" content="<!-- 1~2문장 요약 -->">
  <link rel="canonical" href="https://joungsy.ivyro.net/<!-- 경로/ -->">
  <link rel="stylesheet" href="../../assets/css/style.css">
</head>
<body>
  <header class="site-header"><!-- 로고 → ../../index.html, nav 동일 패턴 --></header>
  <main class="article venue-page">
    <section class="page-hero venue-hero">...</section>
    <section class="venue-intro section-sm">...</section>
    <figure class="article-figure venue-figure">...</figure>
    <section class="venue-info section-sm">...</section>
    <section class="article section-sm">
      <div class="narrow">
        <div class="article-body">
          <!-- h2 + p 반복, 외부 링크 1곳 -->
          <div class="related-links">...</div>
        </div>
      </div>
    </section>
  </main>
  <footer class="site-footer"><!-- BLINDUP 푸터 고정 블록 --></footer>
  <script src="../../assets/js/main.js" defer></script>
</body>
</html>
```

**깊이 주의:** 상세가 `깊이2`(예: `jeju/foo/`)면 CSS·JS·이미지는 `../../assets/...`, 깊이3이면 `../../../assets/...` 로 조정합니다.

---

## 10. 문서 관리

- 이 가이드는 **실제 코드와 충돌할 때 코드 우선**으로 두고, 정책이 바뀌면 본 문서를 함께 수정하세요.
- 새로운 공통 컴포넌트를 도입하면 `style.css`의 섹션 주석과 이 문서 「디자인 시스템」 항목을 짧게 보강하면 이후 업체 추가가 수월합니다.
