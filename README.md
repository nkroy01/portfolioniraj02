# portfolioniraj02
#CSS,,JS




*{margin:0;padding:0;box-sizing:border-box;font-family:Arial}

body{background:#0f172a;color:#fff}

header{padding:20px 60px}
.logo{font-size:18px}

.navbar{display:flex;justify-content:space-between;align-items:center}
.navbar ul{display:flex;gap:25px;list-style:none}
.navbar a{color:#fff;text-decoration:none}
.navbar a.active,.navbar a:hover{color:#4ade80}

/* Home */
.home{display:flex;justify-content:space-between;align-items:center;
padding:70px 60px}
.green{color:#22c55e}
.btn{background:#22c55e;padding:12px 25px;border-radius:95px;border:10}
.social i{margin-top:20px;margin-right:10px;font-size:20px}

.home-img{position:relative}
.circle{width:290px;height:450px;border:10px solid #22c55e;
border-radius:50%;position:absolute;top:-20px;left:-22px}
.home-img img{width:260px;border-radius:50%;}

/* Services */
.section-title{font-size:32px;text-align:center;margin:40px 0}
.section-title span{color:#22c55e}

.services .service-box{
display:grid;grid-template-columns:repeat(3,1fr);gap:20px;
padding:0 60px}
.card{background:#1f2937;padding:30px;border-radius:8px;text-align:center}
.card.active{border:2px solid #22c55e}

/* Resume */
.resume{padding:40px 60px}
.resume-menu{display:flex;gap:10px;margin-bottom:20px}
.tab{padding:10px 20px;border-radius:20px;border:1px solid #22c55e;
background:transparent;color:#fff}
.tab.active{background:#22c55e}

.resume-content{display:none}
.show{display:block}

.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px}
.box{background:#1f2937;padding:25px;border-radius:8px}

/* Skills */
.skills-grid{display:grid;grid-template-columns:repeat(6,1fr);
padding:20px 0}
.skills-grid i{font-size:40px;text-align:center}

/* Portfolio */
.portfolio{padding:40px 60px}
.project{margin-bottom:30px}
.project img{width:300px;border-radius:8px}

/* Contact */
.contact{padding:20px 60px}
.contact-box{background:#1f2937;padding:20px;border-radius:5px}
input,textarea{width:100%;padding:10px;margin:10px 0;border-radius:2px;border:0}









#jS

let tabs = document.querySelectorAll(".tab");
let contents = document.querySelectorAll(".resume-content");

tabs.forEach(tab =>{
  tab.onclick=()=>{
    tabs.forEach(t=>t.classList.remove("active"));
    tab.classList.add("active");

    contents.forEach(c=>c.classList.remove("show"));
    document.getElementById(tab.dataset.tab).classList.add("show");
  }
})
