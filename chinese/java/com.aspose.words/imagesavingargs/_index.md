---
title: ImageSavingArgs
second_title: Aspose.Words for Java API Reference
description: 为事件提供数据。
type: docs
weight: 341
url: /zh/java/com.aspose.words/imagesavingargs/
---

**遗产:**
java.lang.Object
```
public class ImageSavingArgs
```

提供数据为[IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback\#imageSaving-com.aspose.words.ImageSavingArgs-)事件。

要了解更多信息，请访问**Save a Document**文档文章。

默认情况下，当 Aspose.Words 将文档保存为 HTML 时，它会将每个图像保存到单独的文件中。 Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个图像生成唯一文件名。

[ImageSavingArgs](../../com.aspose.words/imagesavingargs)允许重新定义图像文件名的生成方式或通过提供您自己的流对象来完全避免将图像保存到文件中。

要应用您自己的逻辑来生成图像文件名，请使用[getImageFileName()](../../com.aspose.words/imagesavingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs\#setImageFileName-java.lang.String-), [getCurrentShape()](../../com.aspose.words/imagesavingargs\#getCurrentShape--)和[isImageAvailable()](../../com.aspose.words/imagesavingargs\#isImageAvailable--)特性。

要将图像保存到流而不是文件中，请使用**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getCurrentShape()](#getCurrentShape--) | 获取[ShapeBase](../../com.aspose.words/shapebase)与即将保存的形状或组形状相对应的对象。 |
| [getDocument()](#getDocument--) | 获取当前正在保存的文档对象。 |
| [getImageFileName()](#getImageFileName--) | 获取图像将保存到的文件名（不带路径）。 |
| [getImageStream()](#getImageStream--) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen--) | 指定 Aspose.Words 应该在保存图像后保持流打开还是关闭它。 |
| [hashCode()](#hashCode--) |  |
| [isImageAvailable()](#isImageAvailable--) | 如果当前图像可用于导出，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setImageFileName(String value)](#setImageFileName-java.lang.String-) | 设置保存图像的文件名（不带路径）。 |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream-) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean-) | 指定 Aspose.Words 应该在保存图像后保持流打开还是关闭它。 |
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
### getCurrentShape() {#getCurrentShape--}
```
public ShapeBase getCurrentShape()
```


获取[ShapeBase](../../com.aspose.words/shapebase)与即将保存的形状或组形状相对应的对象。

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback)可以在保存形状或组形状时触发。这就是为什么该物业有[ShapeBase](../../com.aspose.words/shapebase)类型。您可以检查它是否是一个组形状比较[ShapeBase.getShape类型()](../../com.aspose.words/shapebase\#getShape类型--)和[Shape类型.GROUP](../../com.aspose.words/shapetype\#GROUP)或通过将其转换为派生类之一：[Shape](../../com.aspose.words/shape)或者[GroupShape](../../com.aspose.words/groupshape).

 Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个图像生成唯一文件名。您可以使用[getCurrentShape()](../../com.aspose.words/imagesavingargs\#getCurrentShape--)属性通过检查形状属性来生成“更好”的文件名，例如[ImageData.getTitle()](../../com.aspose.words/imagedata\#getTitle--) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata\#setTitle-java.lang.String-)（仅形状），[ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) （仅限形状）和[ShapeBase.getName()](../../com.aspose.words/shapebase\#getName--) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase\#setName-java.lang.String-).当然，您可以使用任何其他属性或条件来构建文件名，但请注意辅助文件名在导出操作中必须是唯一的。

文档中的某些图像可能不可用。要检查图像可用性，请使用[isImageAvailable()](../../com.aspose.words/imagesavingargs\#isImageAvailable--)财产。

**退货:**
[ShapeBase](../../com.aspose.words/shapebase) - 这[ShapeBase](../../com.aspose.words/shapebase)与即将保存的形状或组形状相对应的对象。
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取当前正在保存的文档对象。

**退货:**
[Document](../../com.aspose.words/document) - 当前正在保存的文档对象。
### getImageFileName() {#getImageFileName--}
```
public String getImageFileName()
```


获取图像将保存到的文件名（不带路径）。

此属性允许您重新定义在导出到 HTML 期间如何生成图像文件名。

触发事件时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将图像保存到不同的文件中。请注意，文件名必须是唯一的。

当导出为 HTML 格式时，Aspose.Words 会自动为每个嵌入的图像生成一个唯一的文件名。图像文件名的生成方式取决于您是将文档保存到文件还是流中。

将文档保存到文件时，生成的图像文件名如下所示*.![Image 1][].*.

将文档保存到流时，生成的图像文件名如下所示*Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs\#setImageFileName-java.lang.String-)必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径和写入 HTML 的 src 属性的值，[HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)和[HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)特性。


[图1]： 

**退货:**
java.lang.String - 图像将保存到的文件名（无路径）。
### getImageStream() {#getImageStream--}
```
public OutputStream getImageStream()
```




**退货:**
java.io.OutputStream
### getKeepImageStreamOpen() {#getKeepImageStreamOpen--}
```
public boolean getKeepImageStreamOpen()
```


指定 Aspose.Words 应该在保存图像后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**将图像写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isImageAvailable() {#isImageAvailable--}
```
public boolean isImageAvailable()
```


如果当前图像可用于导出，则返回 true。

文档中的某些图像可能不可用，例如，因为图像已链接并且链接不可访问或未指向有效图像。在这种情况下，Aspose.Words 导出一个带有红十字的图标。如果原始图像可用，则此属性返回 true；如果原始图像不可用，则返回 false 并且将提供“无图像”图标以供保存。

保存组形状或不需要任何图像的形状时，此属性始终为 true 。

**退货:**
布尔值 -\{ 如果当前图像可用于导出，则为 true。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setImageFileName(String value) {#setImageFileName-java.lang.String-}
```
public void setImageFileName(String value)
```


设置保存图像的文件名（不带路径）。

此属性允许您重新定义在导出到 HTML 期间如何生成图像文件名。

触发事件时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值以将图像保存到不同的文件中。请注意，文件名必须是唯一的。

当导出为 HTML 格式时，Aspose.Words 会自动为每个嵌入的图像生成一个唯一的文件名。图像文件名的生成方式取决于您是将文档保存到文件还是流中。

将文档保存到文件时，生成的图像文件名如下所示*.![Image 1][].*.

将文档保存到流时，生成的图像文件名如下所示*Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs\#setImageFileName-java.lang.String-)必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径和写入 HTML 的 src 属性的值，[HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)和[HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)特性。


[图1]： 

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 图像将保存到的文件名（无路径）。 |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream-}
```
public void setImageStream(OutputStream value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean-}
```
public void setKeepImageStreamOpen(boolean value)
```


指定 Aspose.Words 应该在保存图像后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**将图像写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

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
