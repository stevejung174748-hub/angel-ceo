# 스토리(경험글) 등록 방법

새 글은 **HTML 본문**을 주시면 `stories/슬러그/index.html`에 반영하고, 목록·사이트맵에 등록합니다.

## 폴더 구조

```
stories/
  index.html              ← 목록 (카드 수동 추가)
  example-story/
    index.html            ← 글 1페이지 (복사 템플릿)
  your-new-slug/
    index.html
assets/css/
  story.css               ← 본문 전용 스타일 (건드리지 않아도 됨)
```

## 새 글 추가 (직접 할 때)

1. `stories/example-story/` 폴더를 복사 → `stories/글-slug/` (영문·숫자·하이픈)
2. `index.html` 수정:
   - `<title>`, `<meta description>`, `<link canonical>`
   - `.story-header` 안 제목·요약·날짜·태그
   - **`.story-content` 안에만** 본문 HTML 붙여넣기
3. `stories/index.html`의 `.story-grid`에 카드 `<a class="story-card">` 추가
4. `sitemap.xml`에 URL 추가
5. `git push`

## 본문 HTML 규칙

- `.story-content` **안에만** 넣기 (헤더·푸터·nav 제외)
- 사용 가능 태그: `p`, `h2`, `h3`, `ul`, `ol`, `li`, `blockquote`, `strong`, `em`, `a`, `img`, `figure`, `figcaption`, `hr`, `table`, `div.story-callout`
- 인라인 `style`은 가급적 사용하지 않기

## CSS

- 공통: `style.css`
- 스토리: `story.css` (목록·카드·본문 타이포)

클래스 예시:

```html
<div class="story-callout">
  <strong>팁</strong>
  강조 박스 문단
</div>
```

## 콘텐츠 레지스트리

| # | 슬러그 | 타겟 키워드 | 앵글 | 백링크 |
|---|--------|------------|------|--------|
| 0 | `example-story` | 제주 룸싸롱 첫 방문 | 경험 서사형 (템플릿) | 내부 링크 |
| 1 | `haeundae-room-salon-mood-types` | 해운대 룸싸롱 분위기 | 비교형 — 분위기 타입 3가지 비교 | hd-login.co.kr |
| 2 | `haeundae-goguryeo-faq` | 해운대 고구려 | FAQ 모음형 — 처음 검색 시 자주 묻는 질문 10가지 | hd-goguryeo.com |
| 3 | `haeundae-hoppa-night-course` | 해운대 호빠 여성 코스 | 동선 코스형 — 식사→바→호빠→귀가 타임라인 | busanhoppa.kr |

## URL 목록

| 슬러그 | URL |
|--------|-----|
| `example-story` | https://angel-ceo.pages.dev/stories/example-story/ |
| `haeundae-room-salon-mood-types` | https://angel-ceo.pages.dev/stories/haeundae-room-salon-mood-types/ |
| `haeundae-goguryeo-faq` | https://angel-ceo.pages.dev/stories/haeundae-goguryeo-faq/ |
| `haeundae-hoppa-night-course` | https://angel-ceo.pages.dev/stories/haeundae-hoppa-night-course/ |
| 목록 | https://angel-ceo.pages.dev/stories/ |

## 에이전트에게 요청할 때

다음 정보와 함께 **본문 HTML**을 보내 주세요.

- 제목, 한 줄 요약, 날짜 (YYYY-MM-DD)
- 태그 (예: 제주, 룸싸롱, 초보)
- 슬러그 (폴더명)
- (선택) 연결할 큐레이션 페이지 경로
