# 「프롬프트로 창업하기」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 생성형AI활용전략_6장.html |
| 모드 / 주 앵커 | 교과서 / D 생활·현장: 밤의 연구실 안 카페 카운터와 쇼핑몰 MD 책상 |
| 시즌 | 기본 |
| 대결 | "카페 창업 계획, 한 줄 프롬프트로 충분할까?" → 결과 R (주판봇 승), 차이 0.60 (0.31 대 0.91) |
| 새로 그릴 그림 | 남은 것 없음 (sc_06_hero는 선택 — 지금은 캐릭터 팩 무대). cover_06 · thumb_06 · og_06은 받아서 반영함 (2026-11-03) |
| 재사용 | 표정 13키 — 캐릭터 팩 fruitfly-lab-expressions @ ea5da3f, 96px 15장 73 KB를 페이지에 넣음 |
| 그림이 없을 때 | 페이지는 픽셀 지도와 캔버스 장면으로 이미 완성 상태 |

## 0-1. 로봇 교체 (2026-11-04)
- 연구실 로봇 Money-Robo → **주판봇**(외국어판 AbaBot). 베이지색 상자형 CRT 몸체, 짙은 초록 화면에 민트 픽셀 눈·입, 주판알 안테나, 회색 마디형 팔, 무한궤도, 나무 주판.
- 표정 그림: 캐릭터 팩 v1.1(`fruitfly-lab-expressions` @ `107ce63`의 `images/jupanbot`)로 다시 뽑았다. 키 이름(`robo_coin` 등)은 그대로, 그림만 주판봇.
- 픽셀 대체 그림: 스킬 부록 A-3 지도로 바꿨다.
- **cover_06 · thumb_06 · og_06**: 예전 표지에 하얀 Money-Robo가 있어 내렸다. 지금은 캐릭터 팩 그림 넷을 칠판 앞에 세운 **임시 표지**(1600 WebP 61 KB)다. `COVER_06_prompt_startup.md`의 새 지시문으로 다시 생성해 받으면 18-15 절차로 바꾼다 (status: `redo`).
- sc_06_hero 무대의 로봇 그림도 주판봇(robo_e16)으로 바꿨다.

## 0. 반영 기록 (2026-11-03)
- **cover_06**: 16:9, 네 캐릭터 외형 일치, 칠판·장부·쇼핑백에 글자 없음. 1600 WebP(140 KB)를 단일 파일 규칙(18-14-5)대로 base64 `src` 하나로 넣었다. 390·768·1280 폭에서 얼굴 잘림 없고 칩이 얼굴을 가리지 않는다. 작은 흠: 로봇 금화에 "?" 무늬가 있다(읽히는 글자는 아님).
- **thumb_06 · og_06**: 받은 파일 그대로 보관. `og:image`는 공개 주소가 정해지면 `<meta property="og:image" content="{주소}/og_06.webp">`로 넣는다.
- **표정 그림**: 캐릭터 팩에서 13키를 골라 넣었다. 팩에 없는 `asst_ledger`는 팩 규칙대로 E07(검지 세워 발표)로 대신한다. 왼쪽을 보는 그림은 본문 쪽을 보도록 좌우를 뒤집었다.
- 그림 합계: 표지 140 KB + 표정 73 KB = 약 213 KB (기준 600 KB 이하).
- **sc_06_hero**: 임시 캔버스 장면을 걷어 내고, 캐릭터 팩 192px 그림 넷(doc_e09 · fly_e08 · asst_e07 · robo_e16, 약 40 KB)으로 만든 무대로 바꿨다. 장면 그림을 따로 받으면 이 자리에 넣는다.
- 그림 합계(갱신): 약 255 KB.

