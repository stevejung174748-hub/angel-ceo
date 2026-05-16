# Angelie Night — 이미지 교체 & AI 생성 가이드

파일명만 맞추면 HTML·CSS 수정 없이 교체 가능합니다.  
JungPM 사이트와 **구도·색감·소품**을 다르게 — Angelie만의 **로즈·플럼·라일락** 큐레이션 무드.

---

## 사이트 공통 비주얼 방향

**브랜드:** Angelie Night — 밤문화 정보 허브 (고급·차분·큐레이션)

**키워드:** `rose quartz` · `plum wine` · `soft lilac` · `midnight lounge` · `editorial` · `cinematic`

### 색감

| 구분 | 가이드 |
|------|--------|
| 배경 | 딥 플럼·와인·차콜 (`#0f0a11` 계열) |
| 포인트 | 로즈골드·더스티 핑크·은은한 라일락 |
| 피하기 | JungPM식 골드·네이비·주황 네온·원색 |

### 조명

- 저조도, 부드러운 림라이트, 보케(아웃포커스 조명)
- 과한 플래시·낮은 현장 스냅 느낌 지양

### 구도 (배너·히어로 공통)

- 왼쪽 **40~50%**는 어둡게 (텍스트 오버레이 영역) — 피사체는 **중앙~우측**
- 이미지 안에 **글자·로고·워터마크 넣지 않음** (HTML 오버레이 사용)
- 인물: 실제 연예인·유명인 닮은 얼굴 금지 → **실루엣·뒷모습·손·소품** 위주 권장

### 스타일 참고

- 프리미엄 라운지 브로슈어, 호텔 바, 에디토리얼 패션 화보
- 과도한 노출·선정적 포즈·미성년 연상 소품 금지

### 형식

| 용도 | 권장 크기 |
|------|-----------|
| 배너 | 1200×380 (약 3.2:1) |
| 히어로 배경 | 1920×1080+ (16:9) |
| 히어로 대표 | 1280×960 (4:3) |
| 파일 형식 | PNG 또는 WebP |

---

## 이미지 목록 요약

| # | 파일명 | 용도 |
|---|--------|------|
| 1 | `hero-angelie-bg.png` | 홈 히어로 배경 |
| 2 | `hero-angelie.png` | 홈 히어로 우측 카드 |
| 3 | `angelie-banner-jeju-room.png` | 제주 룸싸롱 신호등 |
| 4 | `angelie-banner-jeju-nightlife.png` | 제주 유흥 미술관 |
| 5 | `angelie-banner-haeundae-hoppa.png` | 해운대 호빠 |
| 6 | `angelie-banner-songpa-karaoke.png` | 송파 노래방·가라오케 |
| 7 | `angelie-banner-gangnam-hoppa.png` | 강남 호빠 |

저장 위치: `assets/images/`

---

## 1. hero-angelie-bg.png

| 항목 | 내용 |
|------|------|
| **용도** | 홈 히어로 섹션 전체 배경 (CSS `cover`, 우측 위주 노출) |
| **크기** | 1920×1080 이상 (16:9) |

### 어떤 이미지?

밤의 도시 또는 추상적 라운지 분위기. **인물 없이** 공간·빛만.  
왼쪽은 거의 어둡게, 오른쪽에 은은한 빛 번짐.

### 생성 프롬프트 (한글)

```
딥 플럼과 와인 톤의 프리미엄 나이트 라운지 배경, 부드러운 로즈골드와 라일락 조명,
유리와 벨벳 질감, 시네마틱 보케, 왼쪽은 어두운 그라데이션 여백, 오른쪽에 은은한
조명 하이라이트, 에디토리얼 고급스러움, 텍스트 없음, 로고 없음, 16:9 와이드
```

### 생성 프롬프트 (English)

```
Cinematic premium nightlife lounge background, deep plum and wine tones,
soft rose gold and lilac accent lights, velvet and glass textures, heavy bokeh,
dark gradient on the left third for text overlay, brighter mood lighting on the right,
editorial luxury, no text, no logo, no people, wide 16:9
```

