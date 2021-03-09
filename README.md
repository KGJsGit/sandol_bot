<img src = "https://github.com/koptimizer/kakaotalk_chatbot_sandol/blob/master/pics/sandol.jpg">

## 🤖 한국산업기술대학교 챗봇 산돌이
```
안녕하세요! 한국산업기술대학교 챗봇 산돌이입니다!
교내외 학식메뉴, 셔틀시간표, 학교 날씨, 인근역 막차 시간표 등 다양한 정보를 제공합니다!
```
- 개발 및 디자인 : 고광종
  - Github = https://github.com/koptimizer
  - Email = rhkswhdwkd@naver.com // ilovecoding@kakao.com
- 카카오톡 친구추가 URL : http://pf.kakao.com/_pRxlZxb/chat
- Since 20.01.03
<img src = 'https://github.com/koptimizer/kakaotalk_chatbot_sandol/blob/master/pics/cap.jpg'>
<br/>

## 교내 주간지에 소개된 산돌이 (학보 490호 6면)
<img src = "https://github.com/koptimizer/kakaotalk_chatbot_sandol/blob/master/pics/news.jpg" height = "500px">
<br/>

## 📃 작동 방식
1. 학식/외부식당의 경우 각 식당 사장님들의 고유 카카오 아이디 식별을 통해 메뉴를 업로드 받음.

2. 사용자 발화시, kakao openbuilder에서 의도를 캐치하고 해당 AWS lambda로 구현된 skil을 통해 해당 내용을 파싱해서 response

3. 사용자 발화 의도를 캐치하지 못하면, 도움말 바로가기 버튼을 생성해줌으로서 사용자 편의성 고려

4. 산돌이 관련 질문은 Issue에 남겨주세요!
<br/>


## 🔎 구현 상황(20.06.13)
- [x] 셔틀 시간표 조회(img)
- [x] 금일 학식 및 외부 식당 식단 조회
    - [x] 썬푸드 학식
    - [x] E동 식당
    - [x] TIP 한식당
    - [x] 세미콘
    - [x] 미가
- [x] 요일별 인근역(정왕역, 오이도역) 막차 시간 조회
- [ ] 인근정류장 및 전철역의 실시간 상황 조회
- [x] 금일 정왕동 날씨 조회
- [x] 학교 시설물 및 장소 조회
    - [x] 공부 및 스터디장소
    - [x] 휴게장소
    - [x] 큐브 위치
- [x] 학교 내선번호 안내
- [x] 대학로 추천
    - [x] KPU World 적용
- [ ] 학교 공지 조회 (적용 검토중)
    - [x] 학사공지 
- [ ] 게임 정보 조회 (적용 검토중)
    - [x] LoL 인게임 전적 및 티어조회
    - [x] MapleStory 인게임 캐릭터 정보 및 룩 조회
- [x] 후원 및 건의
    - [] 산돌이 건의
    - [x] 후원 등록
<br/>

## 🔧 이슈 사항(21.01.08)
- 크롤링해야하는 대부분의 정보(셔틀, 교내학식 등)가 flash기반으로 웹에 표현되서 해당 정보는 크롤링이 아예 안됨.
  - 셔틀은 어짜피 자주 바뀌는 항목이 아니니 내가 수동으로 입력
  - 학식은 일주일 단위로 식단표가 나오니 1주일에 한번씩 수동으로 개인 홈페이지에 올리고 크롤링.
- 외부 식당끼리의 메뉴 조회 금지 및 식단 수정기능 필요
  - 외부식당 사장님이 '학식조회' 관련 발화을 하면 고유 ID를 식별해서 타 외부 식당을 제외하고 출력하도록 함
  - 위의 기능을 조금 수정해서 메뉴수정의 기능 추가
- NLP 발화 추가 이슈 고민...
<br/>

## 🎓 챗봇강좌문의
- rhkswhdwkd@naver.com
