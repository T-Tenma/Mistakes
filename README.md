# Mistakes
这是当编程中的一些错误集锦


1、依据:html中，当元素为undefined的时，if判断为false。
   需求:当data中没有值时，不显示任何东西。
   代码:
	<pre><code>
		if(data){
			$("td").html(data);
		}
	</code></pre>
   问题:当data为0的情况，判断也不会进入……(这个问题找了很久，主要是一开始怀疑是后台数据问题)。
   解决方案:
   <pre><code>
		if(data != undefined){
			$("td").html(data);
		}
	</code></pre>