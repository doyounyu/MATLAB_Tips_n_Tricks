# MATLAB_Tips_n_Tricks

## invfreqs()

```m:matlab.m
[num,den] = invfreqs(freqency_response,angular_velocity,num_order,den_order)
```

- ```num``` 출력할 전달함수의 분자 계수들의 배열
- ```den``` 출력할 전달함수의 분모 계수들의 배열
- ```freqency_response``` Ae^(jw) 꼴의 주파수 응답
- ```angular_velocity```r 각 주파수 응답에 해당하는 주파수 [rad/s]
- 
