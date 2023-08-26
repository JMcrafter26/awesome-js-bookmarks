# Awesome JS Bookmarks

A collection of awesome JavaScript bookmarks, to make your life easier.

## Table of Contents

- [Awesome JS Bookmarks](#awesome-js-bookmarks)
  - [Table of Contents](#table-of-contents)
  - [JS Bookmarks](#js-bookmarks)
    - [Performance Monitor](#performance-monitor)
    - [In-Page Console](#in-page-console)
    - [Auto Clicker](#auto-clicker)
  - [How to Use](#how-to-use)
    - [Option 1: Dragging to your bookmarks bar](#option-1-dragging-to-your-bookmarks-bar)
    - [Option 2: Manually creating a bookmark](#option-2-manually-creating-a-bookmark)
      - [Chrome](#chrome)
      - [Firefox](#firefox)
      - [Safari](#safari)
      - [Safari (iOS)](#safari-ios)
      - [Opera](#opera)
      - [Edge](#edge)

## JS Bookmarks

### Performance Monitor

Shows performance statistics in the corner of the screen.

<a target="_blank" href="https://api.jm26.net/awesome-js-bookmarks/index.php?id=1">Add Performance Monitor</a>

```javascript
javascript:(function(){var script=document.createElement('script');script.onload=function(){var stats=new Stats();document.body.appendChild(stats.dom);requestAnimationFrame(function loop(){stats.update();requestAnimationFrame(loop)});};script.src='https://mrdoob.github.io/stats.js/build/stats.min.js';document.head.appendChild(script);})()
```

Original Source: [Stats.js by Mr.doob](https://mrdoob.github.io/stats.js/)

### In-Page Console

Adds a console to the page. Click the console icon in the bottom right corner to open it.

<a target="_blank" href="https://api.jm26.net/awesome-js-bookmarks/index.php?id=2">Add In-Page Console</a>

```javascript
javascript:(function () { var script = document.createElement('script'); script.src='https://cdn.jsdelivr.net/npm/eruda'; document.body.append(script); script.onload = function () { eruda.init(); } })();
```

Original Source: [Eruda by liriliri](https://eruda.liriliri.io)


### Auto Clicker

Automatically clicks on a specified element with a specified delay. Click the button in the top left corner to stop the auto clicker.

<a target="_blank" href="https://api.jm26.net/awesome-js-bookmarks/index.php?id=3">Add Auto Clicker</a>

```javascript
javascript:(function () {var DELAY=0;var PULSE=true;if(delay==null||delay==undefined||delay==0){var delay=prompt('Enter delay in milliseconds (default 0):');if(delay){DELAY=parseInt(delay)}}if(document.getElementById('auto-clicker-button')){var remove=confirm('Auto Clicker is already running. Do you want to remove it?');if(remove){document.getElementById('auto-clicker-button').click()}}var autoClickerStyleElement=document.createElement('style');autoClickerStyleElement.innerHTML='*{cursor: crosshair !important;}';autoClickerStyleElement.id='auto-clicker-style';document.body.appendChild(autoClickerStyleElement);var autoClickerButtonStyleElement=document.createElement('style');autoClickerButtonStyleElement.innerHTML=`\n.auto-clicker-button {\n position: fixed !important;\n top: 0 !important;\n left: 0 !important;\n z-index: 9999999 !important;\n background-color: #fe5858 !important;\n border: 1px solid #fe5858 !important;\n border-radius: 10px !important;\n color: white !important;\n padding: 8px 16px !important;\n text-align: center !important;\n font-size: 16px !important;\n cursor: pointer !important;\n margin: 10px !important;\n opacity: 0.5 !important;\n transition all 0.3s ease-in-out !important;\n}\n.auto-clicker-button:hover {\n border: 1px solid transparent;\n border-radius: 10px;\n opacity: 1 !important;\n}\n\n.auto-clicker-pulse-animation {\n animation: auto-clicker-pulse-animation 1s infinite ease-in-out;\n}\n\n@keyframes auto-clicker-pulse-animation {\n 0% {\n transform: scale(0.95);\n box-shadow: 0 0 0 0 rgba(0, 0, 0, 0.7);\n }\n\n 70% {\n transform: scale(1);\n box-shadow: 0 0 0 10px rgba(0, 0, 0, 0);\n }\n\n 100% {\n transform: scale(0.95);\n box-shadow: 0 0 0 0 rgba(0, 0, 0, 0);\n }\n}\n`;autoClickerButtonStyleElement.id='auto-clicker-button-style';document.body.appendChild(autoClickerButtonStyleElement);var autoClickerButton=document.createElement('button');autoClickerButton.innerHTML='Exit Auto Clicker';autoClickerButton.id='auto-clicker-button';autoClickerButton.classList.add('auto-clicker-button');autoClickerButton.addEventListener('click',(function(){console.log('Auto Clicker Deactivated');var autoClickerElements=document.getElementsByClassName('auto-clicker-target');for(var i=0;i<autoClickerElements.length;i++){autoClickerElements[i].classList.remove('auto-clicker-target')}document.body.removeEventListener('click',addClicker);if(PULSE){var autoClickerPulseElements=document.getElementsByClassName('auto-clicker-pulse-animation');for(var i=0;i<autoClickerPulseElements.length;i++){autoClickerPulseElements[i].classList.remove('auto-clicker-pulse-animation')}}if(document.getElementById('auto-clicker-style')){document.getElementById('auto-clicker-style').remove()}document.getElementById('auto-clicker-button-style').remove();autoClickerButton.style.display='none';autoClickerButton.removeEventListener('click',arguments.callee);document.body.removeChild(autoClickerButton)}));document.body.appendChild(autoClickerButton);console.log('Auto Clicker made with ❤ by JMcrafter26 (https://github.com/JMcrafter26)');function addClicker(e){if(!e.isTrusted){return}document.body.removeChild(autoClickerStyleElement);document.body.removeEventListener('click',addClicker);e.preventDefault();var clickableElement=checkClick(e);if(clickableElement==null){alert('The element you clicked is not clickable. Please be more accurate and try again.');autoClickerButton.click();return}if(clickableElement.classList.contains('auto-clicker-target')){clickableElement.classList.remove('auto-clicker-target');if(PULSE){clickableElement.classList.remove('auto-clicker-pulse-animation')}}else{clickableElement.classList.add('auto-clicker-target');if(PULSE){clickableElement.classList.add('auto-clicker-pulse-animation')}}console.log('Auto Clicker Activated');autoClick(clickableElement)}function checkClick(e){if(e.target.getAttribute('onclick')!=null||e.target.tagName=='BUTTON'||e.target.tagName=='A'){return e.target}else{var parent=e.target.parentElement;var child=e.target.firstElementChild;var maxDepth=3;var depth=0;if(parent!=null){while(parent!=null&&depth<maxDepth){if(parent.getAttribute('onclick')!=null||parent.tagName=='BUTTON'||parent.tagName=='A'){return parent}parent=parent.parentElement;depth++}}else{}depth=0;if(child!=null){while(child!=null&&depth<maxDepth){if(child.getAttribute('onclick')!=null||child.tagName=='BUTTON'||child.tagName=='A'){return child}child=child.firstElementChild;depth++}}else{}if(parent==null&&child==null){return}}}function autoClick(element){if(element.classList.contains('auto-clicker-target')){element.click();setTimeout((function(){autoClick(element)}),DELAY)}}document.body.addEventListener('click',addClicker,0);}());
```

Original Source: [Auto Clicker by JMcrafter26](https://github.com/JMcrafter26/awesome-js-bookmarks#auto-clicker)

## How to Use

### Option 1: Dragging to your bookmarks bar

1. Click the "Add JS Bookmark" link of the JS Bookmark you want to add, this will open an new page.
2. Drag the blue button to your bookmarks bar.
3. Done! You can now click the bookmarklet to run it on any page.

![How to use](./how-to-use.gif)

### Option 2: Manually creating a bookmark

Choose your browser: [Chrome](####Chrome), [Firefox](####Firefox), [Safari](####Safari), [Opera](####Opera), [Edge](####Edge)

#### Chrome

1. Copy the code from the JS Bookmark you want to add.
2. Right-click your bookmarks bar and select "Add Page".
3. In the "Name" field, enter the name of the js bookmarklet or whatever you want to call it.
4. Paste the copied code into the URL field of the bookmark.
5. Done! You can now click the bookmarklet to run it on any page.

#### Firefox

1. Copy the code from the JS Bookmark you want to add.
2. Right-click your bookmarks bar and select "Add Bookmark".
3. In the "Name" field, enter the name of the js bookmarklet or whatever you want to call it.
4. Paste the code into the URL field of the bookmark.
5. Done! You can now click the bookmarklet to run it on any page.

#### Safari

1. Copy the code from the JS Bookmark you want to add.
2. Right-click your bookmarks bar and select "Add Bookmark".
3. In the "Name" field, enter the name of the js bookmarklet or whatever you want to call it.
4. Paste the code into the URL field of the bookmark.
5. Done! You can now click the bookmarklet to run it on any page.

#### Safari (iOS)

Beta shortcut: [Get shortcut](https://www.icloud.com/shortcuts/8ee4bc67c55b4f948dd1ec4061521742)


#### Opera

1. Copy the code from the JS Bookmark you want to add.
2. Right-click your bookmarks bar and select "Add Website".
3. In the "Name" field, enter the name of the js bookmarklet or whatever you want to call it.
4. Paste the code into the URL field of the bookmark.
5. Done! You can now click the bookmarklet to run it on any page.

#### Edge

1. Copy the code from the JS Bookmark you want to add.
2. Right-click your bookmarks bar and click on "Manage Favorites".
3. Then click on "Add favorite" at the top of the list.
4. In the "Name" field, enter the name of the js bookmarklet or whatever you want to call it.
5. Paste the code into the URL field of the bookmark.
6. Done! You can now click the bookmarklet to run it on any page.