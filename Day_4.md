## 1. 기초 문법

#### 제어문

1. 조건문
2. 반복문

- Python은 기본적으로 위에서부터 아래로 차례대로 명령을 수행
- 특정 상황에 따라 코드를 선택적으로 실행하거나 계속하여 실행하는 제어가 필요함
- 제어문은 순서도로 표현이 가능
<br>
<br>

## 2. 조건문

- 조건문은 참/거짓을 판단할 수 있는 조건식과 함께 사용
- 조건에는 참/거짓에 대한 조건식
  - 조건이 참인 경우 이후 들여쓰기 되어있는 코드 블록을 실행
  - 이외의 경우 else 이후 들여쓰기 되어있는 코드 블록을 실행
    - else:는 선택적으로 활용할 수 있다

#### 복수 조건문

- 복수의 조건식을 활용할 경우 elif를 활용하여 표현한다
```python
dust = 80

if dust > 150:
    print('매우나쁨')
elif dust > 80:
    print('나쁨')
elif dust > 30:
    print('보통')
else:
    print('좋음')

print('미세먼지 확인 완료!')
```

#### 중첩 조건문

- 조건문은 다른 조건문에 중첩되어 사용될 수 있다
  - 들여쓰기에 유의하여 작성할 것
```python
if 조건:
    # code comes here
    if 조건:
        # code comes here
else:
    # code comes here
```

#### 조건 표현식

- 조건 표현식이란?
  - 조건 표현식을 일반적으로 조건에 따라 값을 정할 때 활용
  - 삼항 연산자로 부르기도 한다

> `true인 경우 값` if `조건` else `false인 경우 값`

<br>
<br>

## 3. 반복문

- 특정 조건을 만족할 때까지 같은 동작을 계속 반복하고 싶을 때 사용

#### 반복문의 종류

1. while 문
     - 종료 조건에 해당하는 코드를 통해 반복문을 종료시켜야 한다
2. for 문
     - 반복가능한 객체를 모두 순회하면 종료
3. 반복 제어
     - break, continue, for-else

#### while 문

- while문은 조건식이 참인 경우 반복적으로 코드를 실행
  - 조건이 참인 경우 들여쓰기 되어 있는 코드 블록이 실행
  - 코드 블록이 모두 실행되고, 다시 조건식을 검사하며 반복적으로 실행
  - while문은 무한 루프를 하지 않도록 종료 조건이 반드시 필요

#### 복합 연산자

- 복합 연산자는 연산과 할당을 합쳐 놓은 것

#### for 문

- for 문은 시퀀스를 포함한 군회 가능한 객체의 요소를 모두 순회
  - 처음부터 끝까지 모두 순회하므로 별도의 종료 조건이 필요하지 않다
- Iterable
  - 순회할 수 있는 자료형
  - 순회형 함수
  

#### 반복문 제어

- break
  - 반복문을 종료
- continue
  - continue 이후의 코드 블록은 수행하지 않고, 다음 반복을 수행
- for-else
  - 끝까지 반복문을 실행한 이후에 else문 실행
    - break를 통해 중간에 종료되는 경우 else문은 실행되지 않는다
- pass 아무것도 하지 않는다
  
## 4. 함수
> 함수를 왜 사용할까

1. 분해
    - 기능을 분해하고 재사용 가능하게 만들기 위해서
2. 추상화
    - 복잡한 내용을 모르더라도 사용할 수 있도록

#### 함수 종류

- 함수는 크게 3 가지로 분류
  - 내장 함수
  - 외장 함수
  - 사용자 정의 함수

#### 함수 정의

- 특정한 기능을 하는 코드의 조각
- 특정 코드를 매번 다시 작성하지 않고, 필요시에만 호출하여 간편히 사용

#### 함수 기본 구조

- 선언과 호출
- 입력
- 문서화
- 범위
- 결과값
  
#### 선언과 호출

- 함수의 선언은 **def 키워드**를 활용한다
- 들여쓰기를 통해 **Function body**를 작성한다
- 함수는 **parameter**를 넘겨줄 수 있다
- 함수는 동작 후에 return을 통해 결과값을 반환한다


#### 함수의 결과값

- Void function
  - 명시적인 return 값이 없는 경우, None을 반환하고 종료
- Value returning function
  - 함수 실행 후, return문을 통해 값 반환
  - return을 하게 되면, 값 반환 후 함수가 바로 종료
  
#### 튜플을 활용한 2 개 이상의 값 반환

