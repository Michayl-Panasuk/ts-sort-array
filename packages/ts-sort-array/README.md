## ts-sort-utils

sync + callback + Promise + Async/Await style sort array utils  implementation in typescript

- bubbleSort,
- bubbleSortSync,
- bubbleSortAsync,
- bucketSort,
- bucketSortSync,
- bucketSortAsync,
- countingSort,
- countingSortSync,
- countingSortAsync,
- heapSort,
- heapSortSync,
- heapSortAsync,
- insertionSort,
- insertionSortSync,
- insertionSortAsync,
- mergeSort,
- mergeSortSync,
- mergeSortAsync,
- quickSort,
- quickSortSync,
- quickSortAsync,
- radixSort,
- radixSortSync,
- radixSortAsync,
- selectionSort,
- selectionSortSync,
- selectionSortAsync,
- shellSort,
- shellSortSync,
- shellSortAsync

## Install

```js
npm install ts-sort-utils --save-dev
yarn add  ts-sort-utils -D
```



### Usages Api for  cjs

```js
    require("ts-sort-utils").bubbleSort,
    require("ts-sort-utils").bubbleSortSync,
    require("ts-sort-utils").bubbleSortAsync,
    require("ts-sort-utils").bucketSort,
    require("ts-sort-utils").bucketSortSync,
    require("ts-sort-utils").bucketSortAsync,
    require("ts-sort-utils").countingSort,
    require("ts-sort-utils").countingSortSync,
    require("ts-sort-utils").countingSortAsync,
    require("ts-sort-utils").heapSort,
    require("ts-sort-utils").heapSortSync,
    require("ts-sort-utils").heapSortAsync,
    require("ts-sort-utils").insertionSort,
    require("ts-sort-utils").insertionSortSync,
    require("ts-sort-utils").insertionSortAsync,
    require("ts-sort-utils").mergeSort,
    require("ts-sort-utils").mergeSortSync,
    require("ts-sort-utils").mergeSortAsync,
    require("ts-sort-utils").quickSort,
    require("ts-sort-utils").quickSortSync,
    require("ts-sort-utils").quickSortAsync,
    require("ts-sort-utils").radixSort,
    require("ts-sort-utils").radixSortSync,
    require("ts-sort-utils").radixSortAsync,
    require("ts-sort-utils").selectionSort,
    require("ts-sort-utils").selectionSortSync,
    require("ts-sort-utils").selectionSortAsync,
    require("ts-sort-utils").shellSort,
    require("ts-sort-utils").shellSortSync,
    require("ts-sort-utils").shellSortAsync

```

### Usages Api for es6

```js
import {
    bubbleSort,
    bubbleSortSync,
    bubbleSortAsync,
    bucketSort,
    bucketSortSync,
    bucketSortAsync,
    countingSort,
    countingSortSync,
    countingSortAsync,
    heapSort,
    heapSortSync,
    heapSortAsync,
    insertionSort,
    insertionSortSync,
    insertionSortAsync,
    mergeSort,
    mergeSortSync,
    mergeSortAsync,
    quickSort,
    quickSortSync,
    quickSortAsync,
    radixSort,
    radixSortSync,
    radixSortAsync,
    selectionSort,
    selectionSortSync,
    selectionSortAsync,
    shellSort,
    shellSortSync,
    shellSortAsync
}
from 'ts-sort-utils' 
```


## commonjs use  [sync + callback + Promise + Async/Await]

