## SSAFY Start Camp 챗봇 퀘스트

광주_1반 박나원, https://github.com/nnnangni 





## Ⅰ. 스펙(Specification)

구현된 어플리케이션의 주요 기능 (텔레그램을 이용한 챗봇만들기)

(1) 앵무새 기능

- 유저가 입력한 데이터 가져오기

  ex)  "안녕하세요"라고 입력하면 똑같이 "안녕하세요" 반환

(2) 로또번호 추천

- 랜덤 모듈을 이용해 1~45 사이의 숫자를 샘플링하여 중복 방지 숫자 6개를 선택함.
- "로또"라고 입력하면 "[2, 20, 22, 35, 38, 45]"를 반환 (입력할 때마다 다시 뽑아서 리스트를 보냄)

(3) 번역 기능

- 네이버 API를 이용해 한글을 영어로 번역
- 번역 안녕하세요 => 번역이 실행되도록 만들기(조건문)
- "번역 명작" → "masterpiece" 반환
- text(유저가 입력한 데이터)의 맨 앞 두글자가 '번역'인지를 확인

(4) 사진 분석 기능

- 사용자가 이미지를 넣었는지 체크함.

- 사진을 네이버 유명인인식 api로 넘겨주고 text로 보내줌.
- 가져온 데이터 중에서 필요한 정보 빼오기(인식이 되었을 때/인식이 되지 않았을 때)

## Ⅱ. 회고(Retrospective)

어플리케이션 구현 과정에서의 어려움과 문제점

- flask를 사용할때 처음 넣어야하는 import가 헷갈림.
- 텔레그램의 토큰을 받는 과정이 헷갈림.
- os.getenv 환경변수를 사용하여 비밀번호를 비밀설정하는 부분이 어려웠음.

- 외부 API를 활용할 때 네이버를 사용하며 생소한 환경설정으로 사용 래퍼런스를 찾아서 해야 했던것이 어려움. 과연 혼자서 할 수 있을지....
- API로 json 데이터를 받아 파싱하는 과정에서 json에 대한 지식 부족으로 어려움.

## Ⅲ. 보완 계획(Feedback)

현재 미완성이지만 추가로 구현할 기능 및 기존 문제점 보완 계획

- 번역챗봇 구현과정에서 번역 뒤에 번역의 글자가 다시 나오면 봇 자체에서 인식이 힘든지 제대로 번역되지 않거나 아예 말이 빠지는 경우가 발생

