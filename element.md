# sass语法及element模拟要点：
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
15. ESLint + Airbnb config    =>   Lint on save  => jest  => 单独文件
16. 如果开始未选择sass，后面使用如下进行下载安装：
      cnpm install node-sass sass-loader --save-dev //如有报错可分开写
17. vue.config.js中设置路径  为常用路径设置别名方便使用
18. sass的遍历方法： 
      @for $i from 0 through 24 {
            .el-col-#{$i} {
                  width: $i / 24 * 100%;
            }
      }
19. 组件名称： export default中设置name属性，与porps、methods等并列，其值即为该组件的name值
20. 获取父组件name值： this.$parent.$options.name 
      gutter () {
            let parent = this.$parent;
            while(parent && parent.$options.name !== "ELRow") {
                  parent = parent.$parent;
            }
            return parent ? parent.gutter : 0;
      }
21. flex-shrink:0   flex布局中不会随着外部容器的大小而缩减
22. 字体设置光滑： -webkit-font-smoothing:antialiased; | -moz-osx-font-smoothing:grayscale;