---
title: Beautify Post by Tag Plugins
date: 2022-04-18 02:08:37
tags: Blog
categories: Blog Update
---
# Why I Create This Post

Using Markdown can help us get a clear website without the knowledge of HTML. There's still several shortages that Markdown's functions are limited compared to HTML. I am also a beginner, so I just try to collect some useful codes for decorating my website pages.

But firstly, we can see that quoting by Markdown syntax can beautify the page.
## Quoting
```markdown
> It's a quoting demonstration.
```
> It's a quoting demonstration.

In the hexo-butterfly theme, the quotation has a blue background. It makes some contents from others distinct from your own ideas.

# Tag Plugins
The next part is for introducing some colorful text boxes to beautify the website.
<div class="note red icon flat"><i class="note-icon fa-solid fa-circle-exclamation"></i><p>What you need to pay attention to is that the following content may <strong>NOT work</strong> for themes other than <strong>hexo-butterfly</strong>, and it is only available in <strong><i>Hexo</i>.</strong></p></div>

The general grammar to create the tag plugins is
```HTML
<div class = "note [color] [class] [icon-choices] [style]">
    <p>PUT YOUR CONTENT HERE</p>
</div>
```

|Name|value|
|---|---|
|color|**red**, **blue**, **green**, **purple**, **pink**, **orange** or just no value for **grey**|
|class|**default**, **primary**, **success**, **info**, **warning**, **danger**|
|icon-choices|**icon** (only available for part of fontawesome icons), **no-icon**|
|style|**simple**, **modern**, **flat**, **disabled**|
## Style

### Style: `flat`


#### Without Content
The original version is `class = "note flat"`.
```HTML
<div class="note flat"></div>
```
<div class="note flat"></div>

