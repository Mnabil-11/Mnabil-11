<iframe srcdoc="<!DOCTYPE html>
<html lang='en'>
<head>
<meta charset='UTF-8'>
<meta name='viewport' content='width=device-width, initial-scale=1.0'>
<style>
  :root {
    --kimi-font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    --kimi-font-mono: 'SF Mono', Monaco, monospace;
    --kimi-color-text-primary: #1a1a1a;
    --kimi-color-text-secondary: #555;
    --kimi-color-text-tertiary: #888;
    --kimi-color-text-quaternary: #bbb;
    --kimi-color-surface: #f5f5f5;
    --kimi-color-surface-muted: #fafafa;
    --kimi-color-surface-raised: #fff;
    --kimi-color-border: #e0e0e0;
    --kimi-color-accent: #2563eb;
    --kimi-color-positive: #16a34a;
    --kimi-color-danger: #dc2626;
    --kimi-chart-1: #2563eb;
    --kimi-chart-2: #dc2626;
    --kimi-chart-3: #16a34a;
    --kimi-chart-4: #7c3aed;
    --kimi-chart-5: #6b7280;
    --t-fast: 150ms;
    --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: var(--kimi-font-sans);
    color: var(--kimi-color-text-primary);
    background: transparent;
    padding: 16px;
    line-height: 1.5;
  }
  .widget {
    max-width: 720px;
    margin: 0 auto;
  }
  .header {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 24px;
    padding-bottom: 20px;
    border-bottom: 1px solid var(--kimi-color-border);
  }
  .avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    background: var(--kimi-color-surface);
    border: 2px solid var(--kimi-color-border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 32px;
    flex-shrink: 0;
  }
  .header-text h1 {
    font-size: 24px;
    font-weight: 500;
    margin-bottom: 4px;
  }
  .header-text p {
    color: var(--kimi-color-text-secondary);
    font-size: 15px;
  }
  .tabs {
    display: flex;
    gap: 4px;
    margin-bottom: 20px;
    border-bottom: 1px solid var(--kimi-color-border);
  }
  .tab {
    padding: 8px 16px;
    border: none;
    background: none;
    color: var(--kimi-color-text-tertiary);
    font-family: inherit;
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    border-bottom: 2px solid transparent;
    margin-bottom: -1px;
    transition: all var(--t-fast) var(--ease-out);
  }
  .tab.active {
    color: var(--kimi-color-text-primary);
    border-bottom-color: var(--kimi-color-text-primary);
  }
  .tab:hover:not(.active) {
    color: var(--kimi-color-text-secondary);
  }
  .panel { display: none; }
  .panel.active { display: block; }
