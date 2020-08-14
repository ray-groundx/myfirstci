##  Getting Started with Klaytn Node API
### Account Pool, Account 생성하기
#### Account Pool 생성
Account Pool 개요 설명 1~2줄 (Account Pool 자체도 여러 개 생성할 수 있다는 설명이 들어가야 함)  
Account Pool 생성 목록 화면 이미지  
Account Pool 생성 방법 설명 1~2줄  
생성된 Account Pool 확인하는 화면 이미지  
   
이 문서 혹은 KAS에 관한 문의는 [개발자 포럼 링크](https://forum.XXX 제품 도메인.com/)를 방문해 도움을 받으십시오.  

#### Account 생성
Account 개요 설명 1줄  
Account 생성 목록 화면 이미지  
Account 생성 방법 설명 1~2줄  
생성된 Account 확인하는 화면 이미지  
   
이 문서 혹은 KAS에 관한 문의는 [개발자 포럼 링크](https://forum.XXX 제품 도메인.com/)를 방문해 도움을 받으십시오.  

### Klaytn Node API 호출하기
#### Account 선택
Account 목록 화면 이미지  
Account 선택 방법 설명 1줄  
Account 선택 메뉴 이미지  
Account ID 설명 1~2줄  
   
이 문서 혹은 KAS에 관한 문의는 [개발자 포럼 링크](https://forum.XXX 제품 도메인.com/)를 방문해 도움을 받으십시오.  

#### X-KRN 정의
x-account-id에 위에서 선택한 Account ID 입력하는 내용 설명 1~2줄  
x-krn 설정할 때 필요한 내용들 소개 3~4줄  
자세한 내용은 [다음](Basics - X-KRN 섹션 링크)을 확인하십시오.  
   
(완성된 API 호출 헤더 예시를 씁니다.)
```text
-u ${your_accessKeyId}:${your_secretAccessKey} \
--header 'x-krn: krn:1001:node' \
--header 'Content-Type: application/json' \
```
   
이 문서 혹은 KAS에 관한 문의는 [개발자 포럼 링크](https://forum.XXX 제품 도메인.com/)를 방문해 도움을 받으십시오.  

#### API 호출
API 호출 방법 설명 1~2줄  
   
(Klaytn Node API 호출 예시를 씁니다.)
{% tabs %}
{% tab title="curl" %}
```text
curl --location --request POST 'https://node-api.beta.klaytn.io/v1/klaytn' \
-u ${your_accessKeyId}:${your_secretAccessKey} \
--header 'x-krn: krn:1001:node' \
--header 'Content-Type: application/json' \
--data-raw '{"jsonrpc":"2.0","method":"klay_blockNumber","params":[],"id":1}'
```
{% endtab %}

{% tab title="caver-js" %}
```text
const accessKeyId = "${your_accessKeyId}";
const secretAccessKey = "${your_secretAccessKey}";

const option = {
  headers: [
    {name: 'Authorization', value: 'Basic ' + Buffer.from(accessKeyId + ':' + secretAccessKey).toString('base64')},
    {name: 'x-krn', value: 'krn:<chain-id>:node'},
  ]
}

const caver = new Caver(new Caver.providers.HttpProvider("https://node-api.beta.klaytn.io/v1/klaytn", option))
```
{% endtab %}

{% tab title="caver-java" %}
```text
HttpService httpService = new HttpService("https://node-api.beta.klaytn.io/v1/klaytn");

String auth = Credentials.basic("${your_accessKeyId}", "${your_secretAccessKey}", StandardCharsets.UTF_8);
httpService.addHeader("Authorization", auth);
httpService.addHeader("x-krn", "krn:<chain-id>:node");

Caver caver = Caver.build(httpService);
```
{% endtab %}
{% endtabs %}
   
이 문서 혹은 KAS에 관한 문의는 [개발자 포럼 링크](https://forum.XXX 제품 도메인.com/)를 방문해 도움을 받으십시오.  

#### API 응답
API 응답 결과 설명 1~2줄  
   
(아래와 같이 Klaytn Node API 응답 예시를 씁니다.)
{% tabs %}
{% tab title="curl" %}
```text
sdfsdfsdf
```
{% endtab %}

{% tab title="caver-js" %}
```text
sdfsdfsdf
```
{% endtab %}

{% tab title="caver-java" %}
```text
sdfsdfsdf
```
{% endtab %}
{% endtabs %}
   
이 문서 혹은 KAS에 관한 문의는 [개발자 포럼 링크](https://forum.XXX 제품 도메인.com/)를 방문해 도움을 받으십시오.  