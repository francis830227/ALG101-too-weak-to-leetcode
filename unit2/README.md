# Unit2：寫程式之前，先學會「看程式」

「看程式碼」指的不是掃過去而已  
而是你在看的時候，就會知道程式碼是怎麼執行的了  
所以這一個單元要讓大家知道程式碼執行流程

## Unit2.1：你其實看不懂程式碼

給兩個範例（虛擬碼）：

1. 陣列總和
2. 找最大值

練習一行一行跑

##  Unit2.2：人體編譯器

給真的程式碼，範例同上


## Unit2.3：Debug 神器：Debugger

chrome devtool debugger 的使用，範例同上


## Unit2.4：Log 雖可恥但有用

傳授 log 大法，log 加好加滿就對了

## Unit2.5：實戰練習：找次大值

直接提供答案，手動模擬電腦執行

## Unit2.6：實戰練習：字串轉大寫

直接提供答案，手動模擬電腦執行

## Unit2.7：實戰練習：刪除特定字元

直接提供答案，手動模擬電腦執行

## Unit2.8：Project2 介紹

人體編譯器

出三個作業，給程式碼讓他們一行行寫下執行流程，記得附上參考解答

作業題目：

### 1. 找次小值

給一個陣列，裡面全都包含了數字（整數），請輸出陣列中的次小值  
範例輸入：[1, 2, 3]  
範例輸出：2

``` js
let arr = [10, 8, 6]
let min = Infinity
let min2 = Infinity
for(let i=0; i<arr.length; i++) {
  if (arr[i] < min) {
    min2 = min
    min = arr[i]
  } else if (arr[i] < min2) {
    min2 = arr[i]
  }
}
console.log(min, min2)
```

## 2. 大小寫互換

給一個字串，請把字串裡的大小寫互換  
範例輸入：hELLo   
範例輸出：HellO

```js
let str = "hELLo"
let ans = ''
for(let i=0; i<str.length; i++) {
  let code = str.charCodeAt(i)
  if (code >= 97 && code <= 122) {
    ans += String.fromCharCode(code - 32)
  } else if (code >= 65 && code <= 90) {
    ans += String.fromCharCode(code + 32)
  } else {
    ans += str[i]
  }
}
console.log(ans)
```

## 3. 印出因數

給一個正整數，請輸出他的所有因數  
範例輸入：15  
範例輸出：

```
1
3
5
15
```

```js
let num = 30
for(let i=1; i<=num; i++) {
  if (num % i === 0) {
    console.log(i)
  }
}
```
