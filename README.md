<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Standard Deviation

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> [Normal][normal-distribution] distribution [standard deviation][standard-deviation].

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/stats-base-dists-normal-stdev
```

</section>

<section class="usage">

## Usage

```javascript
var stdev = require( '@stdlib/stats-base-dists-normal-stdev' );
```

#### stdev( mu, sigma )

Returns the [standard deviation][standard-deviation] for a [normal][normal-distribution] distribution with parameters `mu` (mean) and `sigma` (standard deviation).

```javascript
var y = stdev( 2.0, 1.0 );
// returns 1.0

y = stdev( -1.0, 4.0 );
// returns 4.0
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var y = stdev( NaN, 1.0 );
// returns NaN

y = stdev( 0.0, NaN );
// returns NaN
```

If provided `sigma <= 0`, the function returns `NaN`.

```javascript
var y = stdev( 0.0, 0.0 );
// returns NaN

y = stdev( 0.0, -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var stdev = require( '@stdlib/stats-base-dists-normal-stdev' );

var sigma;
var mu;
var y;
var i;

for ( i = 0; i < 10; i++ ) {
    mu = ( randu()*10.0 ) - 5.0;
    sigma = randu() * 20.0;
    y = stdev( mu, sigma );
    console.log( 'µ: %d, σ: %d, Var(X;µ,σ): %d', mu.toFixed( 4 ), sigma.toFixed( 4 ), y.toFixed( 4 ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-normal-stdev.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-normal-stdev

[test-image]: https://github.com/stdlib-js/stats-base-dists-normal-stdev/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/stats-base-dists-normal-stdev/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-normal-stdev/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-normal-stdev?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-normal-stdev.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-normal-stdev/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-normal-stdev/main/LICENSE

[normal-distribution]: https://en.wikipedia.org/wiki/Normal_distribution

[standard-deviation]: https://en.wikipedia.org/wiki/Standard_deviation

</section>

<!-- /.links -->
