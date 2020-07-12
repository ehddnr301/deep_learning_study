# Background

- `포지셔널은 무조건 키워드 앞으로!`

## parameter란 ? argument란 ?

- parameter : 함수를 정의할때 사용되는 변수
- argument : 함수를 사용할때 사용되는 변수

## positional? keyword?

- positional parameter : 말그대로 파라미터와 알규먼트 위치가 중요함
```
def something(a,b,c):
    return (a+b)*c

something(1,2,3)
```
- keyword : 순서가 중요하지 않고 등호를 사용함
```
def something(a,b,c):
    return (a+b)*c

something(b=2,c=3,a=1)
```

- 혼합해서 쓰려면 positional argument가 먼저 위치해야함!!!

## keyword (parameter)

```
def something(a=1, b=2, c=3):
    return (a+b)*c

something(1,2,6)   // 18
something()        // 9
```

## positional 과 keyword 혼용

```
def something(a, b=2,c=3):
    return (a+b)*c
```


## positional 만 사용할때

- `/` 를 사용합니다.
- positional only
- argument 사용시
```
def something(a,/,b=2,c=3):
    return (a+b)*c
```
- 근데 직접 정의는 불가능하고 내장함수들에 쓰였음

- 예시
```
sum([1,2,3],0)  // 6
```
- positional only 라 keyword사용 불가능

## keyword만 사용할때

- `*` 기준으로 뒤쪽은 keyword만 사용가능
- argument 사용시
```
def something(a,*,b,c=3):
    return (a+b)*c

something(1,b=2,c=3)
```

## var-positional (가변 positional)

- 무한히 많은 argument를 넣을수 있다.
- `*` 붙여줌
```
def something(a,b,*c):
    print(a)
    print(b)
    print(c)

something(1,2,3,4,5,6)
실행하면
1
2
(3,4,5,6)     // 튜플로 묶여서 c로 들어감
```

```
def something(a,b,*c):
    return (a+b)*c

something(1,2,3,4,5,6)
```
- `3 * (3,4,5,6)` 인데 그럼 `(3,4,5,6)` 이 세번 출력됨.
- (3,4,5,6,3,4,5,6,3,4,5,6)

## var-keyword (가변 keyword)

- 무한히 많은 keyword형식 argument
- `**` 붙여줌
```
def somehting(a,b,**c):
    print(a)
    print(b)
    print(c)

somehting(1,2, num1=3,num2=2,num3=4,num5=5)

// 1
// 2
// {'num1':3,'num2':2,'num3':4,'num5':5}
```

- dictionary로 묶여서 들어감