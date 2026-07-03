# GenAI 기초 2: 멀티모달 콘텐츠 제작

## AI 기반 브랜드 광고 패키지: MORNING DROP

---

## 1. 프로젝트 개요

본 과제에서는 가상의 프리미엄 콜드브루 커피 브랜드 **MORNING DROP**을 대상으로 10초 이내의 AI 기반 브랜드 광고 영상을 제작하였다.

최종 광고 영상은 **OpenAI Sora 2**에서 텍스트 프롬프트만으로 생성한 **4초 통합 광고 영상 원본**을 사용하였다.  
초기 제작 과정에서 GPT Image 2로 씬별 키비주얼 이미지를 생성했지만, Sora 2 영상 생성 단계에서는 이미지 첨부 기능을 확인할 수 없어 해당 이미지를 직접 첨부하지 않았다. 따라서 생성 이미지는 최종 영상의 직접 소스가 아니라, 스토리보드와 톤앤매너를 검토하기 위한 사전 기획 자료로 활용하였다.

또한 OpenAI TTS-1으로 한국어 내레이션 파일을 테스트 생성했으나, 최종 Sora 영상 자체에 영어 음성/오디오가 포함되어 있어 TTS 파일은 최종 영상에 적용하지 않았다. 최종 제출 영상의 청각 요소는 Sora 2 원본 영상에 포함된 오디오를 사용하였다.

---

## 2. 브랜드 아이덴티티

| 항목 | 내용 |
|---|---|
| 브랜드명 | MORNING DROP |
| 제품 | 프리미엄 콜드브루 커피 |
| 타겟 | 출근 전 집중이 필요한 20~30대 직장인 |
| 톤앤매너 | 미니멀, 따뜻한 아침빛, 프리미엄, 차분함 |
| USP | 바쁜 아침에도 빠르게 집중 모드로 전환 |
| 광고 목적 | 브랜드 인지도 향상 |
| 핵심 메시지 | 하루의 집중은 첫 한 모금에서 시작된다. |
| 최종 영상 길이 | 약 4초 |
| 최종 영상 형식 | MP4 |
| 최종 영상 제작 방식 | Sora 2에서 4초 통합 광고 영상 1개 생성 |

---

## 3. 캠페인 목표 및 핵심 메시지

### 3.1 캠페인 목표

본 광고의 목표는 출근 전 집중이 필요한 직장인에게 MORNING DROP을 “아침 집중을 시작하게 해주는 프리미엄 콜드브루”로 인식시키는 것이다. 짧은 영상 안에서 흐릿한 아침 분위기, 콜드브루의 제품 경험, 집중 모드로의 전환, 브랜드 인지를 압축적으로 전달하도록 구성하였다.

### 3.2 핵심 메시지

> 하루의 집중은 첫 한 모금에서 시작된다.

---

## 4. 사용 도구 목록

| 구분 | 사용 도구 | 사용 목적 | 실제 적용 방식 | 대체 도구 |
|---|---|---|---|---|
| 기획/스토리보드/프롬프트 설계 | Gemini 3.1 Pro | 브랜드 기획, 씬 구성, 프롬프트 작성 | 최종 스토리보드와 Sora 프롬프트 설계에 사용 | Gemini 3.1 Flash |
| 이미지 생성 | GPT Image 2 | 씬별 키비주얼 생성 | 최종 영상에 직접 첨부하지 않고, 사전 톤앤매너 검토용으로 활용 | Gemini 이미지 생성, Adobe Firefly |
| 영상 생성 | OpenAI Sora 2 | 최종 광고 영상 생성 | 텍스트 프롬프트만으로 4초 통합 광고 영상 1개 생성 | Pika, Kling |
| 오디오 생성 | OpenAI Sora 2 내장 오디오 | 최종 영상의 청각 요소 생성 | Sora 원본 영상에 포함된 영어 음성/오디오를 최종 사용 | OpenAI TTS-1, Suno |
| 음성 생성 테스트 | OpenAI TTS-1 / alloy | 한국어 내레이션 테스트 | 테스트 파일은 생성했으나 최종 영상에는 미적용 | ElevenLabs |
| 편집 | 별도 편집 미사용 | 원본 영상 사용 | Sora 2 원본 MP4를 최종 제출본으로 사용 | CapCut, Premiere Pro |

---

## 5. 제작 전략

### 5.1 전체 제작 방향

