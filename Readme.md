# 순수함수?

부수효과가 없는 함수

1. 함수 몸통에 입출력 관련 코드가 없어야 함
2. 함수 몸통에서 매개변숫값을 변경시키지 않는다. (매개변수는 `const`나 `readonly` 형태로만 사용)
3. 함수는 몸통에서 만들어진 결과를 즉시 반환
4. 함수를 예외를 발생시키지 않음
5. 함수가 콜백 함수로 구현 되어 있거나 함수 몸통에 콜백 함수를 사용하는 코드가 없음
6. 함수 몸통에 `Promise` 같은 비동기 함수가 없다.

# readonly

1. 순수 함수를 쉽게 구현할 수 있도록 제공하는 키워드
2. 매개변수 값을 변경하려고 하면, 디버거에서 알려줌
3. 인터페이스, 클래스, 함수, 매개변수 등의 경우는 `cosnt`를 사용하지 않기 때문에 해당 키워드에서 사용

# 가변 인수(variadic aguments)

1. 함수를 호출할 때 전달하는 인수의 개수를 제한하지 않는 것을 의미
2. 매개변수에 `...aguments`형태로 작성하여 표시함
3. 타입에 상관없이 함수를 동작하게 하려면 제너릭 타입으로 구현해야함

```typescript
export const meargeArray = <T>(...arrays: readonly T[][]): T[] => {};
```

# 튜플

1. 배열의 한 종류로 취급
2. 타 타입 배열이라고 생각하면 됨
3. vanilla js에서는 튜플이 없다
4. 별칭으로 어떤 용도인지 알려주는 것이 중요

```typescript
export type ResultType = [boolean, string];
```
