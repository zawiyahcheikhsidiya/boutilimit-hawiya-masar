
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>بوتلميت… هوية ومسار</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

<style>
:root{
  --green:#003e3d;
  --green2:#005b57;
  --green3:#07867f;
  --gold:#f4bf5d;
  --gold2:#ffd889;
  --cream:#f7f6f1;
  --white:#fff;
  --text:#10272a;
  --muted:#6f7b7d;
  --border:#dfe5e4;
  --shadow:0 12px 40px rgba(0,0,0,.12);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  font-family:"Cairo",sans-serif;
  background:#f5f7f6;
  color:var(--text);
}
button,input,textarea,select{
  font-family:"Cairo",sans-serif;
}
button{cursor:pointer}
a{text-decoration:none;color:inherit}
img{max-width:100%;display:block}

.topbar{
  position:sticky;
  top:0;
  z-index:100;
  height:76px;
  background:linear-gradient(90deg,#002f2f,#004b49);
  color:#fff;
  display:flex;
  align-items:center;
  padding:0 28px;
  border-bottom:1px solid rgba(255,255,255,.14);
}

.nav{
  width:100%;
  max-width:1600px;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:24px;
}

.brand{
  display:flex;
  align-items:center;
  gap:12px;
  min-width:230px;
}

.brand-icon{
  width:51px;
  height:51px;
  border:2px solid var(--gold);
  border-radius:14px;
  display:grid;
  place-items:center;
  font-size:28px;
  color:var(--gold);
}

.brand-title{
  line-height:1.1;
}
.brand-title strong{
  display:block;
  font-size:23px;
  font-weight:900;
}
.brand-title span{
  color:var(--gold);
  font-size:14px;
  font-weight:700;
}

.navlinks{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:28px;
  font-size:14px;
  font-weight:700;
  flex:1;
}
.navlinks a{
  opacity:.9;
  padding:27px 0 22px;
  border-bottom:3px solid transparent;
}
.navlinks a:hover,
.navlinks a.active{
  color:var(--gold);
  border-bottom-color:var(--gold);
}

.nav-tools{
  display:flex;
  align-items:center;
  gap:10px;
}

.search-box{
  width:230px;
  height:42px;
  border:1px solid rgba(255,255,255,.25);
  border-radius:22px;
  display:flex;
  align-items:center;
  padding:0 14px;
  background:rgba(255,255,255,.04);
}
.search-box input{
  width:100%;
  border:0;
  outline:0;
  color:#fff;
  background:transparent;
}
.search-box input::placeholder{color:#c8d5d4}

.hero{
  min-height:575px;
  position:relative;
  display:flex;
  align-items:center;
  overflow:hidden;
  background-position:center;
  background-size:cover;
}

.hero::before{
  content:"";
  position:absolute;
  inset:0;
  background:
    linear-gradient(90deg,rgba(0,31,32,.06) 0%,rgba(0,42,42,.17) 38%,rgba(0,40,40,.92) 100%),
    linear-gradient(0deg,rgba(0,49,47,.76),transparent 42%);
}

.hero-inner{
  width:100%;
  max-width:1600px;
  margin:auto;
  padding:70px 70px 200px;
  position:relative;
  z-index:2;
}

.hero-content{
  width:min(600px,90%);
  margin-right:auto;
  text-align:right;
  color:#fff;
}

.hero-kicker{
  color:var(--gold);
  font-weight:800;
  letter-spacing:2px;
  margin-bottom:8px;
}

.hero h1{
  font-size:74px;
  line-height:1;
  margin:0;
  font-weight:900;
}

.hero h1 span{
  display:block;
  color:var(--gold);
  font-size:43px;
  margin-top:14px;
}

.hero h2{
  font-size:25px;
  margin:25px 0 10px;
}

.hero p{
  line-height:2;
  font-size:17px;
  color:#e8f2f1;
}

.hero-btn{
  margin-top:22px;
  border:0;
  background:linear-gradient(90deg,var(--gold),var(--gold2));
  color:#173535;
  font-size:16px;
  font-weight:900;
  padding:14px 27px;
  border-radius:28px;
  box-shadow:0 7px 25px rgba(244,191,93,.28);
}

.categories-wrap{
  position:relative;
  z-index:5;
  max-width:1600px;
  padding:0 15px;
  margin:-185px auto 0;
}

.categories{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:10px;
}

.cat{
  min-height:220px;
  padding:19px;
  color:#fff;
  border-radius:10px;
  border:1px solid rgba(244,191,93,.72);
  overflow:hidden;
  position:relative;
  background:
    linear-gradient(0deg,rgba(0,42,42,.94),rgba(0,61,60,.64)),
    linear-gradient(135deg,#886238,#004d4a);
  box-shadow:0 8px 22px rgba(0,0,0,.18);
  transition:.25s;
}
.cat:hover{
  transform:translateY(-6px);
}
.cat-number{
  position:absolute;
  left:13px;
  top:13px;
  width:26px;
  height:26px;
  border-radius:50%;
  background:var(--gold);
  color:#163b3b;
  font-weight:900;
  display:grid;
  place-items:center;
}
.cat-icon{
  font-size:32px;
  color:var(--gold);
  margin-bottom:9px;
}
.cat h3{
  margin:2px 0 8px;
  font-size:17px;
}
.cat ul{
  margin:0;
  padding-right:18px;
  color:#e7eded;
  font-size:12px;
  line-height:1.9;
}
.cat-btn{
  position:absolute;
  bottom:13px;
  right:18px;
  left:18px;
  height:32px;
  border:0;
  border-radius:18px;
  background:#005c59;
  color:#fff;
  font-weight:800;
}

.content{
  max-width:1600px;
  margin:18px auto 0;
  padding:0 15px 50px;
  display:grid;
  grid-template-columns:1.1fr 3fr 1.1fr;
  gap:15px;
}

.panel{
  background:#fff;
  border:1px solid #e4e8e7;
  border-radius:13px;
  padding:17px;
  box-shadow:0 5px 20px rgba(0,0,0,.04);
}

.panel-title{
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:15px;
}
.panel-title h2{
  margin:0;
  font-size:21px;
}
.small-btn{
  background:var(--green);
  color:#fff;
  border:0;
  border-radius:17px;
  padding:5px 14px;
  font-weight:700;
}

.articles-grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.article-card{
  border-left:1px solid #e8eceb;
  padding-left:14px;
  cursor:pointer;
}
.article-card:last-child{border:0}
.article-img{
  height:140px;
  width:100%;
  object-fit:cover;
  border-radius:8px;
  background:#d6dfde;
}
.tag{
  display:inline-block;
  background:var(--gold);
  color:#22393a;
  padding:3px 11px;
  border-radius:15px;
  font-size:11px;
  font-weight:800;
  margin-top:-13px;
  position:relative;
  right:10px;
}
.article-card h3{
  font-size:18px;
  line-height:1.6;
  margin:8px 0 5px;
}
.article-card p{
  color:#6d787a;
  line-height:1.8;
  font-size:13px;
}
.meta{
  color:#98a2a4;
  font-size:11px;
  margin-top:8px;
}

.people-list{
  display:flex;
  flex-direction:column;
  gap:10px;
}
.person{
  display:flex;
  align-items:center;
  gap:10px;
  padding-bottom:9px;
  border-bottom:1px solid #edf0ef;
}
.person img{
  width:48px;
  height:48px;
  object-fit:cover;
  border-radius:7px;
  background:#eee;
}
.person strong{
  display:block;
  font-size:13px;
}
.person span{
  color:#7a8587;
  font-size:11px;
}

.video-main{
  position:relative;
  border-radius:9px;
  overflow:hidden;
  background:#ddd;
}
.video-main img{
  width:100%;
  height:145px;
  object-fit:cover;
}
.play{
  position:absolute;
  inset:0;
  margin:auto;
  width:47px;
  height:47px;
  border-radius:50%;
  border:0;
  background:#fff;
  color:var(--green);
  font-size:22px;
}
.video-list{
  margin-top:11px;
  display:flex;
  flex-direction:column;
  gap:10px;
}
.video-row{
  padding-bottom:8px;
  border-bottom:1px solid #edf0ef;
}
.video-row strong{
  display:block;
  font-size:12px;
}
.video-row span{
  font-size:10px;
  color:#8a9495;
}

.gallery-section{
  max-width:1600px;
  margin:0 auto 50px;
  padding:0 15px;
}
.gallery-grid{
  display:grid;
  grid-template-columns:2fr 1fr 1fr;
  grid-auto-rows:240px;
  gap:12px;
}
.gallery-grid img{
  width:100%;
  height:100%;
  object-fit:cover;
  border-radius:14px;
}
.gallery-grid img:first-child{
  grid-row:span 2;
}

.footer{
  background:#003936;
  color:#eaf3f2;
  padding:48px 30px 30px;
  text-align:center;
}
.footer h2{
  color:var(--gold);
  margin:0 0 7px;
}
.footer p{
  margin:4px;
  opacity:.8;
}
.footer-admin{
  margin-top:22px;
  border:1px solid rgba(255,255,255,.25);
  background:transparent;
  color:#fff;
  border-radius:22px;
  padding:8px 18px;
}

/* Article modal */
.modal{
  display:none;
  position:fixed;
  inset:0;
  z-index:500;
  background:rgba(0,0,0,.7);
  padding:25px;
  overflow:auto;
}
.modal.open{display:block}
.modal-box{
  width:min(850px,100%);
  margin:30px auto;
  background:#fff;
  border-radius:18px;
  padding:26px;
  position:relative;
}
.close{
  position:absolute;
  left:17px;
  top:15px;
  width:38px;
  height:38px;
  border:0;
  border-radius:50%;
  background:#f0f2f1;
  font-size:20px;
}
.modal-box img{
  width:100%;
  max-height:420px;
  object-fit:cover;
  border-radius:14px;
}
.modal-box h1{
  font-size:30px;
  line-height:1.5;
}
.article-body{
  line-height:2.2;
  font-size:16px;
}

/* Admin */
.admin-overlay{
  display:none;
  position:fixed;
  inset:0;
  z-index:1000;
  background:#f1f4f3;
  overflow:auto;
}
.admin-overlay.open{display:block}

.admin-head{
  background:var(--green);
  color:#fff;
  padding:18px 25px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  position:sticky;
  top:0;
  z-index:2;
}
.admin-head h2{margin:0}
.admin-head button{
  border:0;
  padding:9px 16px;
  border-radius:8px;
  background:#fff;
  color:var(--green);
  font-weight:800;
}

.admin-main{
  max-width:1200px;
  margin:25px auto;
  padding:0 15px;
}

.login-box{
  width:min(440px,95%);
  margin:100px auto;
  background:#fff;
  border-radius:18px;
  padding:30px;
  box-shadow:var(--shadow);
}
.login-box h2{text-align:center}
.field{
  margin-bottom:14px;
}
.field label{
  display:block;
  font-weight:800;
  margin-bottom:5px;
}
.field input,
.field textarea,
.field select{
  width:100%;
  border:1px solid #dce2e1;
  border-radius:9px;
  padding:11px 13px;
  outline:0;
  background:#fff;
}
.field textarea{
  min-height:120px;
  resize:vertical;
}

.primary{
  border:0;
  background:var(--green);
  color:#fff;
  padding:11px 18px;
  border-radius:9px;
  font-weight:800;
}
.danger{
  border:0;
  background:#a83636;
  color:#fff;
  padding:7px 12px;
  border-radius:7px;
}
.edit{
  border:0;
  background:#e7b34f;
  color:#143b3a;
  padding:7px 12px;
  border-radius:7px;
  font-weight:800;
}

.admin-tabs{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  margin-bottom:18px;
}
.admin-tabs button{
  border:1px solid #d7dfdd;
  background:#fff;
  border-radius:20px;
  padding:8px 18px;
  font-weight:800;
}
.admin-tabs button.active{
  background:var(--green);
  color:#fff;
}

.admin-section{
  display:none;
  background:#fff;
  border-radius:15px;
  padding:20px;
  box-shadow:0 5px 20px rgba(0,0,0,.05);
}
.admin-section.active{display:block}

.admin-grid{
  display:grid;
  grid-template-columns:1fr 1.3fr;
  gap:22px;
}
.admin-list-item{
  display:flex;
  justify-content:space-between;
  gap:12px;
  padding:10px 0;
  border-bottom:1px solid #ecefee;
}
.admin-actions{
  display:flex;
  gap:6px;
  align-items:center;
}

.empty{
  text-align:center;
  padding:35px;
  color:#879192;
}

.mobile-menu{
  display:none;
}

@media(max-width:1200px){
  .categories{
    grid-template-columns:repeat(4,1fr);
  }
  .categories-wrap{margin:-110px auto 0}
  .hero-inner{padding-bottom:140px}
  .content{
    grid-template-columns:1fr 2fr;
  }
  .people-panel{grid-column:1/3}
  .navlinks{display:none}
}

@media(max-width:760px){
  .topbar{height:auto;padding:12px 14px}
  .brand{min-width:0}
  .brand-title strong{font-size:17px}
  .brand-title span{font-size:11px}
  .brand-icon{width:42px;height:42px}
  .search-box{display:none}
  .hero{min-height:580px}
  .hero-inner{
    padding:65px 20px 240px;
  }
  .hero-content{
    width:100%;
  }
  .hero h1{font-size:48px}
  .hero h1 span{font-size:30px}
  .hero h2{font-size:20px}
  .hero p{font-size:14px}
  .categories-wrap{
    margin:-210px auto 0;
  }
  .categories{
    display:flex;
    overflow-x:auto;
    scroll-snap-type:x mandatory;
  }
  .cat{
    min-width:260px;
    scroll-snap-align:start;
  }
  .content{
    grid-template-columns:1fr;
  }
  .people-panel{grid-column:auto}
  .articles-grid{
    grid-template-columns:1fr;
  }
  .article-card{
    border:0;
    border-bottom:1px solid #e8eceb;
    padding-bottom:15px;
  }
  .gallery-grid{
    grid-template-columns:1fr 1fr;
    grid-auto-rows:170px;
  }
  .gallery-grid img:first-child{
    grid-column:1/3;
    grid-row:auto;
  }
  .admin-grid{
    grid-template-columns:1fr;
  }
}

</style>
</head>

<body>

<header class="topbar">
  <div class="nav">

    <div class="brand">
      <div class="brand-icon">⌂</div>
      <div class="brand-title">
        <strong>بوتلميت</strong>
        <span>هوية ومسار</span>
      </div>
    </div>

    <nav class="navlinks">
      <a class="active" href="#home">الرئيسية</a>
      <a href="#about">عن الموقع</a>
      <a href="#articles">المقالات</a>
      <a href="#gallery">الصور والوثائق</a>
      <a href="#videos">الفيديوهات</a>
      <a href="#contact">تواصل معنا</a>
    </nav>

    <div class="nav-tools">
      <div class="search-box">
        🔎
        <input id="searchInput" placeholder="ابحث في الموقع...">
      </div>
    </div>

  </div>
</header>

<section class="hero" id="home">
  <div class="hero-inner">
    <div class="hero-content">
      <div class="hero-kicker">ذاكرة مدينة ومسار وطن</div>
      <h1>
        بوتلميت
        <span id="heroSecondTitle">هوية ومسار</span>
      </h1>

      <h2 id="heroHeading">مدينة العلم والتاريخ والثقافة</h2>

      <p id="heroText">
        نافذة معرفية توثق تاريخ بوتلميت، وتبرز حاضرها،
        وتستشرف مستقبلها في مسار يجمع بين الأصالة والتنمية.
      </p>

      <button class="hero-btn" onclick="document.getElementById('articles').scrollIntoView()">
        استكشف المزيد ←
      </button>
    </div>
  </div>
</section>

<div class="categories-wrap">
  <div class="categories">

    <article class="cat">
      <span class="cat-number">1</span>
      <div class="cat-icon">🏛</div>
      <h3>التاريخ والذاكرة</h3>
      <ul>
        <li>نشأة المدينة</li>
        <li>مسارها عبر القرون</li>
        <li>أعلام بوتلميت</li>
      </ul>
      <button class="cat-btn" onclick="filterCategory('التاريخ والذاكرة')">دخول ←</button>
    </article>

    <article class="cat">
      <span class="cat-number">2</span>
      <div class="cat-icon">📖</div>
      <h3>الحياة الثقافية</h3>
      <ul>
        <li>المحاظر ودورها</li>
        <li>الشعراء والكتاب</li>
        <li>المخطوطات والنوادر</li>
      </ul>
      <button class="cat-btn" onclick="filterCategory('الحياة الثقافية')">دخول ←</button>
    </article>

    <article class="cat">
      <span class="cat-number">3</span>
      <div class="cat-icon">👥</div>
      <h3>المجتمع والتحولات</h3>
      <ul>
        <li>العادات والتقاليد</li>
        <li>التحولات الاجتماعية</li>
        <li>شهادات الأهالي</li>
      </ul>
      <button class="cat-btn" onclick="filterCategory('المجتمع والتحولات')">دخول ←</button>
    </article>

    <article class="cat">
      <span class="cat-number">4</span>
      <div class="cat-icon">🇲🇷</div>
      <h3>السياسة والمسار الوطني</h3>
      <ul>
        <li>دور بوتلميت الوطني</li>
        <li>الشخصيات الوطنية</li>
        <li>الوحدة الوطنية</li>
      </ul>
      <button class="cat-btn" onclick="filterCategory('السياسة والمسار الوطني')">دخول ←</button>
    </article>

    <article class="cat">
      <span class="cat-number">5</span>
      <div class="cat-icon">⚙️</div>
      <h3>التنمية والواقع المعاصر</h3>
      <ul>
        <li>التعليم والصحة</li>
        <li>الشباب والبطالة</li>
        <li>الاستثمار والمشاريع</li>
      </ul>
      <button class="cat-btn" onclick="filterCategory('التنمية والواقع المعاصر')">دخول ←</button>
    </article>

    <article class="cat">
      <span class="cat-number">6</span>
      <div class="cat-icon">💡</div>
      <h3>الحلول والرؤى المستقبلية</h3>
      <ul>
        <li>مقترحات تنموية</li>
        <li>مشاريع قابلة للتنفيذ</li>
        <li>مستقبل المدينة</li>
      </ul>
      <button class="cat-btn" onclick="filterCategory('الحلول والرؤى المستقبلية')">دخول ←</button>
    </article>

    <article class="cat">
      <span class="cat-number">7</span>
      <div class="cat-icon">🖼</div>
      <h3>الصور والوثائق</h3>
      <ul>
        <li>صور قديمة وحديثة</li>
        <li>خرائط ووثائق</li>
        <li>شهادات ومقتنيات</li>
      </ul>
      <button class="cat-btn" onclick="document.getElementById('gallery').scrollIntoView()">دخول ←</button>
    </article>

  </div>
</div>

<main class="content" id="articles">

  <section class="panel video-panel" id="videos">
    <div class="panel-title">
      <h2>أحدث الفيديوهات</h2>
    </div>
    <div id="videosBox"></div>
  </section>

  <section class="panel">
    <div class="panel-title">
      <h2 id="articlesTitle">أحدث المقالات</h2>
      <button class="small-btn" onclick="renderArticles()">عرض الكل</button>
    </div>

    <div class="articles-grid" id="articlesGrid"></div>
  </section>

  <section class="panel people-panel">
    <div class="panel-title">
      <h2>أبرز الشخصيات</h2>
    </div>
    <div class="people-list" id="peopleList"></div>
  </section>

</main>

<section class="gallery-section" id="gallery">
  <div class="panel">
    <div class="panel-title">
      <h2>الصور والوثائق</h2>
    </div>

    <div class="gallery-grid" id="galleryGrid">
      <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=1200" alt="">
      <img src="https://images.unsplash.com/photo-1489493512598-d08130f49bea?w=700" alt="">
      <img src="https://images.unsplash.com/photo-1526778548025-fa2f459cd5c1?w=700" alt="">
      <img src="https://images.unsplash.com/photo-1452421822248-d4c2b47f0c81?w=700" alt="">
      <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=700" alt="">
    </div>
  </div>
</section>

<footer class="footer" id="contact">
  <h2>بوتلميت… هوية ومسار</h2>
  <p>مشروع رقمي لتوثيق ذاكرة المدينة ومسارها العلمي والثقافي والاجتماعي.</p>
  <p>جميع الحقوق محفوظة © 2026</p>

  <button class="footer-admin" onclick="openAdmin()">
    لوحة التحكم
  </button>
</footer>

<!-- Article modal -->
<div class="modal" id="articleModal">
  <div class="modal-box">
    <button class="close" onclick="closeArticle()">×</button>
    <div id="articleModalContent"></div>
  </div>
</div>

<!-- Admin -->
<div class="admin-overlay" id="adminOverlay">

  <div id="loginView" class="login-box">
    <h2>لوحة تحكم بوتلميت</h2>

    <div class="field">
      <label>كلمة المرور</label>
      <input type="password" id="adminPasswordInput" placeholder="أدخل كلمة المرور">
    </div>

    <button class="primary" style="width:100%" onclick="adminLogin()">
      دخول
    </button>

    <button style="width:100%;margin-top:10px;border:0;background:#eee;padding:10px;border-radius:8px"
      onclick="closeAdmin()">
      رجوع للموقع
    </button>
  </div>

  <div id="dashboardView" style="display:none">

    <div class="admin-head">
      <h2>لوحة التحكم</h2>
      <button onclick="closeAdmin()">عرض الموقع</button>
    </div>

    <div class="admin-main">

      <div class="admin-tabs">
        <button class="active" onclick="openAdminTab('articlesAdmin',this)">المقالات</button>
        <button onclick="openAdminTab('videosAdmin',this)">الفيديوهات</button>
        <button onclick="openAdminTab('peopleAdmin',this)">الشخصيات</button>
        <button onclick="openAdminTab('settingsAdmin',this)">إعدادات الموقع</button>
      </div>

      <!-- Articles -->
      <section class="admin-section active" id="articlesAdmin">

        <div class="admin-grid">

          <div>
            <h3>إضافة أو تعديل مقال</h3>

            <input type="hidden" id="articleId">

            <div class="field">
              <label>عنوان المقال</label>
              <input id="articleTitleInput">
            </div>

            <div class="field">
              <label>القسم</label>
              <select id="articleCategoryInput">
                <option>التاريخ والذاكرة</option>
                <option>الحياة الثقافية</option>
                <option>المجتمع والتحولات</option>
                <option>السياسة والمسار الوطني</option>
                <option>التنمية والواقع المعاصر</option>
                <option>الحلول والرؤى المستقبلية</option>
                <option>الصور والوثائق</option>
              </select>
            </div>

            <div class="field">
              <label>ملخص المقال</label>
              <textarea id="articleExcerptInput"></textarea>
            </div>

            <div class="field">
              <label>نص المقال كاملا</label>
              <textarea id="articleBodyInput" style="min-height:220px"></textarea>
            </div>

            <div class="field">
              <label>رابط صورة الغلاف</label>
              <input id="articleImageInput" placeholder="https://...">
            </div>

            <div class="field">
              <label>أو اختر صورة من جهازك</label>
              <input type="file" id="articleImageFile" accept="image/*">
            </div>

            <button class="primary" onclick="saveArticle()">
              حفظ المقال
            </button>

            <button onclick="resetArticleForm()"
              style="border:0;background:#e8eceb;padding:11px 18px;border-radius:9px">
              مقال جديد
            </button>

          </div>

          <div>
            <h3>المقالات الموجودة</h3>
            <div id="adminArticlesList"></div>
          </div>

        </div>

      </section>

      <!-- Videos -->
      <section class="admin-section" id="videosAdmin">
        <div class="admin-grid">

          <div>
            <h3>إضافة فيديو</h3>

            <div class="field">
              <label>عنوان الفيديو</label>
              <input id="videoTitleInput">
            </div>

            <div class="field">
              <label>رابط الفيديو</label>
              <input id="videoUrlInput" placeholder="https://youtube.com/...">
            </div>

            <div class="field">
              <label>صورة الفيديو</label>
              <input id="videoImageInput" placeholder="https://...">
            </div>

            <button class="primary" onclick="addVideo()">إضافة الفيديو</button>
          </div>

          <div>
            <h3>الفيديوهات</h3>
            <div id="adminVideosList"></div>
          </div>

        </div>
      </section>

      <!-- People -->
      <section class="admin-section" id="peopleAdmin">
        <div class="admin-grid">

          <div>
            <h3>إضافة شخصية</h3>

            <div class="field">
              <label>الاسم</label>
              <input id="personNameInput">
            </div>

            <div class="field">
              <label>الصفة</label>
              <input id="personRoleInput">
            </div>

            <div class="field">
              <label>الصورة</label>
              <input id="personImageInput" placeholder="https://...">
            </div>

            <button class="primary" onclick="addPerson()">إضافة الشخصية</button>
          </div>

          <div>
            <h3>الشخصيات</h3>
            <div id="adminPeopleList"></div>
          </div>

        </div>
      </section>

      <!-- Settings -->
      <section class="admin-section" id="settingsAdmin">

        <h3>إعدادات الواجهة</h3>

        <div class="field">
          <label>عنوان الواجهة</label>
          <input id="settingHeading">
        </div>

        <div class="field">
          <label>وصف الواجهة</label>
          <textarea id="settingDescription"></textarea>
        </div>

        <div class="field">
          <label>رابط صورة مدينة بوتلميت في الواجهة</label>
          <input id="settingHeroImage" placeholder="https://...">
        </div>

        <div class="field">
          <label>أو اختر صورة من الجهاز</label>
          <input type="file" id="settingHeroFile" accept="image/*">
        </div>

        <button class="primary" onclick="saveSettings()">حفظ الإعدادات</button>

        <hr style="margin:30px 0;border:0;border-top:1px solid #ddd">

        <h3>نسخة احتياطية</h3>

        <button class="primary" onclick="exportData()">
          تنزيل نسخة من المحتوى
        </button>

        <label class="primary" style="display:inline-block">
          استعادة نسخة
          <input type="file" id="importDataFile" accept=".json" hidden onchange="importData(event)">
        </label>

      </section>

    </div>
  </div>
</div>

<script>

/* ==========================
   البيانات الافتراضية
========================== */

const DEFAULT_DATA = {

  settings:{
    heading:"مدينة العلم والتاريخ والثقافة",
    description:"نافذة معرفية توثق تاريخ بوتلميت، وتبرز حاضرها، وتستشرف مستقبلها في مسار يجمع بين الأصالة والتنمية.",
    heroImage:"https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=2000"
  },

  articles:[
    {
      id:1,
      title:"نشأة بوتلميت ومسارها عبر القرون",
      category:"التاريخ والذاكرة",
      excerpt:"تعد مدينة بوتلميت من المدن الموريتانية ذات الحضور العلمي والتاريخي البارز.",
      body:"تحتل بوتلميت مكانة بارزة في الذاكرة الموريتانية، بما عرفته من حركة علمية وثقافية، وبما احتضنته من محاظر وعلماء وشخصيات كان لها حضور في تاريخ البلاد.\n\nيهدف هذا الركن إلى جمع الروايات والوثائق والمصادر المتعلقة بتاريخ المدينة، وتقديمها بصورة موثقة ومنظمة للأجيال القادمة.",
      image:"https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=900",
      date:"2026-09-30"
    },
    {
      id:2,
      title:"المحاظر في بوتلميت ودورها في الهوية العلمية",
      category:"الحياة الثقافية",
      excerpt:"كانت المحاظر من أهم المنارات العلمية التي أسهمت في تخريج أجيال من العلماء والفقهاء.",
      body:"شكّلت المحاظر في بوتلميت أحد أبرز روافد التعليم التقليدي في موريتانيا، وأسهمت في حفظ العلوم الشرعية والعربية ونقلها بين الأجيال.\n\nوسيعمل الموقع على توثيق تاريخ هذه المحاظر وشيوخها ومناهجها العلمية.",
      image:"https://images.unsplash.com/photo-1481627834876-b7833e8f5570?w=900",
      date:"2026-09-29"
    },
    {
      id:3,
      title:"واقع التعليم في بوتلميت بين التحديات والطموح",
      category:"التنمية والواقع المعاصر",
      excerpt:"قراءة في واقع التعليم وحاجات المؤسسات التعليمية وآفاق تطويرها.",
      body:"يظل التعليم من أهم محاور التنمية المحلية، ويحتاج إلى رؤية شاملة تجمع بين تحسين البنى التحتية، ودعم الكادر التعليمي، وتشجيع المبادرات المجتمعية.",
      image:"https://images.unsplash.com/photo-1523050854058-8df90110c9f1?w=900",
      date:"2026-09-28"
    }
  ],

  people:[
    {
      id:1,
      name:"الشيخ سيديا الكبير",
      role:"عالم من أعلام بوتلميت",
      image:"https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=300"
    },
    {
      id:2,
      name:"علماء بوتلميت",
      role:"ذاكرة علمية وثقافية",
      image:"https://images.unsplash.com/photo-1560250097-0b93528c311a?w=300"
    },
    {
      id:3,
      name:"أدباء المدينة",
      role:"شعر وأدب وفكر",
      image:"https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=300"
    }
  ],

  videos:[
    {
      id:1,
      title:"جولة في مدينة بوتلميت",
      url:"#",
      image:"https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=700"
    },
    {
      id:2,
      title:"شهادات من ذاكرة الأهالي",
      url:"#",
      image:""
    },
    {
      id:3,
      title:"تاريخ المحاظر في بوتلميت",
      url:"#",
      image:""
    }
  ]
};


/* ==========================
   التخزين
========================== */

function loadData(){
  const saved = localStorage.getItem("boutilimit_site_data");

  if(saved){
    try{
      return JSON.parse(saved);
    }catch(e){}
  }

  localStorage.setItem(
    "boutilimit_site_data",
    JSON.stringify(DEFAULT_DATA)
  );

  return JSON.parse(JSON.stringify(DEFAULT_DATA));
}

let DATA = loadData();

function saveData(){
  localStorage.setItem(
    "boutilimit_site_data",
    JSON.stringify(DATA)
  );

  renderEverything();
}


/* ==========================
   المساعدة
========================== */

function escapeHtml(value=""){
  return String(value)
    .replaceAll("&","&amp;")
    .replaceAll("<","&lt;")
    .replaceAll(">","&gt;")
    .replaceAll('"',"&quot;");
}

function nl2br(value=""){
  return escapeHtml(value).replace(/\n/g,"<br>");
}

function fileToBase64(file){
  return new Promise((resolve,reject)=>{
    const reader = new FileReader();

    reader.onload = ()=>resolve(reader.result);
    reader.onerror = reject;

    reader.readAsDataURL(file);
  });
}


/* ==========================
   واجهة الموقع
========================== */

function renderSettings(){

  document.getElementById("heroHeading").textContent =
    DATA.settings.heading;

  document.getElementById("heroText").textContent =
    DATA.settings.description;

  document.querySelector(".hero").style.backgroundImage =
    `url("${DATA.settings.heroImage}")`;
}


function renderArticles(list = DATA.articles){

  const box = document.getElementById("articlesGrid");

  if(!list.length){
    box.innerHTML =
      `<div class="empty">لا توجد مقالات</div>`;
    return;
  }

  box.innerHTML = list
    .slice()
    .reverse()
    .slice(0,6)
    .map(article=>`

      <article class="article-card"
        onclick="openArticle(${article.id})">

        <img class="article-img"
          src="${escapeHtml(article.image || "")}"
          onerror="this.src='https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=900'">

        <span class="tag">
          ${escapeHtml(article.category)}
        </span>

        <h3>
          ${escapeHtml(article.title)}
        </h3>

        <p>
          ${escapeHtml(article.excerpt)}
        </p>

        <div class="meta">
          ${escapeHtml(article.date || "")}
        </div>

      </article>

    `).join("");
}


function filterCategory(category){

  const filtered = DATA.articles.filter(
    a => a.category === category
  );

  document.getElementById("articlesTitle").textContent =
    category;

  renderArticles(filtered);

  document.getElementById("articles")
    .scrollIntoView({behavior:"smooth"});
}


function openArticle(id){

  const article = DATA.articles.find(
    a => Number(a.id) === Number(id)
  );

  if(!article) return;

  document.getElementById("articleModalContent").innerHTML = `

    <img
      src="${escapeHtml(article.image || "")}"
      onerror="this.style.display='none'">

    <div style="margin-top:16px">
      <span class="tag">
        ${escapeHtml(article.category)}
      </span>
    </div>

    <h1>
      ${escapeHtml(article.title)}
    </h1>

    <div class="meta">
      ${escapeHtml(article.date || "")}
    </div>

    <div class="article-body">
      ${nl2br(article.body)}
    </div>
  `;

  document.getElementById("articleModal")
    .classList.add("open");
}


function closeArticle(){
  document.getElementById("articleModal")
    .classList.remove("open");
}


function renderPeople(){

  const box = document.getElementById("peopleList");

  box.innerHTML = DATA.people.map(person=>`

    <div class="person">

      <img
        src="${escapeHtml(person.image || "")}"
        onerror="this.src='https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=300'">

      <div>
        <strong>
          ${escapeHtml(person.name)}
        </strong>

        <span>
          ${escapeHtml(person.role)}
        </span>
      </div>

    </div>

  `).join("");
}


function renderVideos(){

  const box = document.getElementById("videosBox");

  if(!DATA.videos.length){
    box.innerHTML =
      `<div class="empty">لا توجد فيديوهات</div>`;
    return;
  }

  const first = DATA.videos[0];

  box.innerHTML = `

    <div class="video-main">

      <img src="${escapeHtml(first.image || "https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=700")}">

      <button class="play"
        onclick="openVideo('${escapeHtml(first.url)}')">
        ▶
      </button>

    </div>

    <strong style="display:block;margin-top:9px">
      ${escapeHtml(first.title)}
    </strong>

    <div class="video-list">

      ${DATA.videos.slice(1).map(video=>`

        <div class="video-row"
          onclick="openVideo('${escapeHtml(video.url)}')"
          style="cursor:pointer">

          <strong>
            ${escapeHtml(video.title)}
          </strong>

          <span>
            مشاهدة الفيديو
          </span>

        </div>

      `).join("")}

    </div>
  `;
}


function openVideo(url){

  if(!url || url === "#"){
    alert("يمكنك إضافة رابط الفيديو من لوحة التحكم.");
    return;
  }

  window.open(url,"_blank");
}


function renderEverything(){
  renderSettings();
  renderArticles();
  renderPeople();
  renderVideos();
  renderAdminLists();
}


renderEverything();


/* ==========================
   البحث
========================== */

document.getElementById("searchInput")
.addEventListener("input",function(){

  const value = this.value.trim().toLowerCase();

  if(!value){
    document.getElementById("articlesTitle").textContent =
      "أحدث المقالات";

    renderArticles();
    return;
  }

  const filtered = DATA.articles.filter(article=>
    article.title.toLowerCase().includes(value) ||
    article.excerpt.toLowerCase().includes(value) ||
    article.body.toLowerCase().includes(value) ||
    article.category.toLowerCase().includes(value)
  );

  document.getElementById("articlesTitle").textContent =
    "نتائج البحث";

  renderArticles(filtered);
});


/* ==========================
   لوحة التحكم
========================== */

function openAdmin(){

  document.getElementById("adminOverlay")
    .classList.add("open");

  document.body.style.overflow="hidden";
}


function closeAdmin(){

  document.getElementById("adminOverlay")
    .classList.remove("open");

  document.body.style.overflow="";
}


function adminLogin(){

  const password =
    document.getElementById("adminPasswordInput").value;

  const savedPassword =
    localStorage.getItem("boutilimit_admin_password")
    || "2026";

  if(password !== savedPassword){

    alert("كلمة المرور غير صحيحة");
    return;
  }

  document.getElementById("loginView").style.display="none";
  document.getElementById("dashboardView").style.display="block";

  renderAdminLists();
}


function openAdminTab(id,button){

  document.querySelectorAll(".admin-section")
    .forEach(el=>el.classList.remove("active"));

  document.getElementById(id)
    .classList.add("active");

  document.querySelectorAll(".admin-tabs button")
    .forEach(el=>el.classList.remove("active"));

  button.classList.add("active");
}


/* ==========================
   إدارة المقالات
========================== */

async function saveArticle(){

  const id =
    document.getElementById("articleId").value;

  const title =
    document.getElementById("articleTitleInput").value.trim();

  if(!title){
    alert("اكتب عنوان المقال");
    return;
  }

  let image =
    document.getElementById("articleImageInput").value.trim();

  const file =
    document.getElementById("articleImageFile").files[0];

  if(file){
    image = await fileToBase64(file);
  }

  const article = {

    id: id
      ? Number(id)
      : Date.now(),

    title,

    category:
      document.getElementById("articleCategoryInput").value,

    excerpt:
      document.getElementById("articleExcerptInput").value,

    body:
      document.getElementById("articleBodyInput").value,

    image,

    date:
      new Date().toISOString().slice(0,10)
  };

  if(id){

    const index = DATA.articles.findIndex(
      a=>Number(a.id)===Number(id)
    );

    if(index !== -1)
      DATA.articles[index] = article;

  }else{

    DATA.articles.push(article);
  }

  saveData();
  resetArticleForm();

  alert("تم حفظ المقال بنجاح");
}


function editArticle(id){

  const article = DATA.articles.find(
    a=>Number(a.id)===Number(id)
  );

  if(!article) return;

  document.getElementById("articleId").value =
    article.id;

  document.getElementById("articleTitleInput").value =
    article.title;

  document.getElementById("articleCategoryInput").value =
    article.category;

  document.getElementById("articleExcerptInput").value =
    article.excerpt;

  document.getElementById("articleBodyInput").value =
    article.body;

  document.getElementById("articleImageInput").value =
    article.image && !article.image.startsWith("data:")
      ? article.image
      : "";

  window.scrollTo({top:0,behavior:"smooth"});
}


function deleteArticle(id){

  if(!confirm("هل تريد حذف هذا المقال؟"))
    return;

  DATA.articles = DATA.articles.filter(
    a=>Number(a.id)!==Number(id)
  );

  saveData();
}


function resetArticleForm(){

  [
    "articleId",
    "articleTitleInput",
    "articleExcerptInput",
    "articleBodyInput",
    "articleImageInput"
  ].forEach(id=>
    document.getElementById(id).value=""
  );

  document.getElementById("articleImageFile").value="";
}


/* ==========================
   الفيديوهات
========================== */

function addVideo(){

  const title =
    document.getElementById("videoTitleInput").value.trim();

  if(!title){
    alert("اكتب عنوان الفيديو");
    return;
  }

  DATA.videos.push({

    id:Date.now(),

    title,

    url:
      document.getElementById("videoUrlInput").value.trim(),

    image:
      document.getElementById("videoImageInput").value.trim()
  });

  saveData();

  document.getElementById("videoTitleInput").value="";
  document.getElementById("videoUrlInput").value="";
  document.getElementById("videoImageInput").value="";
}


function deleteVideo(id){

  if(!confirm("حذف الفيديو؟"))
    return;

  DATA.videos = DATA.videos.filter(
    v=>Number(v.id)!==Number(id)
  );

  saveData();
}


/* ==========================
   الشخصيات
========================== */

function addPerson(){

  const name =
    document.getElementById("personNameInput").value.trim();

  if(!name){
    alert("اكتب اسم الشخصية");
    return;
  }

  DATA.people.push({

    id:Date.now(),

    name,

    role:
      document.getElementById("personRoleInput").value.trim(),

    image:
      document.getElementById("personImageInput").value.trim()
  });

  saveData();

  document.getElementById("personNameInput").value="";
  document.getElementById("personRoleInput").value="";
  document.getElementById("personImageInput").value="";
}


function deletePerson(id){

  if(!confirm("حذف الشخصية؟"))
    return;

  DATA.people = DATA.people.filter(
    p=>Number(p.id)!==Number(id)
  );

  saveData();
}


/* ==========================
   إعدادات الموقع
========================== */

async function saveSettings(){

  DATA.settings.heading =
    document.getElementById("settingHeading").value.trim();

  DATA.settings.description =
    document.getElementById("settingDescription").value.trim();

  let hero =
    document.getElementById("settingHeroImage").value.trim();

  const file =
    document.getElementById("settingHeroFile").files[0];

  if(file){
    hero = await fileToBase64(file);
  }

  if(hero)
    DATA.settings.heroImage = hero;

  saveData();

  alert("تم حفظ إعدادات الموقع");
}


/* ==========================
   قوائم لوحة التحكم
========================== */

function renderAdminLists(){

  const articlesList =
    document.getElementById("adminArticlesList");

  if(articlesList){

    articlesList.innerHTML =
      DATA.articles.length

      ? DATA.articles.slice().reverse().map(a=>`

        <div class="admin-list-item">

          <div>
            <strong>${escapeHtml(a.title)}</strong>
            <div style="font-size:11px;color:#888">
              ${escapeHtml(a.category)}
            </div>
          </div>

          <div class="admin-actions">

            <button class="edit"
              onclick="editArticle(${a.id})">
              تعديل
            </button>

            <button class="danger"
              onclick="deleteArticle(${a.id})">
              حذف
            </button>

          </div>

        </div>

      `).join("")

      : `<div class="empty">لا توجد مقالات</div>`;
  }


  const videosList =
    document.getElementById("adminVideosList");

  if(videosList){

    videosList.innerHTML =
      DATA.videos.map(v=>`

        <div class="admin-list-item">

          <strong>
            ${escapeHtml(v.title)}
          </strong>

          <button class="danger"
            onclick="deleteVideo(${v.id})">
            حذف
          </button>

        </div>

      `).join("");
  }


  const peopleList =
    document.getElementById("adminPeopleList");

  if(peopleList){

    peopleList.innerHTML =
      DATA.people.map(p=>`

        <div class="admin-list-item">

          <div>
            <strong>
              ${escapeHtml(p.name)}
            </strong>

            <div style="font-size:11px;color:#888">
              ${escapeHtml(p.role)}
            </div>
          </div>

          <button class="danger"
            onclick="deletePerson(${p.id})">
            حذف
          </button>

        </div>

      `).join("");
  }


  const heading =
    document.getElementById("settingHeading");

  if(heading){

    heading.value =
      DATA.settings.heading;

    document.getElementById("settingDescription").value =
      DATA.settings.description;

    document.getElementById("settingHeroImage").value =
      DATA.settings.heroImage.startsWith("data:")
        ? ""
        : DATA.settings.heroImage;
  }
}


/* ==========================
   النسخ الاحتياطي
========================== */

function exportData(){

  const text =
    JSON.stringify(DATA,null,2);

  const blob =
    new Blob([text],{
      type:"application/json"
    });

  const url =
    URL.createObjectURL(blob);

  const a =
    document.createElement("a");

  a.href=url;
  a.download="boutilimit-backup.json";

  a.click();

  URL.revokeObjectURL(url);
}


function importData(event){

  const file =
    event.target.files[0];

  if(!file)
    return;

  const reader =
    new FileReader();

  reader.onload=function(){

    try{

      const imported =
        JSON.parse(reader.result);

      if(!imported.articles ||
         !imported.settings){

        throw new Error();
      }

      DATA=imported;

      saveData();

      alert("تمت استعادة النسخة بنجاح");

    }catch(e){

      alert("الملف غير صالح");
    }
  };

  reader.readAsText(file);
}


/* إغلاق النوافذ */

document.getElementById("articleModal")
.addEventListener("click",function(e){

  if(e.target===this)
    closeArticle();
});

</script>

</body>
</html>
