## How does the Prime validater work?
```
function isPrime( number ) {
  if ( number > 2 && number % 2 == 0 || number < 2 ) {
    return false;
  }
  i = 3
  while ( i * i <= number ) {
    if ( number % i == 0 ) {
      return false
    }
    i += 2
  }
  return true
}
```
A `natural number` is called a `prime number` if it can be formed by multiplication only with 1 and `the number` itself.
```
if ( number > 2 && number % 2 == 0 || number < 2 ) {
  return false;
}
```
If `the number` is greater than 2 and is odd OR `the number` is less than 2:
- Can not be prime, because 2 is the lowest `prime number` and all `even numbers` greater than 2 can be formed by multiplying with 2 too
```
i = 3
```
Set `composit number` to 1 above 2, 2 has not to be checked, because it's the lowest `prime number`
```
while ( i * i <= number ) {
  if ( number % i == 0 ) {
    return false
  }
  i += 2
}
```
While squaring the `composit number` is less or equal to `the number`:
- If dividing the `composit number` through `the number` has no rest value, it's a `composite number` of `the number`:
    `The number` is not a prime
- Else:
    raise value of `the number` by 2 (raising the value of an `odd number` will result in an `even number`, above 2 these can not be `prime numbers`)
```
return true
```
If no condition applied, `the number` is a `prime number`
