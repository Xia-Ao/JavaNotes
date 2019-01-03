
### 变量表达式 ${...}
```html
<p>Today is: <span th:text="${today}">13 february 2011</span>.</p>
```

### 文字国际化表达式 #{...}
```html
<table>
 <th th:text="#{header.address.city}">...</th> 
 <th th:text="#{header.address.country}">...</th> 
</table>

```

### 选择表达式 *{...}

遍历book里面的title
```html
<div th:object="${book}"> 
    ... 
    <span th:text="*{title}">...</span> 
    ... 
</div>
```

### 链接表达式 @{..}
```html
    <a th:href="@{http://www.thymeleaf.org}">Thymeleaf</a>
```
链接既可以是绝对地址，也可以是相对地址

### 分段表达式 th:insert  th:replace
重用片段

### 比较和等价
`>, <, >=, <= (gt, lt, ge, le)`


### 设置属性值 th:attr



