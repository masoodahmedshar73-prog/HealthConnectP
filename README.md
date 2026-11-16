
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HealthConnectP | Global Healthcare Network</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:#f0f2f5;color:#243746;font-family:Arial,sans-serif}
header{background:#087f8c;color:white;padding:15px 5%;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:12px}
.logo{font-size:25px;font-weight:bold}
nav a{color:white;text-decoration:none;margin:8px;font-size:14px}
.container{max-width:1100px;margin:auto;padding:18px}
.welcome{background:linear-gradient(120deg,#087f8c,#13a69a);color:white;padding:30px;border-radius:14px;text-align:center}
.welcome h1{margin:5px}
h2{font-size:21px}
.departments{display:grid;grid-template-columns:repeat(auto-fit,minmax(145px,1fr));gap:12px}
.department{background:white;padding:19px 10px;border-radius:12px;text-align:center;cursor:pointer;border:1px solid #e4e9ed}
.department:hover{border-color:#087f8c;background:#e8f7f6}
.department .emoji{font-size:30px}
.department h3{font-size:15px;color:#087f8c}
.card,.post{background:white;padding:17px;border-radius:12px;margin:12px 0}
input,select,textarea{width:100%;padding:12px;border:1px solid #ccc;border-radius:7px;margin:6px 0;font-size:14px;background:white}
textarea{min-height:85px;resize:vertical}
button{background:#087f8c;color:white;padding:11px 17px;border:0;border-radius:7px;cursor:pointer;margin:5px 3px}
button:hover{background:#075e69}
.filters{display:grid;grid-template-columns:repeat(auto-fit,minmax(145px,1fr));gap:8px}
.muted{color:#6b7c85;font-size:13px}
.section-title{color:#087f8c;margin-bottom:8px}
.status{padding:10px;background:#e8f7f6;border-radius:7px;font-size:13px;margin:8px 0}
footer{background:#075e69;color:white;text-align:center;padding:25px;margin-top:25px}
label{font-size:13px;font-weight:bold;display:block;margin-top:9px}
.grid2{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
.hidden{display:none}
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

<section>
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

<label>Search Name / Specialization</label>
<input id="keyword" placeholder="Enter name or specialization">

<div class="grid2">
<div>
<label>Country</label>
<select id="searchCountry"><option value="">All Countries</option></select>
</div>
<div>
<label>Province / State / Region</label>
<select id="searchRegion"><option value="">All Regions</option></select>
</div>
<div>
<label>District / City</label>
<select id="searchCity"><option value="">All Cities</option></select>
</div>
<div>
<label>Gender</label>
<select id="searchGender">
<option value="All">All</option>
<option value="Male">Male</option>
<option value="Female">Female</option>
</select>
</div>
<div>
<label>Availability</label>
<select id="searchStatus">
<option value="">Online & Offline</option>
<option>Online</option>
<option>Offline</option>
</select>
</div>
</div>
<button onclick="searchProfessionals()">Search Professionals</button>
<p id="searchResult" class="status">Select your filters to search professionals. Professional database will be connected in a later stage.</p>
</div>
</section>

<section id="feed">
<h2>Healthcare Home Feed</h2>
<div class="card">
<strong>Share an update</strong>
<p class="muted">Healthcare news, professional achievements and articles will appear here.</p>
<button onclick="alert('Please register or login to create a post.')">Create Post</button>
</div>
<div class="post">
<strong>Welcome to HealthConnectP!</strong>
<p>Connect with healthcare professionals, discover opportunities and grow your career.</p>
<p class="muted">HealthConnectP Community</p>
</div>
</section>

<section id="shop">
<h2>HealthConnectP Shop</h2>
<div class="card">
<h3>Healthcare Products Marketplace</h3>
<p>Medical equipment, physiotherapy instruments and healthcare supplies.</p>
<p class="muted">Shop listings coming soon.</p>
</div>
</section>

<section id="register">
<h2>Professional Registration</h2>
<div class="card">
<p class="muted">Create your professional profile. Required details can be completed when the registration system is connected.</p>

<div class="grid2">
<div>
<label>Full Name</label>
<input id="fullName" placeholder="Your full name">
</div>
<div>
<label>Email Address</label>
<input id="email" type="email" placeholder="Your email">
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
<label>Professional Specialization</label>
<input id="specialization" placeholder="e.g. Orthopedic Physiotherapy">
</div>
</div>

<h3 class="section-title">Your Current Location</h3>
<div class="grid2">
<div>
<label>Country</label>
<select id="country"><option value="">Loading countries...</option></select>
</div>
<div>
<label>Province / State / Region</label>
<select id="region" disabled><option value="">Select country first</option></select>
</div>
<div>
<label>District / City</label>
<select id="city" disabled><option value="">Select region first</option></select>
</div>
<div>
<label>Postal / ZIP Code</label>
<input id="postal" placeholder="Enter postal or ZIP code">
<button type="button" onclick="lookupPostal()">Find Postal Code</button>
</div>
</div>

<label>Complete Address</label>
<textarea id="address" placeholder="House, street, area, district, city"></textarea>

<h3 class="section-title">Education and Qualification</h3>
<div class="grid2">
<div>
<label>Degree / Qualification</label>
<input id="degree" placeholder="e.g. Doctor of Physical Therapy">
</div>
<div>
<label>University / Institute</label>
<input id="university" placeholder="University name">
</div>
<div>
<label>Country of Degree</label>
<select id="degreeCountry"><option value="">Select country</option></select>
</div>
<div>
<label>City of Degree</label>
<input id="degreeCity" placeholder="City where you studied">
</div>
<div>
<label>Graduation Year</label>
<input id="graduation" type="number" placeholder="e.g. 2026">
</div>
<div>
<label>Professional Registration / License ID</label>
<input id="license" placeholder="Enter official registration number">
</div>
</div>

<label>Experience</label>
<input id="experience" placeholder="e.g. 2 years">

<label>CV / Certificates</label>
<input id="documents" type="file" multiple accept=".pdf,.jpg,.jpeg,.png">
<p class="muted">Document upload is only a form preview at this stage. Secure file storage will be added later.</p>

<button type="button" onclick="submitRegistration()">Submit Registration</button>
<p id="registrationResult" class="status">Registration system is not connected to a database yet.</p>
</div>
</section>

</main>

<footer>
<strong>HealthConnectP</strong>
<p>Connecting Healthcare Professionals Worldwide.</p>
<p>© 2026 HealthConnectP. All Rights Reserved.</p>
</footer>

<script>
const API = "https://countriesnow.space/api/v0.1";
const ZIP_API = "https://api.zippopotam.us";

const pakistanRegions = {
 "Sindh": ["Karachi","Hyderabad","Sukkur","Larkana","Mirpur Khas","Shaheed Benazirabad","Thatta","Badin","Dadu","Jacobabad","Khairpur","Shikarpur","Ghotki","Sanghar","Umerkot","Tharparkar"],
 "Punjab": ["Lahore","Faisalabad","Rawalpindi","Multan","Gujranwala","Sialkot","Bahawalpur","Sargodha","Sahiwal","Gujrat","Jhelum","Dera Ghazi Khan","Rahim Yar Khan","Kasur","Sheikhupura","Okara","Attock","Chiniot"],
 "Khyber Pakhtunkhwa": ["Peshawar","Mardan","Abbottabad","Swat","Kohat","Bannu","Dera Ismail Khan","Charsadda","Nowshera","Mansehra","Haripur","Swabi","Lower Dir","Malakand"],
 "Balochistan": ["Quetta","Gwadar","Turbat","Khuzdar","Chaman","Sibi","Zhob","Loralai","Hub","Dera Murad Jamali","Kalat","Pishin"]
};

let countryList = [];
let selectedCountryCode = "";

function fillSelect(select, items, firstText) {
 select.innerHTML = "";
 let first = document.createElement("option");
 first.value = "";
 first.textContent = firstText;
 select.appendChild(first);
 items.forEach(item => {
   let option = document.createElement("option");
   option.value = item.value || item;
   option.textContent = item.label || item;
   select.appendChild(option);
 });
}

async function loadCountries() {
 const mainSelect = document.getElementById("country");
 const searchSelect = document.getElementById("searchCountry");
 const degreeSelect = document.getElementById("degreeCountry");

 try {
   const response = await fetch(API + "/countries/iso");
   const result = await response.json();
   countryList = (result.data || []).map(item => ({
     name: item.name || item,
     code: item.Iso2 || item.iso2 || ""
   })).filter(item => item.name);

   if (!countryList.length) throw new Error("Country list unavailable");
 } catch(error) {
   countryList = [
     {name:"Pakistan",code:"PK"},
     {name:"United States",code:"US"},
     {name:"United Arab Emirates",code:"AE"},
     {name:"Poland",code:"PL"},
     {name:"United Kingdom",code:"GB"},
     {name:"Canada",code:"CA"},
     {name:"Australia",code:"AU"},
     {name:"India",code:"IN"},
     {name:"Saudi Arabia",code:"SA"},
     {name:"Qatar",code:"QA"},
     {name:"Turkey",code:"TR"},
     {name:"Germany",code:"DE"}
   ];
 }

 const options = countryList.map(c => ({value:c.name,label:c.name}));
 fillSelect(mainSelect, options, "Select Country");
 fillSelect(degreeSelect, options, "Select Degree Country");
 fillSelect(searchSelect, options, "All Countries");
}

async function loadRegions(countryName, target, isSearch=false) {
 const regionSelect = document.getElementById(target);
 const citySelect = document.getElementById(isSearch ? "searchCity" : "city");
 fillSelect(regionSelect, [], "Loading regions...");
 regionSelect.disabled = true;
 fillSelect(citySelect, [], "Select region first");
 citySelect.disabled = true;

 if (!countryName) {
   fillSelect(regionSelect, [], "Select country first");
   return;
 }

 let regions = [];

 if (countryName === "Pakistan") {
   regions = Object.keys(pakistanRegions);
 } else {
   try {
     const response = await fetch(API + "/countries/states", {
       method:"POST",
       headers:{"Content-Type":"application/json"},
       body:JSON.stringify({country:countryName})
     });
     const result = await response.json();
     regions = (result.data && result.data.states || []).map(s => s.name || s);
   } catch(error) {
     regions = [];
   }
 }

 fillSelect(regionSelect, regions, regions.length ? "Select Province / State" : "No regions found - enter manually");
 regionSelect.disabled = false;
}

async function loadCities(countryName, regionName, target, isSearch=false) {
 const citySelect = document.getElementById(target);
 fillSelect(citySelect, [], "Loading cities...");
 citySelect.disabled = true;
 if (!countryName || !regionName) return;

 let cities = [];

 if (countryName === "Pakistan" && pakistanRegions[regionName]) {
   cities = pakistanRegions[regionName];
 } else {
   try {
     const response = await fetch(API + "/countries/state/cities", {
       method:"POST",
       headers:{"Content-Type":"application/json"},
       body:JSON.stringify({country:countryName,state:regionName})
     });
     const result = await response.json();
     cities = result.data || [];
   } catch(error) {
     cities = [];
   }
 }

 fillSelect(citySelect, cities, cities.length ? "Select District / City" : "No cities found - enter manually");
 citySelect.disabled = false;
}

document.getElementById("country").addEventListener("change", e => {
 loadRegions(e.target.value,"region");
});

document.getElementById("region").addEventListener("change", e => {
 loadCities(document.getElementById("country").value,e.target.value,"city");
});

document.getElementById("searchCountry").addEventListener("change", e => {
 loadRegions(e.target.value,"searchRegion",true);
});

document.getElementById("searchRegion").addEventListener("change", e => {
 loadCities(document.getElementById("searchCountry").value,e.target.value,"searchCity",true);
});

async function lookupPostal() {
 const countryName = document.getElementById("country").value;
 const regionName = document.getElementById("region").value;
 const cityName = document.getElementById("city").value;
 const postal = document.getElementById("postal");
 const country = countryList.find(c => c.name === countryName);

 if (!country || !country.code || !cityName) {
   alert("Please select country and city first.");
   return;
 }

 try {
   const url = ZIP_API + "/" + country.code.toLowerCase() + "/" +
     encodeURIComponent(regionName.toLowerCase()) + "/" +
     encodeURIComponent(cityName);
   const response = await fetch(url);
   if (!response.ok) throw new Error("Postal code not found");
   const result = await response.json();
   const codes = (result.places || []).map(p => p["post code"]).filter(Boolean);
   postal.value = [...new Set(codes)].join(", ");
   if (!postal.value) alert("Postal code not available. Please enter it manually.");
 } catch(error) {
   alert("Postal code could not be found automatically. Please enter it manually.");
 }
}

function chooseDepartment(name) {
 document.getElementById("searchDepartment").value = name;
 document.getElementById("searchDepartment").scrollIntoView({behavior:"smooth"});
}

function searchProfessionals() {
 const department = document.getElementById("searchDepartment").value || "All Departments";
 const country = document.getElementById("searchCountry").value || "All Countries";
 const region = document.getElementById("searchRegion").value || "All Regions";
 const city = document.getElementById("searchCity").value || "All Cities";
 const gender = document.getElementById("searchGender").value;
 const keyword = document.getElementById("keyword").value || "Any";
 const status = document.getElementById("searchStatus").value || "All";

 document.getElementById("searchResult").textContent =
 "Filters selected: " + department + " | " + country + " | " +
 region + " | " + city + " | Gender: " + gender +
 " | Search: " + keyword + " | Availability: " + status +
 ". Professional database will be connected in the next development stage.";
}

function submitRegistration() {
 const name = document.getElementById("fullName").value.trim();
 const department = document.getElementById("regDepartment").value;
 const gender = document.getElementById("regGender").value;
 const country = document.getElementById("country").value;

 if (!name || !department || !gender || !country) {
   document.getElementById("registrationResult").textContent =
     "Please enter your name, department, gender and country.";
   return;
 }

 document.getElementById("registrationResult").textContent =
   "Form preview completed for " + name +
   ". This website does not save registrations yet. Database and secure verification will be added later.";
}

loadCountries();
</script>
</body>
</html>

