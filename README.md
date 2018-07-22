###wepy弹框插件
--------
####安装方法
	npm install wepy-dialog --save
	
1.需要配置pug模板引擎
	
	cnpm install wepy-compiler-pug --save
	
	//wepy.config.js
	compiler: {
		pug: {
	      data: {
	        CONTENT_PATH: '/'
      }
    },
	}
####使用方法
import Dialog from "wepy-dialog";

+	调用showModal方法

	```
	this.$invoke("Dialog", "showModal", {
		 title: "这是一个modal",//可自定义,必须
	    content: "这里是modal的主体内容",//可自定义
	    cancel: function() {...}
	    confirm: function() {...}
	    cancelText: "取消",//可自定义
	    confirmText: "确认",//可自定义
	    tip: "这里是tip提示内容",//可自定义
	    type: null,//确定按钮的类型(open-type)//可自定义
	})