.section {
margin-bottom: 20px;
}
.section-title {
font-size: 13px;
font-weight: 500;
color: var(--kimi-color-text-tertiary);
text-transform: uppercase;
letter-spacing: 0.5px;
margin-bottom: 12px;
}
.input-group {
margin-bottom: 16px;
}
label {
display: block;
font-size: 14px;
font-weight: 500;
margin-bottom: 6px;
color: var(--kimi-color-text-secondary);
}
input, textarea, select {
width: 100%;
padding: 10px 12px;
border: 1px solid var(--kimi-color-border);
border-radius: 10px;
font-family: inherit;
font-size: 14px;
background: var(--kimi-color-surface-raised);
color: var(--kimi-color-text-primary);
transition: border-color var(--t-fast) var(--t-fast);
}
input:focus, textarea:focus, select:focus {
outline: none;
border-color: var(--kimi-color-text-primary);
}
textarea {
resize: vertical;
min-height: 80px;
}
.skills-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
gap: 8px;
margin-top: 8px;
}
.skill-tag {
display: flex;
align-items: center;
gap: 6px;
padding: 8px 12px;
border-radius: 6px;
border: 1px solid var(--kimi-color-border);
font-size: 13px;
cursor: pointer;
transition: all var(--t-fast) var(--ease-out);
background: var(--kimi-color-surface-raised);
}
.skill-tag:hover {
border-color: var(--kimi-color-text-secondary);
}
.skill-tag.selected {
background: var(--kimi-color-text-primary);
color: #fff;
border-color: var(--kimi-color-text-primary);
}
.preview-box {
background: var(--kimi-color-surface-muted);
border: 1px solid var(--kimi-color-border);
border-radius: 12px;
padding: 20px;
margin-top: 20px;
position: relative;
}
.preview-header {
display: flex;
justify-content: space-between;
align-items: center;
margin-bottom: 16px;
}
.preview-title {
font-size: 14px;
font-weight: 500;
color: var(--kimi-color-text-secondary);
}
.copy-btn {
padding: 6px 14px;
border-radius: 8px;
border: 1px solid var(--kimi-color-border);
background: var(--kimi-color-surface-raised);
font-family: inherit;
font-size: 13px;
font-weight: 500;
cursor: pointer;
transition: all var(--t-fast) var(--ease-out);
}
.copy-btn:hover {
background: var(--kimi-color-text-primary);
color: #fff;
border-color: var(--kimi-color-text-primary);
}
.copy-btn.copied {
background: var(--kimi-color-positive);
color: #fff;
border-color: var(--kimi-color-positive);
}
pre {
background: var(--kimi-color-surface);
border-radius: 8px;
padding: 16px;
overflow-x: auto;
font-family: var(--kimi-font-mono);
font-size: 12px;
line-height: 1.6;
color: var(--kimi-color-text-primary);
white-space: pre-wrap;
word-break: break-word;
}
.stats-row {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 12px;
margin-bottom: 20px;
}
.stat-card {
padding: 16px;
border-radius: 10px;
border: 1px solid var(--kimi-color-border);
text-align: center;
background: var(--kimi-color-surface-raised);
}
.stat-value {
font-size: 28px;
font-weight: 500;
color: var(--kimi-color-text-primary);
font-variant-numeric: tabular-nums;
}
.stat-label {
font-size: 12px;
color: var(--kimi-color-text-tertiary);
margin-top: 4px;
}
.toggle-row {
display: flex;
align-items: center;
justify-content: space-between;
padding: 10px 0;
border-bottom: 1px solid var(--kimi-color-border);
}
.toggle-row:last-child { border-bottom: none; }
.toggle-label {
font-size: 14px;
color: var(--kimi-color-text-secondary);
}
.switch {
position: relative;
width: 40px;
height: 22px;
background: var(--kimi-color-border);
border-radius: 11px;
cursor: pointer;
transition: background var(--t-fast) var(--ease-out);
}
.switch.active {
background: var(--kimi-color-text-primary);
}
.switch::after {
content: '';
position: absolute;
width: 18px;
height: 18px;
background: #fff;
border-radius: 50%;
top: 2px;
left: 2px;
transition: transform var(--t-fast) var(--ease-out);
}
.switch.active::after {
transform: translateX(18px);
}
.theme-dots {
display: flex;
gap: 8px;
margin-top: 8px;
}
.theme-dot {
width: 32px;
height: 32px;
border-radius: 50%;
cursor: pointer;
border: 2px solid transparent;
transition: all var(--t-fast) var(--ease-out);
}
.theme-dot:hover { transform: scale(1.1); }
.theme-dot.active { border-color: var(--kimi-color-text-primary); }
</head>
<body>
<div class='widget'>
  <div class='header'>
    <div class='avatar'>👤</div>
    <div class='header-text'>
      <h1>GitHub Profile Designer</h1>
      <p>Build a modern, professional README.md</p>
    </div>
  </div>
  <div class='tabs'>
    <button class='tab active' onclick='switchTab(0)'>Profile</button>
    <button class='tab' onclick='switchTab(1)'>Skills</button>
    <button class='tab' onclick='switchTab(2)'>Stats & Social</button>
    <button class='tab' onclick='switchTab(3)'>Preview</button>
  </div>
  <div class='panel active' id='panel-0'>
    <div class='section'>
      <div class='input-group'>
        <label>Name</label>
        <input type='text' id='name' placeholder='Your Name' value='Mnabil-11'>
      </div>
      <div class='input-group'>
        <label>Tagline / Headline</label>
        <input type='text' id='headline' placeholder='Full Stack Developer | Open Source Enthusiast'>
      </div>
      <div class='input-group'>
        <label>Bio</label>
        <textarea id='bio' placeholder='Write a short, engaging bio...'></textarea>
      </div>
      <div class='input-group'>
        <label>Location</label>
        <input type='text' id='location' placeholder='City, Country'>
      </div>
      <div class='input-group'>
        <label>Current Focus</label>
        <input type='text' id='focus' placeholder='Building scalable web apps with React & Node.js'>
      </div>
    </div>
  </div>
  <div class='panel' id='panel-1'>
    <div class='section'>
      <div class='section-title'>Select Your Tech Stack</div>
      <div class='skills-grid' id='skillsGrid'></div>
    </div>
    <div class='section' style='margin-top:20px'>
      <div class='input-group'>
        <label>Custom Skills (comma separated)</label>
        <input type='text' id='customSkills' placeholder='Rust, Go, Kafka, Terraform'>
      </div>
    </div>
  </div>
  <div class='panel' id='panel-2'>
    <div class='section'>
      <div class='section-title'>GitHub Stats Cards</div>
      <div class='toggle-row'>
        <span class='toggle-label'>Show GitHub Stats</span>
        <div class='switch active' onclick='toggle(this, &quot;stats&quot;)'></div>
      </div>
      <div class='toggle-row'>
        <span class='toggle-label'>Show Top Languages</span>
        <div class='switch active' onclick='toggle(this, &quot;langs&quot;)'></div>
      </div>
      <div class='toggle-row'>
        <span class='toggle-label'>Show Streak Stats</span>
        <div class='switch' onclick='toggle(this, &quot;streak&quot;)'></div>
      </div>
      <div class='toggle-row'>
        <span class='toggle-label'>Show Trophy</span>
        <div class='switch' onclick='toggle(this, &quot;trophy&quot;)'></div>
      </div>
    </div>
    <div class='section' style='margin-top:20px'>
      <div class='section-title'>Social Links</div>
      <div class='input-group'>
        <label>Twitter / X</label>
        <input type='text' id='twitter' placeholder='username'>
      </div>
      <div class='input-group'>
        <label>LinkedIn</label>
        <input type='text' id='linkedin' placeholder='username'>
      </div>
      <div class='input-group'>
        <label>Portfolio Website</label>
        <input type='text' id='website' placeholder='https://...'>
      </div>
      <div class='input-group'>
        <label>Email</label>
        <input type='text' id='email' placeholder='hello@example.com'>
      </div>
    </div>
    <div class='section' style='margin-top:20px'>
      <div class='section-title'>Theme</div>
      <div class='theme-dots'>
        <div class='theme-dot active' style='background:#1a1a1a' onclick='setTheme(&quot;dark&quot;, this)'></div>
        <div class='theme-dot' style='background:#f0f0f0;border:1px solid #ccc' onclick='setTheme(&quot;light&quot;, this)'></div>
        <div class='theme-dot' style='background:#2563eb' onclick='setTheme(&quot;blue&quot;, this)'></div>
        <div class='theme-dot' style='background:#7c3aed' onclick='setTheme(&quot;purple&quot;, this)'></div>
        <div class='theme-dot' style='background:#16a34a' onclick='setTheme(&quot;green&quot;, this)'></div>
      </div>
    </div>
  </div>
  <div class='panel' id='panel-3'>
    <div class='preview-box'>
      <div class='preview-header'>
        <span class='preview-title'>README.md Preview</span>
        <button class='copy-btn' onclick='copyCode()'>Copy Markdown</button>
      </div>
      <pre id='preview'></pre>
    </div>
  </div>
