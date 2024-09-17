# My Landing Site Odin Project

## Intro

todo

## Thanks

todo

## How I made this landing page (mistakes and fixes included)

I used VSCode for Windows.

### Let get started

1. Open VSCode
2. File > Open Folder...
3. Navigate to your projects folder
4. New Folder with your project's name
5. Select Folder to open it in VSCode
6. File > New File...
7. Name it `index.html`
8. File > New File...
9. Name it `styles.css`

> Alternatively, you can use the CLI
>
> 1. Open your CLI
> 2. `cd` into your project's folder
> 3. `mkdir my-project-name`
> 4. `cd my-projct-name`
> 5. `touch index.html styles.css`
> 6. `code .`

10. In `index.html` type `!` and enter for the boilerplate
11. Change the title
12. Add `<link rel="stylesheet" href="./styles.css" />` under the title

> This would be a good time to make the initial commit

### The Header (HTML)

#### The Top Part: Nav

13. Nest a `<header></header>` in `<body>`
14. Nest a `<div class="header-container"></div>` in `<header>`
15. Nest a `<div class="header-nav"></div>` in `"header-container"`
16. Nest another `<div class="header-hero"></div>` in `"header-container"`
17. Nest a `<div class="header-logo">Header Logo</div>` in `"header-nav"`
18. Nest another `<div class="header-links"></div>` in `"header-nav"`
19. Nest a `<ul></ul>` in `"header-links"`
20. Nest a `<li>header link one</li>` in `<ul>`
21. Nest another `<li>header link two</li>` in `<ul>`
22. Nest another `<li>header link three</li>` in `<ul>`

#### The Middle (or bottom?) Part: Hero

23. Nest a `<div class="hero-text-container"></div>` in `"header-hero"`
24. Nest another `<div class="hero-img"></div>` in `"header-hero"`
25. Nest a `<div class="hero-main-text">This website is awesome</div>` in `"hero-text-container"`
26. Nest another `<div class="hero-desc-text">This website has ... lower contrast</div>` in `"hero-text-container"`
27. Nest another `<div class="hero-signup-button"></div>` in `"hero-text-container"`
28. Nest a `<button>Sign up</button>` in `"hero-signup-button"`
29. Nest a `<img src="#" alt="this is a placeholder for an image">` in `"hero-img"`

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
