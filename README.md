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
