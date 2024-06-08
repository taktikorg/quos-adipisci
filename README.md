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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Assert

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Assertion utilities.

<section class="installation">

## Installation

```bash
npm install @taktikorg/quos-adipisci
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

```javascript
var assert = require( '@taktikorg/quos-adipisci' );
```

#### assert

Namespace providing utilities for data type testing and feature detection.

```javascript
var o = assert;
// returns {...}
```

To validate the built-in JavaScript data types, the namespace includes the following assertion utilities:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArray( value )`][@taktikorg/quos-adipisci/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="signature">[`isBoolean( value )`][@taktikorg/quos-adipisci/is-boolean]</span><span class="delimiter">: </span><span class="description">test if a value is a boolean.</span>
-   <span class="signature">[`isDateObject( value )`][@taktikorg/quos-adipisci/is-date-object]</span><span class="delimiter">: </span><span class="description">test if a value is a Date object.</span>
-   <span class="signature">[`isFunction( value )`][@taktikorg/quos-adipisci/is-function]</span><span class="delimiter">: </span><span class="description">test if a value is a function.</span>
-   <span class="signature">[`isnan( value )`][@taktikorg/quos-adipisci/is-nan]</span><span class="delimiter">: </span><span class="description">test if a value is NaN.</span>
-   <span class="signature">[`isNull( value )`][@taktikorg/quos-adipisci/is-null]</span><span class="delimiter">: </span><span class="description">test if a value is null.</span>
-   <span class="signature">[`isNumber( value )`][@taktikorg/quos-adipisci/is-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number.</span>
-   <span class="signature">[`isObject( value )`][@taktikorg/quos-adipisci/is-object]</span><span class="delimiter">: </span><span class="description">test if a value is an object.</span>
-   <span class="signature">[`isRegExp( value )`][@taktikorg/quos-adipisci/is-regexp]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression.</span>
-   <span class="signature">[`isString( value )`][@taktikorg/quos-adipisci/is-string]</span><span class="delimiter">: </span><span class="description">test if a value is a string.</span>
-   <span class="signature">[`isSymbol( value )`][@taktikorg/quos-adipisci/is-symbol]</span><span class="delimiter">: </span><span class="description">test if a value is a symbol.</span>
-   <span class="signature">[`isUndefined( value )`][@taktikorg/quos-adipisci/is-undefined]</span><span class="delimiter">: </span><span class="description">test if a value is undefined.</span>

</div>

<!-- </toc> -->

For primitive types having corresponding object wrappers, assertion utilities provide `isObject` and `isPrimitive` methods to test for either objects or primitives, respectively.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Boolean = require( '@stdlib/boolean/ctor' );
var isBoolean = require( '@taktikorg/quos-adipisci/is-boolean' );

var bool = isBoolean.isObject( new Boolean( false ) );
// returns true

bool = isBoolean.isObject( false );
// returns false

bool = isBoolean.isPrimitive( false );
// returns true
```

Many of the assertion utilities have corresponding packages that test whether array elements are of the given data type:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|nan|number|object|regexp|symbol|null|undefined)-array" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArrayArray( value )`][@taktikorg/quos-adipisci/is-array-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of arrays.</span>
-   <span class="signature">[`isBooleanArray( value )`][@taktikorg/quos-adipisci/is-boolean-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of booleans.</span>
-   <span class="signature">[`isDateObjectArray( value )`][@taktikorg/quos-adipisci/is-date-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only Date objects.</span>
-   <span class="signature">[`isFunctionArray( value )`][@taktikorg/quos-adipisci/is-function-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only functions.</span>
-   <span class="signature">[`isNaNArray( value )`][@taktikorg/quos-adipisci/is-nan-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only NaN values.</span>
-   <span class="signature">[`isNullArray( value )`][@taktikorg/quos-adipisci/is-null-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only null values.</span>
-   <span class="signature">[`isNumberArray( value )`][@taktikorg/quos-adipisci/is-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of numbers.</span>
-   <span class="signature">[`isObjectArray( value )`][@taktikorg/quos-adipisci/is-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only objects.</span>
-   <span class="signature">[`isStringArray( value )`][@taktikorg/quos-adipisci/is-string-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of strings.</span>
-   <span class="signature">[`isSymbolArray( value )`][@taktikorg/quos-adipisci/is-symbol-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only symbols.</span>

</div>

<!-- </toc> -->

Where applicable, similar to the assertion utilities for built-in data types, array assertion utilities provides methods for testing for an array of primitives or objects.

<!-- eslint-disable no-new-wrappers -->

```javascript
var isStringArray = require( '@taktikorg/quos-adipisci/is-string-array' );

var bool = isStringArray( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.primitives( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.objects( [ 'hello', 'world' ] );
// returns false

bool = isStringArray.objects( [ new String( 'hello' ), new String( 'world' ) ] );
// returns true
```

The namespace also contains utilities to test for numbers within a certain range or for numbers satisfying a particular "type":

<!-- <toc pattern="is-*+(number|integer)*" ignore="is-number-array" ignore="is-number" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCubeNumber( value )`][@taktikorg/quos-adipisci/is-cube-number]</span><span class="delimiter">: </span><span class="description">test if a value is a cube number.</span>
-   <span class="signature">[`isIntegerArray( value )`][@taktikorg/quos-adipisci/is-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only integers.</span>
-   <span class="signature">[`isInteger( value )`][@taktikorg/quos-adipisci/is-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having an integer value.</span>
-   <span class="signature">[`isNegativeIntegerArray( value )`][@taktikorg/quos-adipisci/is-negative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative integers.</span>
-   <span class="signature">[`isNegativeInteger( value )`][@taktikorg/quos-adipisci/is-negative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative integer value.</span>
-   <span class="signature">[`isNegativeNumberArray( value )`][@taktikorg/quos-adipisci/is-negative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative numbers.</span>
-   <span class="signature">[`isNegativeNumber( value )`][@taktikorg/quos-adipisci/is-negative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative value.</span>
-   <span class="signature">[`isNonNegativeIntegerArray( value )`][@taktikorg/quos-adipisci/is-nonnegative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative integers.</span>
-   <span class="signature">[`isNonNegativeInteger( value )`][@taktikorg/quos-adipisci/is-nonnegative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative integer value.</span>
-   <span class="signature">[`isNonNegativeNumberArray( value )`][@taktikorg/quos-adipisci/is-nonnegative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative numbers.</span>
-   <span class="signature">[`isNonNegativeNumber( value )`][@taktikorg/quos-adipisci/is-nonnegative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative value.</span>
-   <span class="signature">[`isNonPositiveIntegerArray( value )`][@taktikorg/quos-adipisci/is-nonpositive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive integers.</span>
-   <span class="signature">[`isNonPositiveInteger( value )`][@taktikorg/quos-adipisci/is-nonpositive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive integer value.</span>
-   <span class="signature">[`isNonPositiveNumberArray( value )`][@taktikorg/quos-adipisci/is-nonpositive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive numbers.</span>
-   <span class="signature">[`isNonPositiveNumber( value )`][@taktikorg/quos-adipisci/is-nonpositive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive value.</span>
-   <span class="signature">[`isPositiveIntegerArray( value )`][@taktikorg/quos-adipisci/is-positive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive integers.</span>
-   <span class="signature">[`isPositiveInteger( value )`][@taktikorg/quos-adipisci/is-positive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive integer value.</span>
-   <span class="signature">[`isPositiveNumberArray( value )`][@taktikorg/quos-adipisci/is-positive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive numbers.</span>
-   <span class="signature">[`isPositiveNumber( value )`][@taktikorg/quos-adipisci/is-positive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive value.</span>
-   <span class="signature">[`isSafeIntegerArray( value )`][@taktikorg/quos-adipisci/is-safe-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only safe integers.</span>
-   <span class="signature">[`isSafeInteger( value )`][@taktikorg/quos-adipisci/is-safe-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a safe integer value.</span>
-   <span class="signature">[`isSquareNumber( value )`][@taktikorg/quos-adipisci/is-square-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square number.</span>
-   <span class="signature">[`isSquareTriangularNumber( value )`][@taktikorg/quos-adipisci/is-square-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square triangular number.</span>
-   <span class="signature">[`isTriangularNumber( value )`][@taktikorg/quos-adipisci/is-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a triangular number.</span>

</div>

<!-- </toc> -->

The namespace provides utilities for validating typed arrays:

<!-- <toc pattern="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array"> -->

<div class="namespace-toc">

-   <span class="signature">[`isFloat32Array( value )`][@taktikorg/quos-adipisci/is-float32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float32Array.</span>
-   <span class="signature">[`isFloat64Array( value )`][@taktikorg/quos-adipisci/is-float64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float64Array.</span>
-   <span class="signature">[`isInt16Array( value )`][@taktikorg/quos-adipisci/is-int16array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int16Array.</span>
-   <span class="signature">[`isInt32Array( value )`][@taktikorg/quos-adipisci/is-int32array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int32Array.</span>
-   <span class="signature">[`isInt8Array( value )`][@taktikorg/quos-adipisci/is-int8array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int8Array.</span>
-   <span class="signature">[`isUint16Array( value )`][@taktikorg/quos-adipisci/is-uint16array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint16Array.</span>
-   <span class="signature">[`isUint32Array( value )`][@taktikorg/quos-adipisci/is-uint32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint32Array.</span>
-   <span class="signature">[`isUint8Array( value )`][@taktikorg/quos-adipisci/is-uint8array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8Array.</span>
-   <span class="signature">[`isUint8ClampedArray( value )`][@taktikorg/quos-adipisci/is-uint8clampedarray]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8ClampedArray.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating `ndarray`s (n-dimensional arrays).

<!-- <toc keywords="+ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCentrosymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a centrosymmetric matrix.</span>
-   <span class="signature">[`isComplex128MatrixLike( value )`][@taktikorg/quos-adipisci/is-complex128matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128ndarrayLike( value )`][@taktikorg/quos-adipisci/is-complex128ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128VectorLike( value )`][@taktikorg/quos-adipisci/is-complex128vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64MatrixLike( value )`][@taktikorg/quos-adipisci/is-complex64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64ndarrayLike( value )`][@taktikorg/quos-adipisci/is-complex64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64VectorLike( value )`][@taktikorg/quos-adipisci/is-complex64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isFloat32MatrixLike( value )`][@taktikorg/quos-adipisci/is-float32matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32ndarrayLike( value )`][@taktikorg/quos-adipisci/is-float32ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32VectorLike( value )`][@taktikorg/quos-adipisci/is-float32vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64MatrixLike( value )`][@taktikorg/quos-adipisci/is-float64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64ndarrayLike( value )`][@taktikorg/quos-adipisci/is-float64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64VectorLike( value )`][@taktikorg/quos-adipisci/is-float64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isMatrixLike( value )`][@taktikorg/quos-adipisci/is-matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is 2-dimensional ndarray-like object.</span>
-   <span class="signature">[`isndarrayLike( value )`][@taktikorg/quos-adipisci/is-ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is ndarray-like.</span>
-   <span class="signature">[`isNonSymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-nonsymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a non-symmetric matrix.</span>
-   <span class="signature">[`isPersymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a persymmetric matrix.</span>
-   <span class="signature">[`isSkewCentrosymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-skew-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-centrosymmetric matrix.</span>
-   <span class="signature">[`isSkewPersymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-skew-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-persymmetric matrix.</span>
-   <span class="signature">[`isSkewSymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-skew-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-symmetric matrix.</span>
-   <span class="signature">[`isSquareMatrix( value )`][@taktikorg/quos-adipisci/is-square-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object having equal dimensions.</span>
-   <span class="signature">[`isSymmetricMatrix( value )`][@taktikorg/quos-adipisci/is-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a symmetric matrix.</span>
-   <span class="signature">[`isVectorLike( value )`][@taktikorg/quos-adipisci/is-vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating complex numbers and arrays of complex numbers:

<!-- <toc pattern="is-complex*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isComplexLike( value )`][@taktikorg/quos-adipisci/is-complex-like]</span><span class="delimiter">: </span><span class="description">test if a value is a complex number-like object.</span>
-   <span class="signature">[`isComplexTypedArrayLike( value )`][@taktikorg/quos-adipisci/is-complex-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is complex-typed-array-like.</span>
-   <span class="signature">[`isComplexTypedArray( value )`][@taktikorg/quos-adipisci/is-complex-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a complex typed array.</span>
-   <span class="signature">[`isComplex( value )`][@taktikorg/quos-adipisci/is-complex]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit or 128-bit complex number.</span>
-   <span class="signature">[`isComplex128( value )`][@taktikorg/quos-adipisci/is-complex128]</span><span class="delimiter">: </span><span class="description">test if a value is a 128-bit complex number.</span>
-   <span class="signature">[`isComplex128Array( value )`][@taktikorg/quos-adipisci/is-complex128array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex128Array.</span>
-   <span class="signature">[`isComplex64( value )`][@taktikorg/quos-adipisci/is-complex64]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit complex number.</span>
-   <span class="signature">[`isComplex64Array( value )`][@taktikorg/quos-adipisci/is-complex64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex64Array.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating other special arrays or buffers:

<!-- <toc pattern="is-*array*" ignore="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array" ignore="is-*+(number|integer)*" ignore="is-+(array|boolean|date-object|function|string|nan|number|object|primitive|regexp|symbol|null|undefined)-array" ignore="is-array" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isAccessorArray( value )`][@taktikorg/quos-adipisci/is-accessor-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object supporting the accessor (get/set) protocol.</span>
-   <span class="signature">[`isArrayLength( value )`][@taktikorg/quos-adipisci/is-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid array length.</span>
-   <span class="signature">[`isArrayLikeObject( value )`][@taktikorg/quos-adipisci/is-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object.</span>
-   <span class="signature">[`isArrayLike( value )`][@taktikorg/quos-adipisci/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>
-   <span class="signature">[`isArrayBufferView( value )`][@taktikorg/quos-adipisci/is-arraybuffer-view]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer view.</span>
-   <span class="signature">[`isArrayBuffer( value )`][@taktikorg/quos-adipisci/is-arraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer.</span>
-   <span class="signature">[`isBetweenArray( value, a, b[, left, right] )`][@taktikorg/quos-adipisci/is-between-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object where every element is between two values.</span>
-   <span class="signature">[`isBigInt64Array( value )`][@taktikorg/quos-adipisci/is-bigint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt64Array.</span>
-   <span class="signature">[`isBigUint64Array( value )`][@taktikorg/quos-adipisci/is-biguint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigUint64Array.</span>
-   <span class="signature">[`isCircularArray( value )`][@taktikorg/quos-adipisci/is-circular-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array containing a circular reference.</span>
-   <span class="signature">[`isEmptyArrayLikeObject( value )`][@taktikorg/quos-adipisci/is-empty-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array-like object.</span>
-   <span class="signature">[`isEmptyArray( value )`][@taktikorg/quos-adipisci/is-empty-array]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array.</span>
-   <span class="signature">[`isFalsyArray( value )`][@taktikorg/quos-adipisci/is-falsy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only falsy values.</span>
-   <span class="signature">[`isFiniteArray( value )`][@taktikorg/quos-adipisci/is-finite-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only finite numbers.</span>
-   <span class="signature">[`isNumericArray( value )`][@taktikorg/quos-adipisci/is-numeric-array]</span><span class="delimiter">: </span><span class="description">test if a value is a numeric array.</span>
-   <span class="signature">[`isPlainObjectArray( value )`][@taktikorg/quos-adipisci/is-plain-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only plain objects.</span>
-   <span class="signature">[`isProbabilityArray( value )`][@taktikorg/quos-adipisci/is-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only probabilities.</span>
-   <span class="signature">[`isSameArray( v1, v2 )`][@taktikorg/quos-adipisci/is-same-array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both generic arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex128Array( v1, v2 )`][@taktikorg/quos-adipisci/is-same-complex128array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex128Arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex64Array( v1, v2 )`][@taktikorg/quos-adipisci/is-same-complex64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex64Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat32Array( v1, v2 )`][@taktikorg/quos-adipisci/is-same-float32array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float32Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat64Array( v1, v2 )`][@taktikorg/quos-adipisci/is-same-float64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float64Arrays and have the same values.</span>
-   <span class="signature">[`isSharedArrayBuffer( value )`][@taktikorg/quos-adipisci/is-sharedarraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is a SharedArrayBuffer.</span>
-   <span class="signature">[`isTruthyArray( value )`][@taktikorg/quos-adipisci/is-truthy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only truthy values.</span>
-   <span class="signature">[`isTypedArrayLength( value )`][@taktikorg/quos-adipisci/is-typed-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid typed array length.</span>
-   <span class="signature">[`isTypedArrayLike( value )`][@taktikorg/quos-adipisci/is-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is typed-array-like.</span>
-   <span class="signature">[`isTypedArray( value )`][@taktikorg/quos-adipisci/is-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a typed array.</span>
-   <span class="signature">[`isUnityProbabilityArray( value )`][@taktikorg/quos-adipisci/is-unity-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of probabilities that sum to one.</span>

</div>

<!-- </toc> -->

To test for error objects, the namespace includes the following utilities:

<!-- <toc pattern="is-*error*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isError( value )`][@taktikorg/quos-adipisci/is-error]</span><span class="delimiter">: </span><span class="description">test if a value is an Error object.</span>
-   <span class="signature">[`isEvalError( value )`][@taktikorg/quos-adipisci/is-eval-error]</span><span class="delimiter">: </span><span class="description">test if a value is an EvalError object.</span>
-   <span class="signature">[`isRangeError( value )`][@taktikorg/quos-adipisci/is-range-error]</span><span class="delimiter">: </span><span class="description">test if a value is a RangeError object.</span>
-   <span class="signature">[`isReferenceError( value )`][@taktikorg/quos-adipisci/is-reference-error]</span><span class="delimiter">: </span><span class="description">test if a value is a ReferenceError object.</span>
-   <span class="signature">[`isSyntaxError( value )`][@taktikorg/quos-adipisci/is-syntax-error]</span><span class="delimiter">: </span><span class="description">test if a value is a SyntaxError object.</span>
-   <span class="signature">[`isTypeError( value )`][@taktikorg/quos-adipisci/is-type-error]</span><span class="delimiter">: </span><span class="description">test if a value is a TypeError object.</span>
-   <span class="signature">[`isURIError( value )`][@taktikorg/quos-adipisci/is-uri-error]</span><span class="delimiter">: </span><span class="description">test if a value is a URIError object.</span>

</div>

<!-- </toc> -->

The namespace exposes the following constants concerning the current running process:

<!-- <toc pattern="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|big-endian|node|web-worker|windows|docker|mobile|touch-device)" > -->

<div class="namespace-toc">

-   <span class="signature">[`IS_BIG_ENDIAN`][@taktikorg/quos-adipisci/is-big-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is big endian.</span>
-   <span class="signature">[`IS_BROWSER`][@taktikorg/quos-adipisci/is-browser]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web browser.</span>
-   <span class="signature">[`IS_DARWIN`][@taktikorg/quos-adipisci/is-darwin]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Darwin.</span>
-   <span class="signature">[`IS_DOCKER`][@taktikorg/quos-adipisci/is-docker]</span><span class="delimiter">: </span><span class="description">check if the process is running in a Docker container.</span>
-   <span class="signature">[`IS_ELECTRON_MAIN`][@taktikorg/quos-adipisci/is-electron-main]</span><span class="delimiter">: </span><span class="description">check if the runtime is the main Electron process.</span>
-   <span class="signature">[`IS_ELECTRON_RENDERER`][@taktikorg/quos-adipisci/is-electron-renderer]</span><span class="delimiter">: </span><span class="description">check if the runtime is the Electron renderer process.</span>
-   <span class="signature">[`IS_ELECTRON`][@taktikorg/quos-adipisci/is-electron]</span><span class="delimiter">: </span><span class="description">check if the runtime is Electron.</span>
-   <span class="signature">[`IS_LITTLE_ENDIAN`][@taktikorg/quos-adipisci/is-little-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is little endian.</span>
-   <span class="signature">[`IS_MOBILE`][@taktikorg/quos-adipisci/is-mobile]</span><span class="delimiter">: </span><span class="description">check if the current environment is a mobile device.</span>
-   <span class="signature">[`IS_NODE`][@taktikorg/quos-adipisci/is-node]</span><span class="delimiter">: </span><span class="description">check if the runtime is Node.js.</span>
-   <span class="signature">[`IS_TOUCH_DEVICE`][@taktikorg/quos-adipisci/is-touch-device]</span><span class="delimiter">: </span><span class="description">check if the current environment is a touch device.</span>
-   <span class="signature">[`IS_WEB_WORKER`][@taktikorg/quos-adipisci/is-web-worker]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web worker.</span>
-   <span class="signature">[`IS_WINDOWS`][@taktikorg/quos-adipisci/is-windows]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Windows.</span>

</div>

<!-- </toc> -->

To test whether a runtime environment supports certain features, the namespace includes the following utilities:

<!-- <toc pattern="has-*-support" > -->

<div class="namespace-toc">

-   <span class="signature">[`hasArrayBufferSupport()`][@taktikorg/quos-adipisci/has-arraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `ArrayBuffer` support.</span>
-   <span class="signature">[`hasArrowFunctionSupport()`][@taktikorg/quos-adipisci/has-arrow-function-support]</span><span class="delimiter">: </span><span class="description">detect native `arrow function` support.</span>
-   <span class="signature">[`hasAsyncAwaitSupport()`][@taktikorg/quos-adipisci/has-async-await-support]</span><span class="delimiter">: </span><span class="description">detect native `async`/`await` support.</span>
-   <span class="signature">[`hasAsyncIteratorSymbolSupport()`][@taktikorg/quos-adipisci/has-async-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.asyncIterator` support.</span>
-   <span class="signature">[`hasBigIntSupport()`][@taktikorg/quos-adipisci/has-bigint-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt` support.</span>
-   <span class="signature">[`hasBigInt64ArraySupport()`][@taktikorg/quos-adipisci/has-bigint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt64Array` support.</span>
-   <span class="signature">[`hasBigUint64ArraySupport()`][@taktikorg/quos-adipisci/has-biguint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigUint64Array` support.</span>
-   <span class="signature">[`hasClassSupport()`][@taktikorg/quos-adipisci/has-class-support]</span><span class="delimiter">: </span><span class="description">detect native `class` support.</span>
-   <span class="signature">[`hasDataViewSupport()`][@taktikorg/quos-adipisci/has-dataview-support]</span><span class="delimiter">: </span><span class="description">detect native `DataView` support.</span>
-   <span class="signature">[`hasDefinePropertiesSupport()`][@taktikorg/quos-adipisci/has-define-properties-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperties` support.</span>
-   <span class="signature">[`hasDefinePropertySupport()`][@taktikorg/quos-adipisci/has-define-property-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperty` support.</span>
-   <span class="signature">[`hasFloat32ArraySupport()`][@taktikorg/quos-adipisci/has-float32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float32Array` support.</span>
-   <span class="signature">[`hasFloat64ArraySupport()`][@taktikorg/quos-adipisci/has-float64array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float64Array` support.</span>
-   <span class="signature">[`hasFunctionNameSupport()`][@taktikorg/quos-adipisci/has-function-name-support]</span><span class="delimiter">: </span><span class="description">detect native function `name` support.</span>
-   <span class="signature">[`hasGeneratorSupport()`][@taktikorg/quos-adipisci/has-generator-support]</span><span class="delimiter">: </span><span class="description">detect native `generator function` support.</span>
-   <span class="signature">[`hasGlobalThisSupport()`][@taktikorg/quos-adipisci/has-globalthis-support]</span><span class="delimiter">: </span><span class="description">detect `globalThis` support.</span>
-   <span class="signature">[`hasInt16ArraySupport()`][@taktikorg/quos-adipisci/has-int16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int16Array` support.</span>
-   <span class="signature">[`hasInt32ArraySupport()`][@taktikorg/quos-adipisci/has-int32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int32Array` support.</span>
-   <span class="signature">[`hasInt8ArraySupport()`][@taktikorg/quos-adipisci/has-int8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int8Array` support.</span>
-   <span class="signature">[`hasIteratorSymbolSupport()`][@taktikorg/quos-adipisci/has-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.iterator` support.</span>
-   <span class="signature">[`hasMapSupport()`][@taktikorg/quos-adipisci/has-map-support]</span><span class="delimiter">: </span><span class="description">detect native `Map` support.</span>
-   <span class="signature">[`hasNodeBufferSupport()`][@taktikorg/quos-adipisci/has-node-buffer-support]</span><span class="delimiter">: </span><span class="description">detect native `Buffer` support.</span>
-   <span class="signature">[`hasProxySupport()`][@taktikorg/quos-adipisci/has-proxy-support]</span><span class="delimiter">: </span><span class="description">detect native `Proxy` support.</span>
-   <span class="signature">[`hasSetSupport()`][@taktikorg/quos-adipisci/has-set-support]</span><span class="delimiter">: </span><span class="description">detect native `Set` support.</span>
-   <span class="signature">[`hasSharedArrayBufferSupport()`][@taktikorg/quos-adipisci/has-sharedarraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `SharedArrayBuffer` support.</span>
-   <span class="signature">[`hasSymbolSupport()`][@taktikorg/quos-adipisci/has-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol` support.</span>
-   <span class="signature">[`hasToStringTagSupport()`][@taktikorg/quos-adipisci/has-tostringtag-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.toStringTag` support.</span>
-   <span class="signature">[`hasUint16ArraySupport()`][@taktikorg/quos-adipisci/has-uint16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint16Array` support.</span>
-   <span class="signature">[`hasUint32ArraySupport()`][@taktikorg/quos-adipisci/has-uint32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint32Array` support.</span>
-   <span class="signature">[`hasUint8ArraySupport()`][@taktikorg/quos-adipisci/has-uint8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8Array` support.</span>
-   <span class="signature">[`hasUint8ClampedArraySupport()`][@taktikorg/quos-adipisci/has-uint8clampedarray-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8ClampedArray` support.</span>
-   <span class="signature">[`hasWebAssemblySupport()`][@taktikorg/quos-adipisci/has-wasm-support]</span><span class="delimiter">: </span><span class="description">detect native WebAssembly support.</span>
-   <span class="signature">[`hasWeakMapSupport()`][@taktikorg/quos-adipisci/has-weakmap-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakMap` support.</span>
-   <span class="signature">[`hasWeakSetSupport()`][@taktikorg/quos-adipisci/has-weakset-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakSet` support.</span>

</div>

<!-- </toc> -->

The remaining namespace utilities are as follows:

<!-- <toc ignore="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" ignore="is-*+(number|integer)*" ignore="is-*array*" ignore="is-*error*" ignore="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|node|web-worker|windows)" ignore="has-*-support" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`contains( val, searchValue[, position] )`][@taktikorg/quos-adipisci/contains]</span><span class="delimiter">: </span><span class="description">test if an array-like value contains a search value.</span>
-   <span class="signature">[`deepEqual( a, b )`][@taktikorg/quos-adipisci/deep-equal]</span><span class="delimiter">: </span><span class="description">test for deep equality between two values.</span>
-   <span class="signature">[`deepHasOwnProp( value, path[, options] )`][@taktikorg/quos-adipisci/deep-has-own-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path.</span>
-   <span class="signature">[`deepHasProp( value, path[, options] )`][@taktikorg/quos-adipisci/deep-has-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path, either own or inherited.</span>
-   <span class="signature">[`hasOwnProp( value, property )`][@taktikorg/quos-adipisci/has-own-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property.</span>
-   <span class="signature">[`hasProp( value, property )`][@taktikorg/quos-adipisci/has-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property, either own or inherited.</span>
-   <span class="signature">[`hasUTF16SurrogatePairAt( string, position )`][@taktikorg/quos-adipisci/has-utf16-surrogate-pair-at]</span><span class="delimiter">: </span><span class="description">test if a position in a string marks the start of a UTF-16 surrogate pair.</span>
-   <span class="signature">[`instanceOf( value, constructor )`][@taktikorg/quos-adipisci/instance-of]</span><span class="delimiter">: </span><span class="description">test whether a value has in its prototype chain a specified constructor as a prototype property.</span>
-   <span class="signature">[`isAbsoluteHttpURI( value )`][@taktikorg/quos-adipisci/is-absolute-http-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute HTTP(S) URI.</span>
-   <span class="signature">[`isAbsolutePath( value )`][@taktikorg/quos-adipisci/is-absolute-path]</span><span class="delimiter">: </span><span class="description">test if a value is an absolute path.</span>
-   <span class="signature">[`isAbsoluteURI( value )`][@taktikorg/quos-adipisci/is-absolute-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute URI.</span>
-   <span class="signature">[`isAccessorPropertyIn( value, property )`][@taktikorg/quos-adipisci/is-accessor-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has an accessor descriptor.</span>
-   <span class="signature">[`isAccessorProperty( value, property )`][@taktikorg/quos-adipisci/is-accessor-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has an accessor descriptor.</span>
-   <span class="signature">[`isAlphagram( value )`][@taktikorg/quos-adipisci/is-alphagram]</span><span class="delimiter">: </span><span class="description">test if a value is an alphagram.</span>
-   <span class="signature">[`isAlphaNumeric( value )`][@taktikorg/quos-adipisci/is-alphanumeric]</span><span class="delimiter">: </span><span class="description">test whether a string contains only alphanumeric characters.</span>
-   <span class="signature">[`isAnagram( str, value )`][@taktikorg/quos-adipisci/is-anagram]</span><span class="delimiter">: </span><span class="description">test if a value is an anagram.</span>
-   <span class="signature">[`isArguments( value )`][@taktikorg/quos-adipisci/is-arguments]</span><span class="delimiter">: </span><span class="description">test if a value is an arguments object.</span>
-   <span class="signature">[`isArrowFunction( value )`][@taktikorg/quos-adipisci/is-arrow-function]</span><span class="delimiter">: </span><span class="description">test if a value is an `arrow function`.</span>
-   <span class="signature">[`isASCII( value )`][@taktikorg/quos-adipisci/is-ascii]</span><span class="delimiter">: </span><span class="description">test whether a character belongs to the ASCII character set and whether this is true for all characters in a provided string.</span>
-   <span class="signature">[`isBetween( value, a, b[, left, right] )`][@taktikorg/quos-adipisci/is-between]</span><span class="delimiter">: </span><span class="description">test if a value is between two values.</span>
-   <span class="signature">[`isBigInt( value )`][@taktikorg/quos-adipisci/is-bigint]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt.</span>
-   <span class="signature">[`isBinaryString( value )`][@taktikorg/quos-adipisci/is-binary-string]</span><span class="delimiter">: </span><span class="description">test if a value is a binary string.</span>
-   <span class="signature">[`isBlankString( value )`][@taktikorg/quos-adipisci/is-blank-string]</span><span class="delimiter">: </span><span class="description">test if a value is a blank string.</span>
-   <span class="signature">[`isBoxedPrimitive( value )`][@taktikorg/quos-adipisci/is-boxed-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript boxed primitive.</span>
-   <span class="signature">[`isBuffer( value )`][@taktikorg/quos-adipisci/is-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a Buffer object.</span>
-   <span class="signature">[`isCamelcase( value )`][@taktikorg/quos-adipisci/is-camelcase]</span><span class="delimiter">: </span><span class="description">test if a value is a camelcase string.</span>
-   <span class="signature">[`isCapitalized( value )`][@taktikorg/quos-adipisci/is-capitalized]</span><span class="delimiter">: </span><span class="description">test if a value is a string having an uppercase first character.</span>
-   <span class="signature">[`isCircular( value )`][@taktikorg/quos-adipisci/is-circular]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object containing a circular reference.</span>
-   <span class="signature">[`isCircular( value )`][@taktikorg/quos-adipisci/is-circular]</span><span class="delimiter">: </span><span class="description">test if an object-like value contains a circular reference.</span>
-   <span class="signature">[`isClass( value )`][@taktikorg/quos-adipisci/is-class]</span><span class="delimiter">: </span><span class="description">test if a value is a class.</span>
-   <span class="signature">[`isCollection( value )`][@taktikorg/quos-adipisci/is-collection]</span><span class="delimiter">: </span><span class="description">test if a value is a collection.</span>
-   <span class="signature">[`isComposite( value )`][@taktikorg/quos-adipisci/is-composite]</span><span class="delimiter">: </span><span class="description">test if a value is a composite number.</span>
-   <span class="signature">[`isConfigurablePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-configurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is configurable.</span>
-   <span class="signature">[`isConfigurableProperty( value, property )`][@taktikorg/quos-adipisci/is-configurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is configurable.</span>
-   <span class="signature">[`isConstantcase( value )`][@taktikorg/quos-adipisci/is-constantcase]</span><span class="delimiter">: </span><span class="description">test if a value is a constantcase string.</span>
-   <span class="signature">[`isCurrentYear( value )`][@taktikorg/quos-adipisci/is-current-year]</span><span class="delimiter">: </span><span class="description">test if a value is the current year.</span>
-   <span class="signature">[`isDataPropertyIn( value, property )`][@taktikorg/quos-adipisci/is-data-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has a data descriptor.</span>
-   <span class="signature">[`isDataProperty( value, property )`][@taktikorg/quos-adipisci/is-data-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has a data descriptor.</span>
-   <span class="signature">[`isDataView( value )`][@taktikorg/quos-adipisci/is-dataview]</span><span class="delimiter">: </span><span class="description">test if a value is a DataView.</span>
-   <span class="signature">[`isDigitString( value )`][@taktikorg/quos-adipisci/is-digit-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only numeric digits.</span>
-   <span class="signature">[`isDomainName( value )`][@taktikorg/quos-adipisci/is-domain-name]</span><span class="delimiter">: </span><span class="description">test if a value is a domain name.</span>
-   <span class="signature">[`isDurationString( value )`][@taktikorg/quos-adipisci/is-duration-string]</span><span class="delimiter">: </span><span class="description">test if a value is a duration string.</span>
-   <span class="signature">[`isEmailAddress( value )`][@taktikorg/quos-adipisci/is-email-address]</span><span class="delimiter">: </span><span class="description">test if a value is an email address.</span>
-   <span class="signature">[`isEmptyCollection( value )`][@taktikorg/quos-adipisci/is-empty-collection]</span><span class="delimiter">: </span><span class="description">test if a value is an empty collection.</span>
-   <span class="signature">[`isEmptyObject( value )`][@taktikorg/quos-adipisci/is-empty-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty object.</span>
-   <span class="signature">[`isEmptyString( value )`][@taktikorg/quos-adipisci/is-empty-string]</span><span class="delimiter">: </span><span class="description">test if a value is an empty string.</span>
-   <span class="signature">[`isEnumerablePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-enumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is enumerable.</span>
-   <span class="signature">[`isEnumerableProperty( value, property )`][@taktikorg/quos-adipisci/is-enumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is enumerable.</span>
-   <span class="signature">[`isEven( value )`][@taktikorg/quos-adipisci/is-even]</span><span class="delimiter">: </span><span class="description">test if a value is an even number.</span>
-   <span class="signature">[`isFalsy( value )`][@taktikorg/quos-adipisci/is-falsy]</span><span class="delimiter">: </span><span class="description">test if a value is falsy.</span>
-   <span class="signature">[`isFinite( value )`][@taktikorg/quos-adipisci/is-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a finite number.</span>
-   <span class="signature">[`isGeneratorObjectLike( value )`][@taktikorg/quos-adipisci/is-generator-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is `generator` object-like.</span>
-   <span class="signature">[`isGeneratorObject( value )`][@taktikorg/quos-adipisci/is-generator-object]</span><span class="delimiter">: </span><span class="description">test if a value is a `generator` object.</span>
-   <span class="signature">[`isgzipBuffer( value )`][@taktikorg/quos-adipisci/is-gzip-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a gzip buffer.</span>
-   <span class="signature">[`isHexString( value )`][@taktikorg/quos-adipisci/is-hex-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only hexadecimal digits.</span>
-   <span class="signature">[`isInfinite( value )`][@taktikorg/quos-adipisci/is-infinite]</span><span class="delimiter">: </span><span class="description">test if a value is an infinite number.</span>
-   <span class="signature">[`isInheritedProperty( value, property )`][@taktikorg/quos-adipisci/is-inherited-property]</span><span class="delimiter">: </span><span class="description">test if an object has an inherited property.</span>
-   <span class="signature">[`isIterableLike( value )`][@taktikorg/quos-adipisci/is-iterable-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterable`-like.</span>
-   <span class="signature">[`isIteratorLike( value )`][@taktikorg/quos-adipisci/is-iterator-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterator`-like.</span>
-   <span class="signature">[`isJSON( value )`][@taktikorg/quos-adipisci/is-json]</span><span class="delimiter">: </span><span class="description">test if a value is a parseable JSON string.</span>
-   <span class="signature">[`isKebabcase( value )`][@taktikorg/quos-adipisci/is-kebabcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in kebab case.</span>
-   <span class="signature">[`isLeapYear( [value] )`][@taktikorg/quos-adipisci/is-leap-year]</span><span class="delimiter">: </span><span class="description">test if a value corresponds to a leap year in the Gregorian calendar.</span>
-   <span class="signature">[`isLocalhost( value )`][@taktikorg/quos-adipisci/is-localhost]</span><span class="delimiter">: </span><span class="description">test whether a value is a localhost hostname.</span>
-   <span class="signature">[`isLowercase( value )`][@taktikorg/quos-adipisci/is-lowercase]</span><span class="delimiter">: </span><span class="description">test if a value is a lowercase string.</span>
-   <span class="signature">[`isMethodIn( value, property )`][@taktikorg/quos-adipisci/is-method-in]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name, either own or inherited.</span>
-   <span class="signature">[`isMethod( value, property )`][@taktikorg/quos-adipisci/is-method]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name.</span>
-   <span class="signature">[`isMultiSlice( value )`][@taktikorg/quos-adipisci/is-multi-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `MultiSlice`.</span>
-   <span class="signature">[`isNamedTypedTupleLike( value )`][@taktikorg/quos-adipisci/is-named-typed-tuple-like]</span><span class="delimiter">: </span><span class="description">test if a value is named typed tuple-like.</span>
-   <span class="signature">[`isNativeFunction( value )`][@taktikorg/quos-adipisci/is-native-function]</span><span class="delimiter">: </span><span class="description">test if a value is a native function.</span>
-   <span class="signature">[`isNegativeZero( value )`][@taktikorg/quos-adipisci/is-negative-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to negative zero.</span>
-   <span class="signature">[`isNodeBuiltin( value )`][@taktikorg/quos-adipisci/is-node-builtin]</span><span class="delimiter">: </span><span class="description">test whether a string matches a Node.js built-in module name.</span>
-   <span class="signature">[`isNodeDuplexStreamLike( value )`][@taktikorg/quos-adipisci/is-node-duplex-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node duplex stream-like.</span>
-   <span class="signature">[`isNodeReadableStreamLike( value )`][@taktikorg/quos-adipisci/is-node-readable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node readable stream-like.</span>
-   <span class="signature">[`isNodeREPL()`][@taktikorg/quos-adipisci/is-node-repl]</span><span class="delimiter">: </span><span class="description">check if running in a Node.js REPL environment.</span>
-   <span class="signature">[`isNodeStreamLike( value )`][@taktikorg/quos-adipisci/is-node-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node stream-like.</span>
-   <span class="signature">[`isNodeTransformStreamLike( value )`][@taktikorg/quos-adipisci/is-node-transform-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node transform stream-like.</span>
-   <span class="signature">[`isNodeWritableStreamLike( value )`][@taktikorg/quos-adipisci/is-node-writable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node writable stream-like.</span>
-   <span class="signature">[`isNonConfigurablePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-nonconfigurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-configurable.</span>
-   <span class="signature">[`isNonConfigurableProperty( value, property )`][@taktikorg/quos-adipisci/is-nonconfigurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-configurable.</span>
-   <span class="signature">[`isNonEnumerablePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-nonenumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-enumerable.</span>
-   <span class="signature">[`isNonEnumerableProperty( value, property )`][@taktikorg/quos-adipisci/is-nonenumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-enumerable.</span>
-   <span class="signature">[`isNonNegativeFinite( value )`][@taktikorg/quos-adipisci/is-nonnegative-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative finite value.</span>
-   <span class="signature">[`isObjectLike( value )`][@taktikorg/quos-adipisci/is-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is object-like.</span>
-   <span class="signature">[`isOdd( value )`][@taktikorg/quos-adipisci/is-odd]</span><span class="delimiter">: </span><span class="description">test if a value is an odd number.</span>
-   <span class="signature">[`isPascalcase( value )`][@taktikorg/quos-adipisci/is-pascalcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in Pascal case.</span>
-   <span class="signature">[`isPlainObject( value )`][@taktikorg/quos-adipisci/is-plain-object]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object.</span>
-   <span class="signature">[`isPositiveZero( value )`][@taktikorg/quos-adipisci/is-positive-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to positive zero.</span>
-   <span class="signature">[`isPrime( value )`][@taktikorg/quos-adipisci/is-prime]</span><span class="delimiter">: </span><span class="description">test if a value is a prime number.</span>
-   <span class="signature">[`isPrimitive( value )`][@taktikorg/quos-adipisci/is-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript primitive.</span>
-   <span class="signature">[`isPRNGLike( value )`][@taktikorg/quos-adipisci/is-prng-like]</span><span class="delimiter">: </span><span class="description">test if a value is PRNG-like.</span>
-   <span class="signature">[`isProbability( value )`][@taktikorg/quos-adipisci/is-probability]</span><span class="delimiter">: </span><span class="description">test if a value is a probability.</span>
-   <span class="signature">[`isPropertyKey( value )`][@taktikorg/quos-adipisci/is-property-key]</span><span class="delimiter">: </span><span class="description">test whether a value is a property key.</span>
-   <span class="signature">[`isPrototypeOf( obj, prototype )`][@taktikorg/quos-adipisci/is-prototype-of]</span><span class="delimiter">: </span><span class="description">test if an object's prototype chain contains a provided prototype.</span>
-   <span class="signature">[`isReadOnlyPropertyIn( value, property )`][@taktikorg/quos-adipisci/is-read-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is read-only.</span>
-   <span class="signature">[`isReadOnlyProperty( value, property )`][@taktikorg/quos-adipisci/is-read-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is read-only.</span>
-   <span class="signature">[`isReadWritePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-read-write-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable and writable.</span>
-   <span class="signature">[`isReadWriteProperty( value, property )`][@taktikorg/quos-adipisci/is-read-write-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable and writable.</span>
-   <span class="signature">[`isReadablePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-readable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable.</span>
-   <span class="signature">[`isReadableProperty( value, property )`][@taktikorg/quos-adipisci/is-readable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable.</span>
-   <span class="signature">[`isRegExpString( value )`][@taktikorg/quos-adipisci/is-regexp-string]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression string.</span>
-   <span class="signature">[`isRelativePath( value )`][@taktikorg/quos-adipisci/is-relative-path]</span><span class="delimiter">: </span><span class="description">test if a value is a relative path.</span>
-   <span class="signature">[`isRelativeURI( value )`][@taktikorg/quos-adipisci/is-relative-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is a relative URI.</span>
-   <span class="signature">[`isSameComplex128( v1, v2 )`][@taktikorg/quos-adipisci/is-same-complex128]</span><span class="delimiter">: </span><span class="description">test if two arguments are both double-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameComplex64( v1, v2 )`][@taktikorg/quos-adipisci/is-same-complex64]</span><span class="delimiter">: </span><span class="description">test if two arguments are both single-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameNativeClass( a, b )`][@taktikorg/quos-adipisci/is-same-native-class]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same native class.</span>
-   <span class="signature">[`isSameType( a, b )`][@taktikorg/quos-adipisci/is-same-type]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same type.</span>
-   <span class="signature">[`isSameValueZero( a, b )`][@taktikorg/quos-adipisci/is-same-value-zero]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSameValue( a, b )`][@taktikorg/quos-adipisci/is-same-value]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSemVer( value )`][@taktikorg/quos-adipisci/is-semver]</span><span class="delimiter">: </span><span class="description">test if a value is a semantic version string.</span>
-   <span class="signature">[`isSlice( value )`][@taktikorg/quos-adipisci/is-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `Slice`.</span>
-   <span class="signature">[`isSnakecase( value )`][@taktikorg/quos-adipisci/is-snakecase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in snake case.</span>
-   <span class="signature">[`isStartcase( value )`][@taktikorg/quos-adipisci/is-startcase]</span><span class="delimiter">: </span><span class="description">test if a value is a startcase string.</span>
-   <span class="signature">[`isStrictEqual( a, b )`][@taktikorg/quos-adipisci/is-strict-equal]</span><span class="delimiter">: </span><span class="description">test if two arguments are strictly equal.</span>
-   <span class="signature">[`isTruthy( value )`][@taktikorg/quos-adipisci/is-truthy]</span><span class="delimiter">: </span><span class="description">test if a value is truthy.</span>
-   <span class="signature">[`isUNCPath( value )`][@taktikorg/quos-adipisci/is-unc-path]</span><span class="delimiter">: </span><span class="description">test if a value is a UNC path.</span>
-   <span class="signature">[`isUndefinedOrNull( value )`][@taktikorg/quos-adipisci/is-undefined-or-null]</span><span class="delimiter">: </span><span class="description">test if a value is undefined or null.</span>
-   <span class="signature">[`isUppercase( value )`][@taktikorg/quos-adipisci/is-uppercase]</span><span class="delimiter">: </span><span class="description">test if a value is an uppercase string.</span>
-   <span class="signature">[`isURI( value )`][@taktikorg/quos-adipisci/is-uri]</span><span class="delimiter">: </span><span class="description">test if a value is a URI.</span>
-   <span class="signature">[`isWhitespace( value )`][@taktikorg/quos-adipisci/is-whitespace]</span><span class="delimiter">: </span><span class="description">test whether a string contains only white space characters.</span>
-   <span class="signature">[`isWritablePropertyIn( value, property )`][@taktikorg/quos-adipisci/is-writable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is writable.</span>
-   <span class="signature">[`isWritableProperty( value, property )`][@taktikorg/quos-adipisci/is-writable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is writable.</span>
-   <span class="signature">[`isWriteOnlyPropertyIn( value, property )`][@taktikorg/quos-adipisci/is-write-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is write-only.</span>
-   <span class="signature">[`isWriteOnlyProperty( value, property )`][@taktikorg/quos-adipisci/is-write-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is write-only.</span>
-   <span class="signature">[`tools`][@taktikorg/quos-adipisci/tools]</span><span class="delimiter">: </span><span class="description">assertion utility tools.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var assert = require( '@taktikorg/quos-adipisci' );

console.log( objectKeys( assert ) );
```

</section>

<!-- /.examples -->

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@taktikorg/quos-adipisci.svg
[npm-url]: https://npmjs.org/package/@taktikorg/quos-adipisci

[test-image]: https://github.com/taktikorg/quos-adipisci/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/taktikorg/quos-adipisci/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/taktikorg/quos-adipisci/main.svg
[coverage-url]: https://codecov.io/github/taktikorg/quos-adipisci?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/taktikorg/quos-adipisci.svg
[dependencies-url]: https://david-dm.org/taktikorg/quos-adipisci/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/taktikorg/quos-adipisci/tree/deno
[deno-readme]: https://github.com/taktikorg/quos-adipisci/blob/deno/README.md
[umd-url]: https://github.com/taktikorg/quos-adipisci/tree/umd
[umd-readme]: https://github.com/taktikorg/quos-adipisci/blob/umd/README.md
[esm-url]: https://github.com/taktikorg/quos-adipisci/tree/esm
[esm-readme]: https://github.com/taktikorg/quos-adipisci/blob/esm/README.md
[branches-url]: https://github.com/taktikorg/quos-adipisci/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/taktikorg/quos-adipisci/main/LICENSE

<!-- <toc-links> -->

[@taktikorg/quos-adipisci/contains]: https://github.com/taktikorg/quos-adipisci/tree/main/contains

[@taktikorg/quos-adipisci/deep-equal]: https://github.com/taktikorg/quos-adipisci/tree/main/deep-equal

[@taktikorg/quos-adipisci/deep-has-own-property]: https://github.com/taktikorg/quos-adipisci/tree/main/deep-has-own-property

[@taktikorg/quos-adipisci/deep-has-property]: https://github.com/taktikorg/quos-adipisci/tree/main/deep-has-property

[@taktikorg/quos-adipisci/has-own-property]: https://github.com/taktikorg/quos-adipisci/tree/main/has-own-property

[@taktikorg/quos-adipisci/has-property]: https://github.com/taktikorg/quos-adipisci/tree/main/has-property

[@taktikorg/quos-adipisci/has-utf16-surrogate-pair-at]: https://github.com/taktikorg/quos-adipisci/tree/main/has-utf16-surrogate-pair-at

[@taktikorg/quos-adipisci/instance-of]: https://github.com/taktikorg/quos-adipisci/tree/main/instance-of

[@taktikorg/quos-adipisci/is-absolute-http-uri]: https://github.com/taktikorg/quos-adipisci/tree/main/is-absolute-http-uri

[@taktikorg/quos-adipisci/is-absolute-path]: https://github.com/taktikorg/quos-adipisci/tree/main/is-absolute-path

[@taktikorg/quos-adipisci/is-absolute-uri]: https://github.com/taktikorg/quos-adipisci/tree/main/is-absolute-uri

[@taktikorg/quos-adipisci/is-accessor-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-accessor-property-in

[@taktikorg/quos-adipisci/is-accessor-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-accessor-property

[@taktikorg/quos-adipisci/is-alphagram]: https://github.com/taktikorg/quos-adipisci/tree/main/is-alphagram

[@taktikorg/quos-adipisci/is-alphanumeric]: https://github.com/taktikorg/quos-adipisci/tree/main/is-alphanumeric

[@taktikorg/quos-adipisci/is-anagram]: https://github.com/taktikorg/quos-adipisci/tree/main/is-anagram

[@taktikorg/quos-adipisci/is-arguments]: https://github.com/taktikorg/quos-adipisci/tree/main/is-arguments

[@taktikorg/quos-adipisci/is-arrow-function]: https://github.com/taktikorg/quos-adipisci/tree/main/is-arrow-function

[@taktikorg/quos-adipisci/is-ascii]: https://github.com/taktikorg/quos-adipisci/tree/main/is-ascii

[@taktikorg/quos-adipisci/is-between]: https://github.com/taktikorg/quos-adipisci/tree/main/is-between

[@taktikorg/quos-adipisci/is-bigint]: https://github.com/taktikorg/quos-adipisci/tree/main/is-bigint

[@taktikorg/quos-adipisci/is-binary-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-binary-string

[@taktikorg/quos-adipisci/is-blank-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-blank-string

[@taktikorg/quos-adipisci/is-boxed-primitive]: https://github.com/taktikorg/quos-adipisci/tree/main/is-boxed-primitive

[@taktikorg/quos-adipisci/is-buffer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-buffer

[@taktikorg/quos-adipisci/is-camelcase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-camelcase

[@taktikorg/quos-adipisci/is-capitalized]: https://github.com/taktikorg/quos-adipisci/tree/main/is-capitalized

[@taktikorg/quos-adipisci/is-circular]: https://github.com/taktikorg/quos-adipisci/tree/main/is-circular

[@taktikorg/quos-adipisci/is-class]: https://github.com/taktikorg/quos-adipisci/tree/main/is-class

[@taktikorg/quos-adipisci/is-collection]: https://github.com/taktikorg/quos-adipisci/tree/main/is-collection

[@taktikorg/quos-adipisci/is-composite]: https://github.com/taktikorg/quos-adipisci/tree/main/is-composite

[@taktikorg/quos-adipisci/is-configurable-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-configurable-property-in

[@taktikorg/quos-adipisci/is-configurable-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-configurable-property

[@taktikorg/quos-adipisci/is-constantcase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-constantcase

[@taktikorg/quos-adipisci/is-current-year]: https://github.com/taktikorg/quos-adipisci/tree/main/is-current-year

[@taktikorg/quos-adipisci/is-data-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-data-property-in

[@taktikorg/quos-adipisci/is-data-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-data-property

[@taktikorg/quos-adipisci/is-dataview]: https://github.com/taktikorg/quos-adipisci/tree/main/is-dataview

[@taktikorg/quos-adipisci/is-digit-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-digit-string

[@taktikorg/quos-adipisci/is-domain-name]: https://github.com/taktikorg/quos-adipisci/tree/main/is-domain-name

[@taktikorg/quos-adipisci/is-duration-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-duration-string

[@taktikorg/quos-adipisci/is-email-address]: https://github.com/taktikorg/quos-adipisci/tree/main/is-email-address

[@taktikorg/quos-adipisci/is-empty-collection]: https://github.com/taktikorg/quos-adipisci/tree/main/is-empty-collection

[@taktikorg/quos-adipisci/is-empty-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-empty-object

[@taktikorg/quos-adipisci/is-empty-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-empty-string

[@taktikorg/quos-adipisci/is-enumerable-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-enumerable-property-in

[@taktikorg/quos-adipisci/is-enumerable-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-enumerable-property

[@taktikorg/quos-adipisci/is-even]: https://github.com/taktikorg/quos-adipisci/tree/main/is-even

[@taktikorg/quos-adipisci/is-falsy]: https://github.com/taktikorg/quos-adipisci/tree/main/is-falsy

[@taktikorg/quos-adipisci/is-finite]: https://github.com/taktikorg/quos-adipisci/tree/main/is-finite

[@taktikorg/quos-adipisci/is-generator-object-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-generator-object-like

[@taktikorg/quos-adipisci/is-generator-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-generator-object

[@taktikorg/quos-adipisci/is-gzip-buffer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-gzip-buffer

[@taktikorg/quos-adipisci/is-hex-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-hex-string

[@taktikorg/quos-adipisci/is-infinite]: https://github.com/taktikorg/quos-adipisci/tree/main/is-infinite

[@taktikorg/quos-adipisci/is-inherited-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-inherited-property

[@taktikorg/quos-adipisci/is-iterable-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-iterable-like

[@taktikorg/quos-adipisci/is-iterator-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-iterator-like

[@taktikorg/quos-adipisci/is-json]: https://github.com/taktikorg/quos-adipisci/tree/main/is-json

[@taktikorg/quos-adipisci/is-kebabcase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-kebabcase

[@taktikorg/quos-adipisci/is-leap-year]: https://github.com/taktikorg/quos-adipisci/tree/main/is-leap-year

[@taktikorg/quos-adipisci/is-localhost]: https://github.com/taktikorg/quos-adipisci/tree/main/is-localhost

[@taktikorg/quos-adipisci/is-lowercase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-lowercase

[@taktikorg/quos-adipisci/is-method-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-method-in

[@taktikorg/quos-adipisci/is-method]: https://github.com/taktikorg/quos-adipisci/tree/main/is-method

[@taktikorg/quos-adipisci/is-multi-slice]: https://github.com/taktikorg/quos-adipisci/tree/main/is-multi-slice

[@taktikorg/quos-adipisci/is-named-typed-tuple-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-named-typed-tuple-like

[@taktikorg/quos-adipisci/is-native-function]: https://github.com/taktikorg/quos-adipisci/tree/main/is-native-function

[@taktikorg/quos-adipisci/is-negative-zero]: https://github.com/taktikorg/quos-adipisci/tree/main/is-negative-zero

[@taktikorg/quos-adipisci/is-node-builtin]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-builtin

[@taktikorg/quos-adipisci/is-node-duplex-stream-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-duplex-stream-like

[@taktikorg/quos-adipisci/is-node-readable-stream-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-readable-stream-like

[@taktikorg/quos-adipisci/is-node-repl]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-repl

[@taktikorg/quos-adipisci/is-node-stream-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-stream-like

[@taktikorg/quos-adipisci/is-node-transform-stream-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-transform-stream-like

[@taktikorg/quos-adipisci/is-node-writable-stream-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node-writable-stream-like

[@taktikorg/quos-adipisci/is-nonconfigurable-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonconfigurable-property-in

[@taktikorg/quos-adipisci/is-nonconfigurable-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonconfigurable-property

[@taktikorg/quos-adipisci/is-nonenumerable-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonenumerable-property-in

[@taktikorg/quos-adipisci/is-nonenumerable-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonenumerable-property

[@taktikorg/quos-adipisci/is-nonnegative-finite]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonnegative-finite

[@taktikorg/quos-adipisci/is-object-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-object-like

[@taktikorg/quos-adipisci/is-odd]: https://github.com/taktikorg/quos-adipisci/tree/main/is-odd

[@taktikorg/quos-adipisci/is-pascalcase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-pascalcase

[@taktikorg/quos-adipisci/is-plain-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-plain-object

[@taktikorg/quos-adipisci/is-positive-zero]: https://github.com/taktikorg/quos-adipisci/tree/main/is-positive-zero

[@taktikorg/quos-adipisci/is-prime]: https://github.com/taktikorg/quos-adipisci/tree/main/is-prime

[@taktikorg/quos-adipisci/is-primitive]: https://github.com/taktikorg/quos-adipisci/tree/main/is-primitive

[@taktikorg/quos-adipisci/is-prng-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-prng-like

[@taktikorg/quos-adipisci/is-probability]: https://github.com/taktikorg/quos-adipisci/tree/main/is-probability

[@taktikorg/quos-adipisci/is-property-key]: https://github.com/taktikorg/quos-adipisci/tree/main/is-property-key

[@taktikorg/quos-adipisci/is-prototype-of]: https://github.com/taktikorg/quos-adipisci/tree/main/is-prototype-of

[@taktikorg/quos-adipisci/is-read-only-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-read-only-property-in

[@taktikorg/quos-adipisci/is-read-only-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-read-only-property

[@taktikorg/quos-adipisci/is-read-write-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-read-write-property-in

[@taktikorg/quos-adipisci/is-read-write-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-read-write-property

[@taktikorg/quos-adipisci/is-readable-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-readable-property-in

[@taktikorg/quos-adipisci/is-readable-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-readable-property

[@taktikorg/quos-adipisci/is-regexp-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-regexp-string

[@taktikorg/quos-adipisci/is-relative-path]: https://github.com/taktikorg/quos-adipisci/tree/main/is-relative-path

[@taktikorg/quos-adipisci/is-relative-uri]: https://github.com/taktikorg/quos-adipisci/tree/main/is-relative-uri

[@taktikorg/quos-adipisci/is-same-complex128]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-complex128

[@taktikorg/quos-adipisci/is-same-complex64]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-complex64

[@taktikorg/quos-adipisci/is-same-native-class]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-native-class

[@taktikorg/quos-adipisci/is-same-type]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-type

[@taktikorg/quos-adipisci/is-same-value-zero]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-value-zero

[@taktikorg/quos-adipisci/is-same-value]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-value

[@taktikorg/quos-adipisci/is-semver]: https://github.com/taktikorg/quos-adipisci/tree/main/is-semver

[@taktikorg/quos-adipisci/is-slice]: https://github.com/taktikorg/quos-adipisci/tree/main/is-slice

[@taktikorg/quos-adipisci/is-snakecase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-snakecase

[@taktikorg/quos-adipisci/is-startcase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-startcase

[@taktikorg/quos-adipisci/is-strict-equal]: https://github.com/taktikorg/quos-adipisci/tree/main/is-strict-equal

[@taktikorg/quos-adipisci/is-truthy]: https://github.com/taktikorg/quos-adipisci/tree/main/is-truthy

[@taktikorg/quos-adipisci/is-unc-path]: https://github.com/taktikorg/quos-adipisci/tree/main/is-unc-path

[@taktikorg/quos-adipisci/is-undefined-or-null]: https://github.com/taktikorg/quos-adipisci/tree/main/is-undefined-or-null

[@taktikorg/quos-adipisci/is-uppercase]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uppercase

[@taktikorg/quos-adipisci/is-uri]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uri

[@taktikorg/quos-adipisci/is-whitespace]: https://github.com/taktikorg/quos-adipisci/tree/main/is-whitespace

[@taktikorg/quos-adipisci/is-writable-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-writable-property-in

[@taktikorg/quos-adipisci/is-writable-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-writable-property

[@taktikorg/quos-adipisci/is-write-only-property-in]: https://github.com/taktikorg/quos-adipisci/tree/main/is-write-only-property-in

[@taktikorg/quos-adipisci/is-write-only-property]: https://github.com/taktikorg/quos-adipisci/tree/main/is-write-only-property

[@taktikorg/quos-adipisci/tools]: https://github.com/taktikorg/quos-adipisci/tree/main/tools

[@taktikorg/quos-adipisci/has-arraybuffer-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-arraybuffer-support

[@taktikorg/quos-adipisci/has-arrow-function-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-arrow-function-support

[@taktikorg/quos-adipisci/has-async-await-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-async-await-support

[@taktikorg/quos-adipisci/has-async-iterator-symbol-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-async-iterator-symbol-support

[@taktikorg/quos-adipisci/has-bigint-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-bigint-support

[@taktikorg/quos-adipisci/has-bigint64array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-bigint64array-support

[@taktikorg/quos-adipisci/has-biguint64array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-biguint64array-support

[@taktikorg/quos-adipisci/has-class-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-class-support

[@taktikorg/quos-adipisci/has-dataview-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-dataview-support

[@taktikorg/quos-adipisci/has-define-properties-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-define-properties-support

[@taktikorg/quos-adipisci/has-define-property-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-define-property-support

[@taktikorg/quos-adipisci/has-float32array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-float32array-support

[@taktikorg/quos-adipisci/has-float64array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-float64array-support

[@taktikorg/quos-adipisci/has-function-name-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-function-name-support

[@taktikorg/quos-adipisci/has-generator-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-generator-support

[@taktikorg/quos-adipisci/has-globalthis-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-globalthis-support

[@taktikorg/quos-adipisci/has-int16array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-int16array-support

[@taktikorg/quos-adipisci/has-int32array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-int32array-support

[@taktikorg/quos-adipisci/has-int8array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-int8array-support

[@taktikorg/quos-adipisci/has-iterator-symbol-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-iterator-symbol-support

[@taktikorg/quos-adipisci/has-map-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-map-support

[@taktikorg/quos-adipisci/has-node-buffer-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-node-buffer-support

[@taktikorg/quos-adipisci/has-proxy-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-proxy-support

[@taktikorg/quos-adipisci/has-set-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-set-support

[@taktikorg/quos-adipisci/has-sharedarraybuffer-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-sharedarraybuffer-support

[@taktikorg/quos-adipisci/has-symbol-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-symbol-support

[@taktikorg/quos-adipisci/has-tostringtag-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-tostringtag-support

[@taktikorg/quos-adipisci/has-uint16array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-uint16array-support

[@taktikorg/quos-adipisci/has-uint32array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-uint32array-support

[@taktikorg/quos-adipisci/has-uint8array-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-uint8array-support

[@taktikorg/quos-adipisci/has-uint8clampedarray-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-uint8clampedarray-support

[@taktikorg/quos-adipisci/has-wasm-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-wasm-support

[@taktikorg/quos-adipisci/has-weakmap-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-weakmap-support

[@taktikorg/quos-adipisci/has-weakset-support]: https://github.com/taktikorg/quos-adipisci/tree/main/has-weakset-support

[@taktikorg/quos-adipisci/is-big-endian]: https://github.com/taktikorg/quos-adipisci/tree/main/is-big-endian

[@taktikorg/quos-adipisci/is-browser]: https://github.com/taktikorg/quos-adipisci/tree/main/is-browser

[@taktikorg/quos-adipisci/is-darwin]: https://github.com/taktikorg/quos-adipisci/tree/main/is-darwin

[@taktikorg/quos-adipisci/is-docker]: https://github.com/taktikorg/quos-adipisci/tree/main/is-docker

[@taktikorg/quos-adipisci/is-electron-main]: https://github.com/taktikorg/quos-adipisci/tree/main/is-electron-main

[@taktikorg/quos-adipisci/is-electron-renderer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-electron-renderer

[@taktikorg/quos-adipisci/is-electron]: https://github.com/taktikorg/quos-adipisci/tree/main/is-electron

[@taktikorg/quos-adipisci/is-little-endian]: https://github.com/taktikorg/quos-adipisci/tree/main/is-little-endian

[@taktikorg/quos-adipisci/is-mobile]: https://github.com/taktikorg/quos-adipisci/tree/main/is-mobile

[@taktikorg/quos-adipisci/is-node]: https://github.com/taktikorg/quos-adipisci/tree/main/is-node

[@taktikorg/quos-adipisci/is-touch-device]: https://github.com/taktikorg/quos-adipisci/tree/main/is-touch-device

[@taktikorg/quos-adipisci/is-web-worker]: https://github.com/taktikorg/quos-adipisci/tree/main/is-web-worker

[@taktikorg/quos-adipisci/is-windows]: https://github.com/taktikorg/quos-adipisci/tree/main/is-windows

[@taktikorg/quos-adipisci/is-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-error

[@taktikorg/quos-adipisci/is-eval-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-eval-error

[@taktikorg/quos-adipisci/is-range-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-range-error

[@taktikorg/quos-adipisci/is-reference-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-reference-error

[@taktikorg/quos-adipisci/is-syntax-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-syntax-error

[@taktikorg/quos-adipisci/is-type-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-type-error

[@taktikorg/quos-adipisci/is-uri-error]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uri-error

[@taktikorg/quos-adipisci/is-accessor-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-accessor-array

[@taktikorg/quos-adipisci/is-array-length]: https://github.com/taktikorg/quos-adipisci/tree/main/is-array-length

[@taktikorg/quos-adipisci/is-array-like-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-array-like-object

[@taktikorg/quos-adipisci/is-array-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-array-like

[@taktikorg/quos-adipisci/is-arraybuffer-view]: https://github.com/taktikorg/quos-adipisci/tree/main/is-arraybuffer-view

[@taktikorg/quos-adipisci/is-arraybuffer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-arraybuffer

[@taktikorg/quos-adipisci/is-between-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-between-array

[@taktikorg/quos-adipisci/is-bigint64array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-bigint64array

[@taktikorg/quos-adipisci/is-biguint64array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-biguint64array

[@taktikorg/quos-adipisci/is-circular-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-circular-array

[@taktikorg/quos-adipisci/is-empty-array-like-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-empty-array-like-object

[@taktikorg/quos-adipisci/is-empty-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-empty-array

[@taktikorg/quos-adipisci/is-falsy-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-falsy-array

[@taktikorg/quos-adipisci/is-finite-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-finite-array

[@taktikorg/quos-adipisci/is-numeric-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-numeric-array

[@taktikorg/quos-adipisci/is-plain-object-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-plain-object-array

[@taktikorg/quos-adipisci/is-probability-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-probability-array

[@taktikorg/quos-adipisci/is-same-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-array

[@taktikorg/quos-adipisci/is-same-complex128array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-complex128array

[@taktikorg/quos-adipisci/is-same-complex64array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-complex64array

[@taktikorg/quos-adipisci/is-same-float32array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-float32array

[@taktikorg/quos-adipisci/is-same-float64array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-same-float64array

[@taktikorg/quos-adipisci/is-sharedarraybuffer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-sharedarraybuffer

[@taktikorg/quos-adipisci/is-truthy-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-truthy-array

[@taktikorg/quos-adipisci/is-typed-array-length]: https://github.com/taktikorg/quos-adipisci/tree/main/is-typed-array-length

[@taktikorg/quos-adipisci/is-typed-array-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-typed-array-like

[@taktikorg/quos-adipisci/is-typed-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-typed-array

[@taktikorg/quos-adipisci/is-unity-probability-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-unity-probability-array

[@taktikorg/quos-adipisci/is-complex-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex-like

[@taktikorg/quos-adipisci/is-complex-typed-array-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex-typed-array-like

[@taktikorg/quos-adipisci/is-complex-typed-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex-typed-array

[@taktikorg/quos-adipisci/is-complex]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex

[@taktikorg/quos-adipisci/is-complex128]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex128

[@taktikorg/quos-adipisci/is-complex128array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex128array

[@taktikorg/quos-adipisci/is-complex64]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex64

[@taktikorg/quos-adipisci/is-complex64array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex64array

[@taktikorg/quos-adipisci/is-centrosymmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-centrosymmetric-matrix

[@taktikorg/quos-adipisci/is-complex128matrix-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex128matrix-like

[@taktikorg/quos-adipisci/is-complex128ndarray-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex128ndarray-like

[@taktikorg/quos-adipisci/is-complex128vector-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex128vector-like

[@taktikorg/quos-adipisci/is-complex64matrix-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex64matrix-like

[@taktikorg/quos-adipisci/is-complex64ndarray-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex64ndarray-like

[@taktikorg/quos-adipisci/is-complex64vector-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-complex64vector-like

[@taktikorg/quos-adipisci/is-float32matrix-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float32matrix-like

[@taktikorg/quos-adipisci/is-float32ndarray-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float32ndarray-like

[@taktikorg/quos-adipisci/is-float32vector-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float32vector-like

[@taktikorg/quos-adipisci/is-float64matrix-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float64matrix-like

[@taktikorg/quos-adipisci/is-float64ndarray-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float64ndarray-like

[@taktikorg/quos-adipisci/is-float64vector-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float64vector-like

[@taktikorg/quos-adipisci/is-matrix-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-matrix-like

[@taktikorg/quos-adipisci/is-ndarray-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-ndarray-like

[@taktikorg/quos-adipisci/is-nonsymmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonsymmetric-matrix

[@taktikorg/quos-adipisci/is-persymmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-persymmetric-matrix

[@taktikorg/quos-adipisci/is-skew-centrosymmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-skew-centrosymmetric-matrix

[@taktikorg/quos-adipisci/is-skew-persymmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-skew-persymmetric-matrix

[@taktikorg/quos-adipisci/is-skew-symmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-skew-symmetric-matrix

[@taktikorg/quos-adipisci/is-square-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-square-matrix

[@taktikorg/quos-adipisci/is-symmetric-matrix]: https://github.com/taktikorg/quos-adipisci/tree/main/is-symmetric-matrix

[@taktikorg/quos-adipisci/is-vector-like]: https://github.com/taktikorg/quos-adipisci/tree/main/is-vector-like

[@taktikorg/quos-adipisci/is-float32array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float32array

[@taktikorg/quos-adipisci/is-float64array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-float64array

[@taktikorg/quos-adipisci/is-int16array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-int16array

[@taktikorg/quos-adipisci/is-int32array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-int32array

[@taktikorg/quos-adipisci/is-int8array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-int8array

[@taktikorg/quos-adipisci/is-uint16array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uint16array

[@taktikorg/quos-adipisci/is-uint32array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uint32array

[@taktikorg/quos-adipisci/is-uint8array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uint8array

[@taktikorg/quos-adipisci/is-uint8clampedarray]: https://github.com/taktikorg/quos-adipisci/tree/main/is-uint8clampedarray

[@taktikorg/quos-adipisci/is-cube-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-cube-number

[@taktikorg/quos-adipisci/is-integer-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-integer-array

[@taktikorg/quos-adipisci/is-integer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-integer

[@taktikorg/quos-adipisci/is-negative-integer-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-negative-integer-array

[@taktikorg/quos-adipisci/is-negative-integer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-negative-integer

[@taktikorg/quos-adipisci/is-negative-number-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-negative-number-array

[@taktikorg/quos-adipisci/is-negative-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-negative-number

[@taktikorg/quos-adipisci/is-nonnegative-integer-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonnegative-integer-array

[@taktikorg/quos-adipisci/is-nonnegative-integer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonnegative-integer

[@taktikorg/quos-adipisci/is-nonnegative-number-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonnegative-number-array

[@taktikorg/quos-adipisci/is-nonnegative-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonnegative-number

[@taktikorg/quos-adipisci/is-nonpositive-integer-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonpositive-integer-array

[@taktikorg/quos-adipisci/is-nonpositive-integer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonpositive-integer

[@taktikorg/quos-adipisci/is-nonpositive-number-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonpositive-number-array

[@taktikorg/quos-adipisci/is-nonpositive-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nonpositive-number

[@taktikorg/quos-adipisci/is-positive-integer-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-positive-integer-array

[@taktikorg/quos-adipisci/is-positive-integer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-positive-integer

[@taktikorg/quos-adipisci/is-positive-number-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-positive-number-array

[@taktikorg/quos-adipisci/is-positive-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-positive-number

[@taktikorg/quos-adipisci/is-safe-integer-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-safe-integer-array

[@taktikorg/quos-adipisci/is-safe-integer]: https://github.com/taktikorg/quos-adipisci/tree/main/is-safe-integer

[@taktikorg/quos-adipisci/is-square-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-square-number

[@taktikorg/quos-adipisci/is-square-triangular-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-square-triangular-number

[@taktikorg/quos-adipisci/is-triangular-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-triangular-number

[@taktikorg/quos-adipisci/is-array-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-array-array

[@taktikorg/quos-adipisci/is-boolean-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-boolean-array

[@taktikorg/quos-adipisci/is-date-object-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-date-object-array

[@taktikorg/quos-adipisci/is-function-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-function-array

[@taktikorg/quos-adipisci/is-nan-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nan-array

[@taktikorg/quos-adipisci/is-null-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-null-array

[@taktikorg/quos-adipisci/is-number-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-number-array

[@taktikorg/quos-adipisci/is-object-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-object-array

[@taktikorg/quos-adipisci/is-string-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-string-array

[@taktikorg/quos-adipisci/is-symbol-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-symbol-array

[@taktikorg/quos-adipisci/is-array]: https://github.com/taktikorg/quos-adipisci/tree/main/is-array

[@taktikorg/quos-adipisci/is-boolean]: https://github.com/taktikorg/quos-adipisci/tree/main/is-boolean

[@taktikorg/quos-adipisci/is-date-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-date-object

[@taktikorg/quos-adipisci/is-function]: https://github.com/taktikorg/quos-adipisci/tree/main/is-function

[@taktikorg/quos-adipisci/is-nan]: https://github.com/taktikorg/quos-adipisci/tree/main/is-nan

[@taktikorg/quos-adipisci/is-null]: https://github.com/taktikorg/quos-adipisci/tree/main/is-null

[@taktikorg/quos-adipisci/is-number]: https://github.com/taktikorg/quos-adipisci/tree/main/is-number

[@taktikorg/quos-adipisci/is-object]: https://github.com/taktikorg/quos-adipisci/tree/main/is-object

[@taktikorg/quos-adipisci/is-regexp]: https://github.com/taktikorg/quos-adipisci/tree/main/is-regexp

[@taktikorg/quos-adipisci/is-string]: https://github.com/taktikorg/quos-adipisci/tree/main/is-string

[@taktikorg/quos-adipisci/is-symbol]: https://github.com/taktikorg/quos-adipisci/tree/main/is-symbol

[@taktikorg/quos-adipisci/is-undefined]: https://github.com/taktikorg/quos-adipisci/tree/main/is-undefined

<!-- </toc-links> -->

</section>

<!-- /.links -->
