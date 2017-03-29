1.react 中用{}来包变量
2.react 中注释是不能放在最外面的标签的，可以放在嵌套标签中，如：
<div>
{/*这里需要红色*/}
<h1 style={myStyle}>{i>3?'true':'false'}</h1>
</div>