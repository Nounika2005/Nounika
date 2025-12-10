# Nounika
Hello This is Nounika PSGRKCW
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>About NOUNIKA — Interactive</title>
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--muted:#9aa4b2;--accent:#7c3aed;--glass:rgba(255,255,255,0.04)}
    [data-theme="light"]{--bg:#f7fbff;--card:#ffffff;--muted:#5b6b78;--accent:#6b21a8;--glass:rgba(10,10,10,0.03)}
    *{box-sizing:border-box}
    body{font-family:Inter, ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue';margin:0;background:linear-gradient(180deg,var(--bg),#071021);color:#e6eef6;min-height:100vh;padding:28px}
    .wrap{max-width:980px;margin:0 auto}
    header{display:flex;gap:18px;align-items:center}
    .avatar{width:120px;height:120px;border-radius:14px;background:linear-gradient(135deg,var(--accent),#0ea5a3);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:28px;color:white;box-shadow:0 6px 20px rgba(2,6,23,0.6)}
    .card{background:var(--card);padding:18px;border-radius:14px;margin-top:18px;box-shadow:0 8px 30px rgba(2,6,23,0.6)}
    h1{margin:0;font-size:22px}
    .controls{margin-left:auto;display:flex;gap:8px}
    button{background:transparent;border:1px solid rgba(255,255,255,0.06);color:inherit;padding:8px 10px;border-radius:8px;cursor:pointer}
    .grid{display:grid;grid-template-columns:1fr 360px;gap:16px;margin-top:16px}
    .bio{min-height:120px}
    .editable{background:var(--glass);padding:12px;border-radius:10px;border:1px dashed rgba(255,255,255,0.03);min-height:110px}
    .small{color:var(--muted);font-size:13px}
    .skills{display:flex;flex-direction:column;gap:10px}
    .skill{display:flex;align-items:center;gap:10px}
    .bar{flex:1;height:10px;background:rgba(255,255,255,0.06);border-radius:999px;overflow:hidden}
    .bar>i{display:block;height:100%;background:linear-gradient(90deg,var(--accent),#06b6d4);border-radius:999px;width:40%}
    .side{display:flex;flex-direction:column;gap:12px}
    input[type=file]{display:none}
    .photo-preview{width:100%;height:180px;background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);border-radius:10px;display:flex;align-items:center;justify-content:center;color:var(--muted);overflow:hidden}
    .timeline{display:flex;flex-direction:column;gap:8px}
    .event{background:linear-gradient(180deg,rgba(255,255,255,0.01),transparent);padding:10px;border-radius:8px;border-left:4px solid rgba(255,255,255,0.03)}
    footer{margin-top:18px;display:flex;justify-content:space-between;align-items:center}
    .actions{display:flex;gap:8px}
    .chip{padding:6px 8px;border-radius:999px;border:1px solid rgba(255,255,255,0.03);font-size:13px}
    a{color:inherit}
    @media(max-width:880px){.grid{grid-template-columns:1fr;}.controls{margin-left:0}}
  </style>
</head>
<body data-theme="dark">
  <div class="wrap">
    <header>
      <div class="avatar" id="avatar">N</div>
      <div>
        <h1 id="name">NOUNIKA</h1>
        <div class="small">Interactive "About Me" — edit the fields below. Changes are saved locally.</div>
      </div>
      <div class="controls">
        <button id="themeBtn">Toggle Theme</button>
        <button id="downloadBtn">Download HTML</button>
        <button id="resetBtn">Reset</button>
      </div>
    </header>

    <div class="grid">
      <main>
        <section class="card">
          <h3>Bio</h3>
          <div class="bio editable" id="bio" contenteditable="true">Hi — I'm NOUNIKA. I love building things, learning new tools, and experimenting with web UX. Edit this text to tell people about yourself.</div>
          <div style="margin-top:12px;display:flex;gap:10px;align-items:center">
            <div class="chip" id="roleChip">Student • Developer</div>
            <div class="chip" id="locationChip">Chennai, India</div>
            <div class="small">Tip: double-click any text to edit quickly.</div>
          </div>
        </section>

        <section class="card" style="margin-top:12px">
          <h3>Skills</h3>
          <div class="skills" id="skillsList">
            <div class="skill"><div style="width:90px" class="small">HTML/CSS</div><div class="bar"><i style="width:80%"></i></div></div>
            <div class="skill"><div style="width:90px" class="small">JavaScript</div><div class="bar"><i style="width:65%"></i></div></div>
            <div class="skill"><div style="width:90px" class="small">Angular / React</div><div class="bar"><i style="width:55%"></i></div></div>
          </div>
          <div style="margin-top:10px;display:flex;gap:8px">
            <input id="skillName" placeholder="New skill" style="flex:1;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <input id="skillVal" type="number" min="5" max="100" value="50" style="width:90px;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <button id="addSkillBtn">Add</button>
          </div>
        </section>

        <section class="card" style="margin-top:12px">
          <h3>Timeline</h3>
          <div class="timeline" id="timeline">
            <div class="event"><strong>2025</strong> — Started new personal projects and learning AR/AI.</div>
            <div class="event"><strong>2024</strong> — Built small web apps and learned databases.</div>
          </div>
          <div style="margin-top:10px;display:flex;gap:8px">
            <input id="evYear" placeholder="Year" style="width:90px;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <input id="evText" placeholder="Event description" style="flex:1;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <button id="addEventBtn">Add</button>
          </div>
        </section>

      </main>

      <aside class="side">
        <div class="card">
          <h3>Photo</h3>
          <label for="photoInput" class="photo-preview" id="photoPreview">Click to upload a photo<input type="file" id="photoInput" accept="image/*"></label>
          <div class="small" style="margin-top:8px">Preview shown above — your image stays in your browser only.</div>
        </div>

        <div class="card">
          <h3>Contact</h3>
          <div class="small">This demo doesn't send messages. Use it to show contact info.</div>
          <div style="margin-top:10px;display:flex;flex-direction:column;gap:8px">
            <input id="email" placeholder="your@email.com" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <input id="phone" placeholder="+91 98765 43210" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <button id="saveContactBtn">Save</button>
          </div>
        </div>

        <div class="card">
          <h3>Social</h3>
          <div class="small">Add links below</div>
          <div style="margin-top:8px;display:flex;flex-direction:column;gap:8px">
            <input id="git" placeholder="GitHub URL" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <input id="linkedin" placeholder="LinkedIn URL" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            <button id="saveSocialBtn">Save</button>
          </div>
        </div>

      </aside>
    </div>

    <footer>
      <div class="small">Made with ❤️ — interactive About Me. Your edits are stored locally in browser storage.</div>
      <div class="actions">
        <button id="exportProfileBtn">Export JSON</button>
        <button id="importProfileBtn">Import JSON</button>
        <input type="file" id="importFile" style="display:none" accept="application/json">
      </div>
    </footer>
  </div>

  <script>
    // Utilities
    const $ = id => document.getElementById(id);
    const storageKey = 'aboutMe_nounika_v1';

    function getState(){
      return {
        name: $('name').textContent.trim(),
        bio: $('bio').innerHTML,
        role: $('roleChip').textContent,
        location: $('locationChip').textContent,
        skills: Array.from(document.querySelectorAll('#skillsList .skill')).map(s=>({name:s.querySelector('.small').textContent, val:getComputedStyle(s.querySelector('i')).width})),
        timeline: Array.from(document.querySelectorAll('#timeline .event')).map(e=>e.innerText),
        email: $('email').value, phone: $('phone').value, git: $('git').value, linkedin: $('linkedin').value,
        avatarLetter: $('avatar').textContent,
        photo: $('photoPreview').dataset.img || null
      }
    }

    function save(){
      const data = {
        name: $('name').textContent.trim(),
        bio: $('bio').innerHTML,
        role: $('roleChip').textContent,
        location: $('locationChip').textContent,
        skills: Array.from(document.querySelectorAll('#skillsList .skill')).map(s=>({name:s.querySelector('.small').textContent, percent:s.querySelector('i').style.width})),
        timeline: Array.from(document.querySelectorAll('#timeline .event')).map(e=>e.innerHTML),
        email: $('email').value, phone: $('phone').value, git: $('git').value, linkedin: $('linkedin').value,
        avatarLetter: $('avatar').textContent,
        photo: $('photoPreview').dataset.img || null
      };
      localStorage.setItem(storageKey, JSON.stringify(data));
    }

    function load(){
      const raw = localStorage.getItem(storageKey);
      if(!raw) return;
      try{
        const data = JSON.parse(raw);
        if(data.name) $('name').textContent = data.name;
        if(data.bio) $('bio').innerHTML = data.bio;
        if(data.role) $('roleChip').textContent = data.role;
        if(data.location) $('locationChip').textContent = data.location;
        if(data.skills){
          const container = $('skillsList'); container.innerHTML = '';
          data.skills.forEach(s=>{const div=document.createElement('div');div.className='skill';div.innerHTML=`<div style="width:90px" class="small">${s.name}</div><div class="bar"><i style="width:${s.percent}"></i></div>`;container.appendChild(div)});
        }
        if(data.timeline){const t = $('timeline'); t.innerHTML = ''; data.timeline.forEach(ev=>{const d=document.createElement('div');d.className='event';d.innerHTML=ev; t.appendChild(d)});}
        if(data.email) $('email').value = data.email;
        if(data.phone) $('phone').value = data.phone;
        if(data.git) $('git').value = data.git;
        if(data.linkedin) $('linkedin').value = data.linkedin;
        if(data.avatarLetter) $('avatar').textContent = data.avatarLetter[0].toUpperCase();
        if(data.photo) setPhotoFromDataUrl(data.photo);
      }catch(e){console.warn('Could not load saved profile', e)}
    }

    // Initial load
    load();

    // Auto-save when editable fields change
    ['bio','name','roleChip','locationChip'].forEach(id=>{
      const el = $(id);
      if(!el) return;
      el.addEventListener('input', save);
      el.addEventListener('blur', save);
    });

    // Add skill
    $('addSkillBtn').addEventListener('click', ()=>{
      const name = $('skillName').value.trim(); const val = Math.max(5, Math.min(100, Number($('skillVal').value)||50));
      if(!name) return alert('Please enter a skill name');
      const div=document.createElement('div');div.className='skill';div.innerHTML=`<div style="width:90px" class="small">${name}</div><div class="bar"><i style="width:${val}%"></i></div>`;
      $('skillsList').appendChild(div);
      $('skillName').value=''; $('skillVal').value=50; save();
    });

    // Add timeline event
    $('addEventBtn').addEventListener('click', ()=>{
      const y = $('evYear').value.trim(); const t = $('evText').value.trim();
      if(!y || !t) return alert('Enter year and event text');
      const div=document.createElement('div'); div.className='event'; div.innerHTML=`<strong>${y}</strong> — ${t}`;
      $('timeline').prepend(div); $('evYear').value=''; $('evText').value=''; save();
    });

    // Photo upload + preview
    $('photoInput').addEventListener('change', e=>{
      const f = e.target.files[0]; if(!f) return;
      const reader = new FileReader(); reader.onload = ev=>{ setPhotoFromDataUrl(ev.target.result); save(); };
      reader.readAsDataURL(f);
    });
    function setPhotoFromDataUrl(dataUrl){
      $('photoPreview').innerHTML = '';
      const img = document.createElement('img'); img.src = dataUrl; img.style.width='100%'; img.style.height='100%'; img.style.objectFit='cover'; $('photoPreview').appendChild(img); $('photoPreview').dataset.img = dataUrl;
    }

    // Contact & social save
    $('saveContactBtn').addEventListener('click', ()=>{ save(); alert('Contact saved locally'); });
    $('saveSocialBtn').addEventListener('click', ()=>{ save(); alert('Social links saved locally'); });

    // Theme toggle
    $('themeBtn').addEventListener('click', ()=>{
      const el = document.body; const t = el.getAttribute('data-theme') === 'light' ? 'dark' : 'light'; el.setAttribute('data-theme', t);
    });

    // Export/Import JSON
    $('exportProfileBtn').addEventListener('click', ()=>{
      const data = localStorage.getItem(storageKey) || JSON.stringify(getState());
      const blob = new Blob([data], {type:'application/json'});
      const url = URL.createObjectURL(blob); const a=document.createElement('a'); a.href=url; a.download='aboutme_nounika.json'; a.click(); URL.revokeObjectURL(url);
    });
    $('importProfileBtn').addEventListener('click', ()=>$('importFile').click());
    $('importFile').addEventListener('change', e=>{
      const f=e.target.files[0]; if(!f) return; const r=new FileReader(); r.onload=ev=>{ try{const obj=JSON.parse(ev.target.result); localStorage.setItem(storageKey, JSON.stringify(obj)); load(); alert('Profile imported'); }catch(err){alert('Invalid JSON file')} }; r.readAsText(f);
    });

    // Download full HTML (snapshot of current profile)
    $('downloadBtn').addEventListener('click', ()=>{
      const serializer = new XMLSerializer();
      const clone = document.documentElement.cloneNode(true);
      // remove interactive scripts for snapshot
      Array.from(clone.querySelectorAll('script')).forEach(s=>s.remove());
      const doc = '<!doctype html>' + serializer.serializeToString(clone);
      const blob = new Blob([doc], {type:'text/html'});
      const url=URL.createObjectURL(blob); const a=document.createElement('a'); a.href=url; a.download='about-nounika.html'; a.click(); URL.revokeObjectURL(url);
    });

    // Reset
    $('resetBtn').addEventListener('click', ()=>{ if(confirm('Reset stored profile to defaults?')){ localStorage.removeItem(storageKey); location.reload(); }});

    // Simple auto-avatar letter from name edits
    const nameObserver = new MutationObserver(()=>{$('avatar').textContent = $('name').textContent.trim()[0] ? $('name').textContent.trim()[0].toUpperCase() : 'N'; save();});
    nameObserver.observe($('name'), {characterData:true, childList:true, subtree:true});

    // Initial save to ensure defaults are present
    save();
  </script>
</body>
</html>
