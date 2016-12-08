```js
function getCursortPosition (ctrl) {
    //获取光标位置函数
    var CaretPos = 0;    
    if (document.selection) {
        // IE Support
        ctrl.focus ();
        var Sel = document.selection.createRange ();
        Sel.moveStart ('character', -ctrl.value.length);
        CaretPos = Sel.text.length;
    } else if (ctrl.selectionStart || ctrl.selectionStart == '0') {
        // Firefox support
        CaretPos = ctrl.selectionStart;
    }
    return (CaretPos);
}
```

---

```js
function setCaretPosition(ctrl, pos){
    //设置光标位置函数
    if(ctrl.setSelectionRange) {
        ctrl.focus();
        ctrl.setSelectionRange(pos,pos);
    } else if (ctrl.createTextRange) {
        var range = ctrl.createTextRange();
        range.collapse(true);
        range.moveEnd('character', pos);
        range.moveStart('character', pos);
        range.select();
    }
}
```
