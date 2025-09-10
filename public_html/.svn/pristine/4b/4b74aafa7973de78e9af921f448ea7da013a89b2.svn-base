$(function() {
    $(".numericOnly").bind('keypress',function(e){
    	if(e.keyCode == '9' || e.keyCode == '16'){  
    		return;  
    	}  
    	var code;  
    	if (e.keyCode) code = e.keyCode;  
    	else if (e.which) code = e.which; 		
    	if(e.which == 46)  
    		return false;  
    	if (code == 8 || code == 46 || code == 118)  
    		return true;  
    	if (code < 48 || code > 57)  
    		return false;  
    });
    /*$(".numericOnly").bind("paste",function(e) {  
    	e.preventDefault();  
    });*/
    $(".numericOnly").bind('mouseenter',function(e){  
      var val = $(this).val();  
      if (val!='0'){  
    	   val=val.replace(/[^0-9]+/g, "")  
    	   $(this).val(val);  
      }  
    });
    
    $(".decimalnumericOnly").bind('keypress',function(e){
    	if(e.keyCode == '9' || e.keyCode == '16'){  
    		return;  
    	}
        var insrtval=this.value;
        var REgXp = new RegExp(/^\d*\.\d\d$/);
        if (REgXp.test(insrtval))
        {
            return false;
        }
    	var code;  
    	if (e.keyCode) code = e.keyCode;  
    	else if (e.which) code = e.which;
    	if (code == 8)  
    		return true; 
        if (code == 46)
            return true; 
    	if (code < 48 || code > 57)  
    		return false;
        
    });
    $(".decimalnumericOnly").bind("paste",function(e) {  
    	e.preventDefault();  
    });
    

    $("#search").on("keyup",function(){
        gridloader(1);
    });
	$(".codedecimalnumeric2").bind('keypress',function(e){
    	if(e.keyCode == '9' || e.keyCode == '16'){  
    		return;  
    	}
        var insrtval=this.value;
        var REgXp = new RegExp(/^\d*\.\d\d$/);
        if (REgXp.test(insrtval))
        {
            return false;
        }
    	var code;  
    	if (e.keyCode) code = e.keyCode;  
    	else if (e.which) code = e.which;
		//alert(code); 
    	if (code == 8 || code == 32 || code == 37 || code == 39 || code == 43 || code == 44 || code == 45)
            return true;
    	if (code < 48 || code > 57)  
    		return false;
        
    });
    $(".codedecimalnumeric2").bind('mouseenter',function(e){  
      var val = $(this).val();
      if (val!='0'){  
    	   val=val.replace(/[a-zA-Z]+/g, "")  
    	   $(this).val(val);  
      }  
    });
});