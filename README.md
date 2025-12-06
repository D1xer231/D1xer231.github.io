<style>
  :root{
    --bg:#0b1220;
    --card:#0f1724;
    --muted:#9fb0d9;
    --accent:#7c3aed;
    --accent-2:#06b6d4;
    --glass: rgba(255,255,255,0.03);
    font-family: Inter, "Segoe UI", Roboto, system-ui, -apple-system, Arial, sans-serif;
  }
  *{box-sizing:border-box}
  html,body{height:100%}
  body{
    margin:0;
    background: linear-gradient(180deg,#071021 0%, #081426 100%);
    color:#e6eef8;
    -webkit-font-smoothing:antialiased;
    padding:28px;
    display:flex;
    justify-content:center;
    font-size:15px;
    line-height:1.45;
  }
  .wrap{
    width:100%;
    max-width:980px;
  }
  header{
    display:flex;
    gap:16px;
    align-items:center;
    margin-bottom:18px;
  }
  .logo{
    width:64px;height:64px;border-radius:12px;
    background:linear-gradient(135deg,var(--accent),var(--accent-2));
    display:grid;place-items:center;font-weight:700;font-size:22px;color:white;
    box-shadow:0 8px 30px rgba(7,12,20,0.6);
  }
  h1{margin:0;font-size:22px}
  .sub{color:var(--muted);font-size:13px;margin-top:6px}
  .layout{
    display:grid;
    grid-template-columns:320px 1fr;
    gap:20px;
  }

  /* card */
  .card{
    background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    border-radius:14px;
    padding:18px;
    border:1px solid var(--glass);
    box-shadow: 0 12px 30px rgba(2,6,23,0.6);
  }

  /* left column */
  .avatar{
    width:86px;height:86px;border-radius:12px;display:grid;place-items:center;
    background:linear-gradient(180deg,#081024,#021021);font-weight:700;font-size:30px;color:#fff;
    box-shadow: inset 0 -8px 20px rgba(255,255,255,0.02);
  }
  .profile{
    display:flex;gap:12px;align-items:center;
  }
  .bio{color:#d7e7ff;margin-top:12px;font-size:14px}
  .skills{display:flex;flex-wrap:wrap;gap:8px;margin-top:12px}
  .skill{
    padding:8px 10px;border-radius:999px;background:rgba(255,255,255,0.02);
    border:1px solid rgba(255,255,255,0.03);color:var(--muted);font-size:13px;
  }

  .btn-row{display:flex;gap:10px;margin-top:14px}
  .btn{
    padding:10px 12px;border-radius:10px;text-decoration:none;color:white;font-weight:600;
    display:inline-flex;align-items:center;gap:8px;
  }
  .btn-primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));box-shadow:0 8px 20px rgba(124,58,237,0.08)}
  .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}

  /* right column */
  .section{margin-bottom:16px}
  .section h2{margin:0 0 8px 0;font-size:18px}
  .projects{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:12px}
  .project{
    border-radius:12px;padding:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    border:1px solid rgba(255,255,255,0.03);
  }
  .project .tag{font-size:12px;color:var(--muted);margin-bottom:6px}
  .project h3{margin:0;font-size:15px}

  .about-grid{display:grid;grid-template-columns:1fr 180px;gap:12px}
  .chip{display:inline-block;padding:6px 8px;border-radius:999px;background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.03);color:var(--muted);font-size:13px;margin:4px 6px 4px 0;}

  table.skills{width:100%;border-collapse:collapse;margin-top:8px}
  table.skills td{padding:8px 6px;border-top:1px solid rgba(255,255,255,0.02);color:var(--muted)}
  table.skills td.skillname{width:60%}
  .bar{
    height:10px;background:rgba(255,255,255,0.04);border-radius:999px;overflow:hidden;
  }
  .bar > i{display:block;height:100%;background:linear-gradient(90deg,var(--accent-2),var(--accent));width:0%}

  footer{color:var(--muted);text-align:center;margin-top:12px;font-size:13px}

  /* responsive */
  @media (max-width:900px){
    .layout{grid-template-columns:1fr}
    .about-grid{grid-template-columns:1fr}
    .avatar{width:70px;height:70px;font-size:24px}
  }
