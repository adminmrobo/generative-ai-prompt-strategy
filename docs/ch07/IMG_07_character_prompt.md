# 7장 「캐릭터를 설계도로 그리기」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 07_character_prompt.html |
| 모드 / 주 앵커 | 교과서 / D 생활·현장: 주문서 칸, 계단 사진, 볼륨 손잡이, 건물 골조, 청구기호 |
| 시즌 | 기본 |
| 대결 | 다섯 장면 동안 외형을 더 잘 지키는 쪽 → 결과 F (초파리 승), 기준 시트 일치율 90.6% vs 65.6% (차이 25.0%p, 설명용 모형·시드 7) |
| 새로 그릴 그림 | P1 1장(표지, 임시판 반영됨) · P2 2장 · P3 1장 |
| 재사용 | 표정 19장 (캐릭터 팩 96px, fruitfly-lab-expressions @ 5269662) |
| 그림이 없을 때 | 페이지는 캔버스 그림과 CSS 배경으로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: 16비트 RPG풍 픽셀아트, 굵은 어두운 외곽선, 2~3단계 명암
- 캐릭터 고정 외형: 캐릭터 팩 `CHAR_lab4.md` 18-4
- 장소: 밤의 연구실 안 '캐릭터 설계실' — 벽에 여섯 칸 설계도 보드, 카메라 삼각대, 소프트박스 조명
- 장소 영어 묘사: *a character design room inside the same night lab world, a wall board divided into six colored blank slots, a small camera on a tripod and a softbox light, purple lab light spilling in from the left*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|
| 0 | cover_07 | L | 1920×1080 | 임시판 있음 (캐릭터 팩 합성) → 정식판 새로 (COVER_07) | P1 | 맨 위 글 표지 | 현재 임시판 |
| 1 | thumb_07 | I | 600×400 | 있음 (cover_07 잘라냄) | P2 | 목차 카드 | — |
| 2 | og_07 | K | 1200×630 | 있음 (cover_07 잘라냄) | P3 | 공유 미리보기 | — |
| 3 | cut_07_lv2 | G | 960×540 | 새로 | P2 | ② 카메라 칸 컷: 계단 아래·위에서 찍는 조수 | 없음(컷 생략) |
| 4 | sc_07_outro | E | 1200×800 | 새로 | P2 | 아웃트로: 같은 얼굴 다섯 장이 걸린 벽 앞, 초파리 팔짱·주판봇 한숨 | 말풍선만 |
| — | doc_think·doc_magic·doc_judge·doc_front | A | 192×192 | 재사용 | — | 히어로·왜·판정·아웃트로 | — |
| — | asst_smile·asst_shock·asst_spark·asst_report | B | 180×220 | 재사용 | — | 조수 수식 상자·발표 | — |
| — | fly_point·fly_clip·fly_magnify·fly_arms | C | 220×220 | 재사용 (오른쪽을 보게 좌우 뒤집음) | — | 말풍선·대결 | — |
| — | robo_smile·robo_coin·robo_calc·robo_sigh | D | 180×200 | 재사용 | — | 말풍선·대결 | — |
| — | 실험 그림 6종 | — | — | 코드 | — | 캔버스 | — |

## 3. 새로 그릴 그림 상세

### 3-1. `cut_07_lv2` — 계단 아래와 위에서 찍기
| 항목 | 내용 |
|---|---|
| 판 · 크기 | G · 960×540 |
| 구도 | 화면을 둘로: 왼쪽은 계단 아래에서 올려다보며 조수를 찍는 초파리, 오른쪽은 계단 위에서 내려다보며 조수를 찍는 주판봇 |
| 표정·몸짓 | 조수는 같은 자세로 손을 흔듦. 두 촬영자는 집중한 표정 |
| 소품 | 작은 카메라 두 대, 계단 (글자 없음) |
| 피할 것 | 승패 암시, 글자 |
| 대체 글 | 계단 아래와 위에서 같은 조수를 찍는 초파리 연구원과 주판봇 |

```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 16:9 illustration panel, split composition: on the left an anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, crouching at the bottom of a staircase and photographing upward with a small camera; on the right a boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, at the top of the staircase photographing downward; in the middle a girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, waving on the stairs, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-2. `sc_07_outro` — 다섯 장의 같은 얼굴
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 |
| 구도 | 벽에 조수 얼굴 스케치 다섯 장(같은 얼굴, 각도만 다름). 앞에 초파리(팔짱, 앞·크게), 주판봇(한숨, 인정하는 몸짓), 박사(가운데 뒤), 조수(옆에서 표 들고 미소) |
| 피할 것 | 조롱, 글자 |
| 대체 글 | 같은 얼굴 다섯 장이 걸린 벽 앞에서 대결을 마친 연구실 네 식구 |

```
16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, a wall with five pinned sketches of the same pink-haired girl face from different angles, in front the fruit fly researcher with arms crossed and a confident look, the boxy beige CRT robot with half-closed eyes and a small sigh bubble scratching its head good-naturedly, the chibi scientist with thin teal rectangular glasses at the back center smiling, the girl researcher at the side holding a blank striped sheet and smiling, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

## 4. 일관성 지침
- 참고 이미지: 네 캐릭터 기본 그림 4장 (fruitfly-lab-expressions `images/` E13·E08 등)
- 같은 캐릭터는 같은 세션에서. 표정만 바꿀 때: *same character, same size and position, only change the facial expression and pose to ...*
- 투명 배경이 안 되면: *solid flat #00ff00 background*

## 5. 넘겨받은 뒤 처리
1. 비율·글자·네 캐릭터 외형 확인 → 2. WebP(장면 1200×800, 컷 960×540) → 3. `data-img` 자리에 넣고 페이지 그림 합계 600 KB 이하 확인 → 4. 390·768·1280 폭 점검

## 6. 매니페스트
```json
{"page":"07_character_prompt","anchor":"D:design-room","season":"default","duel":{"result":"F","gap":0.25},
 "images":[
  {"key":"cover_07","plate":"L","size":[1920,1080],"status":"temp-done","priority":"P1","slot":"cover","alt":"밤의 연구실에서 네 캐릭터가 여섯 칸 설계도 카드 앞에 선 표지"},
  {"key":"thumb_07","plate":"I","size":[600,400],"status":"done","priority":"P2","slot":"index-card"},
  {"key":"og_07","plate":"K","size":[1200,630],"status":"done","priority":"P3","slot":"og"},
  {"key":"cut_07_lv2","plate":"G","size":[960,540],"status":"new","priority":"P2","slot":"lv2"},
  {"key":"sc_07_outro","plate":"E","size":[1200,800],"status":"new","priority":"P2","slot":"outro"}]}
```
