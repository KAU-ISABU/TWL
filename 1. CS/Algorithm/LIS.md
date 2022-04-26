# LIS(Longest Increasing Subsequence)
## LIS란?
풀어말하면 **최장 증가 부분 수열**이란 의미로 주로 알고리즘에서 자주 활용되는 문제이다.  
수열에서 임의의 원소들을 제거한 **부분수열**이 **오름차순으로 정렬**되어있으면 **증가 부분수열**이 된다.  
한 수열에서 이러한 증가부분수열 중 **가장 긴 길이를 가지는 증가부분수열**을 찾는 문제이다.
## 예시
**3 4 5 1 8 9 19 11**  
3 **4** 5 **1** 8 **9** 19 **11**  
4 1 9 11을 선택하여 부분수열을 만든다  
**4 1 9 11**  
위와 같은 작업으로 임의의 원소를 선택하여 부분수열들을 만든다  
**4 1 9 11**  
**1 9 19 11**  
**3 4 5 8 19**  
**3 4 5 8 9 11**  
위의 부분수열들중에서 오름차순으로 정렬된 부분수열들은  
**3 4 5 8 19**  
**3 4 5 8 9 11**  
위 부분수열중에서는 **3 4 5 8 9 11** 이 LIS가 된다. 위 과정에서 볼수있듯이 LIS는 여러개일수있다.   
## 길이가 N인 수열에서 LIS를 구하기
PS에서는 길이가 N인 수열에서 LIS를 구하는 문제가 자주 출제된다. 이에 대한 접근법들은 여러개가 있다.
### 나이브한 접근 O(N^3)
