---
title: LayoutOptions
second_title: Aspose.Words for Java API Reference
description: Holds the options that allow controlling the document layout process.
type: docs
weight: 364
url: /java/com.aspose.words/layoutoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class LayoutOptions implements Cloneable
```

Holds the options that allow controlling the document layout process.

To learn more, visit the [ Converting to Fixed-page Format ][Converting to Fixed-page Format] documentation article.

You do not create instances of this class directly. Use the [Document.getLayoutOptions()](../../com.aspose.words/document\#getLayoutOptions) property to access layout options for this document.

Note that after changing any of the options present in this class, [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout) method should be called in order for the changed options to be applied to the layout.


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getCallback()](#getCallback) | Gets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) implementation used by page layout model. |
| [getClass()](#getClass) |  |
| [getCommentDisplayMode()](#getCommentDisplayMode) | Gets the way comments are rendered. |
| [getContinuousSectionPageNumberingRestart()](#getContinuousSectionPageNumberingRestart) | Gets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [getIgnorePrinterMetrics()](#getIgnorePrinterMetrics) | Gets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. |
| [getRevisionOptions()](#getRevisionOptions) | Gets revision options. |
| [getShowHiddenText()](#getShowHiddenText) | Gets indication of whether hidden text in the document is rendered. |
| [getShowParagraphMarks()](#getShowParagraphMarks) | Gets indication of whether paragraph marks are rendered. |
| [getTextShaperFactory()](#getTextShaperFactory) | Gets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) implementation used for Advanced Typography rendering features. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setCallback(IPageLayoutCallback value)](#setCallback-com.aspose.words.IPageLayoutCallback) | Sets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) implementation used by page layout model. |
| [setCommentDisplayMode(int value)](#setCommentDisplayMode-int) | Sets the way comments are rendered. |
| [setContinuousSectionPageNumberingRestart(int value)](#setContinuousSectionPageNumberingRestart-int) | Sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [setIgnorePrinterMetrics(boolean value)](#setIgnorePrinterMetrics-boolean) | Sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. |
| [setShowHiddenText(boolean value)](#setShowHiddenText-boolean) | Sets indication of whether hidden text in the document is rendered. |
| [setShowParagraphMarks(boolean value)](#setShowParagraphMarks-boolean) | Sets indication of whether paragraph marks are rendered. |
| [setTextShaperFactory(ITextShaperFactory value)](#setTextShaperFactory-com.aspose.words.ITextShaperFactory) | Sets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) implementation used for Advanced Typography rendering features. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getCallback() {#getCallback}
```
public IPageLayoutCallback getCallback()
```


Gets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) implementation used by page layout model.

**Returns:**
[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) - \{[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) implementation used by page layout model.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCommentDisplayMode() {#getCommentDisplayMode}
```
public int getCommentDisplayMode()
```


Gets the way comments are rendered. Default value is [CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-BALLOONS). Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Returns:**
int - The way comments are rendered. The returned value is one of [CommentDisplayMode](../../com.aspose.words/commentdisplaymode) constants.
### getContinuousSectionPageNumberingRestart() {#getContinuousSectionPageNumberingRestart}
```
public int getContinuousSectionPageNumberingRestart()
```


Gets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. The default value is [ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart\#ALWAYS). It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced. Older page numbering logic demonstrated by MS Word 2016 is available via this option. Please [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) for the behavior description.

**Returns:**
int - The mode of behavior for computing page numbers when a continuous section restarts the page numbering. The returned value is one of [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) constants.
### getIgnorePrinterMetrics() {#getIgnorePrinterMetrics}
```
public boolean getIgnorePrinterMetrics()
```


Gets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is  true .

**Returns:**
boolean - Indication of whether the "Use printer metrics to lay out document" compatibility option is ignored.
### getRevisionOptions() {#getRevisionOptions}
```
public RevisionOptions getRevisionOptions()
```


Gets revision options.

**Returns:**
[RevisionOptions](../../com.aspose.words/revisionoptions) - Revision options.
### getShowHiddenText() {#getShowHiddenText}
```
public boolean getShowHiddenText()
```


Gets indication of whether hidden text in the document is rendered. Default is  false . This property affects all hidden content, not just text.

**Returns:**
boolean - Indication of whether hidden text in the document is rendered.
### getShowParagraphMarks() {#getShowParagraphMarks}
```
public boolean getShowParagraphMarks()
```


Gets indication of whether paragraph marks are rendered. Default is  false .

**Returns:**
boolean - Indication of whether paragraph marks are rendered.
### getTextShaperFactory() {#getTextShaperFactory}
```
public ITextShaperFactory getTextShaperFactory()
```


Gets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) implementation used for Advanced Typography rendering features.

**Returns:**
[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) - \{[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) implementation used for Advanced Typography rendering features.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setCallback(IPageLayoutCallback value) {#setCallback-com.aspose.words.IPageLayoutCallback}
```
public void setCallback(IPageLayoutCallback value)
```


Sets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) implementation used by page layout model.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) | \{[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) implementation used by page layout model. |

### setCommentDisplayMode(int value) {#setCommentDisplayMode-int}
```
public void setCommentDisplayMode(int value)
```


Sets the way comments are rendered. Default value is [CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-BALLOONS). Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The way comments are rendered. The value must be one of [CommentDisplayMode](../../com.aspose.words/commentdisplaymode) constants. |

### setContinuousSectionPageNumberingRestart(int value) {#setContinuousSectionPageNumberingRestart-int}
```
public void setContinuousSectionPageNumberingRestart(int value)
```


Sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. The default value is [ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart\#ALWAYS). It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced. Older page numbering logic demonstrated by MS Word 2016 is available via this option. Please [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) for the behavior description.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The mode of behavior for computing page numbers when a continuous section restarts the page numbering. The value must be one of [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) constants. |

### setIgnorePrinterMetrics(boolean value) {#setIgnorePrinterMetrics-boolean}
```
public void setIgnorePrinterMetrics(boolean value)
```


Sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. |

### setShowHiddenText(boolean value) {#setShowHiddenText-boolean}
```
public void setShowHiddenText(boolean value)
```


Sets indication of whether hidden text in the document is rendered. Default is  false . This property affects all hidden content, not just text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether hidden text in the document is rendered. |

### setShowParagraphMarks(boolean value) {#setShowParagraphMarks-boolean}
```
public void setShowParagraphMarks(boolean value)
```


Sets indication of whether paragraph marks are rendered. Default is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether paragraph marks are rendered. |

### setTextShaperFactory(ITextShaperFactory value) {#setTextShaperFactory-com.aspose.words.ITextShaperFactory}
```
public void setTextShaperFactory(ITextShaperFactory value)
```


Sets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) implementation used for Advanced Typography rendering features.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) | \{[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) implementation used for Advanced Typography rendering features. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

