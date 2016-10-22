## Usage
remove margin effection of children nodes


## HTML
```html
<div class="wrapper">
  <div class="container">
    <div class="item"></div>
    <!-- more .item -->
  </div>
</div>
```

## CSS
```css
.wrapper{
  width:100px;
  height:100px;
}
.container{
  margin-top:-20px;
  width:calc(100% + 20px);
  height:100%;
}
.item{
  margin:20px 20px 0 0;
  width:30px;
  height:30px;
}
```
