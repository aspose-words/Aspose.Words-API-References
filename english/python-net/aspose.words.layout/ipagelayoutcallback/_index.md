---
title: IPageLayoutCallback class
linktitle: IPageLayoutCallback class
articleTitle: IPageLayoutCallback class
second_title: Aspose.Words for Python
description: "aspose.words.layout.IPageLayoutCallback class. Implement this interface if you want to have your own custom method called during build and rendering of page layout model."
type: docs
weight: 30
url: /python-net/aspose.words.layout/ipagelayoutcallback/
---

## IPageLayoutCallback class

Implement this interface if you want to have your own custom method called during build and rendering of page layout model.


### Remarks

The primary use for this interface is to allow application code to abort build process.


It is possible to build page layout model for only a few pages at start of the document then abort process and render only what has been built already.


Note, however, that rendering results may not match what would be rendered for each page if process would have finished.


This technique may not work for every document or may fail completely.




### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#pagelayoutcallbackargs) | This is called to notify of layout build and rendering progress. |

### See Also

* module [aspose.words.layout](../)
* property [LayoutOptions.callback](../layoutoptions/callback/)

