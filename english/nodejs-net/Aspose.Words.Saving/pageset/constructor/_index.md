---
title: PageSet constructor
linktitle: PageSet constructor
articleTitle: PageSet constructor
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PageSet constructor"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Saving/pageset/constructor/
---

## PageSet(page) {#number}

Creates an one-page set based on exact page index.


```js
PageSet(page: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| page | number | Zero-based index of the page. |

### Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering.
int.MaxValue C# constant means the last page in the document.



## PageSet(pages) {#number[]}

Creates a page set based on exact page indices.


```js
PageSet(pages: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| pages | number[] | Zero-based indices of pages. |

### Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering.
int.MaxValue C# constant means the last page in the document.



## PageSet(ranges) {#pagerange[]}

Creates a page set based on ranges.


```js
PageSet(ranges: Aspose.Words.Saving.PageRange[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| ranges | [PageRange](../../pagerange/)[] | Array of page ranges. |

### Remarks

If a range is encountered that starts after the last page in the document, 
an exception will be thrown during rendering.
All ranges that end after the last page are truncated to fit in the document.


## See Also

* module [Aspose.Words.Saving](../../)
* class [PageSet](../)

