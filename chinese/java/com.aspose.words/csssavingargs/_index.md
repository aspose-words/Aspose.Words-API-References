---
title: CssSavingArgs
second_title: Aspose.Words for Java API Reference
description: 为事件提供数据。
type: docs
weight: 96
url: /zh/java/com.aspose.words/csssavingargs/
---

**遗产:**
java.lang.Object
```
public class CssSavingArgs
```

提供数据为[ICssSavingCallback.cssSaving(com.aspose.words.CssSavingArgs)](../../com.aspose.words/icsssavingcallback\#cssSaving-com.aspose.words.CssSavingArgs-)事件。

要了解更多信息，请访问**Save a Document**文档文章。

默认情况下，当 Aspose.Words 将文档保存为 HTML 时，它会内联保存 CSS 信息（作为**style**每个元素的属性）。

[CssSavingArgs](../../com.aspose.words/csssavingargs)允许通过提供您自己的流对象将 CSS 信息保存到文件中。

要将 CSS 保存到流中，请使用**P:Aspose.Words.Saving.CssSavingArgs.CssStream**财产。

要禁止将 CSS 保存到文件中并嵌入到 HTML 文档中，请使用[isExportNeeded()](../../com.aspose.words/csssavingargs\#isExportNeeded--) / [isExportNeeded(boolean)](../../com.aspose.words/csssavingargs\#isExportNeeded-boolean-)财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getCssStream()](#getCssStream--) |  |
| [getDocument()](#getDocument--) | 获取当前正在保存的文档对象。 |
| [getKeepCssStreamOpen()](#getKeepCssStreamOpen--) | 指定 Aspose.Words 应该在保存 CSS 信息后保持流打开还是关闭它。 |
| [hashCode()](#hashCode--) |  |
| [isExportNeeded()](#isExportNeeded--) | 允许指定是否将 CSS 导出到文件并嵌入到 HTML 文档中。 |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean-) | 允许指定是否将 CSS 导出到文件并嵌入到 HTML 文档中。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCssStream(OutputStream value)](#setCssStream-java.io.OutputStream-) |  |
| [setKeepCssStreamOpen(boolean value)](#setKeepCssStreamOpen-boolean-) | 指定 Aspose.Words 应该在保存 CSS 信息后保持流打开还是关闭它。 |
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCssStream() {#getCssStream--}
```
public OutputStream getCssStream()
```




**退货:**
java.io.OutputStream
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取当前正在保存的文档对象。

**退货:**
[Document](../../com.aspose.words/document) - 当前正在保存的文档对象。
### getKeepCssStreamOpen() {#getKeepCssStreamOpen--}
```
public boolean getKeepCssStreamOpen()
```


指定 Aspose.Words 应该在保存 CSS 信息后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.CssSavingArgs.CssStream**将 CSS 信息写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isExportNeeded() {#isExportNeeded--}
```
public boolean isExportNeeded()
```


允许指定是否将 CSS 导出到文件并嵌入到 HTML 文档中。默认为 true 。当此属性为 false 时，CSS 信息不会保存到 CSS 文件中，也不会嵌入到 HTML 文档中。

**退货:**
boolean - 对应的布尔值。
### isExportNeeded(boolean value) {#isExportNeeded-boolean-}
```
public void isExportNeeded(boolean value)
```


允许指定是否将 CSS 导出到文件并嵌入到 HTML 文档中。默认为 true 。当此属性为 false 时，CSS 信息不会保存到 CSS 文件中，也不会嵌入到 HTML 文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCssStream(OutputStream value) {#setCssStream-java.io.OutputStream-}
```
public void setCssStream(OutputStream value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepCssStreamOpen(boolean value) {#setKeepCssStreamOpen-boolean-}
```
public void setKeepCssStreamOpen(boolean value)
```


指定 Aspose.Words 应该在保存 CSS 信息后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.CssSavingArgs.CssStream**将 CSS 信息写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