초기에는 4개 씬을 각각 이미지와 영상으로 제작한 뒤 편집하는 방식을 고려하였다. 그러나 영상 생성은 크레딧 소모가 크고, 별도 편집 시간이 필요하므로 최종적으로 **Sora 2에서 4초 통합 광고 영상 1개를 생성하는 방식**을 선택하였다.

이 방식은 10초 이내 광고 영상이라는 과제 조건을 충족하면서도, 문제 제시 → 제품 경험 → 집중 전환 → 브랜드 인지 흐름을 하나의 짧은 영상 안에 압축할 수 있다는 장점이 있다.

### 5.2 키비주얼 이미지의 역할

GPT Image 2로 생성한 4장의 이미지는 최종 영상에 직접 삽입하거나 Sora에 첨부하지 않았다. 대신 각 씬의 시각 방향을 검토하고, Sora 프롬프트를 구체화하기 위한 사전 기획 자료로 사용하였다.

### 5.3 오디오 적용 방식

최종 Sora 영상 자체에 영어 음성/오디오가 포함되어 있었기 때문에, 별도 생성한 TTS 음성 파일은 최종 영상에 합성하지 않았다. 한국어 TTS를 얹을 경우 기존 영어 음성과 겹쳐 오디오가 혼잡해질 수 있다고 판단하였다. 따라서 최종 영상에는 Sora 2 원본 오디오를 유지하였다.

---

## 6. 스토리보드

최종 영상은 4초 분량이지만, 기획 단계에서는 4씬 구조를 유지하였다. 각 씬은 약 1초 단위로 압축되어 최종 Sora 영상 안에 반영되도록 설계하였다.

| 씬 번호 | 씬 길이 | 목표 메시지 | 화면 구성 | 내레이션/카피 | 사용 도구와 목적 | 입력 프롬프트 요약 | 출력 결과 요약 | 결과 파일명 |
|---|---:|---|---|---|---|---|---|---|
| Scene 1 | 약 1초 | 흐릿한 아침, 집중이 안 되는 순간을 제시한다. | 따뜻한 아침빛의 우드 책상, 노트북, 손, 커피잔 | Sora 원본 영어 오디오 | Sora 2: 통합 영상 생성 | Warm morning wooden desk with laptop, hands, notebook, and iced cold brew. Slightly hazy and tired morning mood. | 아침 업무 장면을 통해 집중 전의 흐릿한 분위기를 제시함 | morning_drop_sora_ad_4s.mp4 |
| Scene 2 | 약 1초 | 콜드브루의 청량함과 제품 경험을 강조한다. | 얼음잔에 콜드브루가 부어지는 클로즈업 | Sora 원본 영어 오디오 | Sora 2: 통합 영상 생성 | Extreme close-up of dark premium cold brew coffee pouring over clear ice cubes in a glass. | 커피가 얼음 위로 부어지는 장면으로 제품의 청량감을 표현함 | morning_drop_sora_ad_4s.mp4 |
| Scene 3 | 약 1초 | 커피 이후 집중 모드 전환을 보여준다. | 노트북 앞에서 타이핑하는 손과 아이스 콜드브루 | Sora 원본 영어 오디오 | Sora 2: 통합 영상 생성 | Hands typing confidently on a laptop with iced cold brew beside it. The mood becomes sharper, brighter, and more focused. | 밝고 선명한 업무 장면으로 집중 상태를 표현함 | morning_drop_sora_ad_4s.mp4 |
| Scene 4 | 약 1초 | 브랜드 인지와 광고 마무리를 수행한다. | 앰버 컬러 콜드브루 보틀과 커피잔의 제품 히어로 컷 | Sora 원본 영어 오디오 | Sora 2: 통합 영상 생성 | Premium product hero shot of an amber cold brew bottle and a glass of iced coffee. Show the brand name “MORNING DROP” clearly and elegantly if possible. | 마지막 컷에서 MORNING DROP 브랜드명과 제품을 보여주며 광고를 마무리함 | morning_drop_sora_ad_4s.mp4 |

---

## 7. 사전 키비주얼 이미지 생성 결과

아래 이미지는 최종 영상에 직접 삽입하지 않았고, Sora에도 첨부하지 않았다.  
다만 광고의 톤앤매너와 장면 구성을 확정하기 위한 사전 시각 검토 자료로 활용하였다.

