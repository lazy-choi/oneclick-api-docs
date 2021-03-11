# 개요 정보

## 1. 기본정보3223423

* 해당 가이드는 XXXXX에서 제공하는 XX**POS 연동형 API** 사용 가이드입니다.
* **XXPOS 연동형 API는** 부릉POS를 통해 실시간으로 배송 신청 및 배송 상태를 조회할 수 있는 API입니다.
* 해당 API 사용하려면 먼저 영업 담당자에게 연동 요청을 해주세요.
* 연동 요청이 확인되면, 인증에 필요한 api key / secret을 발급하여 전달드립니다. \(※ api key / secret은 데모용과 상용이 별도로 발급됩니다.\)
* 데모 테스트의 경우, 직접 테스트를 진행하실 수 있도록 테스트 도구를 제공합니다.

  ​[\[부릉POS 연동형 API\] 테스트 도구](https://www.naver.com/)​

‌

## 2. 정의 <a id="2"></a>

### 1\) 통신 프로토콜 <a id="1-1"></a>

> 본 API를 위한 통신은 HTTP 프로토콜을 이용하여 POST 방식으로 데이터를 전달합니다.

### 2\) 접속 정보 <a id="2-1"></a>

\[인증처리\] 해당 API는 사전에 제공받은 API Key와 Secret을 헤더에 셋팅후 호출해야 합니다.

| 구분 | URL |
| :--- | :--- |
| 테스트 접속 URL | [https://xxx-xxxx.meshxxxxx.com](https://xxx-xxxx.meshxxxxx.com) |
| 실서버 접속 URL | [https://xxx.meshxxxxx.com](https://xxx.meshxxxxx.com) |

### 3\) 메시지 포맷 <a id="3-1"></a>

본 연동 API의 Request, Response Data는 header영역과 JSON 형태의 payload 를 지정하는 data 영역으로 구성되며, UTF-8을 기본 Character Set 으로 합니다.‌

### 4\) 권장 사항 <a id="4"></a>

실시간 조회를 통한 갱신 주기를 1분 이상으로 권장합니다.‌

## 3. 헤더 <a id="3"></a>

| 타입 | 길 | Key | Value | 비고 |
| :--- | :--- | :--- | :--- | :--- |
| String | 16 | Content-type | application/json | ​Content |
| String | 40 | apikey | blablalblalblalblalblalblakey | XXXXX로부터 발급받은 API Key |
| String | 40 | secret | blablalblalblalblalblalblakeysecretsecret | XXXXX로부터 발급받은 secret |
| String | 4 | Accept-Encoding | gzip | 클라이언트 프로그램이 gzip 인코딩 방식을 지원하지 않는다면 보내지 않아도 됩니다. |

