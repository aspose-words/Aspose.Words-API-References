---
title: PageLayoutCallbackArgs
second_title: Aspose.Words for Java API Reference
description: An argument passed into
type: docs
weight: 435
url: /java/com.aspose.words/pagelayoutcallbackargs/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutCallbackArgs
```

An argument passed into [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-)

To learn more, visit the **Converting to Fixed-page Format** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getEvent()](#getEvent--) | Gets event. |
| [getDocument()](#getDocument--) | Gets document. |
| [getPageIndex()](#getPageIndex--) | Gets 0-based index of the page in the document this event relates to. |
### getEvent() {#getEvent--}
```
public int getEvent()
```


Gets event.

**Returns:**
int - Event. The returned value is one of [PageLayoutEvent](../../com.aspose.words/pagelayoutevent) constants.
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Gets document.

**Returns:**
[Document](../../com.aspose.words/document) - Document.
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Gets 0-based index of the page in the document this event relates to. Returns negative value if there is no associated page, or if page was removed during reflow.

**Returns:**
int - 0-based index of the page in the document this event relates to.
