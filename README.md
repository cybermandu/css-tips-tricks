# CSS Tips and Tricks
Cool CSS Tips and tricks collected from around the web

### Finding layout issues
Sometimes it becomes difficult to find the layout issues. Below CSS snippet can be used to hightlight different depth of nodes with different color. It makes easy to see the size of each element on the page, their margin and their padding and can easily find inconsistencies.

    * { background-color: rgba(255,0,0,.2); }
    * * { background-color: rgba(0,255,0,.2); }
    * * * { background-color: rgba(0,0,255,.2); }
    * * * * { background-color: rgba(255,0,255,.2); }
    * * * * * { background-color: rgba(0,255,255,.2); }
    * * * * * * { background-color: rgba(255,255,0,.2); }
    * * * * * * * { background-color: rgba(255,0,0,.2); }
    * * * * * * * * { background-color: rgba(0,255,0,.2); }
    * * * * * * * * * { background-color: rgba(0,0,255,.2); }

### Style Broken Images
Broken images are ugly. We can use CSS to apply styles to the `<img>` element to provide a better experience than the default. Below is the example how we can style broken images. [Source bitsofco.de](https://bitsofco.de/styling-broken-images/) 

    img {
        font-family: 'Helvetica';
        font-weight: 300;
        line-height: 2;  
        text-align: center;
        width: 100%;
        height: auto;
        display: block;
        position: relative;
    }

    img:before { 
      content: "We're sorry, the image below is broken :(";
      display: block;
      margin-bottom: 10px;
    }

    img:after { 
      content: "(url: " attr(src) ")";
      display: block;
      font-size: 12px;
    }

### Responsive font size using clamp()
Found this very good concept for responsive font size using `clamp()` function. [Source css-tricks.com](https://css-tricks.com/min-max-and-clamp-are-css-magic/) Browser support [Caniuse](https://caniuse.com/css-math-functions)

    .el {
        font-size: clamp(0.9rem, 1vw + 1rem, 2.2rem);
    }

### Dark Mode using CSS
Achieving Dark Mode with simple CSS trick [Source Dev.to](https://dev.to/akhilarjun/one-line-dark-mode-using-css-24li)

    html[theme='dark-mode'] {
        filter: invert(1) hue-rotate(180deg);
    }
    
    html[theme='dark-mode'] img{
        filter: invert(1) hue-rotate(180deg);
    }
    
### Browser Support
`@supports` allows you to check the browser support for CSS property:value pairs. The code that is included in the `@supports` block will be rendered only if these conditions are true, otherwise the code has not been read by the browser. In a case where the browser doesn’t understand `@supports`, it doesn’t generate a given part of the code either. [Source creativebloq](https://www.creativebloq.com/features/css-tricks-to-revolutionise-your-layouts)

    @supports (mix-blend-mode: overlay) {
        .example {
            mix-blend-mode: overlay;
         }
    }
