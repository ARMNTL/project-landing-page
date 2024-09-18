# My Landing Site Odin Project

## Intro

todo

## Thanks

todo

## How I made this landing page (mistakes and fixes included)

I used VSCode for Windows.

### Let get started

1. Open VSCode.
2. File > Open Folder...
3. Navigate to your projects folder.
4. New Folder with your project's name.
5. Select Folder to open it in VSCode.
6. File > New File...
7. Name it `index.html`.
8. File > New File...
9. Name it `styles.css`.

> Alternatively, you can use the CLI
>
> 1. Open your CLI.
> 2. `cd` into your project's folder.
> 3. `mkdir my-project-name`.
> 4. `cd my-projct-name`.
> 5. `touch index.html styles.css`.
> 6. `code .`.

10. In `index.html` type `!` and enter for the boilerplate.
11. Change the title.
12. Add `<link rel="stylesheet" href="./styles.css" />` under the title.

> This would be a good time to make the initial commit.

### The Header (HTML)

> Future Me: I like to see the changes for every step. Right click `index.html` in the file explorer then Copy Path. Paste this in your browser's url input field. Refresh it to see any changes in `index.html` and/or `styles.css`.

#### The Top Part: Nav

13. Nest a `<header></header>` in `<body>`.
14. Nest a `<div class="header-container"></div>` in `<header>`.
15. Nest a `<div class="header-nav"></div>` in `"header-container"`.
16. Nest another `<div class="header-hero"></div>` in `"header-container"`.
17. Nest a `<div class="header-logo">Header Logo</div>` in `"header-nav"`.
18. Nest another `<div class="header-links"></div>` in `"header-nav"`.
19. Nest a `<ul></ul>` in `"header-links"`.
20. Nest a `<li>header link one</li>` in `<ul>`.
21. Nest another `<li>header link two</li>` in `<ul>`.
22. Nest another `<li>header link three</li>` in `<ul>`.

#### The Middle (or bottom?) Part: Hero

23. Nest a `<div class="hero-text-container"></div>` in `"header-hero"`.
24. Nest another `<div class="hero-img"></div>` in `"header-hero"`.
25. Nest a `<div class="hero-main-text">This website is awesome</div>` in `"hero-text-container"`.
26. Nest another `<div class="hero-desc-text">This website has ... lower contrast</div>` in `"hero-text-container"`.
27. Nest another `<div class="hero-signup-button"></div>` in `"hero-text-container"`.
28. Nest a `<button>Sign up</button>` in `"hero-signup-button"`.
29. Nest a `<img src="#" alt="this is a placeholder for an image">` in `"hero-img"`.

The `index.html` should look like

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>My Odin Landing Page Project</title>
        <link rel="stylesheet" href="./styles.css" />
    </head>
    <body>
        <header>
            <div class="header-container">
                <div class="header-nav">
                    <div class="header-logo">Header Logo</div>
                    <div class="header-links">
                        <ul>
                            <li>header link one</li>
                            <li>header link two</li>
                            <li>header link three</li>
                        </ul>
                    </div>
                </div>
                <div class="header-hero">
                    <div class="hero-text-container">
                        <div class="hero-main-text">
                            This website is awesome
                        </div>
                        <div class="hero-desc-text">
                            This website has some subtext that goes here under
                            the main title. It's a smaller font and the color is
                            lower contrast
                        </div>
                        <div class="hero-signup-button">
                            <button>Sign up</button>
                        </div>
                    </div>
                    <div class="hero-img">
                        <img src="#" alt="this is a placeholder for an image" />
                    </div>
                </div>
            </div>
        </header>
    </body>
