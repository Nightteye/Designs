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

## Setting up Tailwind CSS [Edited by AI]
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
```

> Now you can start building your website by creating components and adding styles using Tailwind CSS. You can also use the AI tools to help you with code generation and design assistance as you build your website.

---

## Building your website
---
> Before starting to code, it's important to give the AI tool(s) a persona and a context to work with. This will help the AI tool understand your requirements and generate code that is more relevant to your needs. For example, you can give the AI tool the following persona and context: [Persona Prompt](Prompt-Library/Website-Builder/Persona-Prompt.md)

### 1. Hero Section
- This is the first and foremost important section of the website, it should always look catchy and attractive, it should be very intriguing and should make the user want to scroll down and explore the website.

- Don't not hold yourself for Hero Section. Add animations, micro-interactions, and make it as attractive as possible. This is the first thing that the user will see when they visit your website, so make sure to make a good impression.

- You can look the prompt is used to build the Hero Section here: [Hero Section Prompt](nowhere-fast-prompt.md#1-hero-section)

---

### 2. Navbar
- **NEVER** use a traditional navbar, try to be creative and original with your navbar design. You can use a hamburger menu, a sidebar, a bottom navigation, or any other creative way to navigate through your website. The navbar should be easy to use and should not take up too much space on the screen.

- You can also add some animations and micro-interactions to make it more engaging. For example, you can add a hover effect to the navbar items, or you can add a sliding animation when the user clicks on the hamburger menu.

- **DO NOT** add too many items in the navbar, keep it minimal and to the point. The navbar should only contain the most important links that the user needs to navigate through your website. Rest can go to the footer, which will be discussed as we go further in the guide.

- *I don't have a prompt for the navbar, for this website*. You can just ask any AI tool to generate a navbar, it's one of the most simple task for an AI tool, and you can easily customize it to fit your design and vibe.

---

### 3. About Section
- This section should be simple and straightforward, it should give the user an idea about who you are and what you do. You can also add some animations and micro-interactions to make it more engaging.

- I personally like to have a dedicated page for 'About Page' and link it from the homepage, I just add a very brief about in the homepage and then link it to the about page where I go in depth about the story and the journey.

- Never clutter this section with too much information, keep it precise and to the point. If you're building the website for a company or a brand, you can add a timeline of the company's history and milestones in this section. This will give the user a better understanding of the company's journey and achievements. But keep this section in middle or at the end of the website, never put it at the top, because the user will not be interested in reading about you before they know what you have to offer.

- You can look the prompt is used to build the About Section here: [About Section Prompt](nowhere-fast-prompt.md#2-about-section)

---

### 4. Footer 
- The footer is the last thing that the user will see when they scroll down to the bottom of your website, so make sure to make a good impression with your footer design. You can add some animations and micro-interactions to make it more engaging. For example, you can add a hover effect to the social media icons, or you can add a sliding animation when the user clicks on the subscribe button.

- The footer should contain the most important links that the user needs to navigate through your website, such as the contact information, social media links, and legal information. You can also add a newsletter subscription form in the footer to collect email addresses from your visitors. This will help you to build a mailing list and keep your audience updated with your latest content and news.

- I prefer big footers with a lot of information and links, but you can also go for a minimal footer if it fits your design and vibe. Just make sure to include all the important information and links that the user needs to navigate through your website. If you want to add a big footer, make sure to give proper spacing and layout to the footer content, so that it does not look cluttered and overwhelming for the user. You can also add some animations and micro-interactions to make it more engaging. For example, you can add a hover effect to the social media icons, or you can add a sliding animation when the user clicks on the subscribe button.

- You can look the prompt is used to build the Footer Section here: [Footer Section Prompt](nowhere-fast-prompt.md#5-footer)

---

## Planning Folder Structure 


> Always keep the folder structure organized and clean. This will help you and others understand the code better and make it easier to maintain and update in the future. You can create separate folders for components, styles, assets, etc. to keep everything organized. 

> [!TIP]
> After the basic website is ready, immediately push it to Github. This will help you keep track of your changes and also allow you to have version control for you project. This would help you to revert back to previous version if something goes wrong. If you're working in a team, this will allow you to share your code with other and add them as collaborators to your repository. You can also use GitHub Pages to host your website for free.

> Once the persona is set and the context is provided, You can give this specific prompt to the AI tool. I personally use this prompt, this will create the starting point for the website and then you can start building on top of it and adding more features and components as you go along.

This is my own website which I've built with Claude. You can check it out here: [Nowehere Fast](https://nowhere-fast.vercel.app/)
You can find the prompt I used to build this website here: [Nowhere Fast Prompt](./nowhere-fast-prompt.md)

---

> [!NOTE]
> This was just the initial prompt to guide the AI to generate the website, to see the whole chat you can use this [link](https://claude.ai/share/e9f67e3b-2e5b-489f-aad0-3dcf86e59876). Once you get the initial code, start adding components and features one by one. Don't try to do everything at once, this will help you to focus on one thing at a time and also make it easier to debug and test your code. 

> I used Claude to generate the whole website in this case, but you can also use Google Gemini for the initial code generation and then switch to Claude for any further improvements and optimizations. 

---

## Debugging the Website
> Once the basic website is ready, there will be a lot of bugs and issues which you will need to fix manually. This is where your coding skills and knowledge will come into play. You can use the AI tools to help you with debugging and optimizing your code, but always make sure to understand the code and the logic behind it before using it in your projects. You can also use browser developer tools to inspect the elements and debug any issues that may arise.

> [!TIP]
> Always use the Console and Network tabs in the browser developer tools to check for any errors or issues with your code. 90% of the bugs can be fixed by just checking the console, if you're an experienced developer, you can fix the bugs by yourself, but if you're a new developer/don't know any coding, just copy the console error and paste it in the AI Tool of your choice, and the AI tool will give you the full fixed file which you can copy and paste in your project.  

---

>[!NOTE]
> The guide has not been fully completed yet, I will be adding more sections and tips as I go along. If you have any suggestions or resources that you think would be helpful, please feel free to share them with me. This message is temporary and will be removed once the guide is fully completed. You may see this message in future too, once the min guide is complete this message will be removed and the guide will be updated with more sections and tips.

*Thank You*

***Nighteye***