</div>
<script>
const skills = [
  'JavaScript','TypeScript','Python','Java','C++','Go','Rust',
  'React','Vue','Next.js','Node.js','Django','Flask','Spring',
  'PostgreSQL','MongoDB','Redis','Docker','Kubernetes','AWS',
  'Git','GitHub Actions','Linux','Figma','Tailwind CSS'
];
const skillsGrid = document.getElementById('skillsGrid');
skills.forEach(s => {
  const tag = document.createElement('div');
  tag.className = 'skill-tag';
  tag.textContent = s;
  tag.onclick = () => tag.classList.toggle('selected');
  skillsGrid.appendChild(tag);
});

let toggles = { stats: true, langs: true, streak: false, trophy: false };
let theme = 'dark';

function switchTab(n) {
  document.querySelectorAll('.tab').forEach((t,i) => t.classList.toggle('active', i===n));
  document.querySelectorAll('.panel').forEach((p,i) => p.classList.toggle('active', i===n));
  if (n === 3) generatePreview();
}

function toggle(el, key) {
  el.classList.toggle('active');
  toggles[key] = el.classList.contains('active');
}

function setTheme(t, el) {
  theme = t;
  document.querySelectorAll('.theme-dot').forEach(d => d.classList.remove('active'));
  el.classList.add('active');
}

