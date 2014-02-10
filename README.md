javascript-validation
=====================

Javascript Validation

document.getElementById('element_id').onclick = function(e){
		
		validation.run({
					
			element: "form_id",
			rules: {
				fullname: "required",
				birthyear: {required: true, numeric: true, maxlength: 4, minlength: 4},
				university: "required",
				phone: "required",
				email: {required: true, email: true, checkEmail: true}
			},
			messages: {
				fullname: "Enter your name",
				birthyear: {
					required: "Enter your birthyear", 
					numeric: "Must be numeric",
					maxlength: "should be no more than 4-digit",
					minlength: "Must be at least 4-digit"
				},
				phone: "Enter your phone number",
				email: {
					required: Enter your email",
					email: "Email error",
					checkEmail: "Daha önce başvurunuz bulunuyor"
				}
				
			},
			complete: function(msg){
		
			  // form valid actions!
				
			},
			fail: function(obj,msg){
				
		    // form fail actions!
				
			}
			
		});
		
	}
