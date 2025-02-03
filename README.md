<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# FLOAT64_MAX_SAFE_NTH_TRIBONACCI

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Maximum safe nth [Tribonacci number][tribonacci-number] when stored in [double-precision floating-point][ieee754] format.

<section class="installation">

## Installation

```bash
npm install @stdlib/constants-float64-max-safe-nth-tribonacci
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

<!-- eslint-disable id-length -->

```javascript
var FLOAT64_MAX_SAFE_NTH_TRIBONACCI = require( '@stdlib/constants-float64-max-safe-nth-tribonacci' );
```

#### FLOAT64_MAX_SAFE_NTH_TRIBONACCI

Maximum [safe][safe-integers] nth [Tribonacci number][tribonacci-number] when stored in [double-precision floating-point][ieee754] format.

<!-- eslint-disable id-length -->

```javascript
var bool = ( FLOAT64_MAX_SAFE_NTH_TRIBONACCI === 63 );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable id-length -->

<!-- eslint no-undef: "error" -->

```javascript
var FLOAT64_MAX_SAFE_NTH_TRIBONACCI = require( '@stdlib/constants-float64-max-safe-nth-tribonacci' );

function tribonacci( n ) {
    var a;
    var b;
    var c;
    var d;
    var i;

    a = 0;
    b = 0;
    c = 1;
    if ( n === 0 ) {
        return a;
    }
    if ( n === 1 ) {
        return b;
    }
    if ( n === 2 ) {
        return c;
    }
    for ( i = 3; i <= n; i++ ) {
        d = a + b + c;
        a = b;
        b = c;
        c = d;
    }
    return c;
}

var v;
var i;
for ( i = 0; i < 100; i++ ) {
    v = tribonacci( i );
    if ( i > FLOAT64_MAX_SAFE_NTH_TRIBONACCI ) {
        console.log( 'Unsafe: %d', v );
    } else {
        console.log( 'Safe:   %d', v );
    }
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/constants/float64/max_safe_nth_tribonacci.h"
```

#### STDLIB_CONSTANT_FLOAT64_MAX_SAFE_NTH_TRIBONACCI

Maximum [safe][safe-integers] nth [Tribonacci number][tribonacci-number] when stored in [double-precision floating-point][ieee754] format.

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float64-max-safe-nth-tribonacci.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float64-max-safe-nth-tribonacci

[test-image]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float64-max-safe-nth-tribonacci/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float64-max-safe-nth-tribonacci?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float64-max-safe-nth-tribonacci.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float64-max-safe-nth-tribonacci/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/tree/deno
[deno-readme]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/tree/umd
[umd-readme]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/tree/esm
[esm-readme]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float64-max-safe-nth-tribonacci/main/LICENSE

[safe-integers]: http://www.2ality.com/2013/10/safe-integers.html

[tribonacci-number]: https://en.wikipedia.org/wiki/Tribonacci_number

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