- 반환 값을 튜플 사용
- return X -> None
- return O -> 하나를 반환
  - 여러개의 반환을 원하면 튜플을 활용

#### 함수의 입력

- Parameter
  - 함수를 정의할 때 함수 내부에서 사용되는 변수
- Argument
  - 함수를 호출할 때 넣어주는 값
  - Argument는 소괄호 안에 할당 func_name(argument)
    - 필수 Argument: 반드시 전달되어야 하는 argument
    - 선택 Argument: 값을 전달하지 않아도 되는 경우는 기본값이 전달

#### 정해지지 않은 여러 개의 Argument 처리
> print 함수의 Arguments 개수가 변해도 잘 동작하느 이유는?<br>
> Asterisk 혹은 언패킹 연산자라고 불리는 덕분이다.

#### 가변 인자(*args)

- 여러 개의 Positional Argument를 하나의 필수 parameter로 받아서 사용
- 몇 개의 Positional Argument를 받을지 모르는 함수를 정의할 때 유용


#### 패킹 / 언패킹

- 가변 인자를 이해하기 위해서는 패킹, 언패킹을 이해해야 한다
- 패킹
  - 여러 개의 데이터를 묶어서 변수에 할당하는 것
  ```python
  numbers = (1, 2, 3, 4, 5) # 패킹
  print(numvers) # (1, 2, 3, 4, 5)
  ```
- 언패킹
  - 시퀀스 속의 요소들을 여러 개의 변수에 나누어 할당하는 것
  ```python
  numbers = (1, 2, 3, 4, 5)
  a, b, c, d, e = numbers # 언패킹
  print(a, b, c, d, e) # 1 2 3 4 5
  ```
  - 언패킹시 변수의 개수와 할당하고자 하는 요소의 갯수가 동일해야한다
  - 언패킹시 왼쪽의 변수에 asterisk(*)를 붙이면, 할당하고 남은 요소를 리스트에 담을 수 있다

#### Asterisk

- *는 시퀀스 언패킹 연산자라고도 불리며, 말 그대로 시퀀스를 풀어 헤치는 연산자
  - 주로 튜플이나 리스트를 언패킹하는데 사용
  - *를 활용하여 가변 인자를 만들 수 있다.
```python
def func(*args):
    print(args)
    print(type(args))

func(1, 2, 3, 'a', 'b')
'''
(1, 2, 3, 'a', 'b')
<class 'tuple'>
'''
```

#### 가변 키워드 인자(*kwargs)

- 몇 개의 키워드 인자를 받을지 모르는 함수를 정의할 때 유용
- **kwargs는 **딕셔너리로 묶여 처리**

## 5. Scope

- 함수는 코드 내부에 local scope를 생성하며, 그 외의 공간인 global scope로 구분
- scope
  - global scope: 코드 어디에서든 참조할 수 있는 공간
  - local scope: 함수가 만든 scope. 함수 내부에서만 참조 가능
- variable
  - global variable: global scope에 정의된 변수
  - local variable: loacl scope에 정의된 변수

#### 변수의 Lifecylce

- 변수는 각자의 수명주기가 존재
  - built-in scope
    - python이 실행된 이후부터 영원히 유지
  - global scope
    - 모듈이 호출된 시점 이후 혹은 인터프리터가 끝날 때까지 유지
  - local scope
    - 함수가 호출될 때 생성되고, 함수가 종료되는 시점까지 유지

#### 이름 검색 규칙

- python에서 사용되는 이름들은 namespace에 저장되어 있다
- 아래와 같은 순서로 이름을 찾아나가며, LEGB Rule이라고 부른다
  - Local scope
  - Enclosed scope
  - Global scope
  - Built-in scope
- **함수 내에서는 바깥 Scope의 변수에 접근 가능하나 수정은 할 수 없다**

#### global 문

- 현재 코드 블록 전체에 적용되며, 나열된 식별자가 global variable임을 나타낸다
  - global에 나열된 이름은 같은 코드 블록에서 global 앞에 등장할 수 없다
  - global에 나열된 이름은 parameter, for 루프 대상, 클래스/함수 정의 등으로 정의되지 않아야 한다

#### nonlocal

- global을 제외하고 가장 가까운 scope의 변수를 연결하도록 한다
  - nonlocal에 나열된 이름은 같은 코드 블록에서 nonlocal 앞에 등장할 수 없다
  - nonlocal에 나열된 이름은 parameter, for 루프 대상, 클래스/함수 정의 등으로 정의되지 않아야 한다
