# 20220730

## CS STUDY
#### SOFTWARE 20&21<br></br>
#### 10억 개 전화번호에서 이름 찾기 : 이진검색
#### 검색을 쉽게 만드는 정렬 : 선택 정렬 vs 퀵 정렬


### 이진검색 Binary Search (이진탐색)
>정렬된 배열(ex 사전,전화번호부) 에서 검색 범위를 줄여 나가며 검색 값을 찾는 알고리즘   
>검색이 반복될 떄마다 검색 범위가 절반으로 줄어서 속도가 빠르다는 장점   
>정렬된 배열에만 사용할 수 있다는 단점

### 이진검색 동작방식
> 1. 배열의 중간 값을 가져옵니다.
> 2. 중간 값과 검색 값을 비교합니다.   
> 2-1. 중간 값이 검색 값과 같다면 종료합니다.   
> 2-2. 중간 값보다 검색 값이 크다면 중간값 기준 배열의 오른쪽 구간을 탐색합니다.   
> 2-3. 중간 값보다 검색 값이 작다면 중간갑 기준 배열의 왼쪽 구간을 탐색합니다.
> 3. 값을 찾거나 간격이 비어있을 때까지 반복합니다.

### 이진검색 성능
>한번 비교가 이루어질떄마다 범위가 1/2로 줄어듬   
>배열의 크기가 n, 반복 횟수 k 일때 아래와 같은 식이 만들어짐   
>n을 2로 몇번 나누어야 1이 되는지를 말해주는 식
><img src="https://velog.velcdn.com/images/hongsoom/post/18d94ff0-9d43-4727-8c81-83a7db188a2f/image.PNG" width="100" alt="이진검색 식"></img>

>### 이진검색 vs 선형검색   
>배열 {1,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59} 에서 37 찾기
<img src="https://velog.velcdn.com/images/hongsoom/post/32334a8a-e6f2-4004-8b7e-fd6123e37a5b/image.gif" width="1000" alt="이진검색"></img>
>크기가 n인 배열에서  이진검색을 통해선 O(log2 n), 선형검색을 통해서는 최대 O(n)
> 
>>빅오 표기법(Big-O Notation)   
>>알고리즘의 효울성을 표기해주는 표기법   
>>보통 알고리즘의 시간 복잡도와 공간 복잡도를 나타내는데 주로 사용

### 선택정렬 
>배열의 모든 요소를 앞에서부터 차례대로 이미 정렬된 배열 부분과 비교하여 자신의 위치를 찾아서 삽입하는 방식
>주어진 배열에서 최소값을 찾고 그 값을 맨 앞에 위치한 값과 교체하는 정렬 방식 
<img src="https://velog.velcdn.com/images/hongsoom/post/f1967e9c-498c-47e9-87d9-ba3d751e17af/image.png" width="1000" alt="선택정렬"></img>
>크기가 n인 배열에서 선택정렬을 통해서는 O(n^2)

### 퀵정렬
<img src="https://gmlwjd9405.github.io/images/algorithm-quick-sort/quick-sort.png" width="1000" alt="퀵정렬"></img>
### 퀵정렬 시간복잡도
<img src="https://gmlwjd9405.github.io/images/algorithm-quick-sort/sort-time-complexity-etc1.png" width="1000" alt="퀵정렬시간 복잡도"></img>
>크기가 n인 배열에서 퀵정렬을 통해서는 평균적으로 O(nlog2 n) 최악의 경우 O(n^2)   
> 기준값(pivot)에 따라서 시간복잡도가 크게 달라짐


>선택정렬은 단순하지만 비효울적인 방법   
>퀵정렬은 복잡하지만 효울적인 방법