```js

var quickSort = require("ts-sort-utils").quickSort;
quickSort([3,4,57,2,100,27,343],function(data){
    console.log("quickSort cb",data.join('-'))// output: 2-3-4-27-57-100-343
})


var quickSortSync = require("ts-sort-utils").quickSortSync;
console.log('quickSortSync sync',quickSortSync([3,4,57,2,100,27,343]))// output: [2,3, 4, 27, 57,100,343]



var quickSortAsync = require("ts-sort-utils").quickSortAsync;
quickSortAsync([3,4,57,2,100,27,343]).then((res) => {
  console.log('quickSortASync promise',res) // output: [2,3, 4, 27, 57,100,343]
}).catch((error) => {
  console.log('err',error)
})


var quickSortAsyncW = require("ts-sort-utils").quickSortAsync;
(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await quickSortAsyncW(array4)
  console.log('quickSortAsync await',les) // output: [2,3, 4, 27, 57,100,343]
})()


var quickSortAsyncAwait = require("ts-sort-utils").quickSortAsyncAwait;
(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await quickSortAsyncAwait(array4)
  console.log('quickSortAsyncAwait await',les) // output: [2,3, 4, 27, 57,100,343]
})()

```

## es6 use  [sync + callback + Promise + Async Await]

```js 

import { quickSort, quickSortSync, quickSortAsync, quickSortAsyncAwait} from 'ts-sort-utils'

quickSort([3,4,57,2,100,27,343],function(data){
    console.log("quickSort cb",data.join('-'))// output: 2-3-4-27-57-100-343
})

console.log('quickSortSync sync',quickSortSync([3,4,57,2,100,27,343]))

quickSortAsync([3,4,57,2,100,27,343]).then((res) => {
  console.log('quickSortASync promise',res) // output: [2,3, 4, 27, 57,100,343]
}).catch((error) => {
  console.log('err',error)
})

(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await quickSortAsync(array4)
  console.log('quickSortAsyncAwait await',les) // output: [2,3, 4, 27, 57,100,343]
})()


```



## umd web browser use  [sync + callback + Promise + Async Await]

```js

<script src="https://unpkg.com/ts-sort-utils@1.0.1/umd/index.js"></script>

tsSortUtils.bucketSort([3,4,57,2,100,27,343],function(data){
    console.log("bucketSort cb",data.join('-'))// output: 2-3-4-27-57-100-343
})

console.log('bucketSortSync sync',tsSortUtils.bucketSortSync([3,4,57,2,100,27,343]))

tsSortUtils.bucketSortAsync([3,4,57,2,100,27,343]).then((res) => {
  console.log('bucketSortASync promise',res) // output: [2,3, 4, 27, 57,100,343]
}).catch((error) => {
  console.log('err',error)
})

(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await tsSortUtils.bucketSortAsync(array4)
  console.log('bucketSortAsyncAwait await',les) // output: [2,3, 4, 27, 57,100,343]
})()
.....

```



## Dependencies Packages

- `ts-sort-bubble` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/bubbleSort/README.md), [NPM](https://www.npmjs.com/ts-sort-bubble)
- `ts-sort-bucket` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/bucketSort/README.md), [NPM](https://www.npmjs.com/ts-sort-bucket)

- `ts-sort-counting` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/countingSort/README.md), [NPM](https://www.npmjs.com/ts-sort-counting)

- `ts-sort-heap` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/heapSort/README.md), [NPM](https://www.npmjs.com/ts-sort-heap)

- `ts-sort-insertion` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/insertionSort/README.md), [NPM](https://www.npmjs.com/ts-sort-insertion)

- `ts-sort-merge` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/mergeSort/README.md), [NPM](https://www.npmjs.com/ts-sort-merge)

- `ts-sort-quick` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/quickSort/README.md), [NPM](https://www.npmjs.com/ts-sort-quick)

- `ts-sort-radix` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/radixSort/README.md), [NPM](https://www.npmjs.com/ts-sort-radix)

- `ts-sort-selection` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/selectionSort/README.md), [NPM](https://www.npmjs.com/ts-sort-selection)

- `ts-sort-shell` [GitHub repo](https://github.com/jackieli123723/ts-sort-array/blob/master/packages/shellSort/README.md), [NPM](https://www.npmjs.com/ts-sort-shell)






## API 

- arr - The array to sort in place
- callback - function to get sort array result 