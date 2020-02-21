sass语法：
1.  样式值（颜色、尺寸、padding等）提取到一个专门文件中
2. @include
3. @include when(class)   约等于&.class?
4. mix   混合颜色  color: mix{$color1, $color2}
5. &.class   &:hover   &:active
6. @include m(参数) {}
7. @include button-variant(...参数)
8. @mixin button-plain (参数) {}  设置一个混合宏
9. line-height:1  基准线
10. #{变量|值px - 1}；
11. rgba(普通color， 透明度|.5)
12. autofocus   button按钮focus状态
13. @each $type,$color in $typeMap {
           @include m($type){
      	color: @color
            }
      }
14.  []class *= "el-icon-"] {
           $ + span {	//作用到该元素紧挨着的span元素身上
               margin-left: 5px
           }
      }