| 씬 | 생성 이미지 파일명 | 활용 목적 | 출력 결과 요약 |
|---|---|---|---|
| Scene 1 | S1_blurry_desk.png | 아침 업무 장면의 분위기 검토 | 따뜻한 아침빛이 들어오는 책상과 노트북, 커피잔을 통해 집중 전 아침 분위기를 표현하였다. |
| Scene 2 | S2_pouring_coffee.png | 제품 경험 장면 검토 | 얼음잔에 콜드브루가 부어지는 클로즈업으로 제품의 청량감과 프리미엄 이미지를 강조하였다. |
| Scene 3 | S3_sharp_typing.png | 집중 전환 장면 검토 | 노트북 앞에서 타이핑하는 손과 커피잔을 배치해 집중 모드로 전환된 상태를 표현하였다. |
| Scene 4 | S4_brand_packshot.png | 브랜드 엔딩 컷 검토 | 콜드브루 보틀과 잔을 미니멀한 배경에 배치해 브랜드 인지용 제품 컷을 검토하였다. |

---

## 8. 주요 입력 프롬프트

### 8.1 Sora 2 최종 영상 생성 프롬프트

```text
Create a 4-second premium commercial video for a fictional cold brew coffee brand called MORNING DROP.

Use these four storyboard key visuals as references:
1. warm morning desk with laptop, hands, notebook, and iced cold brew
2. close-up of dark cold brew coffee pouring over clear ice cubes
3. focused typing scene with iced cold brew beside the laptop
4. premium amber cold brew bottle and iced coffee hero shot

Video structure:
0-1s: Warm morning wooden desk with laptop, hands, notebook, and iced cold brew. Slightly hazy and tired morning mood.
1-2s: Extreme close-up of dark premium cold brew coffee pouring over clear ice cubes in a glass.
2-3s: Hands typing confidently on a laptop with iced cold brew beside it. The mood becomes sharper, brighter, and more focused.
3-4s: Premium product hero shot of an amber cold brew bottle and a glass of iced coffee on a clean beige background.

Style:
minimal premium beverage advertisement, warm morning sunlight, beige and wood tones, cinematic lighting, clean composition, smooth camera movement, calm and refined mood.

Brand ending:
In the final product hero shot, show the brand name “MORNING DROP” clearly and elegantly if possible. Do not include random text or misspelled words.

Avoid:
no distorted hands, no face close-up, no extra people, no cluttered background, no random letters, no Korean text.
```

### 8.2 이미지 생성 프롬프트

#### Scene 1

```text
First-person view of hands resting heavily on a laptop keyboard on a minimalist wooden desk. Warm morning sunlight, but the overall image is slightly out of focus and hazy. Calm but tired morning mood. Premium minimalist coffee advertisement style. No readable text, no logo, no face.
```

#### Scene 2

```text
Extreme close-up of dark, rich premium cold brew coffee being poured into a clear glass filled with ice. Warm morning light reflecting off the glass. Minimalist wooden table background. Crisp, refreshing, premium beverage commercial style. No readable text, no logo.
```

#### Scene 3

```text
Top-down view of hands typing energetically on a laptop keyboard. A glass of iced cold brew coffee sits next to it. Bright, clear, and crisp warm morning light. Minimalist wooden desk, premium office lifestyle advertisement style. No readable text, no logo, no face.
```

#### Scene 4

```text
A minimalist premium amber glass cold brew bottle next to a glass of iced coffee. Warm morning light casting soft shadows. Clean beige background, calm premium beverage advertisement style. Leave empty space for brand text to be added later. No readable text, no logo.
```

### 8.3 TTS 테스트 프롬프트

아래 문장으로 OpenAI TTS-1 음성 파일을 테스트 생성했으나, 최종 영상에는 적용하지 않았다.

```text
모닝 드롭. 하루의 집중은 첫 한 모금에서.
```

---

## 9. 프롬프트 수정 전/후 기록

### 대상 씬: Scene 1

#### 9.1 수정 전 프롬프트

```text
Cinematic shot, slightly blurry and hazy vision of a tired 20-something office worker's face looking at a laptop. Warm morning sunlight.
```

#### 9.2 문제점

초기 프롬프트는 피곤한 직장인의 얼굴을 중심으로 구성하였다. 그러나 AI 영상 생성에서 인물 얼굴이 포함되면 씬이 바뀔 때마다 동일 인물처럼 보이기 어렵고, 표정이나 얼굴 디테일이 어색하게 생성될 가능성이 있다. 짧은 광고 영상에서는 얼굴 왜곡이나 캐릭터 불일치가 브랜드 완성도를 떨어뜨릴 수 있다고 판단하였다.

