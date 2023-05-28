<!DOCTYPE html>
<html lang="en">
	<head>
		<!-- Required meta tags -->
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
		<title>Student Form</title>

		<!-- Bootstrap CSS -->
		<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/css/bootstrap.min.css" integrity="sha384-B0vP5xmATw1+K9KRQjQERJvTumQW0nPEzvF6L/Z6nronJ3oUOFUFpCjEUQouq2+l" crossorigin="anonymous">
		<!-- Optional JavaScript -->
		<!-- jQuery first, then Popper.js, then Bootstrap JS -->
		<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
		<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
		<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/js/bootstrap.min.js" integrity="sha384-+YQ4JLhjyBLPDQt//I+STsc9iw4uQqACwlvpslubQzn4u2UU2UFM80nGisd026JF" crossorigin="anonymous"></script>
		

	</head>
	<body>
		<style type="text/css">
			body{
				 background-image: linear-gradient(90deg,#00ff82 50%,#00dcff 50%);
			}
			
		</style>
		<h1 style="text-align: center;">Student Form</h1>
		<form class="" action="get.html">
		  
		<div class="form-group">
		    <label for="getName">Name</label>
		    <input type="Name" class="form-control" id="exampleName" placeholder="Enter Name">

		    <label for="getMail">Email </label>
		    <input type="email" class="form-control" id="exampleMail" aria-describedby="emailHelp" placeholder="Enter email">

		    <label for="Tamil">Tamil</label>
		    <input type="number" class="form-control" id="TamizhMark" placeholder="Enter Tamil Mark" >

		    <label for="English">English</label>
		    <input type="number" class="form-control" id="EnglishMark" placeholder="Enter English Mark" >

		    <label for="Maths">Maths</label>
		    <input type="number" class="form-control" id="MathsMark" placeholder="Enter Maths Mark" >

		    <label for="Science">Science</label>
		    <input type="number" class="form-control" id="ScienceMark" placeholder="Enter Science Mark" >

		    <label for="Social">Social</label>
		    <input type="number" class="form-control" id="SocialMark" placeholder="Enter Social Mark" >

		  </div>

		
		  <button type="button" class="btn btn-primary" onclick="Add()">Add</button>
		  <button type="button" class="btn btn-primary" onclick="View()">View</button>
		</form>

		<h3 id="res"></h3>

	</body>
	<script type="text/javascript">
				nameArr=[]
				emailArr=[]
				aArr=[]
				bArr=[]
				cArr=[]
				dArr=[]
				eArr=[]
		function Add(){
				name=document.getElementById("exampleName").value;
				email=document.getElementById("exampleMail").value;
				a=document.getElementById("TamizhMark").value;
				b=document.getElementById("EnglishMark").value;
				c=document.getElementById("MathsMark").value;
				d=document.getElementById("ScienceMark").value;
				e=document.getElementById("SocialMark").value;
				nameArr.push(name);
				emailArr.push(email);
				aArr.push(a);
				bArr.push(b);
				cArr.push(c);
				dArr.push(d);
				eArr.push(e);
				document.getElementById("exampleName").value="";
				document.getElementById("exampleMail").value="";
				document.getElementById("TamizhMark").value="";
				document.getElementById("EnglishMark").value="";
				document.getElementById("MathsMark").value="";
				document.getElementById("ScienceMark").value="";
				document.getElementById("SocialMark").value="";

		}

		function View(){

			tableview="<center><table border='1'><tbody>";
				tableview+="<tr><th>"+"S.no"+"</th>" +" <th>"+"Name"+"</th><th>"+"Email"+"</th>" +" <th>"+"Tamil Mark"+"</th> <th>"+"English Mark"+"</th>" +" <th>"+"Maths Mark"+"</th><th>"+"Science Mark"+"</th>" +" <th>"+"Social Mark"+"</th><th>"+"Total"+"</th> <th>"+"Average"+"</th> <th>"+"Pass or Fail"+"</th><th>"+"Grade"+"</th><th>"+"Action"+"</th> </tr>"
			
				len=nameArr.length
			for(i=0;i<len;i++){				
				j=i+1;
				totalvalue=parseInt(aArr[i])+parseInt(bArr[i])+parseInt(cArr[i])+parseInt(dArr[i])+parseInt(eArr[i]);
				Avevalue=totalvalue/5;
				passorfail=" ";
				grade=" ";

				if(aArr[i]>=35 && bArr[i]>=35 && cArr[i]>=35 && dArr[i]>=35 && eArr[i]>=35)
				{
					passorfail+="Pass";
				}
				else{
					passorfail+="Fail";
				}

				if(aArr[i]>90 && bArr[i]>90 && cArr[i]>90 && dArr[i]>90 && eArr[i]>90){
					grade+="O+";
				}
				else if(aArr[i]>80 && bArr[i]>80 && cArr[i]>80 && dArr[i]>80 && eArr[i]>80){
					grade+="A+"; 
				}
				else if(aArr[i]>70 && bArr[i]>70 && cArr[i]>70 && dArr[i]>70 && eArr[i]>70){
					grade+="A";
				}
				else if(aArr[i]>60 && bArr[i]>60 && cArr[i]>60 && dArr[i]>60 && eArr[i]>60){
					grade+="B+";
				}
				else if(aArr[i]>50 && bArr[i]>50 && cArr[i]>50 && dArr[i]>50 && eArr[i]>50){
					grade+="C";
				}
				else if(aArr[i]>40 && bArr[i]>40 && cArr[i]>40 && dArr[i]>40 && eArr[i]>40){
					grade+="D";
				}
				
				else if(aArr[i]>35 && bArr[i]>35 && cArr[i]>35 && dArr[i]>35 && eArr[i]>35){
					grade+="E";
				}
				else{
					grade+="F";
				}

					tableview+="<tr><td>"+j+"</td><td>"+nameArr[i]+"</td><td>"+emailArr[i]+"</td><td>"+aArr[i]+"</td><td>"+bArr[i]+"</td><td>"+cArr[i]+"</td><td>"+dArr[i]+"</td><td>"+eArr[i]+"</td><td>"+totalvalue+"</td><td>"+Avevalue+"</td><td>"+passorfail+"</td><td>"+grade+"</td> <td>"+"<button type='button' class='btn btn-primary' onclick='Edit("+i+")'>Edit</button> "+"<button type='button' class='btn btn-danger' onclick='Delete("+i+")'>Delete</button>"+"<button type='button' class='btn btn-warning' onclick='update("+i+")'>update</button></td> </tr>"


			}
			
			tableview+="</tbody></table></center>";
			
	
			document.getElementById("res").innerHTML=tableview;	

		}
		function Edit(i){
				//output=[nameArr[i],emailArr[i],aArr[i],bArr[i],cArr[i],dArr[i],eArr[i]]
				document.getElementById("exampleName").value=nameArr[i];
				document.getElementById("exampleMail").value=emailArr[i];
				document.getElementById("TamizhMark").value=aArr[i];
				document.getElementById("EnglishMark").value=bArr[i];
				document.getElementById("MathsMark").value=cArr[i];
				document.getElementById("ScienceMark").value=dArr[i];
				document.getElementById("SocialMark").value=eArr[i];	
		}

		function update(i){
				name=document.getElementById("exampleName").value;
				email=document.getElementById("exampleMail").value;
				a=document.getElementById("TamizhMark").value;
				b=document.getElementById("EnglishMark").value;
				c=document.getElementById("MathsMark").value;
				d=document.getElementById("ScienceMark").value;
				e=document.getElementById("SocialMark").value;

				nameArr.splice(i,1, name);
				emailArr.splice(i,1, email);
				aArr.splice(i,1, a);
				bArr.splice(i,1, b);
				cArr.splice(i,1, c);
				dArr.splice(i,1, d);
				eArr.splice(i,1, e);
				
				View();

				document.getElementById("exampleName").value="";
				document.getElementById("exampleMail").value="";
				document.getElementById("TamizhMark").value="";
				document.getElementById("EnglishMark").value="";
				document.getElementById("MathsMark").value="";
				document.getElementById("ScienceMark").value="";
				document.getElementById("SocialMark").value="";
			
		}


		function Delete(i){
			//output=[nameArr[i],emailArr[i],aArr[i],bArr[i],cArr[i],dArr[i],eArr[i]]

				nameArr.splice(i,1);
				emailArr.splice(i,1);
				aArr.splice(i,1);
				bArr.splice(i,1);
				cArr.splice(i,1);
				dArr.splice(i,1);
				eArr.splice(i,1);

				View();

			
		}
		
		
	</script>
</html>