### 피하기

낮 풍경, 해변 낮, 네온 간판 클로즈업, 얼굴 클로즈업

---

## 2. hero-angelie.png

| 항목 | 내용 |
|------|------|
| **용도** | 홈 히어로 우측 카드 (4:3에 가깝게 crop) |
| **크기** | 1280×960 (4:3) |

### 어떤 이미지?

Angelie 브랜드를 상징하는 **‘큐레이터’** 느낌 — 우아하고 차분.  
정면 얼굴 대신 프로필 실루엣, 손에 와인글라스, 목선·어깨 라인, 또는 고급 드레스 소매 + 조명만 보이는 연출.

### 생성 프롬프트 (한글)

```
로즈·플럼 톤의 고급 나이트 큐레이션 컨셉, 여성 실루엣 또는 목선·손만 보이는
우아한 연출, 부드러운 림라이트, 라일락 하이라이트, 벨벳·진주 소품,
차분하고 세련된 분위기, 얼굴 정면 클로즈업 없음, 텍스트 없음, 4:3
```

### 생성 프롬프트 (English)

```
Elegant night curator concept, rose and plum color grade, female silhouette or
hands with crystal wine glass, soft rim light, lilac highlights, velvet and pearl
props, calm sophisticated mood, no direct face close-up, no text, 4:3 portrait crop
```

### 피하기

카툰·일러스트, 과한 섹시 포즈, 선글라스+섬광 셀카 느낌

---

## 3. angelie-banner-jeju-room.png

| 항목 | 내용 |
|------|------|
| **용도** | 제주 룸싸롱 신호등 — 홈·area·상세 배너 |
| **크기** | 1200×380 (왼쪽 텍스트 오버레이) |

### 어떤 이미지?

제주 프라이빗 룸: 셔츠룸·라운지 느낌, 바다/야경은 **흐릿한 배경만**.  
소파, 테이블, 은은한 조명. 휴양지 고급 라운지.

### 생성 프롬프트 (한글)

```
제주도 프리미엄 프라이빗 라운지 인테리어, 와이드 3.2:1,
로즈·플럼 저조도 조명, 소파와 테이블, 창밖 흐릿한 야경 또는 바다 보케,
왼쪽 어두운 여백, 고급스럽고 차분, 텍스트·로고 없음, 인물 없거나 실루엣만
```

### 생성 프롬프트 (English)

```
Premium private lounge interior Jeju island mood, wide cinematic banner 3.2:1,
rose plum low-key lighting, sofa and table, blurred ocean or night view bokeh,
dark left side for text overlay, calm luxury, no text, no logo
```

---

## 4. angelie-banner-jeju-nightlife.png

| 항목 | 내용 |
|------|------|
| **용도** | 제주 유흥 미술관 |
| **크기** | 1200×380 |

### 어떤 이미지?

**미술관 + 라운지** 콘셉트: 프레임·조각·은은한 갤러리 조명 + 바 테이블.  
예술적이고 지적인 밤 분위기.

### 생성 프롬프트 (한글)

```
아트 갤러리와 프리미엄 라운지가 결합된 공간, 와이드 배너,
플럼·라일락 톤, 벽에 추상화 액자, 바 카운터 은은한 조명,
왼쪽 어둡게, 세련되고 지적인 밤, 텍스트 없음
```

### 생성 프롬프트 (English)

```
Art gallery meets premium lounge, wide banner, plum and lilac tones,
abstract framed art on walls, subtle bar counter lighting, dark left gradient,
intellectual sophisticated night mood, no text
```

---

## 5. angelie-banner-haeundae-hoppa.png

| 항목 | 내용 |
|------|------|
| **용도** | 부산 해운대 호빠 |
| **크기** | 1200×380 |

### 어떤 이미지?

해운대 야경: 고층 창문·바다 반짝임(보케) + 실내 프라이빗 테이블.  
해변 리조트 룸파티보다 **도심 바다뷰 라운지**.

### 생성 프롬프트 (한글)

