# flexbox布局相关CSS属性

* display: 将display设置flex或者inline-flex后, 该元素将使用flexbox来布局它的直接子元素
* flex-direction: 设置flexbox布局的主轴, 主轴决定了flexbox容器如何去排列flex元素. 具体从容器的那个位置开始排列还要看不同地区的文字的显示(有的地方从左往右, 有的地方从右往左).
  * row: 水平排列flex项, 默认值. 在文字排列从左往右的地区, flex项从容器的左侧开始排列; 在文字排列从右往左的地区, flex项从容器的右侧开始排列
  * row-reverse: 反方向水平排列flex项. 排列方向与row相反. 即在文字排列从左往右的地区, flex项从容器的右侧开始排列; 在文字排列从右往左的地区, flex项从容器的左侧开始排列.
  * column: 垂直排列flex项. 从容器的顶部依次排列flex项
  * column-reverse: 反方向垂直排列flex项. 排列方向与column相反
* 