# MATLAB Tips n Tricks

## invfreqs()

주파수 응답을 바탕으로 전달함수를 구해주는 함수

```m:matlab.m
[num,den] = invfreqs(freqency_response,angular_velocity,num_order,den_order)
```

- ```num``` 출력할 전달함수의 분자 계수들의 배열
- ```den``` 출력할 전달함수의 분모 계수들의 배열
- ```freqency_response``` Ae^(jw) 꼴의 주파수 응답
- ```angular_velocity```r 각 주파수 응답에 해당하는 주파수, 단위는 [rad/s]
- ```num_order``` 예상 전달함수의 분모 차수
- ```den_order``` 예상 전달함수의 분자 차수


## lsqcurvefit()

최소제곱법을 이용한 커브피팅 함수

```m:matlab.m
x = lsqcurvefit(fun,x0,t,signal)
```
함수의 해가 2.3sin(2.1x-3.8)라고 하자. 그런데 이 해가 Asin(bx-c) 꼴이라는 것을 알고, 그 A, b, c 값의 대략적인 값을 알 때 쓰는 함수이다.

- ```x``` ```fun```의 계수
- ```x0``` 커브피팅 하기 전 계수들의 초기값. "예상값" 정도로 생각하면 된다. 행렬 형태로 저장 가능.
- ```t``` 함수의 x값
- ```signal``` 실제 신호값들. (y) 값이라고 생각하면 됨.


```m:matlab.m
    fun = @(x, t) x(1)*sin(2*pi*x(2)*t-x(3));
    x0 = [2, 1.2, 1]; %각각 x(1), x(2), x(3)의 예상값
        x = lsqcurvefit(fun,x0,t,signal)

```
