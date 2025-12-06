#TEMPLATE

<html lang="ru">


<head>


<meta charset="utf-8" />


<meta name="viewport" content="width=device-width,initial-scale=1" />


<title>Портфолио — Твоё Имя</title>


<meta name="description" content="Красивое и стильное портфолио — HTML + CSS в одном файле." />


<style>


  :root{


    --bg:#0f1724;


    --card:#0b1220c9;


    --glass: rgba(255,255,255,0.06);


    --accent1: linear-gradient(135deg,#7c3aed,#06b6d4);


    --accent2: linear-gradient(135deg,#06b6d4,#7c3aed);


    --muted: #95a0b5;


    --glass-border: rgba(255,255,255,0.06);


    --glass-strong: rgba(255,255,255,0.08);


    --glass-hover: rgba(255,255,255,0.10);


    --radius: 16px;


    font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;


  }





  /* reset-ish */


  *{box-sizing:border-box}


  html,body{height:100%}


  body{


    margin:0;


    background:


      radial-gradient(800px 400px at 10% 10%, rgba(124,58,237,0.12), transparent 10%),


      radial-gradient(600px 300px at 90% 90%, rgba(6,182,212,0.08), transparent 10%),


      var(--bg);


    color:#e6eef8;


    -webkit-font-smoothing:antialiased;


    -moz-osx-font-smoothing:grayscale;


    line-height:1.4;


    padding:40px 20px;


    display:flex;


    justify-content:center;


    align-items:flex-start;


    gap:20px;


  }





  .wrap{


    width:100%;


    max-width:1100px;


  }





  header{


    display:flex;


    align-items:center;


    justify-content:space-between;


    gap:16px;


    margin-bottom:22px;


  }





  .brand{


    display:flex;


    align-items:center;


    gap:12px;


  }





  .logo{


    width:56px;


    height:56px;


    border-radius:12px;


    background:var(--accent1);


    display:grid;


    place-items:center;


    box-shadow:0 6px 30px rgba(7,12,20,0.6);


    font-weight:700;


    font-size:20px;


    transform:rotate(-6deg);


  }





  nav{display:flex; gap:12px; align-items:center;}





  .nav-btn{


    background:transparent;


    border:1px solid transparent;


    padding:8px 12px;


    border-radius:10px;


    color:var(--muted);


    font-size:14px;


    cursor:pointer;


  }





  .nav-btn:hover{


    color:#fff;


    border-color:var(--glass-border);


    background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));


  }





  main{


    display:grid;


    grid-template-columns: 360px 1fr;


    gap:22px;


    align-items:start;


  }





  /* left column (profile) */


  .card{


    background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));


    border-radius:var(--radius);


    padding:20px;


    backdrop-filter: blur(8px) saturate(110%);


    border: 1px solid var(--glass-border);


    box-shadow: 0 8px 30px rgba(2,6,23,0.6);


  }





  .profile{


    display:flex;


    gap:14px;


    align-items:center;


  }





  .avatar{


    width:86px;


    height:86px;


    border-radius:14px;


    overflow:hidden;


    flex-shrink:0;


    box-shadow: 0 6px 20px rgba(7,12,20,0.6), inset 0 -6px 20px rgba(255,255,255,0.02);


    background:linear-gradient(180deg,#0f1724,#071024);


    display:grid;


    place-items:center;


    font-weight:700;


    font-size:30px;


    color:#fff;


  }





  h1{margin:0;font-size:20px}


  .role{color:var(--muted);font-size:13px;margin-top:6px}





  .bio{


    margin-top:14px;


    color: #dce9ff;


    font-size:14px;


  }





  .skill-list{


    display:flex;


    flex-wrap:wrap;


    gap:8px;


    margin-top:14px;


  }





  .skill{


    padding:8px 10px;


    border-radius:999px;


    font-size:13px;


    color:var(--muted);


    background: linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));


    border:1px solid rgba(255,255,255,0.02);


  }





  .contact{


    margin-top:16px;


    display:flex;


    gap:10px;


  }





  .cta{


    flex:1;


    display:inline-flex;


    gap:8px;


    align-items:center;


    justify-content:center;


    padding:10px 12px;


    border-radius:12px;


    font-weight:600;


    cursor:pointer;


    background:var(--accent1);


    color:white;


    border:none;


    text-decoration:none;


  }





  .ghost{


    padding:10px 12px;


    border-radius:12px;


    border:1px solid rgba(255,255,255,0.06);


    background:transparent;


    color:var(--muted);


    text-decoration:none;


    display:inline-flex;


    align-items:center;


    gap:8px;


  }





  /* right column (content) */


  .content{


    display:flex;


    flex-direction:column;


    gap:18px;


  }





  .section-title{


    display:flex;


    align-items:center;


    justify-content:space-between;


    gap:12px;


    margin-bottom:12px;


  }





  .projects-grid{


    display:grid;


    grid-template-columns: repeat(auto-fill,minmax(240px,1fr));


    gap:14px;


  }





  .project{


    border-radius:14px;


    overflow:hidden;


    position:relative;


    min-height:150px;


    display:flex;


    flex-direction:column;


    justify-content:flex-end;


    padding:14px;


    background:


      linear-gradient(180deg, rgba(0,0,0,0.18), rgba(0,0,0,0.45));


    border:1px solid rgba(255,255,255,0.03);


    transition:transform .28s ease, box-shadow .28s ease;


    cursor:pointer;


  }





  .project:hover{


    transform:translateY(-8px) scale(1.01);


    box-shadow: 0 18px 40px rgba(2,6,23,0.7);


  }





  .project .title{font-weight:700;font-size:15px;margin:0}


  .project .tag{font-size:12px;color:var(--muted);margin-top:6px}





  .project .thumb{


    position:absolute;


    inset:0;


    background-size:cover;


    background-position:center;


    filter:grayscale(.08) contrast(.95) saturate(.95);


    opacity:0.14;


  }





  .project .overlay{


    position:relative;


    z-index:2;


  }





  .stats{


    display:flex;


    gap:10px;


    margin-top:10px;


    color:var(--muted);


    font-size:13px;


  }





  .skills-chip{display:flex;gap:8px;flex-wrap:wrap}





  .about{


    display:grid;


    grid-template-columns: 1fr 160px;


    gap:14px;


  }





  .progress{


    background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));


    border-radius:10px;


    padding:10px;


    border:1px solid rgba(255,255,255,0.03);


  }





  .progress .bar{


    margin-top:8px;


    height:8px;


    background:rgba(255,255,255,0.04);


    border-radius:999px;


    overflow:hidden;


  }





  .progress .bar > i{


    display:block;


    height:100%;


    width:0%;


    border-radius:999px;


    background:linear-gradient(90deg,#06b6d4,#7c3aed);


    transition: width .9s cubic-bezier(.2,.9,.3,1);


  }





  footer{


    margin-top:18px;


    text-align:center;


    color:var(--muted);


    font-size:13px;


  }





  /* responsive */


  @media (max-width:980px){


    main{grid-template-columns:1fr}


    .avatar{width:72px;height:72px}


    .logo{width:48px;height:48px;font-size:18px}


    header{flex-direction:column;align-items:stretch;gap:12px}


  }





  /* small helpers */


  .micro{font-size:12px;color:var(--muted)}


  a.no-deco{color:inherit;text-decoration:none}


  .badge{


    padding:6px 8px;border-radius:999px;background:linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));


    border:1px solid rgba(255,255,255,0.03);


    font-size:12px;color:var(--muted)


  }





  /* tiny float action */


  .fab{


    position:fixed;


    right:28px;


    bottom:28px;


    width:56px;height:56px;border-radius:14px;


    display:grid;place-items:center;


    background:var(--accent2);


    box-shadow:0 12px 30px rgba(6,182,212,0.08);


    cursor:pointer;


    border:none;


  }





  /* small animation for logo / CTA */


  @keyframes pop {


    0%{transform:scale(.96) rotate(-6deg)}


    50%{transform:scale(1.03) rotate(-3deg)}


    100%{transform:scale(1) rotate(-6deg)}


  }


  .logo{animation: pop 4.2s ease-in-out infinite}


