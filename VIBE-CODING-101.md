# Vibe Coding 101

>[!NOTE]
> I've marked some sections of this guide as "Edited by AI" because I used AI tools to help me with the writing and editing process. I wanted to make it clear which parts were generated or edited by AI and which parts were written by me. This is just to be transparent about the use of AI in the creation of this guide.

# HOW TO VIBE CODE AND CREATE BEAUTIFUL WEBSITES
> This is a guide to help you vibe code and create beautiful websites. It covers how to make website using React, Vite, Tailwind CSS, as well as some tips and tricks to make your coding experience more enjoyable.

---

## Prerequisites
> - Find your niche and research the topic a little to know your competitors.
> - Explore others' websites to get to know what they have to offer
> - Find a gap that they are missing, and try to improve or work on that
> - Find your vibe and stick to it, don't try to copy others, be original and creative  

---

## Designing your website
> Before even starting a single line of code, explore designs. 
> Where to find designs?
> - You can choose your own designs. 
> - Here are all the Designs you can use:
> - [Neubrutalism](./Designs/neubrutalism/)
> - [Minimalism](./Designs/minimalism/)
> - [Material Design](./Designs/material-design/)
> - [Flat Design](./Designs/flat-design/)
> - [Skeuomorphism](./Designs/skeuomorphism/)
> - [Brutalism](./Designs/brutalism/)
> - [Neumorphism](./Designs/neumorphism/)
> - [Glassmorphism](./Designs/glassmorphism/)
> - [Liquid Glass](./Designs/liquid-glass/)
> - etc.

