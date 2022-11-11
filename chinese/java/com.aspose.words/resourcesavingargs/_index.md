---
title: ResourceSavingArgs
second_title: Aspose.Words for Java API 参考
description:为事件提供数据。
type: docs
weight: 481
url: /zh/java/com.aspose.words/resourcesavingargs/
---

**遗产:**
java.lang.Object
```
public class ResourceSavingArgs
```

提供数据为[IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback\#resourceSaving-com.aspose.words.ResourceSavingArgs-)事件。

要了解更多信息，请访问**Save a Document**文档文章。

默认情况下，当 Aspose.Words 将文档保存到固定页面 HTML 或 SVG 时，它会将每个资源保存到单独的文件中。 Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个资源生成唯一文件名。

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs)允许重新定义资源文件名的生成方式或通过提供您自己的流对象来完全避免将资源保存到文件中。

要应用您自己的逻辑来生成资源文件名，请使用[getResourceFileName()](../../com.aspose.words/resourcesavingargs\#getResourceFileName--) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs\#setResourceFileName-java.lang.String-)财产。

要将资源保存到流而不是文件中，请使用**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**财产。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDocument()](#getDocument--) | 获取当前正在保存的文档对象。 |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen--) | 指定 Aspose.Words 应该在保存资源后保持流打开还是关闭它。 |
| [getResourceFileName()](#getResourceFileName--) | 获取资源将保存到的文件名（不带路径）。 |
| [getResourceFileUri()](#getResourceFileUri--) | 获取用于从文档中引用资源文件的统一资源标识符 (URI)。 |
| [getResourceStream()](#getResourceStream--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean-) | 指定 Aspose.Words 应该在保存资源后保持流打开还是关闭它。 |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String-) | 设置将保存资源的文件名（不带路径）。 |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String-) | 设置用于从文档中引用资源文件的统一资源标识符 (URI)。 |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream-) |  |
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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取当前正在保存的文档对象。

**退货:**
[Document](../../com.aspose.words/document) - 当前正在保存的文档对象。
### getKeepResourceStreamOpen() {#getKeepResourceStreamOpen--}
```
public boolean getKeepResourceStreamOpen()
```


指定 Aspose.Words 应该在保存资源后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**将资源写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**退货:**
boolean - 对应的布尔值。
### getResourceFileName() {#getResourceFileName--}
```
public String getResourceFileName()
```


获取资源将保存到的文件名（不带路径）。

此属性允许您重新定义在导出到固定页面 HTML 或 SVG 期间如何生成资源文件名。

触发事件时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将资源保存到不同的文件中。请注意，文件名必须是唯一的。

当导出为固定页面 HTML 或 SVG 格式时，Aspose.Words 会自动为每个资源生成一个唯一的文件名。资源文件名的生成方式取决于您是将文档保存到文件还是流中。

将文档保存到文件时，生成的资源文件名如下所示*.![Image 1][].*.

将文档保存到流时，生成的资源文件名如下所示*Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs\#getResourceFileName--) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs\#setResourceFileName-java.lang.String-)必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径和 src 属性的值，用于写入固定页面 HTML 或 SVG，[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)或者[SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-)和[HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-)或者[SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)特性。

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)


[图1]： 

**退货:**
java.lang.String - 将保存资源的文件名（无路径）。
### getResourceFileUri() {#getResourceFileUri--}
```
public String getResourceFileUri()
```


获取用于从文档中引用资源文件的统一资源标识符 (URI)。

此属性允许您更改导出到固定页面 HTML 或 SVG 文档的资源文件的 URI。

在导出到固定页面 HTML 或 SVG 格式期间，Aspose.Words 会自动为每个资源文件生成一个 URI。生成的 URI 引用 Aspose.Words 保存的资源文件。但是，如果要将资源文件移动到其他位置或将资源文件保存到流中，则 URI 可能不正确。此属性允许在这些情况下更正 URI。

触发事件时，此属性包含由 Aspose.Words 生成的 URI。您可以更改此属性的值以提供资源文件的自定义 URI。

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)

**退货:**
java.lang.String - 用于从文档中引用资源文件的统一资源标识符 (URI)。
### getResourceStream() {#getResourceStream--}
```
public OutputStream getResourceStream()
```




**退货:**
java.io.OutputStream
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




### setKeepResourceStreamOpen(boolean value) {#setKeepResourceStreamOpen-boolean-}
```
public void setKeepResourceStreamOpen(boolean value)
```


指定 Aspose.Words 应该在保存资源后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**将资源写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String-}
```
public void setResourceFileName(String value)
```


设置将保存资源的文件名（不带路径）。

此属性允许您重新定义在导出到固定页面 HTML 或 SVG 期间如何生成资源文件名。

触发事件时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将资源保存到不同的文件中。请注意，文件名必须是唯一的。

当导出为固定页面 HTML 或 SVG 格式时，Aspose.Words 会自动为每个资源生成一个唯一的文件名。资源文件名的生成方式取决于您是将文档保存到文件还是流中。

将文档保存到文件时，生成的资源文件名如下所示*.![Image 1][].*.

将文档保存到流时，生成的资源文件名如下所示*Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs\#getResourceFileName--) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs\#setResourceFileName-java.lang.String-)必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径和 src 属性的值，用于写入固定页面 HTML 或 SVG，[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)或者[SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-)和[HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-)或者[SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)特性。

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)


[图1]： 

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 将保存资源的文件名（不带路径）。 |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String-}
```
public void setResourceFileUri(String value)
```


设置用于从文档中引用资源文件的统一资源标识符 (URI)。

此属性允许您更改导出到固定页面 HTML 或 SVG 文档的资源文件的 URI。

在导出到固定页面 HTML 或 SVG 格式期间，Aspose.Words 会自动为每个资源文件生成一个 URI。生成的 URI 引用 Aspose.Words 保存的资源文件。但是，如果要将资源文件移动到其他位置或将资源文件保存到流中，则 URI 可能不正确。此属性允许在这些情况下更正 URI。

触发事件时，此属性包含由 Aspose.Words 生成的 URI。您可以更改此属性的值以提供资源文件的自定义 URI。

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于从文档中引用资源文件的统一资源标识符 (URI)。 |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream-}
```
public void setResourceStream(OutputStream value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.OutputStream |  |

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
