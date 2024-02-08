# Basic JavaScript Exercises Template

## Setup

- This template is has the following directory structure

```bash
.
├── assets
│   ├── css
│   │   ├── reset.css
│   │   └── style.css
│   └── images
│       └── logo.svg
├── index.html
├── index.js
└── README.md
```

- The `index.html` file defines some basic markup for a "in-browser console" window
- It's using [@weyvern/dom-logger](https://www.npmjs.com/package/@weyvern/dom-logger) to output the messages to the "in-browser console" and the native one in developer tools
- You can see the instantiation of this class in `index.js`

```html
<script type="module">
  import DOMLogger from 'https://unpkg.com/@weyvern/dom-logger';
  window.logger = new DOMLogger(document.getElementById('output'), true);
</script>
```

- Within [Visual Studio Code](https://code.visualstudio.com/):

  - Install [Live Preview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server)
  - Right click anywhere on `index.html`
  - Select `Show Preview`
  - A server will start and a preview window will open
    
![Screenshot from 2024-02-07 12-55-15](https://github.com/WebDev-WBSCodingSchool/template-basic-javascript/assets/19370560/a597bb0e-db7f-4156-b417-d7e0dd115737)

  - If the `DOMLogger` was instantiated with a `true` argument for `native`, the message will also be output to the native console
  - You can see those messages by opening the `Output` tab and select `Embedded Live Preview Console` as shown [here](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server#console-output-channel-for-embedded-preview)

![Screenshot from 2024-02-07 12-59-07](https://github.com/WebDev-WBSCodingSchool/template-basic-javascript/assets/19370560/0f77046b-dd50-46c6-9595-0331bc811177)
  
  - You can control the behaviour of Live Refresh with the `livePreview.autoRefreshPreview` setting, or open VSCode settings, looking for Live Preview and changing the value from the dropdown

## Instructions for content creators

- This template is to be used for basic JavaScript exercises for foundational modules
- Click the **Use this template** button on this repo

- Choose a title for the repo following the following naming convention:

```bash
XXX-module-name-topic
```

e.g.

```bash
001-intro-to-js-conditional-statements
```

- If you have any question regarding the naming, contact your Program Owner
- Change the `title` in `index.html` file to match the name of the repo

from this:

```html
<title>xxx-module-name-topic</title>
```

to this:

```html
<title>001-intro-to-js-conditional-statements</title>
```

- In `index.js`, write the instructions for the exercise, e.g.

```js
try {
  // Don't the previous line
  ////////////YOUR CODE GOES FROM HERE////////////
  // Create an if/else statement
  // Create a switch statement
  // Create a function that takes one paramente call param and, with the help of switch statemnt, returns this, this or that
  ////////////TO HERE ////////////
  // Don't modify anything below this line
} catch (error) {
  logger.error(error);
}
```

- Before publishing:
- Edit the `README.md` to remove any instructions for content creators
- :warning: Keep the **Setup** instructions
- Add a section with `##` called `Goal` and write a detailed explanation of the exercise goals
- Add a section with `##` called `Instructions` and write a detailed explanation of the exercise constraints
- Open a PR to the repo with your exercises and `README.md` and select your Program Owner as reviewer
