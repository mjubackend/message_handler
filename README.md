# Mesage handler 관련 예제 코드를 담고 있습니다.

## before 폴더
* network_handler.py : UDP echo server 로 JSON 을 돌려 받은 것을 가지고 if 문을 통해 메시지 타입을 구분해서 핸들러 호출. debug 모드로 들어가는 것을 매 핸들러에서 flag 를 확인해야됨을 보여줌
* network_handler.cpp : 메시지 타입이 string 이 아니라 int 인 경우를 흉내낸 것임. socket 을 붙이면 코드가 더 이해하기 어려우니 cin 으로 받은 것을 메시지 타입으로 가정하고 처리

## after 폴더
* network_handler.py : 메시지 핸들러를 등록한 뒤 debug 모드가 실행되면 핸들러를 바꿔치기 할 수 있음을 보여 줌
* network_handler2.py : 메시지 핸들러가 연속으로 chain 으로 연결되는 경우를 보여줌
* network_handler.cpp : int 형의 메시지 타입이 주어진 경우 handler 를 찾아서 함수 호출하는 것을 보여줌. C++ 의 타입 관련된 코드가 복잡하므로 이해를 돕기 위해서 handler 를 교체하는 것이나, handler 를 연속으로 붙이는 것은 생략했으나 python 의 경우와 유사하게 구현 가능
