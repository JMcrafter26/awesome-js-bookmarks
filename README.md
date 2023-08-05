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

A bookmarklet to monitor the performance of your website.

<a target="_blank" href="javascript:(function(){var script=document.createElement('script');script.onload=function(){var stats=new Stats();document.body.appendChild(stats.dom);requestAnimationFrame(function loop(){stats.update();requestAnimationFrame(loop)});};script.src='https://mrdoob.github.io/stats.js/build/stats.min.js';document.head.appendChild(script);})()">Performance Monitor</a>

```javascript
javascript:(function(){var script=document.createElement('script');script.onload=function(){var stats=new Stats();document.body.appendChild(stats.dom);requestAnimationFrame(function loop(){stats.update();requestAnimationFrame(loop)});};script.src='https://mrdoob.github.io/stats.js/build/stats.min.js';document.head.appendChild(script);})()
```

Original Source: [Stats.js by Mr.doob](https://mrdoob.github.io/stats.js/)

### In-Page Console

A bookmarklet to open a console in the current page. (Useful for mobile devices)

<a target="_blank" href="javascript:(function () { var script = document.createElement('script'); script.src='https://cdn.jsdelivr.net/npm/eruda'; document.body.append(script); script.onload = function () { eruda.init(); } })();" >Console</a>

```javascript
javascript:(function () { var script = document.createElement('script'); script.src='https://cdn.jsdelivr.net/npm/eruda'; document.body.append(script); script.onload = function () { eruda.init(); } })();"
```

Original Source: [Eruda by liriliri](https://eruda.liriliri.io)

## How to Use

### Option 1: Dragging to your bookmarks bar

1. Drag the JS Bookmarks link you want to add to your bookmarks bar.
2. Done! You can now click the bookmarklet to run it on any page.

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

--Coming Soon--
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