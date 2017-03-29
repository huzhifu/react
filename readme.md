1.react 中用{}来包变量
2.react 中注释是不能放在最外面的标签的，可以放在嵌套标签中，如：
< div >
{/*这里需要红色*/}
< h1 style={myStyle} >{i>3?'true':'false'}< /h1 >
< /div >
3.JSX 允许在模板中插入数组，数组会自动展开所有成员,不需要遍历
4.JSX中不支持if else语句，可以用三元运算符代替
5.由于 JSX 就是 JavaScript，一些标识符像 class 和 for 不建议作为 XML 属性名。作为替代，React DOM 使用 className 和 htmlFor 来做对应的属性。