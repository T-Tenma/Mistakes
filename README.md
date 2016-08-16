# Mistakes


1、依据: html中，当元素为undefined的时，if判断为false。
   需求:当data中没有值时，不显示任何东西。
>代码:
   
    if(data){
		$("td").html(data);
	}
   问题: 当data为0的情况，判断也不会进入……(这个问题找了很久，主要是一开始怀疑是后台数据问题)。
>解决方案:

	if(data != undefined){
		$("td").html(data);
	}