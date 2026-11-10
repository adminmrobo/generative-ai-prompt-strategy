# 주판봇 교체 — 05 그림 다시 만들기 (Genspark 편집 지시문)

로봇 캐릭터가 **Money-Robo → 주판봇**(외국어판 AbaBot)으로 바뀌었다. 성격은 그대로이고 겉모습과 소품만 바뀐다.

| 항목 | Money-Robo (옛) | 주판봇 (새) |
|---|---|---|
| 겉모습 | 둥근 흰 머리, 검은 화면에 노란 눈, 다리 없이 떠 있음 | 베이지색 상자형 레트로 컴퓨터 로봇, 초록 화면 얼굴 |
| 소품 | 금화 | 주판(주판알) |
| 영어 묘사 | — | *boxy beige retro computer robot with a green screen face showing simple dark-green pixel eyes and mouth, small stubby arms* |

**새로 만드는 방법:** 이미 받은 그림을 Genspark에 올리고 **로봇만 바꾸라고** 하는 편집 방식이 가장 빠르다. 나머지 세 캐릭터, 구도, 회계실은 그대로 둔다.
**참고 이미지:** 주판봇 기준 그림(기존 글의 베이지 레트로 컴퓨터 로봇)이 있으면 꼭 같이 올린다. 없으면 이번 표지의 주판봇이 이후의 기준이 된다.

| 키 | 올릴 그림 | 받을 크기 | 비고 |
|---|---|---|---|
| cover_05 | 지난번 표지 (1600×900) | 16:9, 가로 1600 이상 | 썸네일 thumb_05(3:2)와 공유 미리보기 og_05(1200×630)는 이 그림을 잘라 다시 만든다 |
| sc_05_hero | 지난번 히어로 장면 (3:2) | 3:2, 1200×800 이상 | 결과 전 장면 |
| sc_05_outro | 지난번 아웃트로 장면 (3:2) | 3:2, 1200×800 이상 | 결과 F (주판봇 짐) |
| bg_05 | — | — | 로봇이 없어 그대로 씀 |

---

## 1. cover_05 (표지)

```
첨부한 그림을 편집해 줘. 비율·구도·그림체·조명·다른 세 캐릭터는 그대로 두고, 오른쪽의 하얀 떠 있는 로봇만 바꿔 줘.
그림 안에 글자·숫자·로고는 넣지 말 것.

Edit the attached image. Keep the same aspect ratio, composition, art style, lighting, room and the other three characters exactly as they are.
Replace only the round white floating robot on the right with a boxy beige retro computer robot with a green screen face showing simple dark-green pixel eyes and a small smile, small stubby arms,
standing on the floor on the right facing left, proudly holding up a small wooden abacus with red and gold beads.
No oval floating shadow, no antenna, no blue chest light. Same 16-bit pixel art style and dark outline as the other characters.
No text, no letters, no numbers, no logos.
```

## 2. sc_05_hero (히어로 장면, 결과 전)

```
첨부한 그림을 편집해 줘. 오른쪽의 하얀 로봇만 바꾸고 나머지는 그대로.

Edit the attached image. Keep everything else exactly the same.
Replace only the round white floating robot on the right with a boxy beige retro computer robot with a green screen face showing narrowed dark-green pixel eyes and a sly grin, small stubby arms,
facing left toward the ledger tower, holding up a small wooden abacus with red and gold beads.
No floating, no antenna, no blue chest light. Same pixel art style. No text, no letters, no numbers, no logos.
```

## 3. sc_05_outro (아웃트로, 결과 F: 초파리 승)

```
첨부한 그림을 편집해 줘. 오른쪽 아래의 하얀 로봇만 바꾸고 나머지는 그대로.

Edit the attached image. Keep everything else exactly the same.
Replace only the white robot at the lower right with a boxy beige retro computer robot with a green screen face showing half-closed dark-green pixel eyes and a small flat mouth, a small sigh puff beside it, arms lowered,
a small wooden abacus resting at its side, nodding in acceptance toward the fruit fly researcher.
Friendly mood, no mocking. Same pixel art style. No text, no letters, no numbers, no logos.
```

**고칠 때 (같은 대화에서):** `Same image. Change only the beige computer robot: {고칠 점}. Still no text.`

---

## 받은 뒤 (SKILL 18-15)

1. 네 캐릭터 외형 확인. 주판봇이 **베이지 상자형·초록 화면·주판**인지, 하얀 로봇이나 금화를 든 모습이 남지 않았는지 본다.
2. WebP로 바꾼다: 표지 1600×900(220 KB 이하)·960×540, 장면 760×506.
3. 표지에서 thumb_05(600×400)와 og_05(1200×630)를 다시 자른다.
4. `data-img` 자리(cover_05, sc_05_hero, sc_05_outro)에 넣는다. 지금 그 자리에는 픽셀 대체 그림이 들어 있다.
5. 저장소의 임시 og_05·thumb_05·목차 표지를 새 그림으로 바꾼다.
6. 주판봇 표정 그림 팩(robo_* 키)이 나오면 픽셀 지도 대신 그 팩을 넣는다.
