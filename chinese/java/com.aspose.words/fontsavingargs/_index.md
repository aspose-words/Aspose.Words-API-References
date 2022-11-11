---
title: FontSavingArgs
second_title: Aspose.Words for Java API Reference
description: 为事件提供数据。
type: docs
weight: 285
url: /zh/java/com.aspose.words/fontsavingargs/
---

**遗产:**
java.lang.Object
```
public class FontSavingArgs
```

提供数据为[IFontSavingCallback.fontSaving(com.aspose.words.FontSavingArgs)](../../com.aspose.words/ifontsavingcallback\#fontSaving-com.aspose.words.FontSavingArgs-)事件。

要了解更多信息，请访问**Save a Document**文档文章。

当 Aspose.Words 将文档保存为 HTML 或相关格式时[HtmlSaveOptions.getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [HtmlSaveOptions.setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)被设定为**true**，它将每个字体主题保存到一个单独的文件中以供导出。

[FontSavingArgs](../../com.aspose.words/fontsavingargs)控制是否应导出特定字体资源以及如何导出。

[FontSavingArgs](../../com.aspose.words/fontsavingargs)还允许重新定义如何生成字体文件名或通过提供您自己的流对象来完全避免将字体保存到文件中。

要决定是否保存特定字体资源，请使用[isExportNeeded()](../../com.aspose.words/fontsavingargs\#isExportNeeded--) / [isExportNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isExportNeeded-boolean-)财产。

要将字体保存到流而不是文件中，请使用**P:Aspose.Words.Saving.FontSavingArgs.FontStream**财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBold()](#getBold--) | 指示当前字体是否为粗体。 |
| [get班级()](#get班级--) |  |
| [getDocument()](#getDocument--) | 获取正在保存的文档对象。 |
| [getFontFamilyName()](#getFontFamilyName--) | 指示当前字体系列名称。 |
| [getFontFileName()](#getFontFileName--) | 获取将保存字体的文件名（无路径）。 |
| [getFontStream()](#getFontStream--) |  |
| [getItalic()](#getItalic--) | 指示当前字体是否为斜体。 |
| [getKeepFontStreamOpen()](#getKeepFontStreamOpen--) | 指定 Aspose.Words 应该在保存字体后保持流打开还是关闭它。 |
| [getOriginalFileName()](#getOriginalFileName--) | 获取带有扩展名的原始字体文件名。 |
| [getOriginalFileSize()](#getOriginalFileSize--) | 获取原始字体文件大小。 |
| [hashCode()](#hashCode--) |  |
| [isExportNeeded()](#isExportNeeded--) | 允许指定是否将当前字体导出为字体资源。 |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean-) | 允许指定是否将当前字体导出为字体资源。 |
| [isSubsettingNeeded()](#isSubsettingNeeded--) | 允许指定当前字体是否在导出为字体资源之前进行子集化。 |
| [isSubsettingNeeded(boolean value)](#isSubsettingNeeded-boolean-) | 允许指定当前字体是否在导出为字体资源之前进行子集化。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFontFileName(String value)](#setFontFileName-java.lang.String-) | 设置将保存字体的文件名（不带路径）。 |
| [setFontStream(OutputStream value)](#setFontStream-java.io.OutputStream-) |  |
| [setKeepFontStreamOpen(boolean value)](#setKeepFontStreamOpen-boolean-) | 指定 Aspose.Words 应该在保存字体后保持流打开还是关闭它。 |
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
### getBold() {#getBold--}
```
public boolean getBold()
```


指示当前字体是否为粗体。

**退货:**
boolean - 对应的布尔值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取正在保存的文档对象。

**退货:**
[Document](../../com.aspose.words/document) - 正在保存的文档对象。
### getFontFamilyName() {#getFontFamilyName--}
```
public String getFontFamilyName()
```


指示当前字体系列名称。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getFontFileName() {#getFontFileName--}
```
public String getFontFileName()
```


获取将保存字体的文件名（无路径）。

此属性允许您重新定义在导出到 HTML 期间如何生成字体文件名。

触发事件时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将字体保存到不同的文件中。请注意，文件名必须是唯一的。

当导出为 HTML 格式时，Aspose.Words 会自动为每个嵌入字体生成一个唯一的文件名。字体文件名的生成方式取决于您是将文档保存到文件还是流中。

将文档保存到文件时，生成的字体文件名如下所示*..*.

将文档保存到流中时，生成的字体文件名如下所示*Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs\#getFontFileName--) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs\#setFontFileName-java.lang.String-)必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径，[HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)和[HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)特性。

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**退货:**
java.lang.String - 字体将保存到的文件名（无路径）。
### getFontStream() {#getFontStream--}
```
public OutputStream getFontStream()
```




**退货:**
java.io.OutputStream
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


指示当前字体是否为斜体。

**退货:**
boolean - 对应的布尔值。
### getKeepFontStreamOpen() {#getKeepFontStreamOpen--}
```
public boolean getKeepFontStreamOpen()
```


指定 Aspose.Words 应该在保存字体后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.FontSavingArgs.FontStream**将字体写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**退货:**
boolean - 对应的布尔值。
### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


获取带有扩展名的原始字体文件名。

此属性包含当前字体的原始文件名（如果已知）。否则它可以是一个空字符串。

**退货:**
java.lang.String - 带有扩展名的原始字体文件名。
### getOriginalFileSize() {#getOriginalFileSize--}
```
public int getOriginalFileSize()
```


获取原始字体文件大小。

此属性包含当前字体的原始文件大小（如果已知）。否则它可以为零。

**退货:**
int - 原始字体文件大小。
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


允许指定是否将当前字体导出为字体资源。默认为 true 。

**退货:**
boolean - 对应的布尔值。
### isExportNeeded(boolean value) {#isExportNeeded-boolean-}
```
public void isExportNeeded(boolean value)
```


允许指定是否将当前字体导出为字体资源。默认为 true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### isSubsettingNeeded() {#isSubsettingNeeded--}
```
public boolean isSubsettingNeeded()
```


允许指定当前字体是否在导出为字体资源之前进行子集化。

字体可以导出为完整的原始字体文件或子集以仅包含文档中使用的字符。子集允许减少生成的字体资源大小。

默认情况下，Aspose.Words 通过比较原始字体文件的大小和在[HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-).您可以通过设置[isSubsettingNeeded()](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded--) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded-boolean-)财产。

**退货:**
boolean - 对应的布尔值。
### isSubsettingNeeded(boolean value) {#isSubsettingNeeded-boolean-}
```
public void isSubsettingNeeded(boolean value)
```


允许指定当前字体是否在导出为字体资源之前进行子集化。

字体可以导出为完整的原始字体文件或子集以仅包含文档中使用的字符。子集允许减少生成的字体资源大小。

默认情况下，Aspose.Words 通过比较原始字体文件的大小和在[HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-).您可以通过设置[isSubsettingNeeded()](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded--) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded-boolean-)财产。

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




### setFontFileName(String value) {#setFontFileName-java.lang.String-}
```
public void setFontFileName(String value)
```


设置将保存字体的文件名（不带路径）。

此属性允许您重新定义在导出到 HTML 期间如何生成字体文件名。

触发事件时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将字体保存到不同的文件中。请注意，文件名必须是唯一的。

当导出为 HTML 格式时，Aspose.Words 会自动为每个嵌入字体生成一个唯一的文件名。字体文件名的生成方式取决于您是将文档保存到文件还是流中。

将文档保存到文件时，生成的字体文件名如下所示*..*.

将文档保存到流中时，生成的字体文件名如下所示*Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs\#getFontFileName--) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs\#setFontFileName-java.lang.String-)必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径，[HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)和[HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)特性。

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字体将保存到的文件名（无路径）。 |

### setFontStream(OutputStream value) {#setFontStream-java.io.OutputStream-}
```
public void setFontStream(OutputStream value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepFontStreamOpen(boolean value) {#setKeepFontStreamOpen-boolean-}
```
public void setKeepFontStreamOpen(boolean value)
```


指定 Aspose.Words 应该在保存字体后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.FontSavingArgs.FontStream**将字体写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

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
