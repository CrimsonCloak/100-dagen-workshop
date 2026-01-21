# Workshop Steps: From Starter to Solution

This document outlines all the steps required to complete the 100-dagen website from the starter file to the solution file.

## Step 1: Add Tailwind CSS CDN
**Location:** `<head>` section, after Google Fonts links

Replace the TODO comment about adding Tailwind CSS with the actual CDN link:
```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

---

## Step 2: Add Website Title
**Location:** `<title>` tag in `<head>` section

Add the page title:
```html
<title>100-dagen website</title>
```

---

## Step 3: Set Default Font for Body
**Location:** `<body>` tag

Add the font class to the body element:
- Add `font-[Bokor]` to the body's class attribute
- Final body tag should be: `<body class="flex flex-col font-[Bokor]">`

---

## Step 4: Implement Second Counter
**Location:** Inside the `$(document).ready()` function in the `<script>` tag

Replace the TODO comment with the actual function call:
```javascript
setTimeout(() => countSecondsSinceBirth(), 1000);
```

---

## Step 5: Style Zone 1 (Scroll Down Section)
**Location:** `<div id="zone1">` element

Modify the element to add:
- Background gradient: `bg-linear-to-r from-red-300 to-amber-500`
- Flex layout: `flex flex-col items-center justify-center`
- Bottom margin: `mb-5`

Also update the `<h1>` tag to:
- Change font to `font-[Indie_Flower]`
- Change text color to `text-lime-600`

Final element should be:
```html
<div id="zone1" class="block w-full h-screen flex flex-col items-center justify-center bg-linear-to-r from-red-300 to-amber-500 mb-5">
    <h1 class="font-[Indie_Flower] text-3xl text-lime-600 font-extrabold">Scroll zachtjes naar beneden</h1>
    <img src="img/navigate-down.png" alt="pijl naar beneden">
</div>
```

---

## Step 6: Style Zone 2 (School Start Section)
**Location:** `<div id="zone2">` element

Add to the zone2 div:
- Layout: `flex flex-row-reverse items-center`
- Background: `bg-linear-to-r from-cyan-500 to-blue-500`

Final element opening tag should be:
```html
<div id="zone2" class="flex flex-row-reverse items-center bg-linear-to-r from-cyan-500 to-blue-500">
```

---

## Step 7: Style Zone 3 (100 Days Section)
**Location:** `<div id="zone3">` element

Add to the zone3 div:
- Background radial gradient: `bg-radial from-yellow-300 from-0% to-yellow-500`

Update the first `<h1>` tag with "Nog":
- Add font class: `font-[Impact]`
- Add text color: `text-white`
- Change the `<span class="special">` to have color: `text-orange-500`

Update the second `<h1>` tag with "En dat moeten":
- Add font class: `font-[Impact]`
- Change text color to: `text-orange-500`

Final elements should be:
```html
<div id="zone3" class="w-full h-screen bg-radial from-yellow-300 from-0% to-yellow-500">
    <h1 class="pt-10 font-[Impact] text-white text-6xl font-extrabold text-right">Nog <span class="special text-orange-500">100</span> dagen</h1>
    <h1 class="vieren pt-28 font-[Impact] text-orange-500 text-6xl font-extrabold text-center">En dat moeten<br />we vieren!!!</h1>
</div>
```

---

## Step 8: Add Background Image to Zone 4
**Location:** `<div id="zone4">` element

Add the background image class:
```html
<div id="zone4" class="flex justify-center items-start w-full h-screen bg-[url('img/feest.jpg')] bg-cover">
```

Also update the inner `<span>` tag to add red color:
```html
<span class="text-red-600">feestje</span>
```

---

## Step 9: Style Zone 5 (When Section)
**Location:** `<div id="zone5">` element

Add background gradient:
```html
<div id="zone5" class="w-full flex justify-between items-center p-16 text-white bg-linear-to-b from-red-500 to-orange-500">
```

---

## Step 10: Style Zone 6 (Where Section)
**Location:** `<div id="zone6">` element

Add background gradient:
```html
<div id="zone6" class="w-full py-20 px-10 text-white bg-linear-to-b from-neutral-600 to-neutral-900">
```

Also add the Google Maps embed code after the TODO comment. Replace the comment with:
```html
<div id="maps" class="embed-map-responsive">
    <div class="embed-map-container">
        <iframe class="embed-map-frame" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://maps.google.com/maps?width=600&height=400&hl=en&q=arbeidstraat%2014%2C%209300%20Aalst&t=&z=16&ie=UTF8&iwloc=B&output=embed"></iframe>
        <a href="https://sprunkiretake.net" style="font-size:2px!important;color:gray!important;position:absolute;bottom:0;left:0;z-index:1;max-height:1px;overflow:hidden">
            sprunki retake
        </a>
    </div>
    <style>.embed-map-responsive{position:relative;text-align:right;width:100%;height:0;padding-bottom:66.66666666666666%;}.embed-map-container{overflow:hidden;background:none!important;width:100%;height:100%;position:absolute;top:0;left:0;}.embed-map-frame{width:100%!important;height:100%!important;position:absolute;top:0;left:0;}</style>
</div>
```

---

## Step 11: Add Audio File Path
**Location:** Inside the zone4 scroll event handler in the `<script>` tag

Replace the empty audio.src with:
```javascript
audio.src = "audio/feest.mp3";
```

---

## Step 12: Add Video File Path
**Location:** `<video id="danceVideo">` element, in the `<source>` tag

Add the video source:
```html
<source src="video/city.mp4" type="video/mp4">
```

---

## Summary of Changes by Category

### HTML Structure Changes
- Add Tailwind CSS CDN
- Add page title
- Add Google Maps embed in Zone 6

### JavaScript Changes
- Implement second counter function call
- Set audio file path
- Set video file path

### Styling Changes (Tailwind CSS Classes)
- Zone 1: Background gradient, flex layout, font customization
- Zone 2: Flex row-reverse, background gradient
- Zone 3: Radial background gradient, font changes, color updates
- Zone 4: Background image, color accents
- Zone 5: Background gradient
- Zone 6: Background gradient

### Font Changes
- Body: Default font `font-[Bokor]`
- Zone 1 heading: `font-[Indie_Flower]` with `text-lime-600`
- Zone 3 headings: `font-[Impact]` with custom colors

### Color/Styling Updates
- Various text colors applied throughout
- Background gradients using linear and radial gradients
- Opacity and spacing adjustments
