## ts-sort-selection

sync + callback + Promise + Async/Await style selectionsort implementation in typescript

## Install

```js
npm install ts-sort-selection --save-dev
yarn add  ts-sort-selection -D
```


## commonjs use  [sync + callback + Promise + Async/Await]

```js

var selectionSort = require("ts-sort-selection").selectionSort;
selectionSort([3,4,57,2,100,27,343],function(data){
    console.log("selectionSort cb",data.join('-'))// output: 2-3-4-27-57-100-343
})


var selectionSortSync = require("ts-sort-selection").selectionSortSync;
console.log('selectionSortSync sync',selectionSortSync([3,4,57,2,100,27,343]))// output: [2,3, 4, 27, 57,100,343]



var selectionSortAsync = require("ts-sort-selection").selectionSortAsync;
selectionSortAsync([3,4,57,2,100,27,343]).then((res) => {
  console.log('selectionSortASync promise',res) // output: [2,3, 4, 27, 57,100,343]
}).catch((error) => {
  console.log('err',error)
})


var selectionSortAsyncW = require("ts-sort-selection").selectionSortAsync;
(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await selectionSortAsyncW(array4)
  console.log('selectionSortAsync await',les) // output: [2,3, 4, 27, 57,100,343]
})()



```

## es6 use  [sync + callback + Promise + Async Await]

```js 

import { selectionSort, selectionSortSync, selectionSortAsync } from 'ts-sort-selection'

selectionSort([3,4,57,2,100,27,343],function(data){
    console.log("selectionSort cb",data.join('-'))// output: 2-3-4-27-57-100-343
})

console.log('selectionSortSync sync',selectionSortSync([3,4,57,2,100,27,343]))

selectionSortAsync([3,4,57,2,100,27,343]).then((res) => {
  console.log('selectionSortASync promise',res) // output: [2,3, 4, 27, 57,100,343]
}).catch((error) => {
  console.log('err',error)
})

(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await selectionSortAsync(array4)
  console.log('selectionSortAsyncAwait await',les) // output: [2,3, 4, 27, 57,100,343]
})()


```


## umd web browser use  [sync + callback + Promise + Async Await]

```js

<script src="https://unpkg.com/ts-sort-radix@1.0.1/umd/index.js"></script>

tsSortSelection.selectionSort([3,4,57,2,100,27,343],function(data){
    console.log("selectionSort cb",data.join('-'))// output: 2-3-4-27-57-100-343
})

console.log('selectionSortSync sync',tsSortSelection.selectionSortSync([3,4,57,2,100,27,343]))

tsSortSelection.selectionSortAsync([3,4,57,2,100,27,343]).then((res) => {
  console.log('selectionSortASync promise',res) // output: [2,3, 4, 27, 57,100,343]
}).catch((error) => {
  console.log('err',error)
})

(async function () {
  var array4 = [3,4,57,2,100,27,343]
  var les = await tsSortSelection.selectionSortAsync(array4)
  console.log('selectionSortAsyncAwait await',les) // output: [2,3, 4, 27, 57,100,343]
})()

```



## API
### selectionSortSync: (arr: number[]) => any;
### selectionSort: (arr: number[], callback: (data: number) => void) => any;
### selectionSortAsync: (arr: number[]) => any;

- arr - The array to sort in place
- callback - function to get sort array result 