##### 1.将主题还原成精简的模式
##### 2.使用hexo插件绘制时序图/流程图本地一直有问题，所以引入了
- jquery-2.1.4.min.js 
- raphael-min.js 
- underscore-min.js 
- sequence-diagram-min.js 
- flowchart-latest.js

直接在post里使用:
- 时序图
```
{% raw %}
<div class="diagram_sequence">
Client->Service:bindService
Service-->Client:返回一个messenger对象
Client->Service:通过messenger发送消息
Service-->Handler:分发消息
</div>
{% endraw %}
```


- 流程图
```
{% raw %}
<div class="diagram_flow">
st=>start: Start:>http://www.google.com[blank]
e=>end:>http://www.google.com
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes
or No?:>http://www.google.com
io=>inputoutput: catch something...
st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1
</div>
{% endraw %}
```


