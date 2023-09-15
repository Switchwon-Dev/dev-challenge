# Switchwon dev-challenge
안녕하세요. 지원자님

스위치원이란 작은 회사의 큰 꿈을 보시고 입사지원을 해주셔서 대단히 감사합니다.

저희가 준비한 문제를 재밌게 작업하시기 전에 지원자님의 github에서 해야할 일이 있습니다. 아래를 읽고 따라해주세요.

# 주의 사항
- 문제를 공유하지 말아주세요.
- 블로그나 SNS 등에 본인의 답과 풀이방법을 올리지 말아주세요.
- 제출 날짜는 2023년 9월 22일 금요일 14시까지 입니다.

# 개발 전 해야할 일
- 지원자님의 github에서 신규 repository를 private 로 만들어주시기 바랍니다.
- repo 이름은 아무거나 상관없습니다.

그 뒤, 아래의 요구사항을 잘 읽고 개발을 하신 후에 저희에게 코드를 제출하신다면 아래를 읽고 따라해주시기 바랍니다.
# 결과물 제출 방법
- github setting -> Collaborators -> Manage access 에서 Add people 을 누르시고 `switchwon-tech` 또는 `tech@switchwon.com` 을 추가해주시면 제출됩니다.

그럼 즐거운 시간 되시길 바라겠습니다. :)

# 문의
작업하다가 궁금하신 부분이 있으면 `tech@switchwon.com` 으로 이메일을 보내주세요.

---

# 과제 설명
스위치원은 환전 서비스로 환율 정보를 고객에게 보여주는 것이 매우 중요한 기능 중 하나입니다.
아래의 api 에 call 하여 얻는 정보를 그래프로 보여주고 날짜를 누르면 그 날의 환율정보를 보여주는 앱을 작성해주세요.

## USD
`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/usd/2023-09-04`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/usd/2023-09-05`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/usd/2023-09-06`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/usd/2023-09-07`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/usd/2023-09-08`

## JPY
`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/jpy/2023-09-04`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/jpy/2023-09-05`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/jpy/2023-09-06`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/jpy/2023-09-07`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/jpy/2023-09-08`

## EUR
`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/eur/2023-09-04`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/eur/2023-09-05`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/eur/2023-09-06`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/eur/2023-09-07`

`GET https://switchwon.s3.ap-northeast-2.amazonaws.com/eur/2023-09-08`

## 개발 제약 사항
* 두 개의 fragment 를 그릴거에요. 하나는 환율 그래프이고 하나는 환율 리스트에요.
* fragment 가 전환 될 때 api call 하지 말아주세요.
### 환율 그래프
* 환율 list 를 json으로 받아 그래프에 환율이 보이게 해주세요.
	* x 축은 시간, y 축은 환율이에요 (그림 참조)
	* x 축의 시간은 9시부터 15시까지만이에요.
* 그래프를 그리기 위한 라이브러리는 자유롭게 선택해서 사용해주세요.
* 그래프 위에 USD, JPY, EUR 버튼을 만들어주세요.
	* 각 환율의 버튼을 누르면 현재 보여지고 있던 날짜의 선택된 환율을 보여주세요.
* 리스트로 보기 버튼을 만들어주세요.
	* 버튼을 누르면 환율 리스트 fragment로 이동해주세요.
	* 이동시 현재 환율의 리스트를 보여주세요.
* 날짜를 text로 보여주세요.
	* 날짜의 초기값은 2023-09-04 이며 이후에는 환율 리스트에서 선택한 날짜를 보여주세요.

![환율 그래프](https://switchwon.s3.ap-northeast-2.amazonaws.com/switchwon-test-1.png)
### 환율 리스트
* 환율 그래프에서 선택한 국가환율을 리스트로 보여주세요.
* 날짜를 선택하는 drop-down 버튼을 만들어주세요.
	* 날짜는 2023년 9월 4일부터 9월 8일까지에요.
	* 리스트에 보여지는 환율 시간은 9시부터 15시까지에요.
	* 버튼을 눌러 날짜를 선택하면 리스트가 변하게 해주세요.
* 상단에 뒤로 가기 버튼을 만들어주세요.
	* 뒤로 가기 버튼을 누르면 환율 리스트 fragment 에서 선택한 날짜의 환율이 그래프에 보여지도록 해주세요.
* 리스트 순서는 시간의 역순 (DESC) 으로 보여주세요.

![환율 리스트](https://switchwon.s3.ap-northeast-2.amazonaws.com/switchwon-test-2.png)
### 공통
* 실제 협업을 하듯 Git commit 의 분리와 commit message를 충실히 작성해주세요. branch는 main 하나만 쓰셔도 돼요.
* 가독성이 높게 작성해주세요. 이 다음 단계인 인터뷰에서 함께 논의할거에요.
* 언급되지 않은 부분은 모두 자유에요.

## 보너스!
* Unit Test 할 부분을 찾아 하시면 `+` 입니다!