```
해운대 야경이 보이는 프리미엄 라운지, 창밖 도시·바다 불빛 보케,
실내 프라이빗 테이블과 소프트 조명, 로즈·플럼 컬러그레이드,
와이드 배너 왼쪽 어두움, 텍스트 없음, 인물 실루엣만 가능
```

### 생성 프롬프트 (English)

```
Haeundae night city and ocean view through lounge windows, bokeh city lights,
private table interior, rose plum color grade, wide banner dark left,
no text, silhouette only if people
```

---

## 6. angelie-banner-songpa-karaoke.png

| 항목 | 내용 |
|------|------|
| **용도** | 송파 노래방·가라오케 |
| **크기** | 1200×380 |

### 어떤 이미지?

고급 프라이빗 노래방 룸: 마이크·소파·LED 무드등(라일락·로즈).  
대형 TV는 꺼진 상태 또는 추상 빛만. 노래방이지만 **키치하지 않게**.

### 생성 프롬프트 (한글)

```
프리미엄 프라이빗 노래방 룸, 와이드 배너, 로즈·라일락 무드 조명,
고급 소파와 테이블, 마이크가 보이지만 캐주얼하지 않음,
플럼 톤 인테리어, 왼쪽 어두운 여백, 텍스트·브랜드 로고 없음
```

### 생성 프롬프트 (English)

```
Luxury private karaoke room, wide banner, rose and lilac mood lighting,
premium sofa, subtle microphone prop, plum interior, not cheesy neon,
dark left for overlay, no text no logos
```

---

## 7. angelie-banner-gangnam-hoppa.png

| 항목 | 내용 |
|------|------|
| **용도** | 강남 호빠 |
| **크기** | 1200×380 |

### 어떤 이미지?

강남 도심 야경(흐림) + 실내 고급 프라이빗 테이블.  
세련된 도심 나이트, 유리·대리석·낮은 조명.

### 생성 프롬프트 (한글)

```
강남 도심 프리미엄 프라이빗 라운지, 와이드 배너,
창밖 흐릿한 강남 야경 보케, 대리석·유리 테이블,
로즈골드 포인트 조명, 플럼·와인 톤, 왼쪽 어둡게, 고급 도심 나이트, 텍스트 없음
```

### 생성 프롬프트 (English)

```
Gangnam premium private lounge, wide banner, blurred city night bokeh,
marble and glass table, rose gold accent lights, plum wine tones,
dark left side, upscale urban night, no text
```

---

## 공통 네거티브 프롬프트

생성 도구의 **Negative prompt**에 붙여 넣기.

### 한글

```
텍스트, 글자, 로고, 워터마크, 저화질, 흐림, 과노출, 낮은 조도 노이즈,
카툰, 일러스트, 3D 렌더 느낌, 원색 네온, 금색 과다, 얼굴 정면 클로즈업,
유명인 닮음, 미성년, 과도한 노출, 선정적 포즈, 술병 라벨 클로즈업,
저가형 노래방, 플라스틱 소품, 낮 시간, 해변 낮 휴양
```

### English

```
text, logo, watermark, low quality, blurry, overexposed, cartoon, illustration,
harsh neon, gold overload, celebrity face, underage, explicit, cheap karaoke,
plastic props, daytime beach, readable signage
```

---

## 상세 페이지 figure

현재 HTML은 위 **배너 이미지를 상세 본문에도 재사용**합니다.

상세만 다른 컷을 쓰려면 예:

- `angelie-detail-jeju-room.png` (820×460, 16:9에 가깝게)
- 해당 `index.html`의 `img src`만 변경

상세용은 배너보다 **한 공간 클로즈업**(테이블·소파·조명 디테일)이 어울립니다.

---

## 체크리스트 (교체 후)

- [ ] 파일명 7개가 정확한지
- [ ] 배너 왼쪽이 충분히 어두운지 (텍스트 가독)
- [ ] JungPM 이미지와 색·구도가 겹치지 않는지
- [ ] 이미지 안에 글자·로고가 없는지
- [ ] 모바일에서 crop 되어도 피사체가 잘리지 않는지
