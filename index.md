(Will never be fully updated, so stay tuned!)
## Research Interests

- Numerical hydrodynamics
- Planet-disk interactions
- 

Claim offer
i am making a website on github, i just chose the minima theme, whcih is fine in _config.yml
theme: jekyll-theme-minimal

i did this, now i am unable to understand, can i put some cool astro stuff and customize it, and how am i supposed to link my other stuff? and how to edit basically 

Yes — the theme: jekyll-theme-minimal line just gives you a starting layout. You can absolutely turn it into a full astro-themed personal/research website with custom pages, images, animations, plots, papers, simulations, etc.

Right now your GitHub Pages site is basically:

a Jekyll site

using the Minimal theme

with markdown + HTML support

customizable through files/folders

The key thing is: you are not locked into the theme. The theme only provides defaults.

How GitHub Pages Structure Works
Your repo probably looks something like:

your-repo/
│
├── _config.yml
├── index.md
├── README.md
You can add:

├── assets/
│   ├── images/
│   ├── css/
│   └── videos/
│
├── papers/
├── simulations/
├── blog/
├── about.md
├── projects.md
└── index.md
The Main Files You Edit
1. _config.yml
Controls global settings.

Example:

title: Gopika SM
description: Dust dynamics | Protoplanetary disks | Computational astrophysics
theme: jekyll-theme-minimal

logo: /assets/images/profile.png

show_downloads: false
2. index.md
This is your homepage.

Example:

# Gopika SM

Astrophysics student working on dust-gas interactions in protoplanetary disks.

## Research

- Dust trapping
- Planet-disk interactions
- Symplectic integrators

## Projects

- [Gap classification](projects.md)
- [Simulations](simulations.md)
Markdown is enough for basic stuff.

YES — You Can Add Cool Astro Stuff
You can add:

JWST backgrounds

Animated stars

Simulation GIFs/videos

Interactive plots

Research pages

CV

Publications

Particle trajectory visualizations

Embedded YouTube videos

Custom CSS

Dark mode

Custom fonts

Even full HTML pages

Easiest Customization Path
Step 1 — Add CSS
Create:

assets/css/style.scss
Put:

---
---

@import "{{ site.theme }}";

body {
    background-color: black;
    color: white;
    font-family: "Helvetica";
}

a {
    color: #66ccff;
}
Now your whole site changes style.

Add Astro Background
You can do:

body {
    background-image: url('/assets/images/jwst.jpg');
    background-size: cover;
    background-attachment: fixed;
}
Put the image in:

assets/images/jwst.jpg
How To Add Pages
Create a file:

projects.md
Inside:

---
title: Projects
---

# Research Projects

## Dust Gap Simulations

Description here.

![gap image](/assets/images/gap.png)
Then link from homepage:

[Projects](projects.md)
How To Add PDFs / Papers
Put PDF in:

assets/papers/my_paper.pdf
Then:

[Read my paper](/assets/papers/my_paper.pdf)
How To Add Images
Put image in:

assets/images/
Then:

![Simulation](/assets/images/sim.png)
How To Add Videos/GIFs
GIF:

![Orbit](/assets/images/orbit.gif)
Video:

<video width="700" controls>
  <source src="/assets/videos/sim.mp4" type="video/mp4">
</video>
How To Edit Properly
The easiest workflow:

Option A — GitHub Web Editor
Just click files directly on GitHub and edit.

Good for:

markdown

small changes

Option B — VS Code (better)
Clone repo locally:

git clone https://github.com/yourname/yourrepo.git
Edit files in VS Code.

Push changes:

git add .
git commit -m "update"
git push
GitHub Pages automatically rebuilds site.

VERY IMPORTANT
If your repo is:

username.github.io
then your site becomes:

https://username.github.io
Otherwise:

https://username.github.io/reponame
A Really Good Structure For Your Case
Honestly for astro/research stuff I'd do:

Home
About
Research
Simulations
Publications
CV
Blog
Contact
And on the homepage:

dark theme

space background

simulation GIF banner

quick intro

research interests

featured plots

You Can Even Override The Entire Theme
Eventually you can ignore Minimal entirely and use:

custom HTML

custom layouts

Bootstrap

Tailwind

full React frontend

But for now:

markdown + CSS is easiest

enough to make it look very good

Minimal Example Homepage
# Gopika SM

Computational astrophysics • Protoplanetary disks • Dust dynamics

![simulation](/assets/images/sim.gif)

## Research Interests

- Dust-gas interactions
- Planet-driven gaps
- Numerical simulations

## Links

