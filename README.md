
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HealthConnectP - Global Healthcare Network</title>
<style>
*{box-sizing:border-box;scroll-behavior:smooth}
body{margin:0;background:#f0f2f5;color:#243746;font-family:Arial,sans-serif}
header{background:#087f8c;color:white;padding:16px 5%;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:12px}
.logo{font-size:25px;font-weight:bold}
nav{display:flex;flex-wrap:wrap;gap:12px}
nav a{color:white;text-decoration:none;font-size:14px}
.container{max-width:1100px;margin:auto;padding:18px}
.welcome{background:linear-gradient(120deg,#087f8c,#13a69a);color:white;padding:35px 15px;border-radius:14px;text-align:center}
.welcome h1{font-size:30px}
h2{font-size:22px;color:#087f8c}
.departments{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:12px}
.department,.card,.post{background:white;padding:18px;border-radius:12px;margin:12px 0}
.department{text-align:center;cursor:pointer;border:1px solid #ddd}
.department:hover{border-color:#087f8c;background:#e8f7f6}
.emoji{font-size:30px}
.department h3{font-size:15px;color:#087f8c}
input,select,textarea{width:100%;padding:12px;border:1px solid #ccc;border-radius:7px;margin:6px 0;font-size:14px;background:white}
textarea{min-height:80px}
label{display:block;font-weight:bold;font-size:13px;margin-top:10px}
button,.register-link{background:#087f8c;color:white;padding:12px 18px;border:0;border-radius:7px;cursor:pointer;text-decoration:none;display:inline-block;margin:6px 3px}
button:hover,.register-link:hover{background:#075e69}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:12px}
.status{padding:12px;background:#e8f7f6;border-radius:7px;font-size:13px}
.muted{color:#687982;font-size:13px}
footer{background:#075e69;color:white;text-align:center;padding:25px;margin-top:25px}
</style>
</head>
<body>

<header>
<div class="logo">HealthConnectP</div>
<nav>
<a href="#home">Home</a>
<a href="#departments">Departments</a>
<a href="#feed">Feed</a>
<a href="#shop">Shop</a>
<a href="#register">Register</a>
</nav>
</header>

<main class="container" id="home">

<div class="welcome">
<h1>Welcome to HealthConnectP</h1>
<p>One Network. All Healthcare Professionals.</p>
<p>Connect • Discover • Grow</p>
<a class="register-link" href="#register">Join HealthConnectP</a>
</div>

<section id="departments">
<h2>Explore Healthcare Departments</h2>
<div class="departments">
<div class="department" onclick="chooseDepartment('DPT / Physiotherapy')">
<div class="emoji">🦿</div><h3>DPT / Physiotherapy</h3>
</div>
<div class="department" onclick="chooseDepartment('MBBS Doctors')">
<div class="emoji">🩺</div><h3>MBBS Doctors</h3>
</div>
<div class="department" onclick="chooseDepartment('Nursing')">
<div class="emoji">👩‍⚕️</div><h3>Nursing</h3>
</div>
<div class="department" onclick="chooseDepartment('Pharmacy')">
<div class="emoji">💊</div><h3>Pharmacy</h3>
</div>
<div class="department" onclick="chooseDepartment('Allied Health Sciences')">
<div class="emoji">🔬</div><h3>Allied Health Sciences</h3>
</div>
<div class="department" onclick="chooseDepartment('Shop')">
<div class="emoji">🛒</div><h3>Shop</h3>
</div>
</div>
</section>

<section id="search">
<h2>Find Healthcare Professionals</h2>
<div class="card">
<label>Department</label>
<select id="searchDepartment">
<option value="">All Departments</option>
<option>DPT / Physiotherapy</option>
<option>MBBS Doctors</option>
<option>Nursing</option>
<option>Pharmacy</option>
<option>Allied Health Sciences</option>
</select>

<label>Name / Specialization</label>
<input id="keyword" placeholder="Search professional">

<div class="grid">
<div>
<label>Country</label>
<select id="searchCountry"><option value="">All Countries</option></select>
</div>
<div>
<label>Province / State</label>
<select id="searchRegion"><option value="">All Regions</option></select>
</div>
<div>
<label>City / District</label>
<select id="searchCity"><option value="">All Cities</option></select>
</div>
<div>
<label>Gender</label>
<select id="searchGender">
<option>All</option>
<option>Male</option>
<option>Female</option>
</select>
</div>
<div>
<label>Availability</label>
<select id="searchStatus">
<option value="">All</option>
<option>Online</option>
<option>Offline</option>
</select>
</div>
</div>
<button onclick="searchProfessionals()">Search</button>
<p id="searchResult" class="status">Professional database will be connected in the next development stage.</p>
</div>
</section>

<section id="feed">
<h2>Healthcare Home Feed</h2>
<div class="card">
<strong>Share an Update</strong>
<p class="muted">Healthcare news, professional achievements and articles.</p>
<button onclick="alert('Please register to create a post.')">Create Post</button>
</div>
<div class="post">
<strong>Welcome to HealthConnectP!</strong>
<p>Connect with healthcare professionals and grow your career.</p>
</div>
</section>

<section id="shop">
<h2>HealthConnectP Shop</h2>
<div class="card">
<h3>Healthcare Products Marketplace</h3>
<p>Medical equipment, physiotherapy instruments and healthcare supplies.</p>
<p class="muted">Product listings coming soon.</p>
</div>
</section>

<section id="register">
<h2>Professional Registration</h2>
<div class="card">
<p>Join the HealthConnectP global healthcare community.</p>

<div class="grid">
<div>
<label>Full Name</label>
<input id="fullName" placeholder="Enter full name">
</div>
<div>
<label>Email Address</label>
<input id="email" type="email" placeholder="Enter email">
</div>
<div>
<label>Password</label>
<input id="password" type="password" placeholder="Create password">
</div>
<div>
<label>Department</label>
<select id="regDepartment">
<option value="">Select Department</option>
<option>DPT / Physiotherapy</option>
<option>MBBS Doctors</option>
<option>Nursing</option>
<option>Pharmacy</option>
<option>Allied Health Sciences</option>
</select>
</div>
<div>
<label>Gender</label>
<select id="regGender">
<option value="">Select Gender</option>
<option>Male</option>
<option>Female</option>
</select>
</div>
<div>
<label>Specialization</label>
<input id="specialization" placeholder="Your specialization">
</div>
</div>

<h3>Current Location</h3>
<div class="grid">
<div>
<label>Country</label>
<select id="country"><option value="">Select Country</option></select>
</div>
<div>
<label>Province / State / Region</label>
<select id="region"><option value="">Select Country First</option></select>
</div>
<div>
<label>District / City</label>
<select id="city"><option value="">Select Region First</option></select>
</div>
<div>
<label>Postal / ZIP Code</label>
<input id="postal" placeholder="Enter postal code">
</div>
</div>
<label>Complete Address</label>
<textarea id="address" placeholder="House, street, area, city"></textarea>

<h3>Education and Qualification</h3>
<div class="grid">
<div>
<label>Degree / Qualification</label>
<input id="degree" placeholder="e.g. Doctor of Physical Therapy">
</div>
<div>
<label>University / Institute</label>
<input id="university" placeholder="University name">
</div>
<div>
<label>Degree Country</label>
<select id="degreeCountry"><option value="">Select Country</option></select>
</div>
<div>
<label>Degree City</label>
<input id="degreeCity" placeholder="City of education">
</div>
<div>
<label>Graduation Year</label>
<input id="graduation" type="number" placeholder="Graduation year">
</div>
<div>
<label>Professional Registration / License ID</label>
<input id="license" placeholder="Official registration ID">
</div>
</div>

<label>Experience</label>
<input id="experience" placeholder="e.g. 2 years">

<label>Upload CV / Certificates</label>
<input id="documents" type="file" multiple accept=".pdf,.jpg,.jpeg,.png">

<p class="muted">Your documents will not be stored until secure database and file storage are connected.</p>

<button type="button" onclick="submitRegistration()">Submit Registration</button>
<p id="registrationResult" class="status">Complete the form to continue.</p>
</div>
</section>

</main>

<footer>
<strong>HealthConnectP</strong>
<p>Connecting Healthcare Professionals Worldwide.</p>
<p>© 2026 HealthConnectP. All Rights Reserved.</p>
</footer>

<script>
const API="https://countriesnow.space/api/v0.1";

const pakistanRegions={
"Sindh":["Karachi","Hyderabad","Sukkur","Larkana","Mirpur Khas","Nawabshah","Thatta","Badin","Dadu","Jacobabad","Khairpur","Shikarpur","Ghotki","Sanghar","Umerkot","Tharparkar"],
"Punjab":["Lahore","Faisalabad","Rawalpindi","Multan","Gujranwala","Sialkot","Bahawalpur","Sargodha","Sahiwal","Gujrat","Jhelum","Dera Ghazi Khan","Rahim Yar Khan","Kasur","Sheikhupura","Okara","Attock","Chiniot"],
"Khyber Pakhtunkhwa":["Peshawar","Mardan","Abbottabad","Swat","Kohat","Bannu","Dera Ismail Khan","Charsadda","Nowshera","Mansehra","Haripur","Swabi"],
"Balochistan":["Quetta","Gwadar","Turbat","Khuzdar","Chaman","Sibi","Zhob","Loralai","Hub","Kalat","Pishin"]
};

let countries=[];

function fill(id,items,first){
let s=document.getElementById(id);
s.innerHTML="";
let o=document.createElement("option");
o.value="";
o.textContent=first;
s.appendChild(o);
items.forEach(item=>{
let x=document.createElement("option");
x.value=item;
x.textContent=item;
s.appendChild(x);
});
}

async function loadCountries(){
let names=[];
try{
let r=await fetch(API+"/countries/iso");
let d=await r.json();
names=(d.data||[]).map(x=>x.name).filter(Boolean);
}catch(e){}
if(!names.length){
names=["Pakistan","United States","United Arab Emirates","Poland","United Kingdom","Canada","Australia","India","Saudi Arabia","Qatar","Turkey","Germany","France","China","Japan","Malaysia","South Africa"];
}
countries=names;
fill("country",names,"Select Country");
fill("degreeCountry",names,"Select Degree Country");
fill("searchCountry",names,"All Countries");
}

async function regionsFor(country){
if(country==="Pakistan")return Object.keys(pakistanRegions);
try{
let r=await fetch(API+"/countries/states",{
method:"POST",
headers:{"Content-Type":"application/json"},
body:JSON.stringify({country:country})
});
let d=await r.json();
return (d.data?.states||[]).map(x=>x.name);
}catch(e){return [];}
}

async function citiesFor(country,region){
if(country==="Pakistan")return pakistanRegions[region]||[];
try{
let r=await fetch(API+"/countries/state/cities",{
method:"POST",
headers:{"Content-Type":"application/json"},
body:JSON.stringify({country:country,state:region})
});
let d=await r.json();
return d.data||[];
}catch(e){return [];}
}

async function updateRegions(countryId,regionId,cityId){
let country=document.getElementById(countryId).value;
fill(regionId,[],"Loading regions...");
fill(cityId,[],"Select Region First");
if(!country){
fill(regionId,[],"Select Country First");
return;
}
let list=await regionsFor(country);
fill(regionId,list,list.length?"Select Province / State":"No regions found");
}

async function updateCities(countryId,regionId,cityId){
let country=document.getElementById(countryId).value;
let region=document.getElementById(regionId).value;
fill(cityId,[],"Loading cities...");
if(!country||!region){
fill(cityId,[],"Select Region First");
return;
}
let list=await citiesFor(country,region);
fill(cityId,list,list.length?"Select City / District":"No cities found");
}

document.getElementById("country").addEventListener("change",()=>{
updateRegions("country","region","city");
});
document.getElementById("region").addEventListener("change",()=>{
updateCities("country","region","city");
});
document.getElementById("searchCountry").addEventListener("change",()=>{
updateRegions("searchCountry","searchRegion","searchCity");
});
document.getElementById("searchRegion").addEventListener("change",()=>{
updateCities("searchCountry","searchRegion","searchCity");
});

function chooseDepartment(name){
if(name==="Shop"){
location.hash="shop";
}else{
document.getElementById("searchDepartment").value=name;
location.hash="search";
}
}

function searchProfessionals(){
let d=document.getElementById("searchDepartment").value||"All Departments";
let c=document.getElementById("searchCountry").value||"All Countries";
let r=document.getElementById("searchRegion").value||"All Regions";
let city=document.getElementById("searchCity").value||"All Cities";
let g=document.getElementById("searchGender").value;
document.getElementById("searchResult").textContent=
"Selected filters: "+d+" | "+c+" | "+r+" | "+city+" | Gender: "+g+". Real professional listings will be connected with the database.";
}

function submitRegistration(){
let name=document.getElementById("fullName").value.trim();
let email=document.getElementById("email").value.trim();
let department=document.getElementById("regDepartment").value;
let gender=document.getElementById("regGender").value;
let country=document.getElementById("country").value;
let result=document.getElementById("registrationResult");

if(!name||!email||!department||!gender||!country){
result.textContent="Please complete Name, Email, Department, Gender and Country.";
return;
}
result.textContent="Form completed for "+name+". This is a preview only. Secure account registration and database saving will be added in the next stage.";
}

loadCountries();
</script>

</body>
</html>
