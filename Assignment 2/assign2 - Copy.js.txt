//Author: Logan Bateman, 000918989

function group_1_choice_1(e){
	let range=document.getElementById("input").value;
	if (isNaN(range)==false || range==0){
		if (range>=13 && range<=17){
			document.getElementById("output").value="In range";
		}else{
			document.getElementById("output").value="Not in range";
		}
	}else{
		document.getElementById("output").value="Not a valid input";
	}

}

function group_1_choice_3(e) {
	let square=document.getElementById("inputSquare").value;
	if (isNaN(square)==false && square>=0) {
		let side=parseFloat(square);
		document.getElementById("perimeter").value=4*side;
		document.getElementById("area").value=side**2;
	}else {
		document.getElementById("perimeter").value="Can't calculate";
		document.getElementById("area").value="Can't calculate";
	}

}

function group_2_choice_1(e){
	let vowel=document.getElementById("vowels").value;
	if(vowel==="a" || vowel==="e" || vowel==="i" || vowel==="o" || vowel==="u" || vowel==="A" || vowel==="E" || vowel==="I" ||vowel==="O" || vowel==="U"){
		document.getElementById("outVow").value="A Vowel";
	}else if (vowel==="y" || vowel==="Y"){
		document.getElementById("outVow").value="Sometimes lol";
	}else {
		document.getElementById("outVow").value="Nah Fam";
	}
}

function group_2_choice_3(e) {
	let fact=document.getElementById("factorial").value;
	let n=parseInt(fact);
	if (n<=0){
		document.getElementById("outFact").value="Cannot compute factorial value";
	}else{
		let num=1;
		for (let i=1; i<=n; i++){
			num*=i;
		}
		document.getElementById("outFact").value=num;
	}
}

function group_3_choice_2(e) {
	let int1=parseInt(document.getElementById("int1").value);
	let operator=document.getElementById("operator").value;
	let int2=parseInt(document.getElementById("int2").value);
	
	if(isNaN(int1)==true || isNaN(int2)==true){
		document.getElementById("equals").value="Invalid number";
	}else if(operator==="+"){
		document.getElementById("equals").value=int1+int2;
	}else if(operator==="-"){
		document.getElementById("equals").value=int1-int2;
	}else if(operator==="*"){
		document.getElementById("equals").value=int1*int2;
	}else if(operator==="/"){
		document.getElementById("equals").value=int1/int2;
	}else if(operator==="%"){
		document.getElementById("equals").value=int1%int2;
	}else{
		document.getElementById("equals").value="Invalid operator";
	}
	
}