</style>


</head>


<body>


  <div class="wrap" role="main">


    <header>


      <div class="brand">


        <div class="logo" aria-hidden="true">TM</div>


        <div>


          <div style="font-weight:700">Твоё Имя</div>


          <div class="micro">Frontend Developer • UI / UX • Creator</div>


        </div>


      </div>





      <nav aria-label="Навигация">


        <button class="nav-btn" onclick="scrollToSection('projects')">Проекты</button>


        <button class="nav-btn" onclick="scrollToSection('about')">Обо мне</button>


        <button class="nav-btn" onclick="scrollToSection('contacts')">Контакты</button>


      </nav>


    </header>





    <main>


      <!-- left column -->


      <aside class="card" aria-labelledby="profile-name">


        <div class="profile">


          <div class="avatar">TI</div>


          <div>


            <h1 id="profile-name">Твоё Имя</h1>


            <div class="role">Frontend Developer / Designer</div>


            <div class="micro" style="margin-top:6px">based in: Dublin • available for remote</div>


          </div>


        </div>





        <p class="bio">


          Я создаю интерфейсы, которые не только выглядят круто, но и работают плавно. Люблю анимации, чистый код и мелкие детали, которые делают UX трушным.


        </p>





        <div class="skill-list" aria-hidden="false">


          <div class="skill">HTML</div>


          <div class="skill">CSS</div>


          <div class="skill">JavaScript</div>


          <div class="skill">React</div>


          <div class="skill">Responsive</div>


          <div class="skill">Figma</div>


        </div>





        <div class="contact">


          <a class="cta" href="mailto:you@example.com">Написать</a>


          <a class="ghost" href="#" onclick="showResume()">Резюме</a>


        </div>





        <div style="margin-top:14px;">


          <div class="micro">Соцсети</div>


          <div style="display:flex;gap:8px;margin-top:8px">


            <a class="badge" href="#" onclick="openLink('#')">Behance</a>


            <a class="badge" href="#" onclick="openLink('#')">GitHub</a>


            <a class="badge" href="#" onclick="openLink('#')">Dribbble</a>


          </div>


        </div>


      </aside>





      <!-- right column -->


      <section class="content">


        <div id="projects" class="card" aria-labelledby="projects-title">


          <div class="section-title">


            <div>


              <div id="projects-title" style="font-weight:700">Выбранные проекты</div>


              <div class="micro">Небольшой срез моих работ</div>


            </div>


            <div class="micro">3 / 12</div>


          </div>





          <div class="projects-grid">


            <article class="project" onclick="openLink('#')" role="link" aria-label="Project One">


              <div class="thumb" style="background-image:url('data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22240%22 height=%22160%22></svg>')"></div>


              <div class="overlay">


                <div class="tag">Web App</div>


                <h3 class="title">Design System Dashboard</h3>


                <div class="stats">


                  <div class="micro">React</div>


                  <div class="micro">UI Kit</div>


                </div>


              </div>


            </article>





            <article class="project" onclick="openLink('#')">


              <div class="thumb" style="background-image:linear-gradient(120deg, rgba(7,12,20,0.1), rgba(7,12,20,0.2));"></div>


              <div class="overlay">


                <div class="tag">Landing</div>


                <h3 class="title">Coffee Shop Landing</h3>


                <div class="stats">


                  <div class="micro">HTML/CSS</div>


                  <div class="micro">Animation</div>


                </div>


              </div>


            </article>





            <article class="project" onclick="openLink('#')">


              <div class="thumb" style="background-image:linear-gradient(90deg, rgba(124,58,237,0.12), rgba(6,182,212,0.08));"></div>


              <div class="overlay">


                <div class="tag">Mobile</div>


                <h3 class="title">Finance Tracker App</h3>


                <div class="stats">


                  <div class="micro">React Native</div>


                  <div class="micro">UX</div>


                </div>


              </div>


            </article>


          </div>





        </div>





        <div id="about" class="card">


          <div class="section-title">


            <div>


              <div style="font-weight:700">Обо мне</div>


              <div class="micro">Коротко и по делу</div>


            </div>


            <div class="micro">5 лет опыта</div>


          </div>





          <div class="about">


            <div>


              <p style="margin-top:0;color:#dce9ff">Я строю интерфейсы, оптимизирую взаимодействие и делаю так, чтобы продукт выглядел целостно. Работаю с командами и одиночками — всегда открыт к новым задачам.</p>





              <h4 style="margin-bottom:8px">Инструменты</h4>


              <div class="skills-chip">


                <div class="skill">VS Code</div>


                <div class="skill">Figma</div>


                <div class="skill">Storybook</div>


                <div class="skill">Git</div>


              </div>





              <h4 style="margin-top:12px;margin-bottom:8px">Что мне нравится</h4>


              <ul style="margin:0;padding-left:18px;color:var(--muted);font-size:14px">


                <li>Чистая архитектура CSS</li>


                <li>Микровзаимодействия</li>


                <li>Оптимизация производительности</li>


              </ul>


            </div>





            <aside class="progress">


              <div class="micro">Навыки</div>


              <div style="margin-top:10px">


                <div class="micro">HTML / CSS</div>


                <div class="bar" data-value="95"><i></i></div>





                <div style="height:10px"></div>





                <div class="micro">JavaScript</div>


                <div class="bar" data-value="88"><i></i></div>





                <div style="height:10px"></div>





                <div class="micro">React</div>


                <div class="bar" data-value="84"><i></i></div>





                <div style="height:10px"></div>





                <div class="micro">Design</div>


                <div class="bar" data-value="78"><i></i></div>


              </div>


            </aside>


          </div>


        </div>





        <div id="contacts" class="card">


          <div class="section-title">


            <div>


              <div style="font-weight:700">Контакты</div>


              <div class="micro">Доступен для фриланса и работы</div>


            </div>


            <div class="micro">reply usually <strong style="color:#cbd6ff">24h</strong></div>


          </div>





          <div style="display:flex;gap:12px;flex-wrap:wrap;align-items:center">


            <a class="cta" href="mailto:you@example.com">you@example.com</a>


            <a class="ghost" href="tel:+441234567890">+44 1234 567 890</a>


          </div>





          <form style="margin-top:14px;display:grid;gap:8px" onsubmit="contactForm(event)">


            <input name="name" placeholder="Имя" style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit" required>


            <input name="email" type="email" placeholder="Email" style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit" required>


            <textarea name="message" rows="4" placeholder="Сообщение" style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit" required></textarea>


            <div style="display:flex;gap:8px">


              <button class="cta" type="submit">Отправить</button>


              <button type="button" class="ghost" onclick="clearForm(this)">Очистить</button>


            </div>


            <div id="form-msg" class="micro" style="display:none;color:var(--muted)"></div>


          </form>





        </div>





        <footer>


          © <span id="year"></span> Твоё Имя — Сделано с ❤️ и CSS магией


        </footer>


      </section>


    </main>





    <button class="fab" title="Написать" onclick="openLink('mailto:you@example.com')">


      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M2 12L22 3L13 22L9 13L2 12Z" fill="white" /></svg>


    </button>


  </div>





