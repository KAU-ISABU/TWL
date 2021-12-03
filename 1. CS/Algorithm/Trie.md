# Trie

## Trie란 무엇인가?
Trie는 트리의 한 종류로, 저장된 문자열을 빠른 시간 안에 검색하는 것에 특화된 알고리즘이다. 
일반적인 트리의 경우 배열을 이용하여 노드 하나하나가 고유의 값을 가지고 있고, 자식 노드에 접근할 경우 인덱스를 이용하지만 Trie의 경우,
```c++
class trie_node {
private: 
    bool leaf = false;
    trie_node* children[26];
    /* ... */

public:
    trie_node () {}
    /* ... */
};
```
와 같이 선언되어 자식 노드의 인덱스가 각 알파벳에 1:1로 연결되고, 값으로는 해당 노드가 문자열의 끝인지 (즉 리프 노드인지) 여부를 저장하게 된다. 즉, 인덱스가 값으로 직접적으로 치환된다.

예제)
 * <a href="https://www.acmicpc.net/problem/14425">14425번: 문자열 집합</a>
 문자열을 N개 저장하여 M개 검색하는 문제이다. map 혹은 set을 이용해서 풀 수 있고 효율이 더 좋지만, Trie를 연습하는 데에 좋은 문제이다.