# flexbox布局相关CSS属性

## 定义在flex容器上的CSS属性

* display: 将display设置flex或者inline-flex后, 该元素将使用flexbox来布局它的直接子元素
* flex-direction: 设置flexbox布局的主轴, 主轴决定了flexbox容器如何去排列flex元素. 具体从容器的那个位置开始排列还要看不同地区的文字的显示(有的地方从左往右, 有的地方从右往左).
  * row: 水平排列flex项, 默认值. 在文字排列从左往右的地区, flex项从容器的左侧开始排列; 在文字排列从右往左的地区, flex项从容器的右侧开始排列
  * row-reverse: 反方向水平排列flex项. 排列方向与row相反. 即在文字排列从左往右的地区, flex项从容器的右侧开始排列; 在文字排列从右往左的地区, flex项从容器的左侧开始排列.
  * column: 垂直排列flex项. 从容器的顶部依次排列flex项
  * column-reverse: 反方向垂直排列flex项. 排列方向与column相反
* jusitify-content: 如何在主轴上排列flex项及分配其周围的空间. 
  * start: 从主轴行首开始排列. 每行第一个元素与行首对齐, 同时所有后续的元素的开始与前一个元素的尾部对齐.
  * center: 每一行所有flex项所组成的块, 在flex容器中居中展示
  * flex-start: 与start相同, 推荐使用该值
  * flex-end: 从主轴行尾开始排列. 每行最后一个弹性元素与行尾对齐, 其他元素将与后一个对齐.
  * left: 从主轴的左边缘开始排列元素. 在大部分地区与flex-start作用相同
  * right: 从主轴的右边缘开始排列元素. 在大部分地区月flex-end作用相同
  * space-between: 在每行上均匀排列元素. 相邻元素之间的间距相同. 每行第一个元素与行首对齐, 每行最后一个元素与行尾对齐. 
  * space-around: 在每行上均匀分配弹性元素. 相邻元素之间的间距相同. 每行第一个元素到行首的距离和每行最后一个元素到行尾的距离将会是相邻元素之间距离的一半.
  * space-evenly: flex项都沿着主轴均匀分布在指定的对齐容器中. 相邻flex项之间的间距, 主轴起始位置到第一个flex项的间距, 主轴结束位置到最后一个flex项的间距都相等. 
  * baseline: 基线对齐
  * first baseline: 第一基线对齐
  * last baseline: 最后基线对齐
* align-items: 将所有直接子节点上的align-self值设置为一个组. 设置该组在交叉轴上的对齐方式, align-items的取值如下:
  * flex-start: flex项对齐交叉轴的开始位置
  * flex-end: flex项对齐交叉轴的结束位置
  * center: 在交叉轴上居中对齐
  * stretch: 弹性元素被在交叉轴方向被拉伸到与容器相同的高度或宽度. 
  * baseline: 向基线对齐
  * first baseline: 向第一基线对齐
  * last baseline: 向最后基线对齐