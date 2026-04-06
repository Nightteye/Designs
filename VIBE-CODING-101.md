# HOW TO VIBE CODE AND CREATE BEAUTIFUL WEBSITES
> This is a guide to help you vibe code and create beautiful websites. It covers how to make website using React, Vite, Tailwind CSS, as well as some tips and tricks to make your coding experience more enjoyable.

---

## Prerequisites
> Find your niche and research the topic a little to know your competitors.
> Explore others' websites to get to know what they have to offer
> Find a gap that they are missing, and try to improve or work on that
> Find your vibe and stick to it, don't try to copy others, be original and creative

## Designing your website
> Before even starting a single line of code, explore designs. 
> Where to find designs?
> - You can choose your own designs. 
> - Here are all the Designs you can use:
> - Neubrutalism
> - Minimalism
> - Material Design
> - Flat Design
> - Skeuomorphism
> - Brutalism
> - Neumorphism
> - Glassmorphism
> - Liquid Glass
> - etc.

> You can also find designs on Dribbble, Behance, Pinterest, etc.
> - dribble.com
> - behance.net
> - pinterest.com

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
> - You can use tools like Figma, Sketch, Adobe XD,Google Stitch etc. to create your wireframe or mockup.
> - figma.com, sketch.com, adobexdplatform.com, stitch.withgoogle.com
> - You can also use pen and paper to create your wireframe or mockup.

## Setting up your development environment
> Once you have your design ready, it's time to set up your development environment.
> - You can use any code editor you like, but I recommend using Visual Studio Code.(https://code.visualstudio.com/)
> - You can also use other code editors like Sublime Text, Atom, etc. but I recommend using Visual Studio Code because of its features and extensions that can help you vibe code and create beautiful websites.

# Tools and Technologies
> - React: A JavaScript library for building user interfaces. (https://reactjs.org/)
> - Vite: A build tool that provides a fast development experience for modern web projects.
> - Tailwind CSS: A utility-first CSS framework for rapidly building custom user interfaces. (https://tailwindcss.com/)
> - Git: A version control system to manage your code and collaborate with others. (https://git-scm.com/)
> - GitHub: A platform for hosting and collaborating on Git repositories. (https://github.com)
> - Figma: A design tool for creating wireframes, mockups, and prototypes. (https://www.figma.com/)

## AI Tools
> - Choose the right AI tools to help you with your coding and design process. Some popular AI tools for web development include:
> - GitHub Copilot: An AI-powered code completion tool that helps you write code faster and with fewer errors. (https://copilot.github.com/)
> - Claude by Anthropic: An AI assistant that can help you with coding, design, and other tasks. (https://www.anthropic.com/claude)
> - Google Gemini AI: A suite of AI tools that can assist you with various aspects of web development, including code generation and design assistance. (https://ai.google.dev/gemini)

> [!NOTE] 
> I personally use Google Gemini and Claude. Claude's free tier is not generous, so use it wisely. Google Gemini is more generous and can be used for a variety of tasks, including code generation, design assistance, and more.

> [!TIP]
> Use Gemini for initial code generation and design assistance, Once you have the basic build and interactive website, you can zip the file and upload it to Claude. Also, use any extensions tools to extract your chat with Google Gemini(https://chromewebstore.google.com/detail/savechat-for-gemini-expor/blndbnmpkgfoopgmcejnhdnepfejgipe). 

>[!TIP]
> Don't just start with coding right away, Plan your website and design with AI Tools, once everything is explained to the AI, and the context is clear, then you can start coding. This will save you a lot of time and effort in the long run.

## Installing dependencies
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