</style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">TM</div>
      <div>
        <h1>Твоё Имя</h1>
        <div class="sub">Frontend Developer • UI / UX • Creator</div>
      </div>
    </header>

    <div class="layout">
      <!-- left -->
      <aside class="card" aria-labelledby="profile">
        <div class="profile">
          <div class="avatar">TI</div>
          <div>
            <div style="font-weight:700">Твоё Имя</div>
            <div class="sub" style="margin-top:6px">Frontend Developer / Designer</div>
            <div class="sub" style="margin-top:6px">based in: Dublin • available for remote</div>
          </div>
        </div>

        <p class="bio">Я делаю интерфейсы, которые выглядят свежо и работают плавно. Люблю микровзаимодействия, чистый код и красивые детали.</p>

        <div class="skills" aria-hidden="false">
          <span class="skill">HTML</span>
          <span class="skill">CSS</span>
          <span class="skill">JavaScript</span>
          <span class="skill">React</span>
          <span class="skill">Responsive</span>
          <span class="skill">Figma</span>
        </div>

        <div class="btn-row">
          <a class="btn btn-primary" href="mailto:you@example.com">Написать</a>
          <a class="btn btn-ghost" href="#" onclick="event.preventDefault()">Резюме</a>
        </div>

        <div style="margin-top:12px;color:var(--muted);font-size:13px">
          Соцсети:
          <div style="margin-top:8px">
            <a class="chip" href="#">GitHub</a>
            <a class="chip" href="#">Behance</a>
            <a class="chip" href="#">Dribbble</a>
          </div>
        </div>
      </aside>

      <!-- right -->
      <main>
        <section class="card section" id="projects">
          <h2>Выбранные проекты</h2>
          <div class="projects">
            <article class="project">
              <div class="tag">Web App</div>
              <h3>Design System Dashboard</h3>
              <p style="color:var(--muted);margin-top:8px">React • UI Kit • Storybook</p>
            </article>

            <article class="project">
              <div class="tag">Landing</div>
              <h3>Coffee Shop Landing</h3>
              <p style="color:var(--muted);margin-top:8px">HTML/CSS • Анимации</p>
            </article>

            <article class="project">
              <div class="tag">Mobile</div>
              <h3>Finance Tracker App</h3>
              <p style="color:var(--muted);margin-top:8px">React Native • UX</p>
            </article>
          </div>
        </section>

        <section class="card section" id="about">
          <h2>Обо мне</h2>
          <div class="about-grid">
            <div>
              <p style="margin-top:0;color:#dce9ff">Я строю понятные интерфейсы, делаю акцент на UX и оптимизирую перформанс. Работаю с командами и самостоятельно.</p>

              <h4 style="margin-bottom:8px">Инструменты</h4>
              <div>
                <span class="chip">VS Code</span>
                <span class="chip">Figma</span>
                <span class="chip">Storybook</span>
                <span class="chip">Git</span>
              </div>

              <h4 style="margin-top:12px;margin-bottom:8px">Люблю</h4>
              <ul style="color:var(--muted);margin:0;padding-left:18px">
                <li>Чистая архитектура CSS</li>
                <li>Микровзаимодействия</li>
                <li>Оптимизация производительности</li>
              </ul>
            </div>

            <aside style="background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03)">
              <div style="color:var(--muted);font-size:13px">Навыки</div>
              <table class="skills" aria-hidden="true">
                <tr><td class="skillname">HTML / CSS</td><td><div class="bar"><i style="width:95%"></i></div></td></tr>
                <tr><td class="skillname">JavaScript</td><td><div class="bar"><i style="width:88%"></i></div></td></tr>
                <tr><td class="skillname">React</td><td><div class="bar"><i style="width:84%"></i></div></td></tr>
                <tr><td class="skillname">Design</td><td><div class="bar"><i style="width:78%"></i></div></td></tr>
              </table>
            </aside>
          </div>
        </section>

        <section class="card section" id="contacts">
          <h2>Контакты</h2>
          <p style="margin:0;color:var(--muted)">Доступен для фриланса и работы</p>
          <div style="display:flex;gap:10px;margin-top:12px;flex-wrap:wrap">
            <a class="btn btn-primary" href="mailto:you@example.com">you@example.com</a>
            <a class="btn btn-ghost" href="tel:+441234567890">+44 1234 567 890</a>
          </div>

          <form style="margin-top:14px;display:grid;gap:8px" onsubmit="event.preventDefault(); alert('Замените обработчик формы на ваш бекенд');">
            <input name="name" placeholder="Имя" required style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <input name="email" type="email" placeholder="Email" required style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <textarea name="message" rows="3" placeholder="Сообщение" required style="padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit"></textarea>
            <div style="display:flex;gap:8px">
              <button class="btn btn-primary" type="submit">Отправить</button>
              <button class="btn btn-ghost" type="reset">Очистить</button>
            </div>
          </form>
        </section>

        <footer>
          © <span id="year"></span> Твоё Имя — Сделано с ❤️ и CSS магией
        </footer>
      </main>
    </div>
  </div>

<script>
  // минимальная интерактивность — анимация прогрессов и год
  document.addEventListener('DOMContentLoaded', () => {
    document.getElementById('year').textContent = new Date().getFullYear();
    // плавный прогресс (редкий, работает только в браузере)
    document.querySelectorAll('.bar > i').forEach((el, idx) => {
      const w = el.style.width || '0%';
      el.style.width = '0%';
      setTimeout(()=> { el.style.transition = 'width .9s cubic-bezier(.2,.9,.3,1)'; el.style.width = w; }, 120 + idx*120);
    });
  });
</script>
</body>
</html>