<script>


  // helpers


  function openLink(href){


    // fallback: if #, do nothing


    if(href === '#' || !href) return;


    window.location.href = href;


  }


  function showResume(){ alert('Резюме: вставь ссылку на резюме или скачивание.'); }





  // progress animation


  document.addEventListener('DOMContentLoaded', () => {


    // year


    document.getElementById('year').textContent = new Date().getFullYear();





    document.querySelectorAll('.bar').forEach(bar => {


      const value = bar.getAttribute('data-value') || 60;


      const el = bar.querySelector('i');


      // animate with slight delay to feel smooth


      setTimeout(()=> el.style.width = value + '%', 120);


    });





    // lazy fill project thumbnails with pleasant placeholders


    const thumbs = document.querySelectorAll('.project .thumb');


    thumbs.forEach((t,i) => {


      // tiny variety of gradient backgrounds (no external images)


      const grads = [


        'linear-gradient(120deg,rgb(124 58 237 / 16%), rgb(6 182 212 / 10%))',


        'linear-gradient(120deg,rgb(16 185 129 / 12%), rgb(59 130 246 / 10%))',


        'linear-gradient(120deg,rgb(234 88 12 / 10%), rgb(124 58 237 / 10%))'


      ];


      t.style.backgroundImage = grads[i%grads.length];


    });


  });





  function scrollToSection(id){


    const el = document.getElementById(id);


    if(!el) return;


    el.scrollIntoView({behavior:'smooth', block:'start'});


  }





  function contactForm(e){


    e.preventDefault();


    const form = e.target;


    const msg = document.getElementById('form-msg');


    // non-functional: simulate success


    msg.style.display = 'block';


    msg.textContent = 'Сообщение отправлено (демо). Замени обработчик на свой бекенд.';


    form.reset();


    setTimeout(()=> msg.style.display='none', 4200);


  }





  function clearForm(btn){


    const form = btn.closest('form');


    if(form) form.reset();


  }


</script>


</body>


</html>
