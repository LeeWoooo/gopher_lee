Array
===

## 배열이란?

배열은 같은 type들로 이루어진 type입니다. 각 요소들의 type은 모두 같아야 하며 배열의 요소의 type으로 또 배열을 선언할 수 있습니다..

배열은 자료 구조이기도 합니다.
>자료구조? Data를 어떻게 저장할 지 나타내는 구조입니다..

<br>

## Usage

```
var <배열 명> [<요소의 갯수>] 자료형 = [<요소의 갯수>] 자료형 {값...}
```

배열을 선언할 때 필요한 값은 다음과 같습니다.

1. 배열 명
2. 요소의 갯수(배열 안에 들어갈 값의 갯수)
3. 자료형 (배열의 요소의 type)

<br>

## 배열은 연속된 Memory입니다.

배열도 변수이기 때문에 선언을 해서 사용해야 한다. 선언을 한다는 것은 Memory가 할당된다는 것입니다.

배열을 선언할 때 요소의 갯수를 정하게 되는데 그 때 정하는 값은 상수를 이용하게 됩니다. 그렇기 때문에 `배열은 고정길이 입니다. 한번 선언해서 정해진 Memory는 변경할 수 없습니다.`

배열의 변수명은 배열의 `Memory의 시작주소를 가지고 있으며` 배열의 type과 요소의 갯수를 통해 `연속 된 Memory의 크기를 알 수 있습니다.`

간단하게 다시 정리해보자면

type 결정 -> 요소의 갯수 결정 -> type과 요소의 갯수를 통해 size가 결정 -> Memory 할당

type은 각각 정해진 크기가 존재하며 type과 요소의 갯수를 통해 배열의 Memory의 크기가 결정됩니다. `(type의 크기 x 배열 요소의 갯수 = 배열의 Memory)`

```
var arr [3]int8 = [3]int8{1, 2, 3}
```

위의 code를 예제로 보자면 arr이라는 변수는 해당 배열의 memory의 시작 주소를 가지고 있으며, 이 배열의 memory의 크기를 구한고자 한다면 아래와 같은 계산식으로 구할 수 있습니다.

```
8byte (int8 의 크기) x 3 (요소의 갯수) = 24byte (연속된 memory의 크기)
```

<br>

## 배열의 순회

배열이 등장하면 자연스럽게 반복문과 같이 이용되게 됩니다. go에서 지원하는 `range` keyword를 이용하여 배열의 `index`와 `요소`를 얻어올 수 있습니다.

이 경우에는 배열의 특정 요소에 대한 `random access`는 되지 않고 전부 순회한다.

```
for index, value := range 배열명 {
    // 반복문 block안에서 index와 value를 이용
}
```

<br>

## 그럼 배열은 어디에 사용하나요?

결론부터 이야기하자면 random access가 자주 일어난 곳에서 배열을 주로 사용합니다.
>random access란 자료구조의 요소에 두서없이 접근을 하는 것을 이야기 합니다.

배열에는 각 요소마다 `index`가 존재하며, 연속된 memory라는 성격을 가지고 있습니다.

이 두 가지 장점을 이용하여 memory의 시작주소부터 index를 이용하여 요소에 접근을 하게 됩니다.