- [Projects](projects.md)
- [CV](assets/papers/cv.pdf)
- [GitHub](https://github.com/yourusername)
One More Important Thing
GitHub Pages with Jekyll supports:

Markdown

HTML

CSS

some JavaScript

But not backend stuff like:

Python servers

Flask

databases

So it’s best for:

portfolio

research website

static visualizations

blogs/documentation

Which is perfect for your use case.




what about my readme.md

README.md is different from your website pages.

People confuse these a lot on GitHub.

README.md
This is mainly for the GitHub repository page itself.

When someone visits:

github.com/yourname/yourrepo
the README is what shows below the files.

It is meant for:

project description

installation instructions

screenshots

documentation

research/project overview

Your Actual Website
Your website homepage is usually:

index.md
or

index.html
NOT the README.

Important Exception
If your repo is specifically:

username.github.io
then GitHub Pages may sometimes render the README content as homepage IF no index.md or index.html exists.

But once you create:

index.md
that becomes the actual homepage.

Recommended Setup
Keep:

README.md
for repository info.

Use:

index.md
for the website.

Example
README.md
# Dust Gap Simulations

Numerical simulations of dust-gas interactions in protoplanetary disks.

## Features

- Symplectic integrator
- Gas drag
- Planet interactions
This appears on GitHub repo page.

index.md
# Gopika SM

Computational astrophysics researcher.

![simulation](/assets/images/sim.gif)

## Research Interests

- Dust dynamics
- Planet-disk interactions
This appears on your website.

You Can Link Between Everything
For example on website:

[GitHub Repository](https://github.com/yourname/repo)
And inside README:

[Project Website](https://yourname.github.io)
Good Strategy
README.md = technical/project documentation
Website = portfolio/research presentation
That separation works really well.




Gopika SM
View My GitHub Profile

Gopika SM
Graduate Student at Purdue University, working on computational astrophysics, especially on protoplanetary disks at the moment.

Research Interests
Numerical Hydrodynamics in Astrophysics
Planet- Disk interactions
Anything that involves disks, always amused about how some structures are everywhere.
Hosted on GitHub Pages — Theme by orderedlist

this is how it looks now, gopika appears twice tho

Yeah, that happens because the Minimal theme automatically displays:

your site title

your description

AND then your index.md probably also contains:

# Gopika SM
So you're getting:

theme-generated title

your own heading

Fix Options
Option 1 (recommended)
Let the theme handle the name.

So in index.md, REMOVE:

# Gopika SM
and just start with content like:

Graduate Student at Purdue University, working on computational astrophysics, especially protoplanetary disks.

## Research Interests

- Numerical hydrodynamics
- Planet-disk interactions
- Dust dynamics
This is the cleanest solution.

Option 2
Keep your custom heading and hide theme title.

In _config.yml:

title: ""
or remove title entirely.

But usually Minimal theme looks nicer with the sidebar title intact.

What’s Happening Internally
Minimal theme basically creates:

<h1>{{ site.title }}</h1>
from _config.yml.

Then your markdown creates another:

# Gopika SM
which becomes another <h1>.

Hence duplication.

What I’d Personally Suggest For Your Site
Something like:

Sidebar:

Gopika SM
Computational Astrophysics
Purdue University
Main page:

Graduate student working on computational astrophysics and protoplanetary disk dynamics.

## Current Research

- Dust-gas interactions
- Planet-driven gap formation
- Numerical simulations

## Links

- CV
- GitHub
- Research Projects
That layout works really well with the Minimal theme.


im on windows how to connect my visual studio to this?

Assuming you already created the GitHub repo and GitHub Pages site, here’s the clean Windows + VS Code workflow.

Step 1 — Install Git
Download:

Git for Windows

Install with default options.

Then open:

Git Bash
and test:

git --version
Step 2 — Install VS Code
Download:

Visual Studio Code

During installation, CHECK:

“Add to PATH”

“Open with Code”

Step 3 — Get Your Repo URL
Go to your GitHub repo.

Click:

Code → HTTPS
Copy something like:

https://github.com/yourusername/yourrepo.git
Step 4 — Clone Repo Locally
Open Git Bash in the folder where you want the website.

Example:

cd Desktop
Then:

git clone https://github.com/yourusername/yourrepo.git
Now enter repo:

cd yourrepo
Step 5 — Open In VS Code
Run:

code .
This opens the entire website folder in VS Code.

Now you can edit:

_config.yml

index.md

CSS

images

everything

Step 6 — Make Changes
Example:

Edit:

index.md
Save.

Step 7 — Push Changes To GitHub
Inside VS Code terminal OR Git Bash:

git add .
git commit -m "updated homepage"
git push
Refresh your website after ~10–30 seconds.

GitHub Pages auto-deploys.

SUPER IMPORTANT
If Git asks identity first time:

git config --global user.name "Your Name"
git config --global user.email "your@email.com"
Use same email as GitHub.

Recommended VS Code Extensions
Install:

Markdown All in One

GitHub Pull Requests

Prettier

Jekyll Syntax Support

Nice Workflow
You’ll basically do:

Edit → Save → git add . → git commit → git push
and site updates automatically.

Optional: Run Website Locally
Later you can install Ruby + Jekyll and preview locally before pushing.

But honestly for now:

edit

push

refresh website

is enough.

Folder Setup I Recommend
yourrepo/
│
├── _config.yml
├── index.md
├── assets/
│   ├── css/
│   ├── images/
│   └── videos/
├── projects.md
├── research.md
├── cv.md
└── simulations.md
VERY Useful Trick
In markdown:

![image](/assets/images/test.png)
means:

image path starts from repo root

easier than relative paths

Another Useful Thing
If your website breaks after editing _config.yml, it’s usually:

spacing issue

tabs instead of spaces

missing ---

YAML is very picky.


i have vscode i have done git cloning and modifications before too so im curios

Then you’re basically already set up — a GitHub Pages/Jekyll site is just another git repo.

The workflow is literally:

clone repo → edit files in VS Code → git push
The only new thing is understanding which files affect the website.

Main Things You’ll Edit
_config.yml
Global settings.

Example:

title: Gopika SM
description: Computational Astrophysics
theme: jekyll-theme-minimal
index.md
Homepage content.

assets/css/style.scss
Custom styling.

This is where the fun astro styling happens.

Minimal Theme Is Just A Base
You can slowly transform it into something much cooler.

For example:

body {
    background-color: #050816;
    color: #e6f1ff;
    font-family: "Helvetica";
}

a {
    color: #64b5ff;
}

h1, h2 {
    color: #ffffff;
}
Easy Astro Upgrade Path
Phase 1
dark mode

better fonts

JWST background

custom links

research pages

Phase 2
animated stars

particle GIFs

embedded simulations

cards/grids

Phase 3
custom HTML layouts

JavaScript visualizations

interactive plots

Where To Put Stuff
Images
assets/images/
PDFs
assets/papers/
CSS
assets/css/
One Important GitHub Pages Thing
Sometimes changes don’t appear because GitHub Pages rebuild takes ~30 sec.

Also:

hard refresh browser

clear cache if CSS seems unchanged

Easiest Cool Improvement Right Now
Make:

assets/css/style.scss
with:

---
---

@import "{{ site.theme }}";

body {
    background-color: #02050f;
    color: #d6e2ff;
}

a {
    color: #7cc7ff;
}
Instantly becomes much nicer.

Another Nice Thing
You can use raw HTML directly inside markdown.

Example:

<div style="text-align:center">
    <img src="/assets/images/disk.png" width="600">
</div>
or even videos:

<video autoplay loop muted width="700">
  <source src="/assets/videos/sim.mp4" type="video/mp4">
</video>
So you are not limited to plain markdown at all.

Honestly Your Use Case Fits GitHub Pages Very Well
Because:

research website

static visualizations

simulation media

publications

blog/project notes

That’s exactly what many astro/math/physics people use it for.




can i creaete my own theme?

Absolutely. And that’s eventually what most good GitHub Pages sites become.

Right now:

theme: jekyll-theme-minimal
just imports somebody else’s layouts + CSS.

But you can override parts gradually or completely replace everything.

There Are 3 Levels Of Customization
Level 1 — Modify Existing Theme (recommended now)
Keep:

theme: jekyll-theme-minimal
Then add your own CSS:

assets/css/style.scss
This overrides the theme styling.

Very easy.

Level 2 — Override Theme Layouts
You can override theme HTML files.

Create folders like:

_layouts/
_includes/
Example:

_layouts/default.html
This replaces the theme’s page structure.

At this point you control:

sidebar

navbar

footer

spacing

structure

while still using Jekyll.

Level 3 — Fully Custom Theme
Remove:

theme: jekyll-theme-minimal
Then build everything yourself.

You create:

HTML layouts

CSS

navigation

styling

animations

basically a full custom static site.

What Most People Actually Do
Usually:

Start with theme
→ override CSS
→ override layouts
→ eventually fully custom
That’s the sane path.

Example Custom Layout
You can literally make:

<!DOCTYPE html>
<html>
<head>
  <title>{{ page.title }}</title>
  <link rel="stylesheet" href="/assets/css/style.css">
</head>

<body>

<div class="sidebar">
  <h1>Gopika SM</h1>
  <p>Computational Astrophysics</p>
</div>

<div class="content">
  {{ content }}
</div>

</body>
</html>
Then every page injects into:

{{ content }}
That’s basically how themes work internally.

You Can Make It VERY Astro
You could have:

starfield backgrounds

nebula overlays

orbit animations

particle motion

terminal-style sections

simulation galleries

research cards

dark glassmorphism UI

parallax scrolling

animated equations

All possible with:

HTML

CSS

a little JavaScript

Honestly: Jekyll Is Just A Static Site Generator
People think “theme” means locked template.

Not really.

Jekyll simply:

reads markdown

injects into layouts

generates static HTML

You control almost everything.

One Thing To Understand
This:

# Hello
eventually becomes:

<h1>Hello</h1>
inside your layout.

That’s all Jekyll is doing.

If You Want Maximum Freedom Later
Eventually many people move to:

Astro

Hugo

Next.js

React/Vite

instead of Jekyll.

BUT for a research portfolio:
GitHub Pages + Jekyll is honestly perfect and simple.

Especially initially.

My Recommendation For You
Do this progression:

Now
keep minimal theme

customize CSS heavily

Later
override layouts

create navbar/pages

Much Later
fully custom theme if you want

You do NOT need to understand all of Jekyll immediately.


this html thing goes where

The HTML goes into layout files or page files depending on what you want to customize.

Here’s the actual structure.

OPTION 1 — Put HTML Directly In A Page
For example inside:

index.md
you can literally do:

# Welcome

This is my website.

<div style="text-align:center">
  <img src="/assets/images/disk.png" width="500">
</div>
Markdown + HTML can mix freely.

This is easiest.

OPTION 2 — Create A Full HTML Homepage
Instead of index.md, make:

index.html
Example:

---
layout: default
---

<h1>Gopika SM</h1>

<p>Computational astrophysics researcher.</p>

<img src="/assets/images/disk.png" width="600">
This gives much more control.

OPTION 3 — Create Custom Layouts (important)
This is where themes are actually controlled.

Create folder:

_layouts/
Then:

_layouts/default.html
Inside:

<!DOCTYPE html>
<html>

<head>
    <title>{{ page.title }}</title>
    <link rel="stylesheet" href="/assets/css/style.css">
</head>

<body>

<div class="sidebar">
    <h1>Gopika SM</h1>
</div>

<div class="content">
    {{ content }}
</div>

</body>
</html>
Now every page using:

layout: default
gets inserted into:

{{ content }}
Example Full Structure
yourrepo/
│
├── _config.yml
├── index.md
│
├── _layouts/
│   └── default.html
│
├── assets/
│   ├── css/
│   │   └── style.css
│   │
│   └── images/
│       └── disk.png
VERY IMPORTANT
Every markdown page usually starts with:

---
layout: default
title: Home
---
This is called front matter.

Without it, Jekyll may not apply layouts properly.

Simplest Custom Theme Setup
Honestly, if I were you:

Keep:
theme: jekyll-theme-minimal
Add:
assets/css/style.scss
Later:
_layouts/default.html
That’s the smoothest progression.

Important Mental Model
Think:

Markdown = content
HTML layout = structure
CSS = appearance
That’s basically the whole website system.


im not planning to add images now so 

Then honestly don’t even touch custom layouts yet.

You can already make the site look clean just with:

index.md

_config.yml

one CSS file

That’s enough initially.

Minimal Good Setup
_config.yml
title: Gopika SM
description: Computational Astrophysics | Purdue University
theme: jekyll-theme-minimal
index.md
Graduate student at Purdue University working on computational astrophysics, especially protoplanetary disks.

## Research Interests

- Numerical hydrodynamics
- Planet-disk interactions
- Dust-gas dynamics
- Computational astrophysics

## Current Work

Studying dust trapping and gap formation in protoplanetary disks using numerical simulations.

## Links

- [GitHub](https://github.com/yourusername)
Then Add One CSS File
Create:

assets/css/style.scss
Put:

---
---

@import "{{ site.theme }}";

body {
    background-color: #050816;
    color: #dce6ff;
    font-family: Helvetica, sans-serif;
}

a {
    color: #7cc7ff;
}

h1, h2, h3 {
    color: white;
}
Then In _config.yml
Add:

title: Gopika SM
description: Computational Astrophysics | Purdue University
theme: jekyll-theme-minimal

plugins:
  - jekyll-feed
Actually Minimal theme automatically loads style.scss if structured properly, so usually no extra linking needed.

Result
You get:

dark astro aesthetic

clean typography

custom colors

simple research website

without touching HTML/layouts yet.

That’s honestly the best starting point.



- Numerical hydrodynamics
- Planet-disk interactions
- Absolutely all in for anything in hydrodynamics in Astrophysics.

i need to add a point like this what exactly i shoudl write

Your idea is good, it just needs slightly smoother wording. Here are some versions that sound natural on an academic/research site.

Good concise versions
- Numerical hydrodynamics
- Planet-disk interactions
- Broadly interested in hydrodynamical phenomena across astrophysics
or

- Numerical hydrodynamics
- Planet-disk interactions
- Fascinated by hydrodynamics and disk physics throughout astrophysics
or slightly more personal:

- Numerical hydrodynamics
- Planet-disk interactions
- Interested in almost anything involving hydrodynamics in astrophysics
or more polished/professional:

- Numerical hydrodynamics
- Planet-disk interactions
- Broad interests in computational and theoretical astrophysical fluid dynamics
I think this one fits your tone best:

- Numerical hydrodynamics
- Planet-disk interactions
- Interested in hydrodynamical phenomena across astrophysics, especially disk systems
It keeps the enthusiasm without sounding too informal for a research webpage.


whenever i change my theme to anything other than this idk i see no change basically, i wanted to have caymen it looks about the same 

That’s actually normal with GitHub Pages themes, especially if:

you already have custom content

the browser cached the CSS

the theme only changes layout subtly

your repo already overrides theme styling

Also, jekyll-theme-minimal and jekyll-theme-cayman are very different normally, so if they look identical, one of these is happening:

Most Common Cause: Browser Cache
Do a hard refresh.

On Windows:

Ctrl + Shift + R
or

Ctrl + F5
This fixes it surprisingly often.

Make Sure _config.yml Is Correct
For Cayman:

theme: jekyll-theme-cayman
NOT:

jekyll-theme-caymen
(spelling mistake is common)

Wait For GitHub Pages Rebuild
After pushing changes:

wait ~30–60 sec

refresh site

GitHub Pages rebuild is not instant.

Check If You Overrode CSS Already
If you created:

assets/css/style.scss
and imported/customized things heavily, your CSS may dominate the theme appearance.

Especially if you changed:

background

fonts

layout widths

colors

Then themes start looking similar.

Cayman Usually Looks Like:
large colored banner header

centered content

modern buttons

wider layout

while Minimal:

left sidebar

compact layout

So if you still see sidebar layout, Cayman is probably not loading.

VERY Important GitHub Pages Detail
GitHub Pages only supports certain themes automatically.

Cayman IS supported, but sometimes you must remove conflicting plugins/custom layouts.

Check GitHub Pages Build Errors
Go to:

Repo → Settings → Pages
Sometimes it says:

failed build

invalid YAML

unsupported config

Another Common Cause
If you have:

_layouts/default.html
then your custom layout overrides the theme layout entirely.

So changing themes won’t visually change much anymore.

Easiest Test
Temporarily make repo ultra minimal:

_config.yml
theme: jekyll-theme-cayman
title: Test
index.md
# Hello
Push.

If it changes drastically:
→ your custom files were overriding theme.

If not:
→ cache/build issue.

Honestly
Themes are mostly:

starter layouts

starter CSS

People often expect WordPress-level transformations, but Jekyll themes are simpler than that.


i want to do something like this too

## Things I did in my Pre-Purdue era

I have done so 

i knowthsi is wayt oo casual so lmk what

Yeah, that exact phrasing is a bit too informal for a research/academic site, especially if this is going on your homepage or “About” section.

You want something that still feels human, but more like a professional portfolio.

Better ways to say it
Clean + professional
## Pre-Purdue Experience

A brief overview of work and projects completed prior to beginning graduate studies at Purdue University.
Slightly more personal (still safe)
## Pre-Purdue Experience

Selected projects and academic work completed prior to joining Purdue University.
If you want the “story” feel but still formal
## Pre-Purdue Experience

Before beginning graduate studies at Purdue University, I worked on several projects in computational and theoretical astrophysics.
If you want to keep your tone but fix the casualness
Instead of:

“Things I did in my Pre-Purdue era”

Use:

## Pre-Purdue Work
or

## Work Prior to Purdue
What NOT to use
Avoid:

“era” (too social-media-ish)

“things I did”

“I have done so” (unfinished, sounds abrupt)

slangy phrasing

Best fit for your site
Given your astrophysics + computational focus, this is the sweet spot:

## Pre-Purdue Experience

Selected research and computational projects completed prior to graduate studies at Purdue University.
If you want, I can also help you structure that section so it looks like a proper research portfolio (projects → methods → tools → results).




%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Medium Length Professional CV
% LaTeX Template
% Version 2.0 (8/5/13)
%
% This template has been downloaded from:
% http://www.LaTeXTemplates.com
%
% Original author:
% Trey Hunner (http://www.treyhunner.com/)
%
% Important note:
% This template requires the resume.cls file to be in the same directory as the
% .tex file. The resume.cls file provides the resume style used for structuring the
% document.
%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%----------------------------------------------------------------------------------------
%	PACKAGES AND OTHER DOCUMENT CONFIGURATIONS
%----------------------------------------------------------------------------------------
\linespread{0.8}
\documentclass{resume} % Use the custom resume.cls style
\usepackage{blindtext}
\usepackage{amsmath}
\usepackage{fontawesome}
\usepackage{xcolor}
\usepackage{hyperref}
\usepackage{multicol}
\usepackage{setspace}

\hypersetup{
    colorlinks=true,
    linkcolor=cyan,
    filecolor=magenta,      
    urlcolor=blue,
    pdftitle={Overleaf Example},
    pdfpagemode=FullScreen,
    }
    
\urlstyle{same}
\usepackage[left= 0.8in,top=0.8in,right=0.8in,bottom=0.7in]{geometry} % Document margins
\newcommand{\tab}[1]{\hspace{.2\textwidth}\rlap{#1}}
\newcommand{\itab}[1]{\hspace{0em}\rlap{#1}}
\name{\large \textbf{Gopika SM}} % Your name
 % Your address
%\address{123 Pleasant Lane \\ City, State 12345} % Your secondary addess (optional)
\address{Email:  smg@purdue.edu  \\  gopikanlsr@gmail.com  } % Your phone number and email

\begin{document}

%----------------------------------------------------------------------------------------
%	ACADEMIC PROFILE SECTION
%----------------------------------------------------------------------------------------


\begin{rSection}{Research interests}

%\item[$\circ$] I am broadly interested in Gravitational wave physics. I intend to explore more aspects of this field during my higher studies, though currently, I find compact objects really interesting.

%\item[$\circ$]Primarily interested in Relativistic Astrophysics, GRMHD and Relativistic Hydrodynamics.
%\item[$\circ$] Currently focusing on compact astrophysical objects and their dynamics, such as accretion,\ relativistic jets and feedback. %I would like to explore the fields such as stellar dynamics, intergalactic medium etc., as well.


%\item[$\circ$] I am broadly interested in astrophysical fluids, with a current interest in compact objects and accretion physics, and relativistic jets. 

%\item[$\circ$]I would also like to explore the fields such as galaxy formation, dark matter, ISM, and other aspects of Cosmology.
%\item[$\circ$] I am broadly interested in Astrophysical fluids; varies from sun to black holes . I have been involved in research on compact objects and Relativistic Astrophysics. I really admire how computational methods have improved our understanding of different astrophysical phenomena and topics.
Computational astrophysics and astrophysical fluid dynamics, particularly the dynamics of gas and dust in protoplanetary disks and planet-disk interactions. Interested in developing numerical simulations to study disk substructures, dust evolution, and planet formation processes.
%\item[$\circ$]I am currently looking for a project where I can explore numerical/data analysis/ theoretical modeling in the above topics.


%\item[$\circ$] I also find interest in making use of data analysis and machine learning techniques to understand the underlying physics in Cosmology.
%\item[$\circ$] I am interested in the study of compact objects in general.
%\item[$\circ$] I am mainly interested in understanding the feedback and jet mechanisms of compact astrophysical objects using GR and Magnetohydrodynamics.
%\item[$\circ$] I also find Numerical Relativity interesting. 

\end{rSection}

\begin{rSection}{Academic Profile}
{\bf Purdue University, Indiana} \hfill {Aug 2024 -  Present}
\\
Department of Physics and Astronomy\\
Graduate Programme \hfill {\textbf{GPA : 4 / 4}} \\
{\bf Tata Institute of Fundamental Research, Mumbai} \hfill {Aug 2023 - April 2024}
\\ 
{\bf Indian Institute of Science Education and Research Kolkata} \hfill {Aug 2018 - June 2023} \\
Department of Physical Sciences (\textit{Major: Physics}) \\
5 year BS-MS Dual Degree Program \hfill {\textbf{GPA : 8.6 / 10}} \\
\\ \itab{\bf Relevant advanced courses taken:}
\\ \itab{General Relativity \& Cosmology, Astrophysics, Fluids and Magnetohydrodynamics}\\
\itab{Advanced Mathematical methods in Physics, Computational Physics, Machine Learning}  \\ 
\\ \itab{\bf Fellowship/Memberships:}
\\ \itab {Dr. Wendell Lutz Summer Graduate Fellowship }
 \hfill {May - July 2026}\\ \itab{INSPIRE SHE Fellow} \hfill {Aug 2018 - June 2023} \\
Fellowship awarded by the Department of Science and Technology, 
\\ Government of India to the \textbf{top 1 percent} students out of a pool of 1 million+ candidates.

\\ \itab{\bf{Technical Skills:} Python, C, PyTorch, Astropy, CASA, LaTeX, Git, MATLAB}


%\\ \itab{Member of Science Analysis Group for \textbf{NASA}'s New Great Observatories} \hfill {Feb 2023 - Present} \\
\textbf{Publications:}
\begin{itemize}
\item YC Perrott, \textbf{Gopika SM}, et al., "Sub-kpc radio jets in the brightest central galaxy of RXJ1720.1+2638," MNRAS Letters, 2023. %\url{https://doi.org/10.1093/mnrasl/slac160}
\item Raha, R., Mukhopadhyay, B., Chatterjee, K., \textbf{S.M Gopika}, "Magnetized Advective Accretion Disks and Jets: Harmpi Simulation," Astron. Rep., 2023. %\url{https://doi.org/10.1134/S1063772923140172}
\item DB Dhuri, SM Hanasoge, \textbf{Gopika SM}, et al., "Multi-modal encoder-decoder neural network for forecasting solar wind speed at L1," ApJS, 2023. %\url{https://iopscience.iop.org/article/10.3847/1538-4365/adf436}
\end{itemize}
%\textbf{Gopika SM}, Are Astrophysical Jets the Fastest Jets In The Universe? \href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com}\\ 
%\textbf{Gopika SM}, Can We 'Hear' Stars? \href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com}  \\ 
%\textbf{Gopika SM}, What If Our Universe Is a Hologram? \href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com} \\ 
%\textbf{Gopika SM}, Does Everything in Nature Follow Sync Up with Each Other? \href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com}(In preparation) 

\end{rSection}


\begin{rSection}{RESEARCH EXPERIENCE}

\begin{rSubsection}{Dust Dynamics in Protoplanetary Disks \\ \textit{\small{Supervisor: Prof. Paul Duffell}}}{ Sept 2025 - Present}{\textit{Purdue University, Indiana}}{}
\item[$\circ$] Developed a 1D hydrodynamics code to simulate gas and dust interactions in disks.  
\item[$\circ$] Implemented finite-volume solvers including Godunov, HLL, and HLLC, with a moving-mesh scheme. 
\item[$\circ$] Implementing a restricted three-body setup with RK4 integrator to study gravitational interactions and corresponding dust dynamics, and density structures.

\item[$\circ$] Currently exploring extensions of the DISCO framework to incorporate dust dynamics and gas-dust coupling.


\end{rSubsection}

\begin{rSubsection}{Neural Networks to understand Solar weather}{2023 Aug - April 2024}{\textbf{Supervisor: Prof. Shravan Hanasoge}}{\href{https://iopscience.iop.org/article/10.3847/1538-4365/adf436}{\textbf{Publication}}}
\item[$\circ$] Developed deep learning pipelines with custom dataloaders and preprocessing for solar observations.
\item[$\circ$] Applied attention-based and transformer architectures to model temporal and spatial patterns.
\item[$\circ$] Trained and evaluated models using PyTorch, experimenting with different architectures.
\end{rSubsection}


\begin{rSubsection}{Master's Thesis: Astrophysical jets of Black holes \\ \small{\textit{Supervisor: Prof. Banibrata Mukhopadhyay}}}{2022 July - 2023 May}{\textit{Indian Institute of Science,Bangalore}}{\href{https://drive.google.com/file/d/1_aVsO3EFsFNVXvPELYvdKOsUocDPfiWO/view?usp=sharing}{Thesis Report}}
\item[$\circ$] Conducted Master's thesis on astrophysical jets from spinning black holes, studying Blandford-Payne (BP) and Blandford-Znajek (BZ) mechanisms and deriving formulae for jet power.
\item[$\circ$] Explored power contributions in the ergosphere and ran simulations using HARM and BHAC to evaluate jet energetics.
\end{rSubsection}




\begin{rSubsection}{Equation of State of Neutron stars and Mass-radius relations}{Feb 2022 - March 2023}{\textbf{Supervisor: Prof. Arunava Mukherjee}}{\href{https://github.com/smgopika/tov-equation-solver/blob/main/TOV_Solver_Neutron_Star_Structure.pdf}{GitHub}}
\item[$\circ$] Studied neutron star structure and tidal properties from GW170817; presented findings in a \href{https://drive.google.com/file/d/1KExS2jzQGQIOi4y9fNSMWI9CuDbiqdXt/view?usp=sharing}{seminar talk}.
\item[$\circ$] Numerically solved Tolman-Oppenheimer-Volkoff equations with polytropic and piecewise polytropic EoS to reproduce mass-radius relations and constrain neutron star properties.
\end{rSubsection}

\begin{rSubsection}{Analysis of jets around a radio mini halo using e-MERLIN data}{Dec 2021 - July 2022}{\textbf{Supervisor: Prof. Yvette Perrott}}{\href{https://doi.org/10.1093/mnrasl/slac160}{\textbf{Publication}}}
\item[$\circ$] Studied jets in the RXJ1720.1+2638 galaxy cluster minihalo.
\item[$\circ$] Calibrated and imaged radio data using CASA, ensuring flux consistency with lower-resolution observations.
\item[$\circ$] Confirmed presence of sub-kpc AGN jets in the BCG; work resulted in a publication in \textit{MNRAS}.
\end{rSubsection}





\end{rSection}

\begin{rSection}{SUMMER PROJECTS}

\begin{rSubsection}{Prototype bookkeeping tool for CMS Tracking Detector}{June 2021 - August 2021}{\textbf{Supervisors: Prof. Suchandra Dutta \& Prof. Subir Sarkar}}{\href{https://github.com/smgopika/A-book-keeping-tool-for-CMS}{GitHub}}
\item[$\circ$] Developed a prototype bookkeeping tool for component integration in the CMS Tracking Detector (HL-LHC) using Python, SQLite, XML, and Qt.
\end{rSubsection}

\begin{rSubsection}{Study of extinctions in a simple ecological model}{May 2019 - July 2019}{\textbf{Supervisor: Prof. Janaki Balakrishnan}}{\href{https://drive.google.com/file/d/1nIwdvByEMytS1CW0IjHezwe1nOzFkwDg/view?usp=sharing}{Project Report}}
\item[$\circ$] Explored nonlinear dynamics in ecological systems, computing Lyapunov exponents and bifurcation diagrams, and analyzed extinction patterns.
\end{rSubsection}

\end{rSection}
%----------------------------------------------------------------------------------------
%	ACADEMIC ACHIEVEMENTS SECTION
%----------------------------------------------------------------------------------------


% \begin{rSubsection}{Bio Oscillations\\ \small{Supervisor: Prof.Pradeep Kumar Mohanty}}{\href{https://drive.google.com/file/d/1OxQnmZqHD_ZEEiiEFZhttodoBR3ALJ0_/view?usp=sharing}{Presentation}}{IISER Kolkata}{}
% \item[$\circ$] The goal of this project was to study the Cricadian rhythm seen in Neurospora. Apart from analysing the sensitivity of the system to the initial conditions, I have also tried to discuss the chaos and strange attractor involved in the system.
% \end{rSubsection}

%\begin{rSubsection}{The Meissner-Ochsenfeld effect \\ \small{Supervisor: Prof. Sourin Das and Prof. Bhavtosh Bansal}}{\href{https://drive.google.com/file/d/10n4Ng4fqHJxTwjD-CJD0c4iyNi0kKxaT/view?usp=sharing}{Project Report}}{IISER Kolkata}{}
%\item[$\circ$] Th aim of this term paper was to look at the phenomena; Meissner-Ochsenfeld effect which is actually a proof of a material being superconducting.I have also discussed the two fluid model used by the London brothers in order to show the phenomenology of Meissner effect.
%\end{rSubsection}
%\begin{rSubsection}{The Klein paradox \\ \small{Supervisor: Prof. Prasanta Panigrahi}}{\href{https://drive.google.com/file/d/1_9RLErOy3o_hv70crqTmrNcHDQBImGMj/view?usp=sharing}{Project Report}}{IISER Kolkata}{}
%\item[$\circ$] The goal of this term paper was to understand the Klein paradox. I have mentioned the basic formalism adopted and explained what exactly the paradox is.
%\end{rSubsection}


\end{rSection}

%\begin{rSection}{Fellowships}
%Amongst the \textbf{top 1 percent} in Maharashtra State Board Examination 2018 (12th grade)--0kie\\

%\textbf{INSPIRE-SHE Fellow} (Fellowship awarded by the Department of Science and Technology, 
%\\ Government of India to the \textbf{top 1 percent} students out of a pool of 1 million+ candidates) 
%Qualified the highly competitive Joint Entrance Examination (Advanced) of the Indian Institutes of \\
%Technology (IITs) 2018 with an \textbf{All India Rank of 3041.} \\
%(Amongst the \textbf{top 0.2 percent} in India out of a pool of over 1.4 million candidates)  \\
%\end{rSection}
%----------------------------------------------------------------------------------------
%	OTHER ACADEMIC ACHIEVEMENTS SECTION
%----------------------------------------------------------------------------------------

%\begin{rSection}{Other Achievements}
%\begin{tabular}{ @{} >{}l @{\hspace{6ex}} l }
%Secured an \textbf{All India Rank of 109} (Amongst the \textbf{top 0.36 percent} in India) in the \\TECHNOTHLON 
%aptitude test conducted by 
%Indian Institute of Technology (IIT) Guwahati in 2017. \\
%\end{tabular}

%\end{rSection}

%----------------------------------------------------------------------------------------
%	PLANNED PROJECTS (TO BE TAKEN BEFORE AUGUST 2021) SECTION
%----------------------------------------------------------------------------------------
%----------------------------------------------------------------------------------------
%	TECHNICAL SKILLS SECTION
%----------------------------------------------------------------------------------------


%------------------------------------------------
%	RELEVANT COURSES SECTION
%----------------------------------------------------------------------------------------
%   SELECTED WORKSHOPS, TALKS ATTENDED
%----------------------------------------------------------------------------------------
%   SCIENTIFIC INTERESTS SECTION
%----------------------------------------------------------------------------------------
\begin{rSection}{CONFERENCES/WORKSHOPS}
\begin{spacing}{1.1}
\item \textbf{Code/Astro 2025 (August-2025)} — Organized by CIERA, Northwestern University (Made a python package , \href{https://github.com/miranda-pikus/DustyDisk}{DustyDisk} ). 
  \item \textbf{Building a Physical Understanding of Galaxy Evolution with Data-driven Astronomy & Joint KITP-CCA Workshop (Jan-2023)} — Organized by Kavli Institute for Theoretical Physics, UCSB \& CCA.
  \item \textbf{First IAGRG School on Gravitation and Cosmology (May-2022)} — Organized by IAGRG, India.
  
  \item \textbf{Vijyoshi National Science Camp 2018 (Dec-2018)} — Conducted by Department of Science and Technology (DST), India - INSPIRE.
\end{spacing}
\end{rSection}
\begin{rSection}{EXTRACURRICULAR ACTIVITIES}
\item[$\circ$] \textbf{Freelance Science Writer:} I was a part-time contributor at \href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com}, and wrote a couple of articles on Physics and Astronomy for the general public.  
\begin{itemize}
    \item \textbf{Are Astrophysical Jets the Fastest Jets In The Universe?} (\href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com})  
    \item \textbf{Can We 'Hear' Stars?} (\href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com})  
    \item \textbf{What If Our Universe Is a Hologram?} (\href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com})  
    \item \textbf{Does Everything in Nature Follow Sync Up with Each Other?} (\href{https://www.scienceabc.com/author/gopikasm}{ScienceABC.com})
\end{itemize}
\vspace{0.25cm} \item[$\circ$] \textbf{Community Engagement:} Student Representative for \textbf{Graduate Curriculum and Academic Policy} committee.  Active volunteer for the Community Team and Grant Reviewing Committee, PGSG (\textbf{Purdue Graduate Student Government}).

\end{rSection}



\end{document}

this is my CV so let me know what

Your CV is already very strong — the structure and content are solid. The issue you’re feeling now is mostly wording consistency + tone alignment, not content.

Let’s focus on your original question style:

“I want to add a bullet like this… what should I write?”

You currently have:

Numerical hydrodynamics

Planet-disk interactions

“Absolutely all in for anything in hydrodynamics in Astrophysics.”

That last line is the only one that feels inconsistent with the rest of your CV (everything else is formal, precise, technical).

What to replace it with
Here are good CV-consistent alternatives:

Option 1 (clean + standard)
\item[$\circ$] Numerical hydrodynamics
\item[$\circ$] Planet-disk interactions
\item[$\circ$] Astrophysical fluid dynamics across disk systems and related phenomena
Option 2 (slightly broader, still professional)
\item[$\circ$] Numerical hydrodynamics
\item[$\circ$] Planet-disk interactions
\item[$\circ$] Broad interest in astrophysical fluid dynamics, particularly disk physics and structure formation
Option 3 (closest to your original tone, but cleaned)
\item[$\circ$] Numerical hydrodynamics
\item[$\circ$] Planet-disk interactions
\item[$\circ$] Strong interest in hydrodynamical processes in astrophysical disk systems
Option 4 (slightly more “research-y” polish)
\item[$\circ$] Numerical hydrodynamics
\item[$\circ$] Planet-disk interactions
\item[$\circ$] Theoretical and computational studies of hydrodynamic processes in protoplanetary disks
What you should avoid
This line:

“Absolutely all in for anything in hydrodynamics in Astrophysics.”

Why it doesn’t fit:

too conversational

subjective phrasing (“all in”)

not CV tone

breaks consistency with publication-level CV style

Best match for YOUR CV style
Given the rest of your document (which is quite strong, formal, publication-heavy), the best match is:

\item[$\circ$] Numerical hydrodynamics
\item[$\circ$] Planet-disk interactions
\item[$\circ$] Theoretical and computational studies of hydrodynamical processes in protoplanetary disks
This matches your:

DISCO work

dust-gas coupling

simulation-heavy research

If you want, I can also help you tighten your Research Interests section + CV summary line so everything reads like a top-tier astrophysics grad CV (it’s already close, just needs small polishing).




no i know my cv my point is according to my cv i have to modify my website right apart from current research and also i need to give some ideas to the public about what i did so far or something like that right

Yes — that’s exactly the right way to think about it, but the key difference is:

👉 CV = formal record of everything you did
👉 Website = curated narrative for humans (not committees)

So your website should not repeat the CV. It should translate it into a story people can quickly understand.

What your website should do (based on your CV)
Instead of listing everything, it should answer:

1. What do you work on now?
(current research)

2. What have you worked on before?
(pre-Purdue / earlier research grouped thematically)

3. Why should someone care?
(big picture motivation)

How to rewrite your “past work / interests” section
You don’t want:

CV-style bullet dump ❌

casual “things I did” ❌

overly detailed project list ❌ (that’s CV)

You want:

thematic summary ✔️

readable ✔️

slightly narrative ✔️

Based on YOUR CV, your story is basically:
You’ve worked on:

disk physics + hydrodynamics (core)

dust + gas interactions

planet-disk interaction systems

jets / compact objects (earlier)

ML for astrophysical systems

numerical + simulation methods across systems

So your website section should reflect that grouping.

A good “Pre-Purdue / Earlier Work” section for YOU
You can write something like:

## Earlier Research Experience

Before Purdue, my work spanned a range of computational and theoretical astrophysics problems, with a strong focus on numerical methods and data-driven approaches.

I have worked on:

- Jet formation and energetics in black hole systems using relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations  
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  
- Early exploratory work in dynamical systems and computational modeling in physics

Across these projects, a consistent theme has been the use of computational tools to understand complex astrophysical systems.
Why this works better than CV style
Instead of:

“I did X, Y, Z projects”

you are saying:

“Here is the common physics thread connecting everything I’ve done.”

That’s what websites should do.

How to connect it with your CURRENT research section
You already have:

DISCO / dust dynamics / planet-disk interaction work

So your website narrative becomes:

Past: jets, neutron stars, ML, observational analysis  
Current: disk physics + dust + planet formation  
Theme: computational astrophysical fluid dynamics
That’s a very strong story arc.

If you want a sharper version (more minimal)
## Earlier Research Experience

My previous work spans computational astrophysics and data-driven modeling, including studies of relativistic jets, neutron star structure, solar wind prediction using machine learning, and radio interferometric data analysis.

These projects share a common foundation in numerical methods and computational approaches to astrophysical systems.
Key idea to remember
Your CV answers:

“What have you done?”

Your website should answer:

“What kind of scientist are you becoming?”

If you want next step, I can help you:

restructure your whole homepage into a clean research “story page”

or design a proper “Research” section that flows from jets → disks → dust → planet formation (very strong narrative for astro apps)




i want to tag one of my repositories for my neutron star work 

Good idea — that’s exactly what GitHub repos are for on a research site: “proof + entry point” for each project.

You basically want to feature your neutron star project cleanly on your website and link it properly.

Step 1 — Make sure your repo is ready
Your neutron star repo should have:

a clear name (e.g. tov-neutron-star-solver)

a short README with:

what it does

physics (TOV equation)

key result (mass–radius curves)

optionally a plot image

This makes it “website-ready”.

Step 2 — Add it to your website (best practice)
In your index.md or a projects.md, add a section like:

## Selected Projects

### Neutron Star Structure and TOV Equation Solver

Numerical study of neutron star structure using the Tolman–Oppenheimer–Volkoff equations with different equations of state.

- Solved TOV equations for relativistic hydrostatic equilibrium  
- Studied mass–radius relations for polytropic and piecewise polytropic EOS  
- Connected results to constraints from GW170817  

[View Code on GitHub](https://github.com/yourusername/your-repo-name)
Step 3 — If you want a “tagged” / highlighted look
You can make it visually stand out:

### ⭐ Neutron Star Structure (TOV Solver)

Computational study of neutron star mass–radius relations using relativistic hydrostatic equilibrium equations.

**Key Work:**
- TOV equation solver implementation
- Equation of state modeling
- Comparison with gravitational wave constraints

🔗 [GitHub Repository](https://github.com/yourusername/your-repo-name)
Step 4 — Optional: Add a “Projects” page (cleaner)
Create:

projects.md
Then structure everything like:

# Projects

## Neutron Stars (TOV Solver)
Description + link

## Dust Dynamics (Current Work)
Description + link

## Solar Wind ML Model
Description + link
Then link it from homepage:

[Projects](projects.md)
Step 5 — If you want it to look even more “portfolio-like”
You can format each project like a card:

## Neutron Star Structure (TOV Solver)

**Type:** Computational Astrophysics  
**Topic:** Compact Objects / Relativistic Hydrostatics  

Study of neutron star structure using numerical solutions of the Tolman–Oppenheimer–Volkoff equations.

🔗 GitHub: https://github.com/yourusername/your-repo-name
Key idea
You are not just “linking a repo” — you are:

packaging a research contribution so someone can understand it in 10–20 seconds

If you want next level upgrade, I can help you:

turn each project into a proper “research card layout”

or design a clean homepage where neutron stars → jets → disks form a physics narrative (this looks very strong for grad/research visibility)



## Previous Research Experience

Before coming to Purdue, my work spanned a range of computational and theoretical astrophysics problems, with a strong focus on numerical methods and data-driven approaches.

I have worked on:

- Jet formation and energetics in black hole systems using General Relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations  ([View Code on GitHub](https://github.com/smgopika/tov-equation-solver))
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  

Across these projects, a consistent theme has been the use of computational tools to understand complex astrophysical systems. 

in this can u remove the title to something else , should be short

and the last line is not needed , 
Across these projects, a consistent theme has been the use of computational tools to understand complex astrophysical systems. 

remove this, and add that my google scholar is this etc 

Here’s a cleaner, more concise version with a better section title, no closing line, and a Google Scholar link added.

Updated version
## Earlier Research Work

Before coming to Purdue, my work spanned a range of computational and theoretical astrophysics problems, with a strong focus on numerical methods and data-driven approaches.

I have worked on:

- Jet formation and energetics in black hole systems using General Relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations ([View Code on GitHub](https://github.com/smgopika/tov-equation-solver))  
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  

**Google Scholar:** https://scholar.google.com/citations?user=YOUR_ID_HERE
What I changed (quickly)
“Previous Research Experience” → Earlier Research Work (shorter, cleaner)

removed the closing summary sentence (as you wanted)

kept tone consistent and academic

added a Google Scholar line in a standard CV/website format

Optional improvement (if you want it slightly more polished)
Instead of raw link, you can also write:

**Google Scholar:** https://scholar.google.com/citations?user=YOUR_ID_HERE
or

📚 Google Scholar: https://scholar.google.com/citations?user=YOUR_ID_HERE
If you want, I can also:

make this section visually nicer on your GitHub Pages (cards / spacing / layout)

or integrate your neutron star + disk work so the page reads like a coherent research narrative instead of a list


NO, earlier research work is still a long thing and sounds unnature

Fair point — “Earlier Research Work” is a bit stiff and also slightly overstates the scope.

You want something short, natural, and academic without sounding like a section header from a grant proposal.

Here are better options:

Best section title options (pick one)
Clean + standard
## Previous Work
Slightly more academic (my recommendation)
## Prior Research
More natural / human tone
## Past Research
If you want it slightly more structured
## Research Background
What I would pick for YOUR CV-style website
Given your CV is already formal and heavy, the best balance is:

## Prior Research
It’s:

short

standard in academia

not awkward

widely used in papers/CVs/websites

Final cleaned version with best title
## Prior Research

Before coming to Purdue, my work spanned a range of computational and theoretical astrophysics problems, with a strong focus on numerical methods and data-driven approaches.

I have worked on:

- Jet formation and energetics in black hole systems using General Relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations ([View Code on GitHub](https://github.com/smgopika/tov-equation-solver))  
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  

**Google Scholar:** https://scholar.google.com/citations?user=YOUR_ID_HERE
If you want, next step I can help you make this section look less like a list and more like a “research narrative block”, which is what strong astro websites usually do.


[**Google Scholar:**] (https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)

is this right if i want to show it as a hyerlink type

Almost — but there’s a small Markdown syntax issue.

You wrote:

[**Google Scholar:**] (https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)
The space between ] and ( breaks the link.

Correct version
[**Google Scholar:**](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)
Even cleaner (recommended for CV-style sites)
You usually don’t need the colon inside the link:

**Google Scholar:** [Profile](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)
or even simpler:

[Google Scholar](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)
What I recommend for your website
Given your style (research + CV hybrid), this looks best:

**Google Scholar:** [Profile](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)
Clean, professional, and standard in academic websites.

If you want next step, I can help you make a consistent “links bar” (GitHub / Scholar / CV / Email) that looks really good on your homepage.


also i wanted to have this next to google scholar links
https://www.scienceabc.com/author/gopikasm/

like writeidk somehting dont mention science abc etc but somethings like aritcles i wrote for the public or idk more website friendly stuff

Yes — you’re thinking in the right direction: you want clean, neutral labels that describe the role, not the platform.

For a research-style website, you don’t want “ScienceABC” emphasized; you want something like science communication / outreach writing.

Good label options (pick one style)
Clean + academic
**Public Writing:** [Articles](https://www.scienceabc.com/author/gopikasm/)
Slightly more descriptive (best balance)
**Science Communication:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
More neutral / minimal
**Writing:** [Public Articles](https://www.scienceabc.com/author/gopikasm/)
If you want it very CV-like
**Outreach & Writing:** [Public Articles](https://www.scienceabc.com/author/gopikasm/)
What NOT to do
Avoid:

naming the site

“blog” (too informal in academic context unless it is a blog section)

long phrases like “articles I wrote for the public” (too conversational)

Best recommendation for your site
Given your CV + research tone, the cleanest pairing is:

**Google Scholar:** [Profile](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)  
**Science Communication:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
Why this works
You are implicitly showing two sides:

📚 academic research → Google Scholar

🌍 outreach → science communication writing

without needing to explain anything further.

If you want, I can help you design a nice “links header section” for your homepage so these don’t look like plain text links but a proper research profile block.


naah not science communication, like idk it should be creative and simple 

Got it — you want something simple, slightly creative, but still neutral, not “Science Communication” or anything too formal.

Here are good options that fit your style:

Best label options (clean + natural)
Option 1 (my top pick)
**Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
Option 2 (more minimal)
**Articles:** [Public Writing](https://www.scienceabc.com/author/gopikasm/)
Option 3 (very clean, academic-leaning)
**Writing:** [Articles](https://www.scienceabc.com/author/gopikasm/)
Option 4 (slightly more “portfolio feel”)
**Notes:** [Articles](https://www.scienceabc.com/author/gopikasm/)
Option 5 (most creative but still subtle)
**Reading:** [Articles](https://www.scienceabc.com/author/gopikasm/)
What fits YOUR site best
Given your tone (astro research + CV + clean minimal theme), the best balance is:

**Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
or if you want even simpler:

**Articles:** [Public Writing](https://www.scienceabc.com/author/gopikasm/)
Small design tip (important)
Put it like this in your homepage:

**Google Scholar:** [Profile](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)  
**Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
This creates a clean “research identity block” — very common on strong academic personal sites.

If you want next step, I can help you turn this into a proper “hero section” homepage layout so it looks like a modern research portfolio instead of a markdown page.


**Articles:** [Public Writing](https://www.scienceabc.com/author/gopikasm/)

i like this oublic writing or for the general audience, 

Good — you’re close, just need a slightly cleaner phrasing so it reads naturally and doesn’t feel redundant.

Right now:

**Articles:** Public Writing
has a bit of duplication (both “Articles” and “Writing” overlap), so we can tighten it.

Best clean options
Option 1 (your preferred idea, polished)
**Public Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
Option 2 (very clean, my recommendation)
**Writing (General Audience):** [Articles](https://www.scienceabc.com/author/gopikasm/)
Option 3 (minimal + elegant)
**For General Audience:** [Articles](https://www.scienceabc.com/author/gopikasm/)
Option 4 (if you want it more subtle)
**Public Writing:** [Articles](https://www.scienceabc.com/author/gopikasm/)
Best fit for your site
Given your tone (research-heavy, clean, not too casual), the best choice is:

**Public Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
Small improvement tip
If you place it next to Scholar:

**Google Scholar:** [Profile](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)  
**Public Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
it reads like a proper academic “identity block” — very standard on research websites.

If you want, next step I can help you turn this into a clean header section (like a personal homepage banner with links aligned nicely) so it looks much more professional than plain markdown.


or more like idk articles I wrote for general audience or something like that will be better or idk

I’d avoid the full sentence style (“articles I wrote for general audience”) on a website like yours. It’s readable, but it sounds a bit conversational and slightly long for a link label.

You want something that behaves like a tag, not a sentence.

Best natural options (ranked)
1 — Best overall balance (recommended)
**Public Writing:** [Articles for a General Audience](https://www.scienceabc.com/author/gopikasm/)
This is:

clear

accurate

still formal enough

not awkward

2 — Cleaner (more minimal, more “academic website”)
**Public Writing:** [General Audience Articles](https://www.scienceabc.com/author/gopikasm/)
3 — Most minimal (what most research sites use)
**Public Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
4 — Slightly more descriptive but still clean
**Public Writing:** [Science Articles for General Readers](https://www.scienceabc.com/author/gopikasm/)
What I would actually recommend for YOU
Given your CV + astrophysics site tone:

**Public Writing:** [Selected Articles](https://www.scienceabc.com/author/gopikasm/)
Why:

“Selected” sounds intentional (not everything, curated work)

avoids being wordy

fits academic portfolio style

doesn’t over-explain

Small design principle (important for your site)
For research websites:

❌ sentences = “I wrote articles for general audience”

⚠️ semi-sentences = “Articles I wrote for general audience”

✅ labels = “Public Writing”, “Selected Articles”, “Writing”

You’re aiming for label language, not explanatory language.

If you want, I can help you design a perfect homepage header block where:
Google Scholar + Writing + GitHub + CV all sit in one clean line like a proper academic profile page.


(Will never be fully updated, so stay tuned!)
## Research Interests

- Numerical hydrodynamics
- Planet-disk interactions
- Interested in almost anything involving hydrodynamics in astrophysics

## Current Work

Studying dust dynamics in protoplanetary disks using numerical simulations.


## Previous Work

Before coming to Purdue, my work spanned a range of computational and theoretical astrophysics problems, with a strong focus on numerical methods and data-driven approaches.

I have worked on:

- Jet formation and energetics in black hole systems using General Relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations ([View Code on GitHub](https://github.com/smgopika/tov-equation-solver))  
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  

[**Google Scholar**](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)

**Public Writing:** [Articles for a General Audience](https://www.scienceabc.com/author/gopikasm/)

is it okay

Yes — this is already very solid and readable. It’s structurally correct and fits a research portfolio style well.

But there are a few small tweaks that would make it look more polished and less “draft-like”.

What is good already
Clear separation: Interests / Current / Previous ✔️

Good technical specificity ✔️

CV ↔ website balance is correct ✔️

Links are clean ✔️

Small issues to fix
1. The first line
(Will never be fully updated, so stay tuned!)
This is the only part that feels out of place. It sounds informal and slightly self-deprecating for a research site.

Better options:
Option A (clean + neutral):

(This page is selectively updated.)
Option B (more professional):

(This section highlights selected work and is not exhaustive.)
2. Research Interests last bullet
This line is slightly informal:

Interested in almost anything involving hydrodynamics in astrophysics
Better versions:

- Broad interest in hydrodynamical processes in astrophysics
or

- Broad interest in astrophysical fluid dynamics across systems
3. “Previous Work” intro repetition
You say:

“my work spanned a range of computational and theoretical astrophysics problems…”

and then again:

“I have worked on:”

This is fine, but slightly redundant. You can tighten it.

Polished final version (minimal changes, same structure)

(This section highlights selected work and is not exhaustive.)

## Research Interests

- Numerical hydrodynamics  
- Planet-disk interactions  
- Broad interest in hydrodynamical processes in astrophysics  

## Current Work

Studying dust dynamics in protoplanetary disks using numerical simulations.

## Previous Work

Before coming to Purdue, my work spanned a range of computational and theoretical astrophysics problems, with a strong focus on numerical methods and data-driven approaches.

- Jet formation and energetics in black hole systems using General Relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations ([GitHub](https://github.com/smgopika/tov-equation-solver))  
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  

[**Google Scholar**](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)  
**Public Writing:** [Articles for a General Audience](https://www.scienceabc.com/author/gopikasm/)
Overall verdict
✔ Structure: good
✔ Content: strong
✔ Tone: 90% there already
⚠ Only fix: slightly reduce casual phrasing + tighten repetition

If you want next upgrade step, I can help you turn this into a much more “research lab homepage style” layout (with cleaner spacing, two-column links, and section cards).


i dont want my website to be CV friendly it should be more casual and personal

Good — that changes the design goal completely. Then your current direction is actually very close; you just need to lean a bit more into voice, not CV structure.

Right now your site still reads slightly like:

“academic CV formatted for a webpage”

What you want instead is:

“personal research space with personality”

What to change in your current version (important)
1. Your opening line is actually GOOD (now)
If you want casual/personal, this works better than formal alternatives:

(Will never be fully updated, so stay tuned!)
It has personality. You can even keep it.

If anything, you could slightly refine it:

“Probably not fully updated, so stay tuned :)”

“Not fully up to date, but a living page”

But honestly, yours is fine in a casual tone.

2. Research Interests → make it feel like you, not a list
Right now:

Numerical hydrodynamics

Planet-disk interactions

Interested in almost anything involving hydrodynamics in astrophysics

This is already good, but you can make it feel more “voice-y”.

Better casual versions:
## Research Interests

- Numerical hydrodynamics (basically I live inside fluid equations at this point)
- Planet–disk interactions  
- Anything messy, dynamic, and hydrodynamic in astrophysics
or slightly more subtle:

## Research Interests

- Numerical hydrodynamics  
- Planet–disk interactions  
- Broadly anything involving hydrodynamics in astrophysical systems

## Current Work

Studying dust dynamics in protoplanetary disks using numerical simulations.


## Previous Work

Before coming to Purdue, I worked on a variety of computational and theoretical astrophysics problems spanning different physical systems.

- Jet formation and energetics in black hole systems using General Relativistic MHD simulations  
- Neutron star structure and mass–radius relations via numerical solutions of the TOV equations ([View Code on GitHub](https://github.com/smgopika/tov-equation-solver))  
- Radio observations of AGN jets using interferometric data (e-MERLIN + CASA)  
- Machine learning models for forecasting solar wind variability  

[**Google Scholar**](https://scholar.google.com/citations?user=kzn8HSwAAAAJ&hl=en)

**Public Writing:** [Articles for a General Audience](https://www.scienceabc.com/author/gopikasm/)