function generatePreview() {
  const name = document.getElementById('name').value || 'Your Name';
  const headline = document.getElementById('headline').value;
  const bio = document.getElementById('bio').value;
  const loc = document.getElementById('location').value;
  const focus = document.getElementById('focus').value;
  const selectedSkills = Array.from(document.querySelectorAll('.skill-tag.selected')).map(s => s.textContent);
  const custom = document.getElementById('customSkills').value.split(',').map(s => s.trim()).filter(s => s);
  const allSkills = [...selectedSkills, ...custom];
  const twitter = document.getElementById('twitter').value;
  const linkedin = document.getElementById('linkedin').value;
  const website = document.getElementById('website').value;
  const email = document.getElementById('email').value;
  
  let md = `<div align=&quot;center&quot;>\n\n`;
  md += `# Hi, I'm ${name} 👋\n\n`;
  if (headline) md += `**${headline}**\n\n`;
  md += `</div>\n\n`;
  
  if (bio) md += `## About Me\n\n${bio}\n\n`;
  if (loc || focus) {
    md += `<table>\n<tr>\n`;
    if (loc) md += `<td>📍 ${loc}</td>\n`;
    if (focus) md += `<td>🔭 ${focus}</td>\n`;
    md += `</tr>\n</table>\n\n`;
  }
  
  if (allSkills.length) {
    md += `## Tech Stack\n\n`;
    md += `<p align=&quot;center&quot;>\n`;
    allSkills.forEach(s => {
      md += `<img src=&quot;https://img.shields.io/badge/-${encodeURIComponent(s.replace(/-/g,'--'))}-333?style=flat-square&amp;logo=${encodeURIComponent(s.toLowerCase().replace(/[^a-z]/g,''))}&amp;logoColor=white&quot; /> `;
    });
    md += `\n</p>\n\n`;
  }
  
  if (toggles.stats || toggles.langs || toggles.streak) {
    md += `## GitHub Stats\n\n<div align=&quot;center&quot;>\n\n`;
    if (toggles.stats) md += `<img src=&quot;https://github-readme-stats.vercel.app/api?username=${name}&amp;show_icons=true&amp;theme=${theme}&amp;hide_border=true&amp;count_private=true&quot; height=&quot;150&quot; />\n`;
    if (toggles.langs) md += `<img src=&quot;https://github-readme-stats.vercel.app/api/top-langs/?username=${name}&amp;layout=compact&amp;theme=${theme}&amp;hide_border=true&quot; height=&quot;150&quot; />\n`;
    if (toggles.streak) md += `<img src=&quot;https://github-readme-streak-stats.herokuapp.com/?user=${name}&amp;theme=${theme}&amp;hide_border=true&quot; height=&quot;150&quot; />\n`;
    md += `\n</div>\n\n`;
  }
  
  if (toggles.trophy) {
    md += `## Trophies\n\n<div align=&quot;center&quot;>\n  <img src=&quot;https://github-profile-trophy.vercel.app/?username=${name}&amp;theme=${theme}&amp;no-frame=true&amp;row=1&quot; />\n</div>\n\n`;
  }
  
  const socials = [];
  if (twitter) socials.push(`<a href=&quot;https://twitter.com/${twitter}&quot;><img src=&quot;https://img.shields.io/badge/-@${twitter}-1DA1F2?style=flat-square&amp;logo=twitter&amp;logoColor=white&quot; /></a>`);
  if (linkedin) socials.push(`<a href=&quot;https://linkedin.com/in/${linkedin}&quot;><img src=&quot;https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&amp;logo=linkedin&amp;logoColor=white&quot; /></a>`);
  if (website) socials.push(`<a href=&quot;${website}&quot;><img src=&quot;https://img.shields.io/badge/-Portfolio-000?style=flat-square&amp;logo=firefox&amp;logoColor=white&quot; /></a>`);
  if (email) socials.push(`<a href=&quot;mailto:${email}&quot;><img src=&quot;https://img.shields.io/badge/-Email-EA4335?style=flat-square&amp;logo=gmail&amp;logoColor=white&quot; /></a>`);
  
  if (socials.length) {
    md += `## Connect With Me\n\n<p align=&quot;center&quot;>\n  ${socials.join('\n  ')}\n</p>\n\n`;
  }
  
  md += `---\n\n<div align=&quot;center&quot;>\n  <img src=&quot;https://komarev.com/ghpvc/?username=${name}&amp;style=flat-square&quot; alt=&quot;Profile views&quot; />\n</div>`;
  
  document.getElementById('preview').textContent = md;
}

function copyCode() {
  const code = document.getElementById('preview').textContent;
  navigator.clipboard.writeText(code).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = 'Copied!';
    btn.classList.add('copied');
    setTimeout(() => {
      btn.textContent = 'Copy Markdown';
      btn.classList.remove('copied');
    }, 2000);
  });
}

// Initialize preview on load
generatePreview();
</script>
</body>
</html>" style="width:100%;height:600px;border:none;border-radius:12px;"></iframe>
