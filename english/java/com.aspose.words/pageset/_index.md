---
title: PageSet
second_title: Aspose.Words for Java API Reference
description: Describes a random set of pages.
type: docs
weight: 439
url: /java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object
```
public class PageSet
```

Describes a random set of pages.

To learn more, visit the **Programming with Documents** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [PageSet(int page)](#PageSet-int-) | Creates an one-page set based on exact page index. |
| [PageSet(int[] pages)](#PageSet-int...-) | Creates a page set based on exact page indices. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...-) | Creates a page set based on ranges. |
## Methods

| Method | Description |
| --- | --- |
| [getAll()](#getAll--) | Gets a set with all the pages of the document in their original order. |
| [getEven()](#getEven--) | Gets a set with all the even pages of the document in their original order. |
| [getOdd()](#getOdd--) | Gets a set with all the odd pages of the document in their original order. |
### PageSet(int page) {#PageSet-int-}
```
public PageSet(int page)
```


Creates an one-page set based on exact page index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| page | int | Zero-based index of the page. If a page is encountered that is not in the document, an exception will be thrown during rendering.  means the last page in the document. |

### PageSet(int[] pages) {#PageSet-int...-}
```
public PageSet(int[] pages)
```


Creates a page set based on exact page indices.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pages | int[] | Zero-based indices of pages. If a page is encountered that is not in the document, an exception will be thrown during rendering.  means the last page in the document. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...-}
```
public PageSet(PageRange[] ranges)
```


Creates a page set based on ranges.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange) | Array of page ranges. If a range is encountered that starts after the last page in the document, an exception will be thrown during rendering. All ranges that end after the last page are truncated to fit in the document. |

### getAll() {#getAll--}
```
public static PageSet getAll()
```


Gets a set with all the pages of the document in their original order.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - A set with all the pages of the document in their original order.
### getEven() {#getEven--}
```
public static PageSet getEven()
```


Gets a set with all the even pages of the document in their original order. Even pages have odd indices since page indices are zero-based.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - A set with all the even pages of the document in their original order.
### getOdd() {#getOdd--}
```
public static PageSet getOdd()
```


Gets a set with all the odd pages of the document in their original order. Odd pages have even indices since page indices are zero-based.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - A set with all the odd pages of the document in their original order.