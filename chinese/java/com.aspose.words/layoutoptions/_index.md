---
title: LayoutOptions
second_title: Aspose.Words for Java API 参考
description: 包含允许控制文档布局过程的选项。
type: docs
weight: 362
url: /zh/java/com.aspose.words/layoutoptions/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class LayoutOptions implements Cloneable
```

包含允许控制文档布局过程的选项。

要了解更多信息，请访问**Converting to Fixed-page Format**文档文章。

您不直接创建此类的实例。使用[Document.getLayoutOptions()](../../com.aspose.words/document\#getLayoutOptions--)属性以访问此文档的布局选项。

请注意，在更改此类中存在的任何选项后，[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)应该调用方法以便将更改的选项应用于布局。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCallback()](#getCallback--) | 获取[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback)页面布局模型使用的实现。 |
| [getClass()](#getClass--) |  |
| [getCommentDisplayMode()](#getCommentDisplayMode--) | 获取评论的呈现方式。 |
| [getContinuousSectionPageNumberingRestart()](#getContinuousSectionPageNumberingRestart--) | 获取连续部分重新开始页码编号时计算页码的行为模式。 |
| [getIgnorePrinterMetrics()](#getIgnorePrinterMetrics--) | 获取是否忽略“使用打印机指标布局文档”兼容性选项的指示。 |
| [getRevisionOptions()](#getRevisionOptions--) | 获取修订选项。 |
| [getShowHiddenText()](#getShowHiddenText--) | 获取是否呈现文档中隐藏文本的指示。 |
| [getShowParagraphMarks()](#getShowParagraphMarks--) | 获取是否呈现段落标记的指示。 |
| [getTextShaperFactory()](#getTextShaperFactory--) | 获取[ITextShaperFactory](../../com.aspose.words/itextshaperfactory)用于高级排版渲染功能的实现。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCallback(IPageLayoutCallback value)](#setCallback-com.aspose.words.IPageLayoutCallback-) | 套[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback)页面布局模型使用的实现。 |
| [setCommentDisplayMode(int value)](#setCommentDisplayMode-int-) | 设置评论的呈现方式。 |
| [setContinuousSectionPageNumberingRestart(int value)](#setContinuousSectionPageNumberingRestart-int-) | 设置当连续部分重新开始页码时计算页码的行为模式。 |
| [setIgnorePrinterMetrics(boolean value)](#setIgnorePrinterMetrics-boolean-) | 设置是否忽略“使用打印机指标布局文档”兼容性选项的指示。 |
| [setShowHiddenText(boolean value)](#setShowHiddenText-boolean-) | 设置是否呈现文档中的隐藏文本的指示。 |
| [setShowParagraphMarks(boolean value)](#setShowParagraphMarks-boolean-) | 设置是否呈现段落标记的指示。 |
| [setTextShaperFactory(ITextShaperFactory value)](#setTextShaperFactory-com.aspose.words.ITextShaperFactory-) | 套[ITextShaperFactory](../../com.aspose.words/itextshaperfactory)用于高级排版渲染功能的实现。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getCallback() {#getCallback--}
```
public IPageLayoutCallback getCallback()
```


获取[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback)页面布局模型使用的实现。

**退货:**
[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) -\{[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback)页面布局模型使用的实现。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getCommentDisplayMode() {#getCommentDisplayMode--}
```
public int getCommentDisplayMode()
```


获取评论的呈现方式。默认值为[CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-BALLOONS).请注意，修订不会在气球中呈现[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**退货:**
int - 评论的呈现方式。返回值是以下之一[CommentDisplayMode](../../com.aspose.words/commentdisplaymode)常数。
### getContinuousSectionPageNumberingRestart() {#getContinuousSectionPageNumberingRestart--}
```
public int getContinuousSectionPageNumberingRestart()
```


获取当连续部分重新开始页码编号时计算页码的行为模式。默认值为[ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart\#ALWAYS).它与 MS Word 2019 的行为相匹配，MS Word 2019 是引入该选项时的最新版本。通过此选项可以使用 MS Word 2016 演示的旧页码逻辑。请[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart)对于行为描述。

**退货:**
 int - 当连续部分重新开始页码时计算页码的行为模式。返回值是以下之一[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart)常数。
### getIgnorePrinterMetrics() {#getIgnorePrinterMetrics--}
```
public boolean getIgnorePrinterMetrics()
```


获取是否忽略“使用打印机指标来布置文档”兼容性选项的指示。默认为真。

**退货:**
布尔值 - 指示是否忽略“使用打印机指标来布置文档”兼容性选项。
### getRevisionOptions() {#getRevisionOptions--}
```
public RevisionOptions getRevisionOptions()
```


获取修订选项。

**退货:**
[RevisionOptions](../../com.aspose.words/revisionoptions) - 修订选项。
### getShowHiddenText() {#getShowHiddenText--}
```
public boolean getShowHiddenText()
```


获取是否呈现文档中的隐藏文本的指示。默认为假。此属性影响所有隐藏的内容，而不仅仅是文本。

**退货:**
boolean - 指示是否呈现文档中的隐藏文本。
### getShowParagraphMarks() {#getShowParagraphMarks--}
```
public boolean getShowParagraphMarks()
```


获取是否呈现段落标记的指示。默认为假。

**退货:**
boolean - 指示是否呈现段落标记。
### getTextShaperFactory() {#getTextShaperFactory--}
```
public ITextShaperFactory getTextShaperFactory()
```


获取[ITextShaperFactory](../../com.aspose.words/itextshaperfactory)用于高级排版渲染功能的实现。

**退货:**
[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) -\{[ITextShaperFactory](../../com.aspose.words/itextshaperfactory)用于高级排版渲染功能的实现。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCallback(IPageLayoutCallback value) {#setCallback-com.aspose.words.IPageLayoutCallback-}
```
public void setCallback(IPageLayoutCallback value)
```


套[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback)页面布局模型使用的实现。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) | \{[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback)页面布局模型使用的实现。 |

### setCommentDisplayMode(int value) {#setCommentDisplayMode-int-}
```
public void setCommentDisplayMode(int value)
```


设置评论的呈现方式。默认值为[CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-BALLOONS).请注意，修订不会在气球中呈现[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 评论的呈现方式。该值必须是其中之一[CommentDisplayMode](../../com.aspose.words/commentdisplaymode)常数。 |

### setContinuousSectionPageNumberingRestart(int value) {#setContinuousSectionPageNumberingRestart-int-}
```
public void setContinuousSectionPageNumberingRestart(int value)
```


设置当连续部分重新开始页码时计算页码的行为模式。默认值为[ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart\#ALWAYS).它与 MS Word 2019 的行为相匹配，MS Word 2019 是引入该选项时的最新版本。通过此选项可以使用 MS Word 2016 演示的旧页码逻辑。请[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart)对于行为描述。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 当连续部分重新开始页码时计算页码的行为模式。该值必须是其中之一[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart)常数。 |

### setIgnorePrinterMetrics(boolean value) {#setIgnorePrinterMetrics-boolean-}
```
public void setIgnorePrinterMetrics(boolean value)
```


设置是否忽略“使用打印机指标布局文档”兼容性选项的指示。默认为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否忽略“使用打印机度量来布置文档”兼容性选项的指示。 |

### setShowHiddenText(boolean value) {#setShowHiddenText-boolean-}
```
public void setShowHiddenText(boolean value)
```


设置是否呈现文档中的隐藏文本的指示。默认为假。此属性影响所有隐藏内容，而不仅仅是文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否呈现文档中的隐藏文本。 |

### setShowParagraphMarks(boolean value) {#setShowParagraphMarks-boolean-}
```
public void setShowParagraphMarks(boolean value)
```


设置是否呈现段落标记的指示。默认为假。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否呈现段落标记。 |

### setTextShaperFactory(ITextShaperFactory value) {#setTextShaperFactory-com.aspose.words.ITextShaperFactory-}
```
public void setTextShaperFactory(ITextShaperFactory value)
```


套[ITextShaperFactory](../../com.aspose.words/itextshaperfactory)用于高级排版渲染功能的实现。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) | \{[ITextShaperFactory](../../com.aspose.words/itextshaperfactory)用于高级排版渲染功能的实现。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
