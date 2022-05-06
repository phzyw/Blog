---
title: JavaScript笔记
date: 2022-05-06 10:08:07
tags:
  - JavaScript
categories:
  - 前端	
---



- 数组去重 

    ES6 方法  new Set()

    ```html
        <script>
            // 数组去重
            let arr = [1,3,3,6];
            let newArr = new Set(arr);
            console.log(newArr);//输出结果为 Set(3) {1,3,6}
            // 遍历去重后的数组
            newArr.forEach(element => {
                console.log(element);//输出结果为 1，3，6
            });
        </script>
    ```

    

- 数组合并

  合并 ：concat（）

  ```html
      <script>
          // 数组合并，利用array.concat(array1,array2...,arrayn)
          // array 代表合并在哪个数组里
          // array1,array2...,arrayn  指的是可以合并多个数组
          let arr = [1,3,3,6];
          let arr2 = [7,8,9];
          let arr3 = [7,8,9];
          let totalArr = arr.concat(arr2);
          let totalArr2 = arr.concat(arr2,arr3);
          console.log(totalArr);// 输出结果为 [1, 3, 3, 6, 7, 8, 9]
          console.log(totalArr2);// 输出结果为 [1, 3, 3, 6, 7, 8, 9, 7, 8, 9]
      </script>
  ```

  

- 数组排序

  sort() 方法。主要作用于对数组的元素进行排序。其中，sort()方法有一个可选参数。但是，此参数必须是函数。数组在调用sort()方法时，如果没有传参将按字母顺序（字符编码顺序）对数组中的元素进行排序，如果想按照其他标准进行排序，就需要进行传一个参数且为函数，该函数要比较两个值，并且会返回一个用于说明这两个值的相对顺序的数字。
  
  ```HTML
  <script>
          // 
          // 数组排序（升序、降序）
          // 利用 array.sort()
          let arr = [1,3,6,5,4,2,11];
          arr.sort(function (a,b) {
              // 升序
              return a - b; // 输出结果：[1, 2, 3, 4, 5, 6, 11]
              // 降序
              // return b - a;// 输出结果：[11, 6, 5, 4, 3, 2, 1]
          })
          console.log(arr);
          
  </script>
  ```
  
  

