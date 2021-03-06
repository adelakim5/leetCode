## 9. Palindrome Number

> leetCode [9](https://leetcode.com/problems/palindrome-number/)

### 풀이

1. 숫자 x를 문자열로 바꾼다.
2. x의 길이가 짝수면
   - 마지막 인덱스를 반으로 나눈 만큼만 돌면서 팰린드롬인지 확인한다.
   - 처음과 끝이 같은지 확인한다.
   ```js
   x = 123321;
   mid = Math.floor(5 / 2); // 마지막 인덱스 5를 반으로 나눈 몫, 즉 2가 됨
   x[0] = 1;
   x[5 - 0] = 1; // 같음
   x[1] = 2;
   x[5 - 1] = 2; // 같음
   x[2] = 3; // mid 도달
   x[5 - 2] = 3; // 같음
   // true
   ```
3. x의 길이가 홀수면
   - 마지막 인덱스를 반으로 나눈 수의 **전까지** 돌면서 팰린드롬인지 확인한다.
   - 처음과 끝이 같은지 확인한다.
   ```js
   x = 12341;
   mid = Math.floor(4 / 2); // 마지막 인덱스 4를 반으로 나눈 몫, 즉 2가 됨
   x[0] = 1;
   x[4 - 0] = 1; // 같음
   x[1] = 2;
   x[4 - 1] = 4; // 다름
   // false
   ```
