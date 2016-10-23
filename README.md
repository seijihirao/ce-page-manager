# \<ce-page-manager\>

Custom Element to help managing pages using polymer.

## INSTALL

```
$ bower install --save ce-page-manager
```

## IMPORT

```HTML
    <link rel="import" href="../bower_components/ce-page-manager/json-page-manager.html">
```

## USING

```HTML
    <ce-page-manager 
        site-map="/my/sitemap.json" 
        pages-dir="/my/pages/dir">
    </ce-page-manager>
```

```json
{
    "": "my-page-home",
    "page1": "my-page-element1",
    "page2": "my-page-element2",
    "subpages1": {
        "page1": "my-page-element3",
        "page2": "my-page-element4"
    },
    "subpages2": {
        "": "my-page-element5",
        "page1": "my-page-element6",
        "page2": "my-page-element7"
    },
    "*": "my-dynamic-page"
}
```

This is for the following folder structure

```
my/
    sitemap.json
    pages/
        dir/
            my-page-home.html
            my-page-element1.html
            my-page-element2.html
            my-page-element3.html
            my-page-element4.html
            my-page-element5.html
            my-page-element6.html
            my-page-element7.html
            my-dynamic-page.html
```

And produce the following urls

```
/
/page1
/page2
/subpages1/page1
/subpages1/page2
/subpages2/page1
/subpages2/page2
/*
```

> Note that any url that doesn't exists will go to /*
