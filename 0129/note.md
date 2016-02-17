第六章 列表应用样式与创建导航条

1.使用内边距和背景图为li元素添加列表小图标，这对图标的可控性更强。
2.创建导航条：

□一般规范

①无需多余无语义的div嵌套，直接上<ul><li></li><li></li></ul>

②li元素内的锚元素a直接设display为block方便设置样式。li的宽度通过a的padding控制，高度通过a的行高控制。

□可用滑动门技术创建标签页式导航

□纯css弹出菜单：利用:hover与定位，注意IE6、7中此法无效。
3.CSS图像映射

□原理同纯css弹出菜单。利用伪类:hover在锚元素a的属性，通过定位来实现映射。

 

第七章 对表单和数据表格应用样式
1.对数据表格应用样式：

1）summary和caption：应使用table中的summary属性对表格的内容进行描述，table标题使用caption元素。

2）thead、tbody和tfoot：thead（内部必须使用th而非td）和tfoot只能用一次，但可用多个tfoot对表格进行内容划分。

★IE6、IE7中不理解css的border-spacing属性，只能使用table元素的cellspacing属性控制单元格之间的距离。
2.关于表单:

1）用label元素与表单关联（两种方式）：

□隐式实现：把表单元素嵌套在label元素中：

<label>email<input name="email" type="text" /></label>

□显式方法：用label的for属性设置为相关联的表单元素的id名称：

<label for="email">email</label><input name="email" id="email" type="text" />

2）利用fieldset元素定义对相关信息块分组，使用legend元素对信息块进行描述。由于legend的表现在各浏览器下可控性都比较差，如果需要控制标题表现，建议使用h元素。

3）label元素对于表单的可访问性很重要，如果不希望页面出现label的文字可以负缩进隐藏，但在HTML代码中含label对可访问性很重要。

4）关于提交按钮：有三种设置提交按钮的方式——input元素type为submit和image时，使用button元素时。

□input的缺陷：无法只使用元素选择器选择。可以使用使用属性选择器选择，但IE6不支持，所以只能用ID或类选择器选择。

□button的问题：IE6（某种程度上还有IE7）处理提交的方式。其他浏览器提交value属性的内容，但是IE6、IE7提交元素本身的内容。

