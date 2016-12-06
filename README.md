# phone-number-encodes-
判断用户名是否为手机号码，是就加密


```html
<!DOCTYPE html>
<html>
<head>
    <title></title>
</head>
<body>
<p id="number">13202629601</p>
<p id="text">1q大</p>
<script type="text/javascript" src="jquery.min.js"></script>
<script type="text/javascript">
    var num=$("#number");
    var text=$("#text")
    secret(num)
    secret(text)
    function secret(str){
    	var reg=new RegExp("[0-9]+");
        var strArr=str.text().split("");
        var flag=true;
        for(var i=0;i<strArr.length;i++){
        	if(!reg.test(strArr[i])){
        		flag=false;
        		return
        	}
        }
        if(true){
        	if(!strArr.length==11){
        		return
        	}
        	else{
        		strArr[3]="*";
        		strArr[4]="*";
        		strArr[5]="*";
        		strArr[6]="*";       		
        		var secretPhone="";
        		for(var j=0;j<strArr.length;j++){
        			secretPhone+=strArr[j]
        		}
        		str.text(secretPhone);
         	}

        }
    }
</script>
</body>
</html>
```
