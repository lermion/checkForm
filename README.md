# checkForm
function checkForm(){
			var f = document.forms["myForm"];
			var els = f.elements;
			var isEmpty = false;
			for(var i = 0; i < els.length; i++){
				if(els[i].type === "text"){
					if(els[i].value === ""){
						els[i].style.borderColor = "red";
						isEmpty = true;
					}else{
						els[i].style.borderColor = "";
					}
				}
			} // конец for
			if(isEmpty){
				alert("Заполните все поля!");
				return false;
			}else{
				f.submit();
			}
		}
