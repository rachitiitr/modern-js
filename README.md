# modern-js

* Point Free Functions
  * const isEven = not(isOdd); // no arguments or shape of function is discussed
  * const isOdd = compose(eq(1), mod(2))
  * const mod = x => y => y % x;
  * const eq = x => y => y == x;
* Thunk
  * Function with no params but returns a value
* Async Thunk
  * Function that takes a callback and calls the callback with the value it holds
  * Basis of promises
  * th1(out1 => { output(out1); th2(out2 => { output(out2); }) });
* Callbacks are bad because
  * the 3rd party may call it too often
  * the 3rd party may not call it at all
  * Same is with (err, result) kind of callbacks, what if err and result both exist
* Promises invert this control, you don't pass callbacks, you listen for success / error events and react.