- global과는 달리 이미 존재하는 이름과의 연결만 가능하다
  
#### 함수의 범위 주의

- 기본적으로 함수에서 선언된 변수는 Local scope에 생성되며, 함수 종료 시 사라진다
- 해당 scope에 변수가 없는 경우 LEGB Rule에 의해 이름을 검색한다
  - 변수에 접근은 가능하지만, 해당 변수를 수정할 수는 없다
  - 값을 할당하는 경우 해당 scope의 namespace에 새롭게 생성되기 때문이다
  - **단, 함수 내에서 필요한 상위 scope 변수는 argument로 넘겨서 활용할 것**
- 상위 scope에 있는 변수를 수정하고 싶다면 global, nonlocal 키워드를 활용 가능
  - 단, 코드가 복잡해지면서 변수의 변경을 추적하기 어렵고, 예기치 못한 오류가 발생
  - 가급적 사용하지 않는 것을 권장하며, **함수로 값을 바꾸고자 한다면 항상 argument로 넘기고 리턴값을 사용하는 것을 추천**

#### 함수 응용
- 내장 함수
  - Python 인터프리터에는 항상 사용할 수 있는 많은 함수와 형이 내장되어 있다
- map
  - 순회 가능한 데이터구조의 모든 요소에 함수 적용하고, 그 결과를 map object로 반환
- filter
  - 순회 가능한 데이터구조의 모든 요소에 함수 적용하고 그 결과가 True인 것들을 filter object로 반환
- zip
  - 복수의 iterable을 모아 튜플을 원소로 하는 zip object를 반환
- lambda 함수
  - 표현식을 계산한 결과값을 반환하는 함수로, 이름이 없는 함수여서 익명함수라고도 불림
  - return문을 가질 수 없다
  - 간편 조건문 외 조건문이나 반복문을 가질 수 없다
  - 함수를 정의해서 사용하는 것보다 간결하게 사용 가능
  - def를 사용할 수 없는 곳에서도 사용 가능
- 재귀 함수
  - 자기 자신을 호출하는 함수
  - 무한한 호출을 목표로 하는 것이 아니며, 알고리즘 설계 및 구현에서 유용하게 활용
  - 1개 이상의 base case가 존재하고, 수렴하도록 작성

## 모듈

- 합, 평균, 표준편차, ... 자주 쓰는 기능을 하는 코드를 python 파일 단위로 작성한 것
  
#### 모듈과 패키지

- 모듈
  - 다양한 기능을 하나의 파일에 담음
- 패키지
  - 다양한 파일을 하나의 폴더에 담음
- 라이브러리
  - 다양한 패키지를 하나의 묶음으로 만듦
- pip
  - 이것을 관리하는 관리자
- 가상환경
  - 패키지의 활용 공간

#### Python 표준 라이브러리

- [Python에 기본적으로 설치된 모듈과 내장 함수](https://docs.python.org/ko/3/library/index.html)
  
## 패키지

- 특정 기능과 관련된 여러 모듈의 집합
- 패키지 안에는 또 다른 서브 패키지를 포함

#### 패키지 만들기

- 계산 기능이 들어간 calculator 패키지를 아래와 같이 구성
  - check.py에서 calculator의 tools.py의 기능을 사용
    ```
    ▿ my_package
      ▿ calculator
        🦋__init__.py
        🦋tools.py
      🦋__init.py__
      🦋check.py
    ```

#### 모듈 만들기 - calculator

- calculator/tools.py에 add 함수와 minus 함수 작성
  ```python
  def add(num1, num2):
    return num1 + num2

  def minus(num1, num2):
    return num1 - num2
  ```
#### 모듈 활용하기 - check

- 모듈을 활용하기 위해서는 import문을 통해 가져와야 한다
  ```python
  from calculator import tools

  print(tools.add(5,3))
  # 8
  ```

#### 가상환경
>Python 표준 라이브러리가 아닌 외부 패키지와 모듈을 사용하는 경우 모두 pip를 통해 설치를 해야한다.<br>
복수의 프로젝트를 하는 경우 버전이 상이할 수 있다.<br>
이러한 경우 가상환경을 만들어 프로젝트별로 독립적인 패키지를 관리할 수 있다.<br>
특정 디렉토리에 가상환경을 만들고, 고유한 Python 패키지 집합을 가질 수 있다.
