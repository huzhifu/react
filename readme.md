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
<li>8.es6的展开运算符...
let a = {aa:'aa'}
let b = {bb:'bb'}
let c = {...a,...b}
console.log(c)
// {"aa":"aa","bb":"bb"}
</li>
<li>组件名字必须首字母为大写，不然不认；自定义样式的时候，css的蛇形命名属性（font-size）都必须写为驼峰命名属性（fontSize），否则也不认</li>
<li>JSX 的基本语法规则：遇到 HTML 标签（以 < 开头），就用 HTML 规则解析；遇到代码块（以 { 开头），就用 JavaScript 规则解析。</li>
<li>React 提供一个工具方法 React.Children 来处理 this.props.children 。我们可以用 React.Children.map 来遍历子节点，而不用担心 this.props.children 的数据类型是 undefined 还是 object</li>
<li>有时需要从组件获取真实 DOM 的节点，这时就要用到 ref 属性</li>
<li>父组件向子组件传值，props;子组件向父组件传值：1.先在父组件初始化state 2.定义处理state函数 3.通过属性（props）将该函数传给子组件4.在子组件中通过监听事件关联该函数（或者子组件的监听事件关联子组件的函数，子组件的函数再去关联该函数）</li>