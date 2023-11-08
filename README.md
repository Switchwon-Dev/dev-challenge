# Switchwon dev-challenge
안녕하세요. 지원자님

스위치원이란 작은 회사의 큰 꿈을 보시고 입사 지원을 해주셔서 대단히 감사합니다.

저희가 준비한 문제를 재밌게 작업하시기 전에 지원자님의 github에서 해야 할 일이 있습니다. 아래를 읽고 따라해주세요.

# 주의 사항
- 문제를 공유하지 말아주세요.
- 블로그나 SNS 등에 본인의 답과 풀이 방법을 올리지 말아주세요.
- 제출 날짜는 본 문제 링크가 적힌 메일을 받은 시각에 일주일(168시간)을 더한 시간까지 입니다.
- 예) 2023년 9월 15일 13시에 메일을 받으셨다면 정확히 2023년 9월 22일 13시까지가 제출 마감기한입니다.

# 개발 전 해야 할 일
- 지원자님의 github에서 신규 repository를 private 로 만들어 주시기를 바랍니다.
- repo 이름은 아무거나 상관없습니다.

그 뒤, 아래의 요구사항을 잘 읽고 개발을 하신 후에 저희에게 코드를 제출하신다면 아래를 읽고 따라해 주시기를 바랍니다.
# 결과물 제출 방법
- github setting -> Collaborators -> Manage access 에서 Add people 을 누르시고 `switchwon-tech` 또는 `tech@switchwon.com` 을 추가해 주시면 제출됩니다.
- 또한 결과물을 앱에서 구현한 영상 파일이나 링크를  `tech@switchwon.com` 로 송부해주세요. 송부 시 Git ID 를 메일에 함께 적어주세요.

그럼 즐거운 시간 되시길 바라겠습니다. :)

# 문의
작업하다가 궁금하신 부분이 있으면 `tech@switchwon.com` 으로 이메일을 보내주세요.

---

# 과제 설명
스위치원은 환전 서비스로 환율 정보를 고객에게 보여주는 것이 매우 중요한 기능 중 하나입니다.
아래의 api 에 call 하여 얻는 정보를 그래프로 보여주고 날짜를 누르면 그 날의 환율정보를 보여주는 앱을 작성해 주세요.

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
* 두 개의 fragment 를 그릴 거에요. 하나는 환율 그래프이고 하나는 환율 리스트에요.
### 환율 그래프
* 환율 list 를 json으로 받아 그래프에 환율이 보이게 해주세요.
	* x 축은 시간, y 축은 환율이에요 (그림 참조)
	* x 축의 시간은 9시부터 15시까지만이에요.
* 그래프를 그리기 위한 라이브러리는 자유롭게 선택해서 사용해 주세요.
* 그래프 위에 USD, JPY, EUR 버튼을 만들어 주세요.
	* 각 환율의 버튼을 누르면 현재 보이던 날짜의 선택된 환율을 보여주세요.
* 리스트로 보기 버튼을 만들어 주세요.
	* 버튼을 누르면 환율 리스트 fragment로 이동해 주세요.
	* 이동 시 현재 환율의 리스트를 보여주세요.
* 날짜를 text로 보여주세요.
	* 날짜의 초기값은 2023-09-04 이며 이후에는 환율 리스트에서 선택한 날짜를 보여주세요.

![환율 그래프](https://switchwon.s3.ap-northeast-2.amazonaws.com/switchwon-test-1.png)
### 환율 리스트
* 환율 그래프에서 선택한 국가환율을 리스트로 보여주세요.
* 날짜를 선택하는 drop-down 버튼을 만들어 주세요.
	* 날짜는 2023년 9월 4일부터 9월 8일까지예요.
	* 리스트에 보이는 환율 시간은 9시부터 15시까지예요.
	* 버튼을 눌러 날짜를 선택하면 리스트가 변하게 해주세요.
* 상단에 뒤로 가기 버튼을 만들어 주세요.
	* 뒤로 가기 버튼을 누르면 환율 리스트 fragment 에서 선택한 날짜의 환율이 그래프에 보이도록 해주세요.
* 리스트 순서는 시간의 역순 (DESC) 으로 보여주세요.

![환율 리스트](https://switchwon.s3.ap-northeast-2.amazonaws.com/switchwon-test-2.png)
### 공통
* 실제 협업을 하듯 Git commit 의 분리와 commit message를 충실히 작성해주세요.
* 가독성이 높게 작성해 주세요.
* 그 외에 모든 부분은 자유롭게 구현해 주시면 됩니다.

## 보너스!
* 테스트코드 추가 시 가산점이 있습니다!
