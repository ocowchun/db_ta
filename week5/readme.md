
* install Ruby!!!
* basic Ruby
* 網站開發框架(Web framework)
* 基本的CRUD
* MVC,RESTful

##優秀作業

#### http://102306071.github.io/calculator/
[repo](https://github.com/102306071/calculator)
功能實作完全,重複的程式碼過多

####http://lindacwl.github.io/calculator/ 
[repo](https://github.com/lindacwl/calculator)
功能實作完全,使用eval

####https://github.com/Michelle12369/calculator
[repo](http://michelle12369.github.io/calculator/)
功能實作完全

####http://aleoliu566.github.io/calculator/calculator
[repo](https://github.com/aleoliu566/calculator)

####http://wxc900211.github.io/calculator.html
[repo](https://github.com/wxc900211/wxc900211.github.io)
畫面很棒


##bad case
### avoid use `eval`
weicheng103
```
$('#btn_equal').on('click',function(){
		if(operation == 1) { currentText = eval(memory) + eval(currentText);};//+
		if(operation == 2) { currentText = eval(memory) - eval(currentText);};//-
		if(operation == 3) { currentText = eval(memory) * eval(currentText);};//*
		if(operation == 4) { currentText = eval(memory) / eval(currentText);};///
		$('#message').text(currentText);


	});					
```

###avoid use switch
[https://github.com/andywu42000/Calculator](https://github.com/andywu42000/Calculator)

###不要宣告沒用到的變數
[https://github.com/aleoliu566/calculator/blob/master/app.js]


###use css instead of style
[https://github.com/lovejess520/lovejess520.github.io/blob/master/index.html](https://github.com/lovejess520/lovejess520.github.io/blob/master/index.html)
