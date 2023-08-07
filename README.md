# Awesome JS Bookmarks

A collection of awesome JavaScript bookmarks, to make your life easier.

## Table of Contents

- [Awesome JS Bookmarks](#awesome-js-bookmarks)
  - [Table of Contents](#table-of-contents)
  - [JS Bookmarks](#js-bookmarks)
    - [Performance Monitor](#performance-monitor)
    - [In-Page Console](#in-page-console)
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
javascript:(function () { var script = document.createElement('script'); script.src='https://cdn.jsdelivr.net/npm/eruda'; document.body.append(script); script.onload = function () { eruda.init(); } })();"
```

Original Source: [Eruda by liriliri](https://eruda.liriliri.io)

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