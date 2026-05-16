# Angel CEO — 작업 기록

> 프로젝트 작업 요약. Git 계정·이메일 등 개인 정보는 `GIT_ACCOUNTS.local.md` 참고.

---

## 사이트 데이터 위치 (중요)

| 구분 | 경로 / URL |
|------|------------|
| **로컬 소스 (편집하는 폴더)** | `F:\workspace\seo page templet\angel-ceo` |
| **GitHub 레포** | https://github.com/stevejung174748-hub/angel-ceo |
| **라이브 사이트** | https://angel-ceo.pages.dev |
| **Cloudflare 프로젝트명** | `angel-ceo` |

로컬 폴더 구조 (레포 루트 = 사이트 루트):

```
angel-ceo/                       ← Git 루트 & Angel CEO 사이트 전체
├── index.html                   ← 홈
├── area/
├── jeju/room-salon/  jeju/nightlife/
├── busan/haeundae-hoppa/
├── songpa/karaoke/
├── gangnam/hoppa/
├── assets/css/  assets/js/  assets/images/
├── sitemap.xml  robots.txt
├── README.md
├── GIT_ACCOUNTS.example.md      ← Git 템플릿 (공개 OK)
├── GIT_ACCOUNTS.local.md        ← 개인 계정 메모 (Git 제외)
└── WORK_LOG.md                  ← 이 파일
```

**참고:** 예전 `angelie-night/` 폴더는 없어졌고, 내용은 **위 루트로 합쳐짐**.

### JungPM (이 레포·GitHub와 무관)

| 구분 | 내용 |
|------|------|
| 로컬만 | `..\jungpm-nightlife-guide\` (FTP용, Git 없음) |
| 배포 | **FTP → 별도 서버** (예: joungsy.ivyro.net) |
| GitHub `angel-ceo` | **올리지 않음** — `.gitignore`로 제외 |

JungPM 수정 후에는 FTP로만 업로드. `git add .` 할 때 JungPM 폴더가 포함되지 않는지 확인.

---

## 2026-05-17 작업 요약

### 브랜드·레포
- Angelie Night → **Angel CEO** (`angel-ceo`) 리브랜딩
- Git 레포: **angel-ceo만** (JungPM 제외), 사이트 파일은 **레포 루트**
- 이미지 파일명: `angel-banner-*`, `hero-angel*`

### Git / 보안
- HTTPS + `credential.useHttpPath` (계정별 자격 증명 분리)
- `GIT_ACCOUNTS.local.md` 로컬 전용, `.gitignore` 강화
- 커밋 작성자: GitHub noreply 이메일로 히스토리 정리 후 force push

### 배포
- **Cloudflare Pages** 연동 (GitHub `main` → 자동 배포)
- Build: Framework **None**, output **`/`**
- URL: https://angel-ceo.pages.dev

### SEO / GSC
- `sitemap.xml`, `robots.txt`, 전 페이지 `canonical` → `angel-ceo.pages.dev`
- `index.html`에 Google Search Console 인증 메타 태그 추가
- GSC 속성 등록·소유권 확인 완료, 사이트맵 `sitemap.xml` 제출
- URL 수동 색인 요청은 GSC 일일 할당량으로 일부만 가능 → 사이트맵으로 나머지 크롤 대기

### 콘텐츠 (이전 세션 포함)
- 5개 파트너 상세 페이지 보강 (요금표, 시간, 체크리스트 등)
- 해운대 호빠 연락처: **010-5037-6142**

### 파트너 백링크 (상세당 1개)
| 경로 | 앵커 |
|------|------|
| `/jeju/room-salon/` | 제주도 룸싸롱 |
| `/jeju/nightlife/` | 제주도 유흥 |
| `/busan/haeundae-hoppa/` | 해운대 호빠 |
| `/songpa/karaoke/` | 송파 노래방 |
| `/gangnam/hoppa/` | 강남 호빠 |

- 홈 제휴 문의만: https://t.me/Jungpm

---

## 다음에 할 일

- [ ] GSC **페이지** 보고서로 색인 진행 확인 (며칠~2주)
- [ ] 커스텀 도메인 연결 시: Cloudflare Custom domains + `sitemap`/`canonical` URL 일괄 변경 + GSC 새 속성
- [ ] `YOUR-ANGEL-CEO-DOMAIN` → 실제 도메인으로 교체 (현재는 `angel-ceo.pages.dev` 사용 중)

---

## 자주 쓰는 명령

```powershell
cd "F:\workspace\seo page templet\angel-ceo"
python -m http.server 5500
git add .
git commit -m "메시지"
git push
```

---

*마지막 업데이트: 2026-05-17*