## 1. 그림체와 고정 외형
- 스타일: SKILL 18-3 (16비트 RPG 픽셀아트, 굵은 외곽선, 2~3단계 명암)
- 캐릭터 고정 외형: SKILL 18-4 표 그대로
- 이 페이지 장소: 밤의 연구실 한쪽에 작은 카페 카운터(커피잔, 원두 병)와 쇼핑몰 MD 책상(옷걸이 랙, 쇼핑백, 원단 견본)이 마주 놓인 공간. 가운데 칠판에는 글자 없는 여덟 칸 주문 카드. 생물 앵커가 아니므로 현미경·초파리 해부 소품은 넣지 않는다.
- 장소 영어 묘사: *a small cafe counter with a coffee cup and bean jars facing a fashion buyer's desk with a clothing rack, shopping bags and fabric swatches, both inside the same night lab world, a blank order card with eight colored empty slots pinned on a chalkboard between them, purple lab light spilling in from one side*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|
| 0 | cover_06 | L | 1920×1080 | 새로 (COVER_06_prompt_startup.md) | P1 | 맨 위 글 표지 | 대체 표지 (캔버스 + 픽셀 넷) |
| 1 | sc_06_hero | E | 1200×800 | 새로 | P1 | 히어로 오른쪽 무대 | 캔버스 장면 |
| 2 | doc_think | A | 192×192 | 공용·필요 | P1 | 히어로 대화창 | doc_front |
| 3 | asst_smile | B | 180×220 | 공용 | — | 히어로, 등장인물 | — |
| 4 | fly_point | C | 220×220 | 공용 | — | 히어로, ①칸 말풍선, 대결 전 | fly_clip |
| 5 | robo_coin | D | 180×200 | 공용 | — | 히어로, 대결 전 | robo_smile |
| 6 | doc_front | A | 192×192 | 공용 | — | 등장인물, 아웃트로 | — |
| 7 | fly_clip | C | 220×220 | 공용 | — | 등장인물 | — |
| 8 | robo_smile | D | 180×200 | 공용 | — | 등장인물, ③칸 말풍선 | — |
| 9 | doc_magic | A | 192×192 | 공용·필요 | P2 | ⑤칸 말풍선 (핵심 한 줄) | doc_front |
| 10 | asst_ledger | B | 180×220 | 공용·필요 | P1 | 대결 숫자 발표, 꾸러미 섹션 | asst_firm |
| 11 | doc_judge | A | 192×192 | 공용 | — | 대결 판정 | doc_front |
| 12 | robo_happy | D | 180×200 | 공용 | — | 대결 후, 아웃트로 | robo_smile |
| 13 | fly_cry | C | 220×220 | 공용 | — | 대결 후 (차이 10%p 이상), 아웃트로 | fly_coffee |
| 14 | asst_spark | B | 180×220 | 공용 | — | 아웃트로 | asst_smile |
| 15 | thumb_06 | I | 600×400 | 새로 (cover_06을 3:2로 자르기) | P2 | 목차 카드 (목차 페이지에서 사용) | 색 카드 |
| 16 | og_06 | K | 1200×630 | 새로 (cover_06 자르기) | P3 | 공유 미리보기 (넣을 때 `<meta property="og:image">` 추가) | 없음 |
| — | 행동으로 보기, 손님 NPC | — | — | 코드 | — | 캔버스 | — |

히어로 배경 `bg_06`(F판)은 표지가 있으므로 만들지 않는다(18-6 R1, P3).

## 3. 새로 그릴 그림 상세

### 3-1. `cover_06` — 여덟 칸 주문 카드 앞의 네 캐릭터
상세와 Genspark 붙여 넣기 블록은 **COVER_06_prompt_startup.md**에 있다.

