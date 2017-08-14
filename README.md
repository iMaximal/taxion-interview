## 1. Promises
Написать собственную имплементацию Promise

https://promisesaplus.com/

https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Promise

*Пример:*
```javascript
function MyPromise (f) {
  // FIXME
}

const p = new MyPromise((resolve, reject) => {
  setTimeout(() => {
   if (Math.random() < 0.5) resolve()
   else reject()
  }, 200)
});

p.then(() => {
  console.log('passed')
}).catch(() => {
  console.log('failed')
})
```

## 2. Equality
Написать функцию проверяющую равенство любых двух объектов

*Пример*
```javascript
deepEqual(1, 1)  // true
deepEqual({ a: [1, 2, 3], b: { foo: 'bar' } }, { a: [1, 2, 3], b: { foo: 'bar' } }) // true
deepEqual({ a: 1 b: 2 }, { a: 1, c: 2 }) // false
```

## 3. Async processing
Написать функцию запускающую асинхронную операцию над каждым елементом массива и ограничивающую количество одновременно запущенных задач заданным числом.

*Пример*
```javascript
function launchInParallel (func, data, n, callback) {
  // не более n функций должны исполняться в любой момент времени
  // FIXME
}

function sleep (s, callback) {
  setTimeout(callback, s * 1000)
}

const data = [1, 3, 2, 1, 1, 4, 2, 5]

launchInParallel(sleep, data, 5, () => {
  // должно завершиться через 6 секунд
  console.log('done')
})
```

## 4. Balanced brackets
Написать функцию проверяющую корректность расставленых скобок в строке

*Пример*
```javascript
isBalanced('foo([1, 2, 3])')  // true
isBalanced('{} + [() => {}]')  // true
isBalanced('(] {()()} [)')  // false
```

## 5. Permutations
Написать функцию возвращающую все возможные перестановки символов

*Пример*
```javascript
permute('12')  // ['12', '21']
permute('abc')  // ['abc', 'acb', 'bca', 'bac', 'cba', 'cab']
```
