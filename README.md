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

