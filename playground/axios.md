## Ajax (Asynchoronous Javascript and xml)
* 비동기적으로 서버에서 데이터를 가져옴.
* 데이터 호출, 가져오기, 수정 등
* jQuery.ajax()


기존: vue-resource
- HTTP 통신 라이브러리, 지금은 사용하지 않음

# Axios
- 깃헙: https://github.com/axios/
- HTTP 통신 라이브러리, Vue에서 권장
- Promise 기반(JavaScript의 비동기 처리 패턴)


JavaScript의 비동기 처리 패턴
비동기: 특정 로직의 실행이 끝날 때까지 기다리지 않고 나머지 코드를 계속해서 실행함.
* callback: 특정 로직이 끝나면 다른 동작 실행
``` JavaScript
function getData(callbackFunc) {
	$.get('https://domain.com/products/1', function(response) {
		callbackFunc(response); // 서버에서 받은 데이터 response를 callbackFunc() 함수에 넘겨줌
	});
}

getData(function(tableData) {
	console.log(tableData); // $.get()의 response 값이 tableData에 전달됨
});
```
** 그러나, 콜백 지옥 발생할 수 있음. (콜백 안에 콜백,,) 이를 해결하려면 promise나 async, await 사용.

* promise
``` JavaScript
function getData(callback) {
  // new Promise() 추가
  return new Promise(function(resolve, reject) {
    $.get('url 주소/products/1', function(response) {
      // 데이터를 받으면 resolve() 호출
      resolve(response);
    });
  });
}

// getData()의 실행이 끝나면 호출되는 then()
getData().then(function(tableData) {
  // resolve()의 결과 값이 여기로 전달됨
  console.log(tableData); // $.get()의 reponse 값이 tableData에 전달됨
});
```
** Promise의 상태
*** Pending
*** Fulfilled
*** Rejected


* promise + generator
* async, await

