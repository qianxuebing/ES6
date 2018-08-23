# ES6
ESMAScript6 入门

ES6又称`ES2015`

#### 内容简介

* 变量
	* var ----- 重复声明  		 函数级		
	* let ----- 不能重复声明  块级    变量		
	* cosnt --- 不能重复声明  块级    常量
		
* 解构赋值
	* 左右解构相同		
	* 右边是合法的东西		
	* 声明和赋值一次完成
		
	```
	let [a,b,c]=[1,2,3]		
	```
		
* 函数
	* 箭头函数
		* 如果只有一个参数，()可以省略
		* 乳沟只有一个return， {}可以省略

* 数组
	* 参数扩展：...args
	* 默认参数
		
	```
	function show(a,b=2){
		alert(a,b);
	}
				
	show(5); // 5  2				
	```
	* 数组方法：
		* map ------- 映射，一个对一个
		* reduce ---- 汇总，一堆 --> 一个
		* filter ---- 过滤，一堆 --> 剩下的
		* forEach --- 循环 
		
* 字符串
	* startsWith,endsWith
	* 字符串模板
		
	```
	${a}xxx${b}		
	```

* 面向对象

```
	class Text{
		constructor(name,age){
			this.name=name;
			this.age=age;
		},
		showName(){
			alert(this.name);
		},
		showAge(){
			alert(this.age);
		}			
	}
		
	class Test2 extends Text{
		constructor(name,age,sex){
			super(name,age);
			this.sex=sex;
		},
		showSex(){
			alert(this.sex);
		}
	}
		
	let u1 = new Test2("xiaoming","12","boy");
	u1.showName();	// xiaoming	
	u1.showAge();		// 12
	u1.showSex();		// boy		
```

* Promise
	* 封装异步操作
	
	```
	Promise.all([
		let one=$.ajax({url:"data/arr.txt",dataType:"json"});
		let one=$.ajax({url:"data/json.txt",dataType:"json"});
		let one=$.ajax({url:"data/num.txt",dataType:"json"});
	]).then(result=>{
		let [arr,json,num]=result;
		alert("成功");
		console.log(arr,json,num);
	},err=>{
		alert("失败");
	})		
	```

* generator
	* generator函数----中间能停(常用于解决异步操作)
		
	```
	function *show(){
		alert("a");
		yield;
		alert("b");
	}
	let demo=show();
	demo.next(); // a
	demo.next(); // a b		
	```

* 模块化

#### 编译，转换

* 在线转换

* 提前编译(babel[推荐])

