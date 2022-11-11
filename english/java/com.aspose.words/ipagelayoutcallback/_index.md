---
title: IPageLayoutCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to have your own custom method called during build and rendering of page layout model.
type: docs
weight: 653
url: /java/com.aspose.words/ipagelayoutcallback/
---
```
public interface IPageLayoutCallback
```

Implement this interface if you want to have your own custom method called during build and rendering of page layout model. The primary use for this interface is to allow application code to abort build process.

It is possible to build page layout model for only a few pages at start of the document then abort process and render only what has been built already.

Note, however, that rendering results may not match what would be rendered for each page if process would have finished.

This technique may not work for every document or may fail completely.
## Methods

| Method | Description |
| --- | --- |
| [notify(PageLayoutCallbackArgs args)](#notify-com.aspose.words.PageLayoutCallbackArgs-) | This is called to notify of layout build and rendering progress. |
### notify(PageLayoutCallbackArgs args) {#notify-com.aspose.words.PageLayoutCallbackArgs-}
```
public abstract void notify(PageLayoutCallbackArgs args)
```


This is called to notify of layout build and rendering progress.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../com.aspose.words/pagelayoutcallbackargs) | An argument of the event. Exception when thrown by implementation aborts layout build process. |