### 3-2. `sc_06_hero` — 카페 카운터와 MD 책상 사이의 작전 회의
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 (2배 2400×1600 가능) |
| 배경 | 그림 전체 |
| 구도 | 왼쪽 카페 카운터 앞에 초파리 연구원(오른쪽을 봄), 오른쪽 MD 책상 옆에 주판봇(왼쪽을 봄), 가운데 뒤 칠판 앞에 박사, 오른쪽 앞에 조수. 중요한 것은 위쪽 62% 안에 |
| 표정·몸짓 | 박사 doc_think(턱에 손), 초파리 fly_point(한쪽 겹눈 가늘게, 칠판 가리킴), 주판봇 robo_coin(주판알을 반짝 튕겨 보임), 조수 asst_ledger(줄무늬 장부와 펜) |
| 소품 | 칠판의 여덟 칸 빈 주문 카드(파랑 2칸·분홍 4칸·초록 2칸, 글자 없음), 김이 나는 커피잔, 쇼핑백과 옷걸이 랙 |
| 빛·분위기 | 밤의 보라 조명, 칠판 카드에 따뜻한 노란 빛이 모임, 시험관 선반의 분홍·초록 작은 빛 |
| 피할 것 | 승패 암시(결과 전 장면), 칠판·장부·쇼핑백의 글자와 로고, 실제 카페·패션 브랜드, 현미경 |
| 대체 글 (alt) | 카페 카운터와 쇼핑몰 책상 사이, 여덟 칸 빈 주문 카드가 붙은 칠판을 네 캐릭터가 바라보는 연구실 장면 |
| 대신 쓰는 그림 | 캔버스 장면 |

**프롬프트 (복사해서 사용)**
```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, a small cafe counter with a steaming coffee cup and bean jars on the left facing a fashion buyer's desk with a clothing rack and shopping bags on the right, both inside the same night lab world, at the back center a blank chalkboard with an order card of eight empty colored slots (two blue, four magenta, two green) glowing with warm yellow light, chibi scientist with round glasses and black hair with one white streak in a white lab coat over black vest and tie standing in front of the chalkboard with a hand on his chin, anthropomorphic fruit fly researcher with black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat and transparent wings standing by the cafe counter on the left, facing right, one eye narrowed, pointing at the card, boxy beige retro CRT-monitor robot with a dark green screen face with mint pixel eyes and mouth, a short antenna topped with a red-brown abacus bead, gray segmented arms and two small tank treads, on the right facing left, holding a wooden abacus and flicking one shiny bead, girl researcher with pink hair in two round buns with a navy streak, blue eyes, white lab coat over lavender hoodie and jeans in the front right holding a striped ledger and a pen, curious and friendly mood before any result, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-3. 공용 표정 중 "필요" 키 (IMG_00_index.md가 없을 때만 여기서 만든다)

`doc_think` (A, 192×192, 투명)
```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, single character, transparent background, centered with a small margin, facing front, bust, chibi scientist with round glasses, black hair with one white streak, white lab coat over black vest and tie, eyebrows raised, mouth closed, one hand on his chin, thinking, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
`doc_magic` (A, 192×192, 투명)
```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, single character, transparent background, centered with a small margin, facing front, bust, chibi scientist with round glasses, black hair with one white streak, white lab coat over black vest and tie, big laugh, small purple sparks in both hands, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
`asst_ledger` (B, 180×220, 투명)
```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, single character, transparent background, centered with a small margin, facing front, bust, girl researcher with pink hair in two round buns with a navy streak, blue eyes, white lab coat over lavender hoodie, serious eyes, closed mouth, holding an open ledger with blank striped pages and a pen, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
표정만 바꿀 때 덧붙일 문장: *same character, same size and position, only change the facial expression and pose to ...*

## 4. 일관성 지침
- 참고 이미지: 네 캐릭터 기본 표정 4장 (GitHub `adminmrobo/fruitfly-lab-expressions`)
- 같은 캐릭터는 같은 세션에서 연달아. 시드를 고를 수 있으면 캐릭터마다 고정
- 투명 배경이 안 되면: *solid flat #00ff00 background*로 받아 지운다
- 64×64로 줄여 기존 표정과 나란히 놓고 머리 크기·색 비교

## 5. 넘겨받은 뒤 처리
1. 크기·투명 배경 확인, 단색 배경 제거
2. 빌드 크기로 줄이고 WebP 압축 (A 128×128, B·C·D 높이 180, E 너비 760)
3. `data-img` 키 자리에 넣는다. 히어로 `sc_06_hero`는 지금 캔버스이므로, 그림이 오면 `<img class="pixelart" data-img="sc_06_hero" ...>`로 바꾼다
4. 그림 합계 확인: 표지 제외 400 KB, 표지 포함 600 KB 이하
5. 표지는 SKILL 18-15 절차 (비율·글자·네 캐릭터 확인 → WebP 1600/960 → 390·768·1280 폭 점검)

