---
title: PageLayoutEvent
second_title: Aspose.Words for Java API Reference
description: A code of event raised during page layout model build and rendering.
type: docs
weight: 436
url: /java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

A code of event raised during page layout model build and rendering.

Page layout model is built in two steps. First, "conversion step", this is when page layout pulls document content and creates object graph. Second, "reflow step", this is when structures are split, merged and arranged into pages.

Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format. For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Default value |
| [WATCH_DOG](#WATCH-DOG) | Corresponds to a checkpoint in code which is often visited and which is suitable to abort process. |
| [BUILD_STARTED](#BUILD-STARTED) | Build of the page layout has started. |
| [BUILD_FINISHED](#BUILD-FINISHED) | Build of the page layout has finished. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | Conversion of document model to page layout has started. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | Conversion of document model to page layout has finished. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Reflow of the page layout has started. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Reflow of the page layout has finished. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Reflow of the page has started. |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Reflow of the page has finished. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Rendering of page has started. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Rendering of page has finished. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pageLayoutEvent)](#getName-int-) |  |
| [toString(int pageLayoutEvent)](#toString-int-) |  |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


Default value

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Corresponds to a checkpoint in code which is often visited and which is suitable to abort process.

While inside [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-) throw custom exception to abort process.

You can throw when handling any callback event to abort process.

Note that if process is aborted the page layout model remains in undefined state. If process is aborted upon reflow of a complete page, however, it should be possible to use layout model up to the end of that page.

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


Build of the page layout has started. Fired once. This is the first event which occurs when [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) is called.

### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


Build of the page layout has finished. Fired once. This is the last event which occurs when [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) is called.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Conversion of document model to page layout has started. Fired once. This occurs when layout model starts pulling document content.

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Conversion of document model to page layout has finished. Fired once. This occurs when layout model stops pulling document content.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Reflow of the page layout has started. Fired once. This occurs when layout model starts reflowing document content.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Reflow of the page layout has finished. Fired once. This occurs when layout model stops reflowing document content.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Reflow of the page has started. Note that page may reflow multiple times and that reflow may restart before it is finished.

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Reflow of the page has finished. Note that page may reflow multiple times and that reflow may restart before it is finished.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Rendering of page has started. This is fired once per page.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Rendering of page has finished. This is fired once per page.

### length {#length}
```
public static int length
```


### getName(int pageLayoutEvent) {#getName-int-}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
### toString(int pageLayoutEvent) {#toString-int-}
```
public static String toString(int pageLayoutEvent)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
### fromName(String pageLayoutEventName) {#fromName-java.lang.String-}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