#### 9.3 수정 후 프롬프트

```text
Cinematic shot, slightly blurry and hazy view of a minimalist desk. A pair of hands resting heavily on a laptop keyboard. Warm morning sunlight, out of focus.
```

#### 9.4 수정 이유

인물 얼굴 중심 구성을 손과 사물 중심 구성으로 변경하여 캐릭터 일관성 문제를 줄이고자 하였다. 노트북, 손, 책상, 아침빛만으로도 “아직 집중이 되지 않는 아침”이라는 메시지를 전달할 수 있으므로, 얼굴을 제외하는 편이 더 안정적이라고 판단하였다.

#### 9.5 결과 변화

수정 후에는 얼굴 왜곡 위험이 줄었고, 손·노트북·아침빛 중심의 미니멀한 브랜드 톤이 강화되었다. 또한 이후 집중 타이핑 장면과 자연스럽게 연결되어 “흐릿한 아침 → 집중 전환” 흐름을 안정적으로 표현할 수 있었다.

---

## 10. 최종 영상 정보

| 항목 | 내용 |
|---|---|
| 최종 영상 파일명 | morning_drop_sora_ad_4s.mp4 |
| 원본 업로드 파일명 | 8a609210-f695-49d8-ae9d-3c023d8e5eae.mp4 |
| 영상 길이 | 약 4.1초 |
| 해상도 | 1280x720 |
| 프레임레이트 | 30fps |
| 비디오 코덱 | H.264 |
| 오디오 코덱 | AAC |
| 최종 영상 생성 도구 | OpenAI Sora 2 |
| 최종 오디오 출처 | Sora 2 원본 영상 내 포함 오디오 |
| 별도 편집 여부 | 없음 |
| TTS 적용 여부 | 미적용 |

---

## 11. 제작 파이프라인 설명

### 11.1 기획

Gemini 3.1 Pro를 사용하여 MORNING DROP의 브랜드 아이덴티티, 광고 목표, 타겟, 톤앤매너, 핵심 메시지를 정의하였다.

### 11.2 스토리보드 구성

광고 구조는 문제 제시, 제품 경험, 집중 전환, 브랜드 인지의 4단계로 설계하였다. 과제 조건인 10초 이내를 충족하기 위해 각 장면을 약 1초씩 압축해 4초 광고로 구성하였다.

### 11.3 키비주얼 생성

GPT Image 2로 씬별 키비주얼 이미지를 생성하였다. 해당 이미지는 최종 영상에 직접 사용하지 않았지만, Sora 프롬프트의 시각 요소를 구체화하는 데 참고하였다.

### 11.4 영상 및 오디오 생성

OpenAI Sora 2에 텍스트 프롬프트를 입력하여 4초 통합 광고 영상을 생성하였다. 최종 영상에는 Sora에서 생성된 시각 요소와 영어 오디오가 함께 포함되어 있어, 별도 TTS 합성 없이 최종 제출본으로 사용하였다.

### 11.5 편집

최종 제출 영상은 별도 편집 없이 Sora 2 원본 MP4 파일을 사용하였다. 영상 자체가 4초 안에 제품 경험과 브랜드 인지를 포함하고 있으며, 오디오도 포함되어 있어 최종 광고 영상으로 적합하다고 판단하였다.

---

## 12. 도구별 역할과 차이

| 도구 | 강점 | 약점 | 본 과제에서의 역할 |
|---|---|---|---|
| Gemini 3.1 Pro | 기획, 문서화, 스토리보드 구성, 프롬프트 작성에 강함 | 직접 영상 파일을 생성하는 도구는 아님 | 전체 기획 및 프롬프트 설계 |
| GPT Image 2 | 장면별 키비주얼을 빠르게 확인할 수 있음 | 이미지가 최종 영상에 직접 연결되지는 않음 | 사전 톤앤매너 검토 |
| OpenAI Sora 2 | 텍스트만으로 짧은 영상과 오디오를 함께 생성 가능 | 한글 텍스트나 정확한 브랜드 텍스트 렌더링에는 한계가 있음 | 최종 광고 영상 생성 |
| OpenAI TTS-1 | 짧은 내레이션 생성에 적합 | 기존 영상 오디오와 겹치면 어색할 수 있음 | 한국어 내레이션 테스트 |

