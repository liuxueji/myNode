思路：需要通过正则匹配空格，如何替换成 '' 空字符

实现：

- 去除所有空格：`str.replace(/\s/g,'') `

  > 正则中 \s 表示空格， \S 表示非空格
  >
  > /  /g ，表示正则匹配全局
  >
  > 利用字符串方法 replace进行替换

- 去除两边空格：`str.trim()` 

  > 正则不会写。。。