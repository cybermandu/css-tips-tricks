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