## 6. 체크리스트 (18-13)
- [x] HTML의 모든 `data-img` 키가 이 표에 있음 (15키). thumb_06·og_06은 목차·메타용으로 HTML 본문에 자리가 없음
- [x] 대결 후 표정: R, 차이 0.60 → fly_cry, robo_happy, doc_judge, asst_spark(아웃트로)
- [x] 결과 전 그림(표지·히어로)에 승패 암시 없음
- [x] 모든 프롬프트에 18-4 고정 외형과 금지 구절
- [x] 장소가 D 앵커, 현미경·해부 소품 없음
- [x] 그림 안 글자 없음, 실존 브랜드 없음
- [x] 새로 그릴 P1 2장 (6장 이하)

## 7. 매니페스트
```json
{
  "page": "genai-strategy-06-prompt-startup",
  "anchor": "D:cafe-counter+md-desk",
  "season": "default",
  "duel": {"result": "R", "gap": 0.60},
  "images": [
    {"key":"cover_06","plate":"L","size":[1920,1080],"status":"redo","note":"Money-Robo가 그려진 표지라 내림. 임시 표지(캐릭터 팩 합성) 사용 중","priority":"P1","slot":"cover","fallback":"canvas-pixel-four","alt":"밤의 연구실에서 네 캐릭터가 카페 카운터와 쇼핑몰 책상 사이의 여덟 칸 빈 주문 카드를 바라보는 표지"},
    {"key":"sc_06_hero","plate":"E","size":[1200,800],"status":"new","priority":"P1","slot":"hero-stage","fallback":"canvas-scene","alt":"카페 카운터와 쇼핑몰 책상 사이, 여덟 칸 빈 주문 카드가 붙은 칠판을 네 캐릭터가 바라보는 연구실 장면"},
    {"key":"doc_think","plate":"A","size":[192,192],"status":"shared-needed","priority":"P1","slot":"hero-dialog","fallback":"doc_front","alt":""},
    {"key":"doc_magic","plate":"A","size":[192,192],"status":"shared-needed","priority":"P2","slot":"lv5-say","fallback":"doc_front","alt":""},
    {"key":"asst_ledger","plate":"B","size":[180,220],"status":"shared-needed","priority":"P1","slot":"duel-after","fallback":"asst_firm","alt":""},
    {"key":"asst_smile","plate":"B","size":[180,220],"status":"reuse","slot":"hero-dialog","alt":""},
    {"key":"asst_spark","plate":"B","size":[180,220],"status":"reuse","slot":"outro","fallback":"asst_smile","alt":""},
    {"key":"doc_front","plate":"A","size":[192,192],"status":"reuse","slot":"cast","alt":""},
    {"key":"doc_judge","plate":"A","size":[192,192],"status":"reuse","slot":"duel-verdict","fallback":"doc_front","alt":""},
    {"key":"fly_point","plate":"C","size":[220,220],"status":"reuse","slot":"duel-before","fallback":"fly_clip","alt":""},
    {"key":"fly_clip","plate":"C","size":[220,220],"status":"reuse","slot":"cast","alt":""},
    {"key":"fly_cry","plate":"C","size":[220,220],"status":"reuse","slot":"duel-after","fallback":"fly_coffee","alt":""},
    {"key":"robo_coin","plate":"D","size":[180,200],"status":"reuse","slot":"duel-before","fallback":"robo_smile","alt":""},
    {"key":"robo_smile","plate":"D","size":[180,200],"status":"reuse","slot":"cast","alt":""},
    {"key":"robo_happy","plate":"D","size":[180,200],"status":"reuse","slot":"duel-after","fallback":"robo_smile","alt":""},
    {"key":"thumb_06","plate":"I","size":[600,400],"status":"redo","priority":"P2","slot":"index-card","fallback":"color-card","alt":"프롬프트로 창업하기 목차 카드"},
    {"key":"og_06","plate":"K","size":[1200,630],"status":"redo","priority":"P3","slot":"og","fallback":"none","alt":"프롬프트로 창업하기 공유 미리보기"}
  ]
}
```
