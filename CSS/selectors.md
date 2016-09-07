## 层级

`X + Y`
相邻选择器，匹配在X后面的第一个Y。(只匹配一个元素)

`X > Y`
子选择器，只匹配X下的子元素Y。（与`X Y`的区别，`X Y`是子孙选择器，即无视层级）

`X ~ Y`
相邻选择器，与`X + Y`类似，不同的是`X ~ Y`匹配的是元素集合。(传递匹配，不止匹配一个元素)

---

## 伪类

`X:not(selector)`
否定伪类选择器。(排除X匹配项中的selector匹配项)

`X:first-line`

`X:first-letter`

---

## 属性

`X[attr*=""]`
模糊匹配。

`X[attr^=""]`
排除匹配。

`X[attr$="foo"]`
匹配以foo结尾的属性。（文件扩展名）

`X[foo~=""]`
a[data-info~="external"] {color: red;}
a[data-info~="image"] {border: 1px solid black;}
这也是非常少用的选择器，加上~号，有一种情况特别适用，比如有个data-filetype=”external image”属性，这时候需要分别针对external和image样式控制。
上述代码会匹配data-filetype=”external”、data-filetype=”image”、data-filetype=”external image”的a。
