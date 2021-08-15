# Pixel Font Maker
![](.github/screenshot.PNG)

픽셀 폰트를 디자인하고 TTF 파일로 뽑을 수 있는 프로그램입니다.

## 조작
### 보드
- mouse (left|right) (칠하기, 지우기)
- keyboard (left|right|up|down) (보드 이동)
- ctrl+(z|x|c|v) (되돌리기, 자르기, 복사, 붙여넣기)
- ctrl+s (프로젝트 저장)
- (1|2|3) (브러시 크기 조절)
### 기타
- Components에서 컴포넌트를 좌클릭하면 해당 컴포넌트를 편집합니다. 우클릭하면 해당 컴포넌트를 지울 수 있습니다.

## 프로젝트 속성
- Descent : baseline 기준으로 가장 아래쪽까지의 길이
- Ascent : baseline 기준으로 가장 위쪽까지의 길이
- WidthType
  - Monospace : 모든 글리프가 너비가 Fixed-Width의 배수가 되도록 설정됩니다.
  - Proportional : 글리프의 너비가 (가장 오른쪽에 있는 픽셀까지의 X거리) + (Letter Spacing) 가 되도록 설정됩니다.
  - 위의 규칙과 다르게 너비를 설정하고 싶다면 에디터 하단에 Advance Width를 클릭해서 설정하면 됩니다.

## 한글 폰트 작성법 & 한글 템플릿
한글 템플릿을 사용하면 모든 한글 글자 (11172자) 를 하나하나 찍는 대신 형태에 맞게 초성, 중성, 종성을 따로 찍어 조합하는 식으로 작업량이 줄어듭니다. (172개 또는 344개 자모만 찍으면 됩니다.)

1. 프로젝트를 만들 때 한글 템플릿을 선택 (자모 컴포넌트가 `Private Set` 글리프셋에서 생성됩니다.)
2. `Korean Syllable (모든 11172자)` 또는 `KS X 1001 Korean Syllable (자주 쓰는 2350자)` 글리프셋을 선택
3. Components 에서 자모 컴포넌트를 선택해서 그리기

템플릿은 [여기](https://github.com/TandyRum1024/hangul-johab-render-gms#%EA%B8%80%EA%BC%B4-%EA%B4%80%EB%A0%A8)서 가져왔습니다.

### ZIK님 템플릿
- 초성 4벌, 중성 2벌, 종성 2벌 `(4*19 + 2*21 + 2*27) = 172자`
- 초성 : 총 4벌 (4줄)
    - 1벌 : 받침 있고 중성 `[ㅏ ㅐ ㅑ ㅒ ㅓ ㅔ ㅕ ㅖ ㅣ]` 와 결합 (EX : `먄, 먠, 미`)
    - 2벌 : 받침 있고 중성 `[ㅗ ㅘ ㅙ ㅚ ㅛ ㅜ ㅝ ㅞ ㅟ ㅠ ㅡ ㅢ]` 와 결합 (EX : `옹, 왱, 융`)
    - 3벌 : 받침 없고 중성 `[ㅏ ㅐ ㅑ ㅒ ㅓ ㅔ ㅕ ㅖ ㅣ]` 와 결합 (EX : `개, 네, 아`)
    - 4벌 : 받침 없고 중성 `[ㅗ ㅘ ㅙ ㅚ ㅛ ㅜ ㅝ ㅞ ㅟ ㅠ ㅡ ㅢ]` 와 결합 (EX : `오, 뇌, 위`)
- 중성 : 총 2벌 (2줄)
    - 1벌 : 받침 있는 글자의 중성부분 (EX : `감, 괨, 굼`)
    - 2벌 : 받침 없는 글자의 중성부분 (EX : `오, 우, 야`)
- 종성(받침) : 총 2벌 (2줄)
    - 1벌 : 중성 `[ㅏ ㅐ ㅑ ㅒ ㅓ ㅔ ㅕ ㅖ ㅣ]` 와 결합 (EX : `펭, 귄, 웱`)
    - 2벌 : 중성 `[ㅗ ㅘ ㅙ ㅚ ㅛ ㅜ ㅝ ㅞ ㅟ ㅠ ㅡ ㅢ]` 와 결합 (EX : `뫔, 뭄, 밈`)

### 도깨비한글 8x4x4벌식 글꼴
- 초성 8벌, 중성 4벌, 종성 4벌 `(8*19 + 4*21 + 4*27) = 344자`
- 초성 : 총 8벌 (8줄)
    - 1벌 : 받침없는 `[ㅏ ㅐ ㅑ ㅒ ㅓ ㅔ ㅕ ㅖ ㅣ]` 와 결합
    - 2벌 : 받침없는 `[ㅗ ㅛ ㅡ]`
    - 3벌 : 받침없는 `[ㅜ ㅠ]`
    - 4벌 : 받침없는 `[ㅘ ㅙ ㅚ ㅢ]`
    - 5벌 : 받침없는 `[ㅝ ㅞ ㅟ]`
    - 6벌 : 받침 ***있는*** `[ㅏ ㅐ ㅑ ㅒ ㅓ ㅔ ㅕ ㅖ ㅣ]` 와 결합
    - 7벌 : 받침있는 `[ㅗ ㅛ ㅜ ㅠ ㅡ]`
    - 8벌 : 받침있는 `[ㅘ ㅙ ㅚ ㅢ ㅝ ㅞ ㅟ]`
- 중성 : 총 4벌 (4줄)
    - 1벌 : 받침없는 `[ㄱ ㅋ]` 와 결합 (EX : `괴, 가, 큐, 캬`)
    - 2벌 : 받침없는 `[ㄱ ㅋ]` 이외의 자음과 결합 (EX : `외, 나, 류, 먀`)
    - 2벌 : 받침 ***있는*** `[ㄱ ㅋ]` 와 결합 (EX : `광, 쾅, 굉, 괽`)
    - 3벌 : 받침있는 `[ㄱ ㅋ]` 이외의 자음과 결합 (EX : `웅, 얅, 약, 약`)
- 종성 : 총 4벌 (4줄)
    - 1벌 : 중성 `[ㅏ ㅑ ㅘ]` 와 결합
    - 2벌 : 중성 `[ㅓ ㅕ ㅚ ㅝ ㅟ ㅢ ㅣ]`
    - 3벌 : 중성 `[ㅐ ㅒ ㅔ ㅖ ㅙ ㅞ]`
    - 4벌 : 중성 `[ㅗ ㅛ ㅜ ㅠ ㅡ]`