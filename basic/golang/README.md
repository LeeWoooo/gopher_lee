Go언어의 특징
===

Go언어는 정적 타입, 강 타입의 특징을 가지고 있습니다.

프로그래밍 언어에서 타입은 자료형을 뜻합니다. 그리고 자료형에서 보통 정수, 실수, boolean, string, 객체등이 있습니다.

여기서 자료형을 컴파일할 때(Compile-time) 결정하면 정적 타입이고, 실행할 때(Run-time) 결정하면 동적 타입이라 합니다.

`Go언어는 정적 타입이기 때문에 컴파일을 할 때 자료형이 결정됩니다.`

약 타입(weakly-typed)는 값의 타입을 바쑬 수 있습니다. 여기서 값의 타입 바꾸기를 형 변환이라 합니다. 즉 약 타입 언어는 자료형이 달라도 컴파일 또는 실행 시점에 정해진 규칙에 따라 암시적 형 변환(Implicit conversion)을 해주는 방식입니다.

강 타입(strongly-typed)은 값 자체가 타입이며, 타입을 바꿀 수 없습니다. 즉 컴파일 또는 실행할 때 자료형이 다르면 error를 발생시킵니다.

`Go 언어는 강 타입 언어이므로 암시적 형 변환을 하지 않습니다.`


