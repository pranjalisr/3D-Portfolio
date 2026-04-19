## Features

* Single HTML file — no build step, no npm, no framework. Drop it anywhere and it works.
* CONFIG-driven — every word on the page (name, experience, projects, skills, resume) lives in one JavaScript object at the top of the script. Fork and fill in your details in minutes.
* Animated 2D neural network background — pure Canvas API, no Three.js, no heavy libraries. Signal pulses travel along layer edges in real time.
* Embedded PDF resume — base64-encoded directly in the file. Preview, download, and full-screen view all work without a server.
* Typing animation — rotating phrases in the hero section driven by the config array.
* Scroll reveal animations — sections fade up as you scroll.
* Custom cursor — magnetic cursor ring that reacts to hover states.
* Fully responsive — mobile nav, responsive grids, fluid typography.
* One-click deploy — drag the file to Netlify and get a live URL in ~10 seconds.


## Tech Stack
| Layer        | Technology                       |
| ------------ | -------------------------------- |
| Structure    | HTML5                            |
| Styling      | CSS3 (Flexbox, Grid, Animations) |
| Logic        | Vanilla JavaScript (ES6+)        |
| Animation    | Canvas 2D API                    |
| Fonts        | Google Fonts (Syne, DM Sans)     |
| Hosting      | Netlify                          |
| Dependencies | None                             |


## How to Fork & Personalise
* Step 1 — Clone or download
* bashgit clone https://github.com/pranjalisr/3D-Portfolio.git
* cd 3D-Portfolio
* Or just download index.html directly.
  
* Step 2 — Open in any text editor
* VS Code, Notepad, Sublime — anything works.
  
* Step 3 — Find the CONFIG block
* Near the top of the <script> tag you'll see:
  
 ★  PERSONAL CONFIGURATION — EDIT EVERYTHING IN THIS BLOCK  ★
 
 * Edit the CONFIG object. Every field has an inline comment explaining what it does:

* Step 4 — Replace the resume PDF
  
  Convert your PDF to a base64 string and paste it as RESUME_BASE64.
 
  Mac / Linux:
 
  bashbase64 -i your_resume.pdf | tr -d '\n'
 
  Windows (PowerShell):
 
  powershell[Convert]::ToBase64String([IO.File]::ReadAllBytes("your_resume.pdf"))
  
  Copy the entire output string and replace the existing value of RESUME_BASE64 in the CONFIG.

*  Step 5 — Preview locally
  
   Just open the file in your browser:
 
   bashopen index.html        # Mac
 
   start index.html       # Windows
 
   xdg-open index.html    # Linux
 
   Or use VS Code's Live Server extension for auto-refresh on save.

* Deploy to Netlify (free, public URL, 1 minute)
  
* Option A — Drag & Drop (no CLI needed)

  Go to netlify.com and sign up (free)

  Create a folder called portfolio/ and put index.html inside it
 
  On the Netlify dashboard → Add new site → Deploy manually
 
  Drag and drop the portfolio/ folder onto the page
 
  Your site is live at https://random-name.netlify.app
 
  Rename it under Site Settings → Site name

* Option B — GitHub + Auto-deploy

  Push this repo to GitHub
 
  Netlify → Add new site → Import from Git → select your repo
 
  Build command: (leave blank)
 
  Publish directory: .
 
  Every git push automatically redeploys your live site


* Customisation Tips
  
  Adding a new project card:
 
  Find projects: in the CONFIG array and add a new object following the same structure. The page renders it automatically.
 
  Adding a new experience entry:
 
  Find experience: in the CONFIG array and add a new object. Order in the array = order on the page.
 
  Changing the typing phrases:
 
  Edit the typingPhrases array. Add as many strings as you want — the animation cycles through all of them.
 
  

* License
  
MIT — free to fork, personalise, and deploy. Attribution appreciated but not required.
