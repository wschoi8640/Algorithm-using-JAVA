# 순차검색(Sequential Search)

* 문제 : n개의 키로 구성된 배열 S에 키 x가 있는가?

* 입력(매개변수) : 양의 정수 n, 1에서 n까지의 첨자를 가진 키의 배열 S, 그리고 키 x

* 출력 : S안에 x의 위치를 가리키는 location(S안에 x가 없으면 0)

```java
// 배열의 처음부터 끝까지 돌면서 키값을 확인한다.
int seqSearch(int n, int [] S, int x)
{
    int location = 1;
    
    // 배열이 끝나거나 키값이 등장할때 까지 반복
    while (location <= n && S[location] != x)
    {
        location = location + 1;
    }
    // 키값이 등장하지 않은 경우
    if (location > n) 
    {
        location = 0;
    }
    return location;    
}
```
