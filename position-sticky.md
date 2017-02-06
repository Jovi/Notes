# position: sticky

这是一个新的 css3 属性，表现类似 position: relative 和 position: fixed 的合体：目标区域在页面中可见时，它的行为类似于 position: relative；否则像 position: fixed 一样跟随页面滚动。可以看到，sticky 的行为与用 JS 实现 Affix 的思路是一样的。
Chrome 23+ 和 Firefox 26+ 都支持这个属性，不过都需要手动开启：
- Chrome：进入 chrome://flags，启用「experimental Web Platform features（实验性网络平台功能）」；
- Firefox：进入 about:config，将「layout.css.sticky.enabled」选项值设置为 True；

它的使用方法很简单，像下面这样：
```CSS
.aside {
    position : sticky; 
    top : 0;
}
```
