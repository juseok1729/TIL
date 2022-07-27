# Proxy
- Proxy란? : 대리(대신하여 일을 처리한다)
- Proxy Server : 클라이언트와 서버간의 중계 서버로, 통신을 대리 수행하는 서버  
- Proxy의 종류
  - Forward Proxy
  - Reverse Proxy
- Load Balancer 의 역할도 한다.

#
### Forward Proxy
일반적으로 말하는 프록시는 Forward Proxy 이다.  
```text
"Proxy 서버 설정을 한다",  
"인터넷 속도 향상을 위해 Proxy 설정을...",  
"테스트를 위해 Proxy 설정을...",  
"IP추적을 방지하기 위해 Proxy 설정을..."  
```
**특징**  
- 캐싱 : 요청에 대한 응답을 기억해놨다가 동일 요청이 들어오면 기억하고 있던 정보를 반환한다.  
-> 응답 전송시간 절약, 외부 요청 감소, 불필요한 응답 감소  
- 익명성 : 요청을 보낸 클라이언트 정보를 서버로부터 숨길 수 있다.  

서버가 받은 요청을 누가 보냈는지 알지 못하게 한다.  
-> 요청을 한 클라이언트가 누군지 모르게 한다, 서버가 받은 요청 IP = Proxy IP  

#
### Reverse Proxy
**특징**
- 캐싱 : Forward Proxy 와 동일
- 보안 : 서버 정보를 클라이언트로부터 숨길 수 있다

클라이언트는 Reverse Proxy를 실제 서버라고 생각하여 요청하고,  
요청을 받은 Reverse Proxy는 자기가 알고 있는 Server에게 각각 요청을 전달한다.  
-> 실제 서버의 IP가 노출되지 않는다.  

#
### Load Balancing
: 여러 대의 서버 앞에서 요청을 분산 처리할 수 있도록 나눠주는 서비스

#
### Reference
[우아한 테크톡_제이미](https://www.youtube.com/watch?v=YxwYhenZ3BE)
