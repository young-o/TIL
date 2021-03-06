## Tree

* 한 개 이상의 노드로 이루어진 집합
  * 최상위 노드 **루트**와 나머지 노드들의 집합
  * 나머지들은 각각 하나의 **서브 트리**가 됨
* 노드: 트리의 원소
* 간선(edge): **부모 노드**와 **자식 노드**를 연결하는 선
* **단말(리프) 노드**: 자식이 없는 노드 (마지막 노드)



### 이진 트리

* 노드가 자식 노드를 최대 2개까지만 갖는 트리
* 순회
  1. 전위 순회
  2. 중위 순회
  3. 후위 순회



### 이진 트리의 표현

* 노드 번호의 성질

  1. 노드 번호 i 인 노드의 부모 노드: i/2
  2. 노드 번호 i 인 노드의 왼쪽 자식 노드: 2*i
  3. 노드 번호 i 인 노드의 오른쪽 자식 노드: 2*i +1

  ![image](https://user-images.githubusercontent.com/46865281/73280772-5a5c0700-4232-11ea-97bb-4f6626f064c1.png)



* 만약 일반적인 리스트(배열)로 이진 트리를 표현할 경우, 2^n의 크기를 할당한다. 이때 이진 트리가 편향되었을 경우 메모리 낭비가 심해지므로 일반적인 리스트가 아닌 링크드 리스트를 이용해 이진 트리를 만드는 것이 좋다.



### 이진 탐색 트리

* key(왼쪽 서브 트리) < key(root) < key(오른쪽 서브 트리)로 정렬되어 있는 트리
* 탐색을 효율적으로 할 수 있음, 순차 -> 이진
  * 평균 O(log n), 최악의 경우 O(n)의 시간 복잡도



### 힙

* 완전 이진 트리의 노드 중 키 값이 가장 큰 노드나 가장 작은 노드를 찾기 위해 만든 자료구조

* 최대 힙

  * 키 값이 가장 큰 노드를 찾기 위한 완전 이진 트리

  * 부모 노드의 키 값 > 자식 노드의 키 값

    => 루트 노드가 최대 값

* 최소 힙

  * 키 값이 가장 작은 노드를 찾기 위한 완전 이진 트리

  * 부모 노드의 키 값 < 자식 노드의 키 값

    => 루트 노드가 최소 값

    

* 삽입: 루트 노드가 20인 최대 힙에 23을 추가한다고 가정하자.

  1. 비어 있는 곳에 임시로 23 삽입
  2. 부모 노드와 자식 노드를 비교해서 위치 바꾸기
  3. 자리 확정

  

* 삭제: 힙에서는 루트 노드의 원소만을 삭제할 수 있음.
  1. 루트 노드의 원소 삭제
  2. 마지막 노드를 루트 노드 위치로 이동
  3. 루트부터 부모 노드와 자식 노드들을 비교하여 자리 바꾸기
  4. 자리 확정

