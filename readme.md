<li>1.react 中用{}来包变量</li>
<li>2.react 中注释是不能放在最外面的标签的，可以放在嵌套标签中，如：
< div >
{/*这里需要红色*/}
< h1 style={myStyle} >{i>3?'true':'false'}< /h1 >
< /div ></li>
<li>3.JSX 允许在模板中插入数组，数组会自动展开所有成员,不需要遍历</li>
<li>4.JSX中不支持if else语句，可以用三元运算符代替</li>
<li>5.由于 JSX 就是 JavaScript，一些标识符像 class 和 for 不建议作为 XML 属性名。作为替代，React DOM 使用 className 和 htmlFor 来做对应的属性。</li>
<li>6.实例中 name 属性通过 this.props.name 来获取。
<pre><code>
      var HelloMessage = React.createClass({
        render: function() {
          return < h1 >Hello {this.props.name}< /h1 >;
        }
      });

      ReactDOM.render(
        <HelloMessage name="Runoob" />,
        document.getElementById('example')
      );
</code></pre>
</li>
<li>7.import与export是模块开发的主要方法，
其中export default只能有一个，export可以有多个；
import 可以{，，，} 也可以import aaa(相当于import {default as aaa})；
from 一般是一个js路径，如果是一个文件夹，那么这个文件夹下一定有一个index.js,index.js中会有一系列的import...  最后是export {,,,}
</li>