> You can also find designs on websites like:
> - [Dribbble](https://dribbble.com)
> - [Behance](https://www.behance.net)
> - [Pinterest](https://www.pinterest.com)

> Once you find a design that you like, try to analyze it and understand how it works.
> - What are the colors used?
> - What are the fonts used?
> - What are the shapes used?
> - What are the animations used?
> - What are the interactions used?
> - What are the components used?
> - What are the layouts used?
> - What are the patterns used?
> - What are the principles used?
> - What are the best practices used?
> - What are the accessibility features used?

> Once you understand the design, try to create a wireframe or a mockup of your website.
> - You can use tools like [Figma](https://www.figma.com/), [Sketch](https://www.sketch.com/), [Adobe XD](https://adobexdplatform.com/), [Google Stitch](https://stitch.withgoogle.com/) etc. to create your wireframe or mockup.
> - You can also use pen and paper to create your wireframe or mockup.

---

## Setting up your development environment
> Once you have your design ready, it's time to set up your development environment.
> - You can use any code editor you like, but I recommend using [Visual Studio Code](https://code.visualstudio.com/).
> - You can also use other code editors like [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom-editor.cc/), etc. but I recommend using Visual Studio Code because of its features and extensions that can help you vibe code and create beautiful websites.

---

# Tools and Technologies
> - [React](https://reactjs.org/): A JavaScript library for building user interfaces. 
> - [Vite](https://vitejs.dev/): A build tool that provides a fast development experience for modern web projects.
> - [Tailwind CSS](https://tailwindcss.com/): A utility-first CSS framework for rapidly building custom user interfaces.
> - [Git](https://git-scm.com/): A version control system to manage your code and collaborate with others.
> - [GitHub](https://github.com): A platform for hosting and collaborating on Git repositories.
> - [Figma](https://www.figma.com/): A design tool for creating wireframes, mockups, and prototypes.

---

## AI Tools [Edited by AI]
> - Choose the right AI tools to help you with your coding and design process. Some popular AI tools for web development include:
> - [GitHub Copilot](https://copilot.github.com/): An AI-powered code completion tool that helps you write code faster and with fewer errors.
> - [Claude by Anthropic](https://www.anthropic.com/claude): An AI assistant that can help you with coding, design, and other tasks.
> - [Google Gemini AI](https://ai.google.dev/gemini): A suite of AI tools that can assist you with various aspects of web development, including code generation and design assistance.

> [!NOTE] 
> I personally use Google Gemini and Claude. Claude's free tier is not generous, so use it wisely. Google Gemini is more generous and can be used for a variety of tasks, including code generation, design assistance, and more.

> [!TIP]
> Use Gemini for initial code generation and design assistance, Once you have the basic build and interactive website, you can zip the file and upload it to Claude. Also, use any extensions tools to extract your chat with Google Gemini [extension](https://chromewebstore.google.com/detail/savechat-for-gemini-expor/blndbnmpkgfoopgmcejnhdnepfejgipe). 

>[!TIP]
> Don't just start with coding right away, Plan your website and design with AI Tools, once everything is explained to the AI, and the context is clear, then you can start coding. This will save you a lot of time and effort in the long run.

---

## Installing dependencies [Edited by AI]
> Once you have your development environment set up, it's time to install the necessary dependencies for your project. You can use npm or yarn to install the dependencies. For example, to create a new React project with Vite and Tailwind CSS, you can run the following commands:
```bash
npm create vite@latest my-react-app -- --template react
cd my-react-app
npm install
```
> After installing the dependencies, you can start the development server by running:
```bash 
npm run dev
```
> This will start the development server and you can view your website at http://localhost:3000.

---

## Setting up Tailwind CSS
> Installing Tailwind CSS v4 with React and Vite:
```bash
npm install tailwindcss @tailwindcss/vite
```
> Configure the Vite Plugin
Open your `vite.config.js` file and add the Tailwind CSS plugin:
```javascript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite' // [!code ++]

export default defineConfig({
  plugins: [
    react(),
    tailwindcss(), // [!code ++]
  ],
})
```

> Now the dependecies are installed and the folder structure is ready. The folder structure should look like this:
```my-react-app/
├── node_modules/
├── public/
├── src/ 
│   ├── App.jsx <-- This the the main component of your website. You can create other components and import them here.>
│   ├── index.css <-- This is where you can import your Tailwind CSS styles. You can also add your custom styles here.>
│   └── main.jsx <-- This is the entry point of your application. It renders the App component to the DOM.>
├── .gitignore
├── index.html
├── package.json
├── vite.config.js <-- This is where you configure your Vite plugins and Tailwind CSS is also loaded from here in v4.>
└── README.md
>[!NOTE]
> Edited by AI
```

> Now you can start building your website by creating components and adding styles using Tailwind CSS. You can also use the AI tools to help you with code generation and design assistance as you build your website.

---

## Building your website
> Before starting to code, it's important to give the AI tool(s) a persona and a context to work with. This will help the AI tool understand your requirements and generate code that is more relevant to your needs. For example, you can give the AI tool the following persona and context:

```markdown
You are a senior front-end developer with 10 years of experience in building beautiful and responsive websites. You have a strong 

understanding of React, Vite, Tailwind CSS, and other modern web development technologies. You are also familiar with design 

principles and best practices for creating user-friendly interfaces. Your task is to help me build a website based on the design 

I will provide you with. The website should be responsive, accessible, and visually appealing. You should also provide me with 

explanations and comments in the code to help me understand how it works. I will provide you with the design and the content for 

the website, and you will generate the code for me. You should also help me with any questions or issues I may have during the 

development process. Your goal is to help me create a website that is not only functional but also beautiful and enjoyable to 

use. You should also help me with any optimizations and improvements that can be made to the code and the design to make it even 

better. You should also help me with any testing and debugging that may be needed to ensure that the website works perfectly 

across different browsers and devices. Your ultimate goal is to help me create a website that I can be proud of and that will 

provide a great user experience for my visitors. You should also help me with any deployment and hosting options for the website 

once it is ready. You should also help me with any maintenance and updates that may be needed in the future to keep the website 

up-to-date and secure. Your role is not just to generate code, but to be a mentor and a guide throughout the entire process of 

building the website. You should also help me with any design decisions and suggestions that can improve the overall look and 

feel of the website. Your ultimate goal is to help me create a website that is not only functional but also beautiful, 

user-friendly, and enjoyable to use.
```

> [!TIP]
> Always keep the folder structure organized and clean. This will help you and others understand the code better and make it easier to maintain and update in the future. You can create separate folders for components, styles, assets, etc. to keep everything organized. 

> [!TIP]
> After the basic website is ready, immediately push it to Github. This will help you keep track of your changes and also allow you to have version control for you project. This would help you to revert back to previous version if something goes wrong. If you're working in a team, this will allow you to share your code with other and add them as collaborators to your repository. You can also use GitHub Pages to host your website for free.

> Once the persona is set and the context is provided, You can give this specific prompt to the AI tool. I personally use this prompt, this will create the starting point for the website and then you can start building on top of it and adding more features and components as you go along.

This is my own website which I've built with Claude. You can check it out here: [Nowehere Fast](https://nowhere-fast.vercel.app/)
> **This prompt was generated by Claude.**
```markdown
Build a punky, hyper-animated React + Vite website for a travel YouTuber called "NOWHERE FAST" — 
a solo traveler who ditches comfort zones and documents raw, chaotic, beautiful places around 
the world. The vibe is: skate zine meets travel blog meets concert poster. Think neon ink on 
black, ripped edges, brutal typography, glitch energy.

---

## TECH STACK
- React 18 + Vite
- Framer Motion for all animations
- GSAP (via CDN or npm) for the scrollytelling
- @studio-freight/lenis for smooth scrolling
-  Tailwind CSS v4 
- Google Fonts only (suggest: Bebas Neue + Space Mono or similar punk pairings)

---

## AESTHETIC DIRECTION — COMMIT HARD TO THIS

Color palette (use CSS variables):
  --black: #080808
  --white: #F0EDE4 (slightly warm, like old zine paper)
  --neon-yellow: #D4FF00
  --hot-pink: #FF2D78
  --electric-blue: #00F0FF
  --glitch-red: #FF2020

Typography rules:
  - Hero display font: Something brutal and condensed (Bebas Neue, Anton, Black Ops One)
  - Body/accent font: Monospace (Space Mono, Courier Prime, IBM Plex Mono)
  - Mix sizes aggressively: massive 200px+ display text clashing with tiny 11px labels
  - Uppercase everything in headers
  - Use letter-spacing: -0.04em on display type for that compressed zine feel

Layout rules:
  - Asymmetric. Overlapping. Grid-breaking.
  - Use CSS Grid with named areas and intentional overflow
  - Decorative elements: ✦ ◆ ▶ → × + used as dividers and accents
  - Diagonal slashes (clip-path: polygon) on section dividers
  - Mix portrait and landscape "photo frames" with CSS border styles 
    (dashed, double, ridge) in neon colors
  - Grain overlay on entire page (SVG noise filter or CSS pseudo-element)

---

## PAGE STRUCTURE

### 1. HERO SECTION — SCROLLYTELLING (most important part)

Build a full-screen sticky scrollytelling sequence using GSAP ScrollTrigger with 
at least 5 "chapters" pinned to the hero wrapper. As the user scrolls:

  Chapter 1 — TITLE SLAM:
    - Black screen, then "NOWHERE" crashes in from the left (x: -200vw → 0, 
      duration 0.6s, ease: "expo.out")
    - "FAST" slams from the right simultaneously
    - Letters shake/vibrate on arrival (keyframe animation, 3 cycles)
    - Subtitle fades up: "52 countries. 1 camera. No plan." in Space Mono
    - Hot pink horizontal rule draws across screen (scaleX: 0 → 1)

  Chapter 2 — DESTINATION BURST:
    - 6 destination names (TOKYO · MARRAKECH · REYKJAVIK · OAXACA · TBILISI · MANILA)
      fly in staggered from random directions, scattered across screen
    - Each is huge (clamp(60px, 10vw, 140px)) and in a different neon accent color
    - They settle into a loose, overlapping layout (absolute positioned)
    - Background: grainy dark texture pulses subtly

  Chapter 3 — STAT COUNTER:
    - 3 massive counters animate up: "847 VIDEOS" / "31M VIEWS" / "52 COUNTRIES"
    - Each counter has a neon-yellow underline that draws in
    - Small Space Mono caption below each: "and counting ↓"

  Chapter 4 — GLITCH FRAME:
    - A fake "video thumbnail" card slides in from below
    - Apply a CSS glitch animation: duplicate layers offset by 2-4px in red and blue 
      (classic RGB split glitch)
    - Text overlay says "LATEST DROP ▶" with a pulsing play button
    - Card has a dashed hot-pink border, slightly rotated (-2deg)

  Chapter 5 — CTA EXPLOSION:
    - "SUBSCRIBE OR MISS OUT" in 120px Bebas Neue
    - Two brutal buttons: [WATCH NOW →] [JOIN THE CHAOS]
    - Buttons have clip-path on hover: diagonal wipe reveal
    - Confetti burst (CSS-only with ::before/::after and keyframes) on CTA entrance

After Chapter 5, unpin and let page continue scrolling normally.

---

### 2. ABOUT SECTION

- Split layout: Left side = a large "photo" placeholder (stylized with CSS — 
  use a bold gradient + noise as fake photo, with a ripped-paper bottom edge via clip-path)
- Right side: Large pull-quote in display font, small bio in Space Mono below
- Decorative stamp element: a circle with "EST. 2019 · WORLDWIDE" rotated text inside 
  (CSS-only rotating text around a circle path or just a styled badge)
- Section enters with a horizontal slide + fade from left/right (Framer Motion 
  whileInView)

### 3. LATEST VIDEOS SECTION — "THE REEL"

- Horizontal scrolling row of video cards (overflow-x: scroll, no scrollbar)
- Cards are deliberately misaligned: alternate cards rotate +2deg / -2deg
- Each card: dark background, fake thumbnail area with gradient, episode number in 
  giant display font, destination name, and a "WATCH ▶" label in mono
- Cards have a neon border that animates color on hover (animation cycling through 
  all 3 accent colors)
- Section heading: "THE REEL" with each letter stagger-animating in on scroll

### 4. NEWSLETTER — "THE DISPATCH"

- Full-bleed dark section with grain
- Heading: "GET THE WEEKLY CHAOS REPORT" in massive type
- Single line email input: brutalist styled (no border-radius, thick neon-yellow border, 
  monospace font, placeholder text: "your@email.com")
- Submit button [SEND IT →]: on hover, button shakes (keyframe: rotate ±2deg rapidly) 
  then slides neon-yellow fill from left (clip-path wipe)
- Subtext: "No spam. Just chaos. Unsubscribe whenever." in tiny mono

### 5. FOOTER

- Three columns: Navigation / Platforms / Legal
- Large "NOWHERE FAST" watermark text behind footer content (opacity: 0.04, 
  pointer-events: none)
- Social icons as ASCII-style characters or styled emoji: 
  [YT] [IG] [TT] [PATREON]
- Top edge: jagged/torn SVG divider shape in the page background color

---

## GLOBAL EFFECTS & POLISH

1. Custom cursor: replace default with a small crosshair (+) in neon-yellow that 
   scales up on hover over interactive elements

2. Grain overlay: full-page ::before pseudo-element with an SVG noise filter 
   (feTurbulence) at ~8% opacity, pointer-events: none, position: fixed

3. Page load sequence (runs once):
   - Flash of white (50ms)
   - Screen wipes to black using a div that slides from left to right (0.4s)
   - Then hero content begins its scroll sequence

4. Scrolling behavior: smooth with @studio-freight/lenis, easing: "exponential"

5. Selection color: background: var(--neon-yellow), color: var(--black)

6. All section transitions: use Framer Motion's AnimatePresence + whileInView with 
   viewport: { once: true, margin: "-100px" }

---

## CODE REQUIREMENTS

- Project structure:
  src/
    components/
      Hero.jsx          ← scrollytelling, GSAP
      About.jsx
      Videos.jsx
      Newsletter.jsx
      Footer.jsx
      Cursor.jsx
    App.jsx
    main.jsx

- Use useRef + useLayoutEffect for GSAP ScrollTrigger (always clean up in return)
- Framer Motion's LazyMotion with domAnimation for bundle size
- All colors via CSS variables, never hardcoded hex in JSX
- Animations must be performant: only animate transform and opacity (never width/height)
- Include package.json with all dependencies listed

Generate the complete, fully working code for all files. Do not abbreviate or use 
placeholder comments — write every component in full.
```
---

> [!NOTE]
> This was just the initial prompt to guide the AI to generate the website, to see the whole chat you can use this [link](https://claude.ai/share/e9f67e3b-2e5b-489f-aad0-3dcf86e59876). Once you get the initial code, start adding components and features one by one. Don't try to do everything at once, this will help you to focus on one thing at a time and also make it easier to debug and test your code. 

> I used Claude to generate the whole website in this case, but you can also use Google Gemini for the initial code generation and then switch to Claude for any further improvements and optimizations. 

---

## Debugging the Website
> Once the basic website is ready, there will be a lot of bugs and issues which you will need to fix manually. This is where your coding skills and knowledge will come into play. You can use the AI tools to help you with debugging and optimizing your code, but always make sure to understand the code and the logic behind it before using it in your projects. You can also use browser developer tools to inspect the elements and debug any issues that may arise.

> [!TIP]
> Always use the Console and Network tabs in the browser developer tools to check for any errors or issues with your code. 90% of the bugs can be fixed by just checking the console, if you're an experienced developer, you can fix the bugs by yourself, but if you're a new developer/don't know any coding, just copy the console error and paste it in the AI Tool of your choice, and the AI tool will give you the full fixed file which you can copy and paste in your project.  



>[!NOTE]
> The guide has not been fully completed yet, I will be adding more sections and tips as I go along. If you have any suggestions or resources that you think would be helpful, please feel free to share them with me.

