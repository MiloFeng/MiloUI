[TOC]

# 目前总结的是工作中最常涉及到的底层样式

- normalize
    - reset样式。[原作者](https://github.com/necolas/normalize.css)
    - 修改地方
        - html 增加作者公司常用字体,添加 -webkit-font-smoothing: antialiased;
        - 移除<hgroup>
        - img默认垂直居中 vertical-align: middle;
        - 将header,footer,main,aside等元素设置为块属性
        - 所有元素都设置box-sizing:border-box
- base
    - center: 水平居中
    - hide: 隐藏元素(display:none)
    - hidden：隐藏元素(visibility:hidden)
    - fl: 左浮动
    - fr：有浮动
    - text-left:文字左对齐
    - text-right:文字右对齐
    - text-center：文字居中对齐
    
    ```html
    <div class="center">
      <div class="fl"><p class="text-right">这里的文字右对齐</p></div>
      <div class="fr"><p class="text-left">这里的文字左对齐</p></div>
      <p class="hidden">这里的文字不显示，但是起到占位作用</p>
      <p class="hide">这里的文字不显示并且不占位</p>
    </div>
    ```
    
- box-sizing
    
    ```scss
        @include box-sizing();
     ```

- clearfix
    ```scss
        @include clearfix();
     ```
    
- keyframe

    ```scss
    @include keyframes(animate1) {
      from {
        
      }
      to {
    
      }
    }
  
    .object {
      @include animation('animate1' 1s infinite 1s);
    }
    ```
    
- text-ellipsis
   ```scss
       @include text-ellipsis();
    ```
    
    
- px2rem 计算移动端字体，将px转换成rem

- responsive 移动端适配，如果不做移动端，_func中可以不引用px2rem和resonsive两个文件