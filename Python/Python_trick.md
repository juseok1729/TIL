# 파이썬 트릭

### switch 구현
파이썬 함수는 객체이며, 다른 객체와 같이 리스트의 항목으로 집어넣을 수 있다.  
그렇다면 함수 참조를 리스트에서 추출해 호출할 수 있다.  
```python
fn = [func1, func2, func3, func4, func5][n-1]
fn(arg)
```
위 코드에서 n 에 1이 들어가면 index 0번의 `func1`이 실행된다.  
n의 값에 따라 다른 함수를 호출하는 switch문을 구현했다.  
장황한 if-elif 문으로 구현할것을 간결하게 구현할 수 있다.  


### 함수 테이블
함수들을 딕셔너리와 조합하면 유연하게 제어할 수 있다.  
이는 다음과 같이 switch 문과 동일하게 구현할 수 있다.  
```python
menu = {'load': load_func, 'save': save_func, 'exit': exit_func, 'update': update_func}
menu['load']()
```
