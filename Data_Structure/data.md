# 자료구조

## 선형리스트(LinearList)
- 데이터를 논리적인 순서대로 메모리에 연속하여 저장하는 구현하는 방식
- 데이터의 논리적인 순서와 기억 장소에 저장되는 물리적 순서가 일치하는 구조다.
- 배열을 이용해 구현한다.

<br>

## 장점
- 인덱스(Index)로 접근할 수 있기 때문에 접근 속도가 매우 빠르다.

- 연속된 메모리 공간에 존재하기 때문에 관리하기가 편하다.

<br>

## 단점

- <strong>삽입 & 삭제 연산 후에 연속적인 물리 주소를 유지하기 위해 원소들을 이동시키는 추가 작업과 시간이 소요된다.</strong>

- 원소들의 이동 작업으로 인한 오버헤드로 원소의 개수가 많고 삽입 & 삭제 연산이 많은 경우 더 많이 발생한다.

- <strong>배열을 이용해 구현하기 때문에 배열이 갖고 있는 메모리 사용의 비효율성 문제를 그대로 가지고 있다.</strong> 

### <strong>ex.</strong> 
 배열의 크기 >> 데이터 수 : 메모리 공간의 낭비를 가져온다.

 배열의 크기 << 데이터 수 : 데이터를 저장할 수 없다.

<br>

<br>

## <strong>선형리스트를 C언어로 구현해보자</strong>

``` c
#include <stdio.h>

#define LIST_SIZE 10

int list[LIST_SIZE] = { 0 };
int numOfDatas = 0;

// LinearList - 데이터 ,메모리 연속적인 공간을 사용하여 저장-관리
// 포인터 필요 없다 왜 ? 배열의 index 라는 개념이 있으니까. 

void listInit() {
	// 초기화할 수 있다.
	numOfDatas = 0;
}

void insert(int data) {
	if (numOfDatas < LIST_SIZE) {
		list[numOfDatas++] = data;
	}
	else
		printf("리스트가 꽉 참");
}

// 탐색 
int search(int searchData) {

	if (numOfDatas == 0) {
		printf("리스트에 데이터가 없음");
		return -1;
	}

	for (int i = 0; i < numOfDatas; i++) {
		if (list[i] == searchData) {
			return i;
		}

		return -1;
	}
}

// 변경
void update(int targetData, int updateData) {

	if (numOfDatas == 0) {
		printf("리스트에 데이터가 없음");
		return;
	}

	for (int i = 0; i < numOfDatas; i++) {
		if (list[i] == targetData) {
			list[i] = updateData;
			return;
		}

	}
}

// 삭제
void doDelete(int deleteData) {

	if (numOfDatas == 0) {
		printf("리스트에 데이터가 없음");
		return;
	}

	for (int i = 0; i < numOfDatas; i++) {
		if (list[i] == deleteData) {
			for (int j = i; j < numOfDatas - 1; j++) {
				list[j] = list[j + 1]; 
			}
			numOfDatas -= 1;
			i -= 1;
		}

	}
}

printAll() {
	for (int i = 0; i < numOfDatas; i++) {
		printf("[%d] ", list[i]);
	}
	printf("\n\n");
}

int main() {
	listInit();

	insert(1);
	insert(2); 
	insert(4);
	insert(5);
	insert(3);
	insert(5);
	insert(5);

	printAll();

	doDelete(5);

	printAll();

	

	return 0;
}
```

<br>

