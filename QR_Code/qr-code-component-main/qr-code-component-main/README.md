# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

* [Overview](#Overview)
* [Screenshot](#screenshot)
* [Links](#links)


* [My process](#my-process)
* [Built with](#built-with)
* [What I learned](#what-i-learned)
* [Continued development](#continued-development)
* [AI Collaboration](#ai-collaboration)


* [Author](#author)

## Overview
A QR code component built using basic HTML and CSS. 
### Screenshot
[My output](QR_Code\qr-code-component-main\my_output.png)
### Links

* Solution URL: [Add solution URL here](https://github.com/robotraja96/frontend_mentor/tree/main/QR_Code/qr-code-component-main/qr-code-component-main)
* Live Site URL: [Add live site URL here](https://frontendmentor-qr-code-component-ma-blush.vercel.app/)

## My process
Initially I was struggling to get the sizing right. Then i figured out Figma and how to get individual dimensions. So once i got that, most of the design fell into place. One problem I had with was whether i should make body as a flex box or not. I decided this was the only way I know how to do. So in that way I have some knowledge gap. AI search suggested Grid Box method which I have not learnt yet. But generally body is left as default block it seems. The final polishing and refining required some AI help. 
### Built with

* Semantic HTML5 markup
* CSS custom properties
* Flexbox
* Google Fonts (`Outfit`)

### What I learned

Working through this project helped me understand the CSS box model and how `box-sizing: border-box` keeps declared dimensions accurate when adding padding. My research pointed out that Figma width and height includes padding. So i had to go with border-box method.

I also learned how `margin: auto` distributes unallocated space inside a Flexbox container(used to position footer at the bottom): 

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.container {
  width: 320px;
  padding: 16px 16px 40px 16px;
  margin: auto;
}

```

Adding horizontal padding directly to text elements also showed me how to precisely control line wraps:

```css
p {
  padding: 0 16px;
}

```

### Continued development

In future challenges, I want to keep practicing:

* Writing semantic container elements (like `<main>` and `<article>`).
* Handling responsiveness across different viewport widths.
* Positioning utility items like footers cleanly without disrupting primary centered layouts.

### AI Collaboration

* **Tools used:** AI Assistant
* **How it was used:** Guided debugging to diagnose card sizing discrepancies, box-model behavior, text wrapping, and Flexbox auto-margin distribution.
* **Key takeaways:** Rather than generating copy-paste solutions, discussing the layout mechanics helped build a solid mental model of how padding affects total element width.

## Author

* Frontend Mentor - [@robotraja96](https://www.frontendmentor.io/profile/robotraja96)