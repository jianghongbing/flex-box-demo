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
* flex-wrap: 当所有flex元素在主轴方向的长度之和大于容器时, 是否换行(或者换列)展示. 
  * nowarp: 不换行展示, 默认值
  * wrap: 换行展示, flex项会沿着交叉轴的地方开始排列
  * wrap-reverse: 换行展示, flex项会交叉轴结束地方开始排列
* flex-flow: flex-direction 和 flex-wrap的简写
* align-content: 同align-items功能类似, 不过align-content是以行作为维度来设置在交叉轴上的对齐方式. align-content只对多行flex容器模型有效. 该属性的取值如下: 
  * flex-start: 所有行从交叉轴起点开始填充. 第一行的交叉轴起点边和容器的交叉轴起点边对齐. 接下来的每一行紧跟前一行.
  * flex-end: 所有行从交叉轴末尾开始填充. 最后一行的交叉轴终点和容器的交叉轴终点对齐. 同时所有后续行与前一个对齐.
  * center: 所有行朝向容器的中心填充. 每行互相紧挨, 相对于容器居中对齐. 容器的交叉轴起点边和第一行的距离相等于容器的交叉轴终点边和最后一行的距离.
  * space-between: 所有行在容器中平均分布. 相邻两行间距相等. 容器的交叉轴起点边和终点边分别与第一行和最后一行的边对齐.
  * space-around: 所有行在容器中平均分布, 相邻两行间距相等. 容器的交叉轴起点边和终点边分别与第一行和最后一行的距离是相邻两行间距的一半.
  * space-evenly: 每一行与交叉轴的边缘以及每行之间的间距都相等
  * stretch: 拉伸所有行来填满剩余空间. 剩余空间平均地分配给每一行. 该是也是多行flex容器中的默认值
  * baseline: 行使用基线对齐
  * first baseline: 第一基线对齐
  * last baseline: 最后一条基线对齐
* place-content: align-content和jusitify-content的简写
* column-gap: 设置列间距
* row-gap: 设置行间距
* gap: column-gap和row-gap的简写

## 定义在flex项中的CSS属性

* flex-grow: 在主轴方向上, flex容器剩余空间(flex容器在主轴上的大小减去所有flex项的大小加起来的大小)分配比例. 它指定了flex容器中剩余空间的多少应该分配给项目. 该属性的值需要大于等于0, 默认为0.
* flex-shrink: 指定flex项的收缩系数. flex项仅在默认宽度之和大于容器的时候才会发生收缩, 其收缩的大小是依据flex-shrink的值和所有flex项在主轴方向上超过flex容器的长度. 该值为一个非负数, 初始值是1. 
* flex-basis: 指定flex项在主轴方向上的初始大小. 当设置flex-grow和flex-shrink的值都为0时, 将使用该值来作为flex项的大小并进行布局. flex-basis的取值可以如下
  * 一个长度值
  * content: 基于flex项的内容自动调整大小. 
* flex: flex-grow, flex-shrink和flex-basis的简写. 一般通过该属性来设置里面包含的属性的值. flex的取值可以如下:
  * initial: flex项会根据自身宽高设置尺寸. 当所有flex项的长度大于flex容器在主轴上的长度时, 它会缩短自身以适应flex容器, 当小于时, 不会伸长并吸收flex容器中的额外自由空间来适应flex容器. 相当于将属性设置为"flex: 0 1 auto", 该值也是flex的默认值.
  * auto: 元素会根据自身的宽度与高度来确定尺寸, 但是会伸长并吸收flex容器中额外的自由空间, 也会缩短自身来适应flex容器. 这相当于将属性设置为 "flex: 1 1 auto".
  * none: 元素会根据自身宽高来设置尺寸. 元素不会缩短, 也不会伸长来适应flex容器. 相当于将属性设置为"flex: 0 0 auto"。
  * 有一个值的时候会有情况: 
    * 一个无单位数: 相当于 flex: number, 1, 0. 将该值赋值给flex-grow, flex-shrink默认为1, flex-basis默认为0.
    * 一个带有长度单位的值: 该值会被作为flex-basis的值
  * 有2个值时, 第一个值为flex-grow的值, 后面一个值有下面的情况
    * 如果是一个无单位数, 该值会被赋值给flex-shrink
    * 如果是一个带有带有单位的数, 该值赋值给flex-basis
  * 有3个值, 分别赋值给flex-grow, flex-shrink和flex-basis
* order: flex项在布局时的顺序, 默认值为0. 值越小越先布局. 值相同则按照元素出现的顺序先后布局. 