You can see grey (I think it's grey) color ribbon appear after you execute your code.

#### Add Text
Then let's increase some texts.
```HTML
<div class="note flat"><p>Hello World!</p></div>
```

<div class="note flat"><p>Hello World!</p></div>

Actually, the result is quite similar to the Markdown quotation on its original renderer.
#### Change Color
Let's change the color of the text box.

```HTML
<div class="note blue flat"><p>Hello World! But in blue background.</p></div>
```
<div class="note blue flat"><p>Hello World! But in blue background.</p></div>

It looks better compared to the original version! 
#### Add Emoji :smiling_face_with_three_hearts:
We can still make more changes to it like add some emojis.

```HTML
<div class="note blue flat"><p>:sunglasses:Hello World in blue background with emoji.:cowboy_hat_face:</p></div>
```
<div class="note blue flat"><p>:sunglasses:Hello World in blue background with emoji.:cowboy_hat_face:</p></div>

#### Add Icon
Alright, it seems to be the end of that part. However, did you notice the empty space between your beginning of text and the beginning of the text box. We can add a icon here. 
```HTML
<div class="note green icon flat"><i class="note-icon fas fa-rocket"></i><p>:point_left:Green rocket is on the left.</p></div>
```

<div class="note green icon flat"><i class="note-icon fas fa-rocket"></i><p>:point_left:Green rocket is on the left.</p></div>

The color of the icon is the same as the text box.

If you don't like the icon, and don't want there's a waste of space in the text box, that's also fine.
```HTML
<div class="note green no-icon flat"></i><p>:disappointed:No icon here.</p></div>
```
<div class="note green no-icon flat"></i><p>:disappointed:No icon here.</p></div>

#### Some Other Colors
```HTML
<div class="note orange icon flat"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon flat">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon flat">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon flat">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>
```
The results are shown below :point_down:.
<div class="note orange icon flat"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>
<div class="note red icon flat">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon flat">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon flat">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>

### Style: `simple`
I will use the same content in the **Style: `flat`** section for the comparison.

```HTML
<div class="note simple"><p>Hello World!</p></div>

<div class="note blue no-icon simple"><p>😎Hello World in blue background with emoji. (Actually, there's no more blue background anymore.:cry:)</p></div>

<div class="note green icon simple"><i class="note-icon fas fa-rocket"></i><p>👈Green rocket is on the left.</p></div>

<div class="note orange icon simple"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon simple">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon simple">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon simple">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>
```

<div class="note simple"><p>Hello World!</p></div>

<div class="note blue no-icon simple"><p>😎Hello World in blue background with emoji. (Actually, there's no more blue background anymore.:cry:)</p></div>

<div class="note green icon simple"><i class="note-icon fas fa-rocket"></i><p>👈Green rocket is on the left.</p></div>

<div class="note orange icon simple"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon simple">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon simple">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon simple">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>

It looks much simpler and cleaner.

### Style: `modern`

The `modern` style is close to the `flat` style. The color of your text will change to the same color as the background.

```HTML
<div class="note modern"><p>Hello World!</p></div>

<div class="note blue no-icon modern"><p>😎Hello World in blue background with emoji. (Actually, there's no more blue background anymore.:cry:)</p></div>

<div class="note green icon modern"><i class="note-icon fas fa-rocket"></i><p>👈Green rocket is on the left.</p></div>

<div class="note orange icon modern"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon modern">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon modern">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon modern">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>
```

<div class="note modern"><p>Hello World!</p></div>

<div class="note blue no-icon modern"><p>😎Hello World in blue background with emoji. (Actually, there's no more blue background anymore.:cry:)</p></div>

<div class="note green icon modern"><i class="note-icon fas fa-rocket"></i><p>👈Green rocket is on the left.</p></div>

<div class="note orange icon modern"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon modern">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon modern">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon modern">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>

### style: `disabled`
No background, the simplest version.

```HTML
<div class="note disabled"><p>Hello World!</p></div>

<div class="note blue no-icon disabled"><p>😎Hello World in blue background with emoji. (Actually, there's no more blue background anymore.:cry:)</p></div>

<div class="note green icon disabled"><i class="note-icon fas fa-rocket"></i><p>👈Green rocket is on the left.</p></div>

<div class="note orange icon disabled"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon disabled">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon disabled">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon disabled">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>
```


<div class="note disabled"><p>Hello World!</p></div>

<div class="note blue no-icon disabled"><p>😎Hello World in blue background with emoji. (Actually, there's no more blue background anymore.:cry:)</p></div>

<div class="note green icon disabled"><i class="note-icon fas fa-rocket"></i><p>👈Green rocket is on the left.</p></div>

<div class="note orange icon disabled"><i class="note-icon fas fa-magic"></i><p>Do something <strong>WISELY</strong></p></div>

<div class="note red icon disabled">
    <i class="note-icon fa-brands fa-github"></i>
    <p>First 
        <code>git add .</code>, then 
        <code>git commit -m"xxx"</code>, finally 
        <code>git push</code>.
    </p>
</div>

<div class="note purple icon disabled">
    <i class="note-icon fa-solid fa-apple-whole"></i>
    <p>Alright, do you like purple?</p>
</div>

<div class="note pink icon disabled">
    <i class="note-icon fa-solid fa-anchor"></i>
    <p>Pink color looks so cute.</p>
</div>

## Class
You can change the color for the different classes, but the icon in the classes will not change as the color changes. So I don't encourage you to change the color of the classes, if you still want to do so, try to use the `class = "note [color] [icon] [style]"` instead.

### Class: `default`
```HTML
<div class="note default flat"><p>It is the default class.</p></div>
```
<div class="note default flat"><p>It is the default class.</p></div>

### Class: `primary`
```HTML
<div class="note primary flat"><p>It is the primary class.</p></div>
```
<div class="note primary flat"><p>It is the primary class.</p></div>

### Class: `success`
```HTML
<div class="note success flat"><p>It is the success class.</p></div>
```
<div class="note success flat"><p>It is the success class.</p></div>

### Class: `info`
```HTML
<div class="note info flat"><p>It is the info class.</p></div>
```
<div class="note info flat"><p>It is the info class.</p></div>

### Class: `warning`
```HTML
<div class="note warning flat"><p>It is the warning class.</p></div>
```
<div class="note warning flat"><p>It is the warning class.</p></div>

Personally, it seems to be more persuasive to use the red color to show the warning.

Maybe you can try
```HTML
<div class="note red icon flat"><i class="note-icon fa-solid fa-circle-exclamation"></i><p>Strong warning is always in red.</p></div>
```
<div class="note red icon flat"><i class="note-icon fa-solid fa-circle-exclamation"></i><p>Strong warning is always in red.</p></div>

### Class: `danger`
```HTML
<div class="note danger flat"><p>It is the danger class.</p></div>
```
<div class="note danger flat"><p>It is the danger class.</p></div>

# In The End
That's' all for this post, if you are using the hexo-butterfly theme, hope the blog will help you. And in the future I will try to make the tag plugins available in my way. Thanks for your reading.

