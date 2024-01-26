---
title: PageLayoutEvent
linktitle: PageLayoutEvent
second_title: Aspose.Words for Java
description: A code of event raised during page layout model build and rendering in Java.
type: docs
weight: 464
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

 **Examples:** 

Shows how to track layout changes with a layout callback.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | Build of the page layout has finished. |
| [BUILD_STARTED](#BUILD-STARTED) | Build of the page layout has started. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | Conversion of document model to page layout has finished. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | Conversion of document model to page layout has started. |
| [NONE](#NONE) | Default value |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Reflow of the page has finished. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Reflow of the page has started. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Rendering of page has finished. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Rendering of page has started. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Reflow of the page layout has finished. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Reflow of the page layout has started. |
| [WATCH_DOG](#WATCH-DOG) | Corresponds to a checkpoint in code which is often visited and which is suitable to abort process. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


Build of the page layout has finished. Fired once. This is the last event which occurs when [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is called.

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


Build of the page layout has started. Fired once. This is the first event which occurs when [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is called.

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Conversion of document model to page layout has finished. Fired once. This occurs when layout model stops pulling document content.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Conversion of document model to page layout has started. Fired once. This occurs when layout model starts pulling document content.

### NONE {#NONE}
```
public static int NONE
```


Default value

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Reflow of the page has finished. Note that page may reflow multiple times and that reflow may restart before it is finished.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Reflow of the page has started. Note that page may reflow multiple times and that reflow may restart before it is finished.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Rendering of page has finished. This is fired once per page.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Rendering of page has started. This is fired once per page.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Reflow of the page layout has finished. Fired once. This occurs when layout model stops reflowing document content.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Reflow of the page layout has started. Fired once. This occurs when layout model starts reflowing document content.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Corresponds to a checkpoint in code which is often visited and which is suitable to abort process.

While inside [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) throw custom exception to abort process.

You can throw when handling any callback event to abort process.

Note that if process is aborted the page layout model remains in undefined state. If process is aborted upon reflow of a complete page, however, it should be possible to use layout model up to the end of that page.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageLayoutEvent) {#toString-int}
```
public static String toString(int pageLayoutEvent)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
