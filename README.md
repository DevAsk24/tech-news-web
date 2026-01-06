<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>أخبار التقنية</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    *{
      box-sizing:border-box;
      font-family: Tahoma, Arial;
    }
    body{
      margin:0;
      background:#f4f6f8;
      color:#333;
    }
    header{
      background:#0d6efd;
      color:#fff;
      padding:20px;
      text-align:center;
    }
    nav{
      background:#fff;
      padding:10px;
      display:flex;
      justify-content:center;
      gap:10px;
      box-shadow:0 2px 5px rgba(0,0,0,.1);
    }
    nav button{
      border:none;
      background:#0d6efd;
      color:#fff;
      padding:8px 16px;
      border-radius:20px;
      cursor:pointer;
    }
    nav button:hover{
      background:#084298;
    }
    main{
      max-width:1000px;
      margin:30px auto;
      padding:0 15px;
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:20px;
    }
    article{
      background:#fff;
      padding:20px;
      border-radius:12px;
      box-shadow:0 4px 10px rgba(0,0,0,.08);
    }
    article h2{
      margin-top:0;
      color:#0d6efd;
    }
    .tag{
      display:inline-block;
      margin-top:10px;
      background:#e9f2ff;
      color:#0d6efd;
      padding:4px 10px;
      border-radius:12px;
      font-size:12px;
    }
    footer{
      text-align:center;
      padding:15px;
      background:#fff;
      margin-top:40px;
      font-size:13px;
    }
  </style>
</head>
<body>

<header>
  <h1>📰 أخبار التقنية</h1>
  <p>تعلم تطوير الويب بـ HTML و CSS و JavaScript</p>
</header>

<nav>
  <button onclick="filter('all')">الكل</button>
  <button onclick="filter('html')">HTML</button>
  <button onclick="filter('css')">CSS</button>
  <button onclick="filter('js')">JavaScript</button>
</nav>

<main>
  <article data-cat="html">
    <h2>شنو الجديد فـ HTML5؟</h2>
    <p>HTML5 سهلات بناء الصفحات باستعمال عناصر منظمة وسهلة القراءة.</p>
    <span class="tag">HTML</span>
  </article>

  <article data-cat="css">
    <h2>Flexbox و Grid</h2>
    <p>أقوى تقنيات CSS لبناء تصميم متجاوب واحترافي.</p>
    <span class="tag">CSS</span>
  </article>

  <article data-cat="js">
    <h2>قوة JavaScript</h2>
    <p>JavaScript كتخلي الموقع تفاعلي وذكي.</p>
    <span class="tag">JavaScript</span>
  </article>
</main>

<footer>
  © 2026 - Tech News Web | HTML + CSS + JS
</footer>

<script>
function filter(cat){
  document.querySelectorAll("article").forEach(a=>{
    a.style.display = (cat==="all" || a.dataset.cat===cat)
      ? "block" : "none";
  });
}
</script>

</body>
</html>

