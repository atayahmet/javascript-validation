javascript-validation
=====================

Javascript Validation

<a href="https://github.com/atayahmet/javascript-validation/wiki">Dökümantasyon için tıklayınız</a>

validation.run({
	element: "form_register",
	rules: {
		fullname: "required",
		birthyear: {required: true, numeric: true, maxlength: 4, minlength: 4},
		phone: "required",
		email: {required: true, email: true, checkEmail: false}
	},
	messages: {
		fullname: "Enter your name",
		birthyear: {
			required: "Doğum yılınızı giriniz", 
			numeric: "Doğum yılınızı rakam ile belirtiniz",
			maxlength: "Doğum yılınız 4 haneli olmalıdır",
			minlength: "Doğum yılınız 4 haneli olmalıdır"
		},
		phone: "Cep telefonunuzu giriniz",
		email: {
			required: "Lütfen e-posta adresinizi giriniz",
			email: "E-posta adresinizi hatalı girdiniz",
			checkEmail: "Daha önce başvurunuz bulunuyor"
		}
		
	},
	complete: function(msg){
		
	},
	fail: function(obj,msg){
		
		
		
	}
});