---

## 13. 제약 대응 전략

### 13.1 크레딧 부족 대응

영상 생성 횟수를 줄이기 위해 씬별 영상을 따로 만들지 않고, Sora 2에서 4초 통합 광고 영상 1개를 생성하였다.

### 13.2 이미지 첨부 제한 대응

Sora 2 영상 생성 화면에서 이미지 첨부 기능을 확인할 수 없었기 때문에, GPT Image 2로 만든 키비주얼 이미지를 직접 첨부하지 않았다. 대신 텍스트 프롬프트 안에 각 장면의 시각 요소를 상세히 기술하였다.

### 13.3 캐릭터 일관성 대응

인물 얼굴 중심 구성을 피하고 손, 노트북, 커피잔, 제품 보틀 중심으로 구성하였다. 이를 통해 인물 얼굴 왜곡과 캐릭터 불일치 문제를 줄였다.

### 13.4 오디오 미스매치 대응

TTS로 한국어 음성을 생성했지만, Sora 원본 영상에 이미 영어 음성과 오디오가 포함되어 있었다. 두 음성을 합치면 오디오가 겹쳐 어색해질 수 있으므로, 최종 영상에는 Sora 원본 오디오만 사용하였다.

### 13.5 텍스트 렌더링 대응

한글 텍스트는 영상 생성 AI에서 깨질 가능성이 있어 사용하지 않았다. 대신 영어 브랜드명 “MORNING DROP”만 마지막 제품 컷에서 인지되도록 요청하였다.

### 13.6 저작권 및 윤리 준수

직접 촬영 영상이나 유료 스톡 영상은 사용하지 않았고, 모든 주요 시각 및 청각 요소는 생성형 AI 결과물로 구성하였다. 실제 인물이나 유명인의 얼굴을 사용하지 않았으며, 유해 콘텐츠도 포함하지 않았다.

---

## 14. 최종 결과물 목록

| 산출물 | 파일명 | 최종 제출 여부 | 설명 |
|---|---|---|---|
| 스토리보드 문서 | morning_drop_multimodal_ad_package_revised.md | 제출 | 브랜드 아이덴티티, 스토리보드, 사용 도구, 프롬프트, 제작 파이프라인 정리 |
| 최종 광고 영상 | morning_drop_sora_ad_4s.mp4 | 제출 | Sora 2로 생성한 4초 통합 광고 영상 원본 |
| 키비주얼 이미지 1 | S1_blurry_desk.png | 참고 자료 | 최종 영상에 직접 적용하지 않은 사전 기획용 이미지 |
| 키비주얼 이미지 2 | S2_pouring_coffee.png | 참고 자료 | 최종 영상에 직접 적용하지 않은 사전 기획용 이미지 |
| 키비주얼 이미지 3 | S3_sharp_typing.png | 참고 자료 | 최종 영상에 직접 적용하지 않은 사전 기획용 이미지 |
| 키비주얼 이미지 4 | S4_brand_packshot.png | 참고 자료 | 최종 영상에 직접 적용하지 않은 사전 기획용 이미지 |
| TTS 테스트 파일 | morning_drop_voice.mp3 | 미제출/선택 | 최종 영상에는 적용하지 않은 한국어 음성 테스트 파일 |

---

## 15. 결론

본 과제에서는 MORNING DROP이라는 가상의 콜드브루 커피 브랜드를 대상으로 AI 기반 4초 광고 영상을 제작하였다. Gemini 3.1 Pro로 기획과 프롬프트를 설계하고, GPT Image 2로 키비주얼을 사전 검토한 뒤, OpenAI Sora 2로 최종 통합 광고 영상을 생성하였다.

최종 영상은 Sora 2에서 생성한 원본 MP4를 사용하였으며, 영상 자체에 영어 오디오가 포함되어 있어 별도 TTS 합성 없이 시각 요소와 청각 요소를 모두 포함한 광고 영상으로 완성되었다. 또한 인물 얼굴을 제외하고 손, 노트북, 커피, 제품 보틀 중심으로 구성하여 캐릭터 일관성 문제를 줄였다.

결과적으로 본 제작 과정은 기획 의도 → 프롬프트 설계 → 키비주얼 검토 → Sora 통합 영상 생성 → 최종 광고 영상 제출로 이어지는 현실적인 멀티모달 콘텐츠 제작 파이프라인을 보여준다.
