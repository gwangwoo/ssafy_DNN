# ssafy_DNN
Deep learning study

1강

### 퍼셉트론(인공뉴런) : 1957년에 고안된 알고리즘

### 퍼셉트론은 딥러닝(신경망)의 기원이 되는 알고리즘

### 퍼셉트론은 다수의 신호를 입력받아 하나의 신호를 출력한다.

### 여기서 신호는 전류나 물의 흐름을 생각해 볼 수 있다.

### 신호의 흐름을 표현할 때 두가지값을 갖는데 0,1의 값을 갖는다.
### 0은 안흐른다. 1은 신호가 흐른다.

[ 퍼셉트론 식 ]

w1 * x1 + w2 * x2 ≤  Ø
w1 * x1 + w2 * x2  > Ø

x1,x2는 압력신호, y는 출력신호, w1,w2는 가중치를 의미한다.
(w는 weight를 의미) Ø는 임계값

w1 * x1 + w2 * x2 값이 임계값 이하 일때는 0
아닐 때는 1

가중치가 클수록 해당신호가 강해진다

[ 논리 회로 ]
 * AND 게이트 진리표
------------------
x1  	  x2	y
0	0	0
0	1	0
1	0	0
1	1	1
입력이 모두 1일때만 1을 출력한다.

퍼셉트론으로 AND게이트를 표현하고자 할 때는 w1, w2, Ø 값을 어떤 값으로 설정할 것인지 생각해 봐야 한다.

AND게이트를 만족하는 w1,w2,Ø의 조합은 무수히 많다.

 * NAND 게이트 진리표
x1	x2	y
0	0	1
0	1	1
1	0	1
1	1	0

 * OR 게이트 진리표
x1	x2	y
0	0	0
0	1	1
1	0	1
1	1	1

퍼셉트론 표현할 때는 가중치와 임계값을 설정하여 표현할 수 있다.

이 매개변수의 값(w, Ø)을 적절히 조절하면 AND, NAND, OR 게이트를 표현 할 수 있다.



#3강

[ 가중치와 편향을 도입한 퍼셉트론 식 ]

편향 : bias

 * 위의 퍼셉트론 식에서 Ø를 -b로 치환하면

w1 * x1 + w2 * x2 + b  으로 바꿔 줄 수 있다.

퍼셉트론은 입력신호에 가중치를 곱한 값과 편향을 합하여, 그 값이 0을 넘으면 1을 출력하고, 그렇지 않으면 0을 출력한다.


#4강

 * XOR 게이트 진리표
 
 XOR 게이트는 배타적논리합이라고 한다
 x1과 x2 중 어느 한쪽이 1일 때만 1을 출력하는 논리회로
 
 퍼셉트론으로는 XOR 게이트를 구현 할 수 없다.
 
 직선 하나로는 XOR 게이트의 출력을 구분할 수 없다.(구분 불가능)
 
 퍼셉트론(단층 퍼셉트론)은 직선 하나로 나눈 영역만 표현할 수 있다는 한계가 있다.
 
 
 ![100](/img/100.jpg)
 
 
 
 하지만 시간이 지나고 비선형 그래프로 XOR문제를 풀 수 있게 된다.
 
 다층 퍼셉트론을 사용하면 나눌 수 있게 된다.
 
 ![101](/img/101.png)
 
 
 
 선형  : 직선의 영역을 선형 영역
 비선형 : 곡선의 영역을 비선형 영역
 
 
 
 
 ### 다층 퍼셉트론(Multi Layer Perceptron)
 
 기존 게이트 (AND, OR, NAND) 조합
 
 
 
