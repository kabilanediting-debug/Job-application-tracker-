Open Notepad

Create a new file and save it as job.html




2️⃣ Start HTML

<!DOCTYPE html>
<html>
<body>




3️⃣ Add a title

<h2>Job Application Tracker</h2>




4️⃣ Make input boxes

Company: <input id="c"><br>
Role: <input id="r"><br>
Date: <input id="d" type="date"><br>
Status: <input id="s"><br>




5️⃣ Add a button

<button onclick="addJob()">Add</button>



6️⃣ Create a table to show data

<table border="1" id="list"></table>



7️⃣ Start JavaScript

<script>
let jobs = [];



8️⃣ Write function to add job

function addJob(){
  let c=document.getElementById('c').value;
  let r=document.getElementById('r').value;
  let d=document.getElementById('d').value;
  let s=document.getElementById('s').value;
  jobs.push([c,r,d,s]);
  show();
}



9️⃣ Write function to show jobs

function show(){
  let t="<tr><th>Company</th><th>Role</th><th>Date</th><th>Status</th></tr>";
  for(let j of jobs){
    t += `<tr><td>${j[0]}</td><td>${j[1]}</td><td>${j[2]}</td><td>${j[3]}</td></tr>`;
  }
  document.getElementById('list').innerHTML = t;
}
</script>




🔟 Close HTML

</body>
</html>