</html>
```

> Time to commit!

### The Header (CSS)

> One thing a like to do is to reset all padding and margins. Optionally, showing a border for all elements.

```css
* {
    margin: 0;
    padding: 0;
    border: 2px dotted red;
}
```

30. Get the font by adding the following at the top of `styles.css`.

```css
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");
```

31. Set the font.

```css
body {
    font-family: Roboto, Arial, sans-serif, system-ui;
}
```

32. Set font and background color.

```css
header {
    background-color: #1f2937;
    color: #fff;
}
```

33. Flex the header container.

```css
.header-container {
    display: flex;
    flex-direction: column;
}
```

34. Flex the header nav.

```css
.header-nav {
    display: flex;
    justify-content: space-between;
}
```

35. Flex the header links, make the bullet points disappear and set a gap.

```css
.header-links ul {
    display: flex;
    list-style-type: none;
    gap: 1em;
}
```

> My first mistake: I just realized didn't wrap the links with `<a></a>`. 'Header Logo' and 'header link ...' should be a links. Doing it now.

```html
<div class="header-logo">
    <!-- edit here -->
    <a href="#">Header Logo</a>
</div>
```

> Same for the other links.

36. Style the ugly links.

```css
a {
    text-decoration: none;
    color: white;
}
```

37. Flex the header hero container.

```css
.header-hero-container {
    display: flex;
    gap: 2em;
    padding: 100px 0;
}
```

38. Add padding to header-container.

```css
.header-container {
    ...
    padding: 0 200px;
}
```

39. Add padding to header-nav.

```css
.header-nav {
    ...
    padding: 1em 0;
}
```

40. Flex grow hero-text-container and hero-img.

```css
.hero-text-container {
    display: flex;
    flex-direction: column;
    gap: 8px;
    flex: 1;
}

.hero-img {
    flex: 1;
    background-color: #6d747d;
}
```

> For the image placeholder background color, I used an online color picker

41. Change font size and color for main hero message as instructed.

```css
.hero-main-text {
    color: #f9faf8;
    font-size: 48px;
    font-weight: 900;
}
```

> Before this the text color was white, I changed them all to #f9faf8

42. Change font size and color for secondary text and header links as instructed.

```css
a {
    text-decoration: none;
    color: #e5e7eb;
    font-size: 18px;
}

.hero-desc-text {
    color: #e5e7eb;
    font-size: 18px;
}
```

43. Change header logo text as instructed.

```css
.header-logo a {
    color: #f9faf8;
    font-size: 24px;
    font-weight: 700;
    /* easy guess the font weight */
}
```

44. Change the button as instructed.

```css
.hero-signup-button button {
    border: none;
    border-radius: 8px;
    color: #e5e7eb;
    background-color: #3882f6;
    padding: 8px 24px;
    font-size: 18px;
    font-weight: bold;
}
```

> Commit, commit, commit!

### The Information Section (HTML)

45. Nest a `<section></section>` in `<body>` under `<header>`.
46. Nest a `<div class="information-container"></div>` in `<section>`.
47. Nest a `<div class="information-header-text">Some random information.</div>` in `information-container`.
48. Nest a `<div class="cards-container"></div>` in `information-container` under `information-header-text`.
49. Nest four (4) `<div class="card"></div>` in `cards-container`.
50. Nest four (4) `<img src="#" alt="some image">` in `card`.
51. Nest four (4) `<p>this is some subtext under an illustration or image</p>` in `card` under `<img>`.

> Commit?

### The Information Section (CSS)

52. Change header text as instructed.

```css
.information-header-text {
    font-size: 36px;
    color: #1f2937;
    font-weight: 900;
}
```

53. Flex information-container.

```css
.information-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 48px 240px;
    gap: 48px;
}
```

54. Flex cards-container.

```css
.cards-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 36px;
}
```

> Here, I decided to go wrap expecting more info cards will be added.

55. Flex card.

```css
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 8px;
}
```

56. Set the card images sizes and border.

```css
.card img {
    min-width: 160px;
    min-height: 160px;
    border: 4px solid #3882f6;
    border-radius: 16px;
}
```

57. Set the card subtext width and alignment.

```css
.card p {
    max-width: 160px;
    text-align: center;
}
```

> Got commit?

### The Testimonial Section (HTML)

58. Nest a `<section></section>` under the last `<section>`.
59. Nest a `<div class="testimonial-container"></div>` in `<section>`
60. Nest a `<p>This is an inspiring quote ... it looks nice.</p>` in `testimonial-container`.
61. Nest a `<div class="signature">-Thor, God of Thunder</div>` in `testimonial-container` under `testimonial`.

> Too soon to commit?
