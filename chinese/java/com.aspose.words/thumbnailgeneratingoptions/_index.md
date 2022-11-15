---
title: ThumbnailGeneratingOptions
second_title: Aspose.Words for Java API 参考
description: 可用于在为文档生成缩略图时指定其他选项。
type: docs
weight: 578
url: /zh/java/com.aspose.words/thumbnailgeneratingoptions/
---

**遗产:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

可用于在为文档生成缩略图时指定其他选项。用户可以调用方法[Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-)生成[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---)为一份文件。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage--) | 指定是从文档的第一页还是从第一张图像生成缩略图。 |
| [getThumbnailSize()](#getThumbnailSize--) | 生成的缩略图的大小（以像素为单位）。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean-) | 指定是从文档的第一页还是从第一张图像生成缩略图。 |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension-) | 生成的缩略图的大小（以像素为单位）。 |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getGenerateFromFirstPage() {#getGenerateFromFirstPage--}
```
public boolean getGenerateFromFirstPage()
```


指定是从文档的第一页还是从第一张图像生成缩略图。默认为 true ，这意味着缩略图将从文档的第一页生成。如果值为 false 并且文档中没有图像，则将从文档的第一页生成缩略图。

**退货:**
boolean - 对应的布尔值。
### getThumbnailSize() {#getThumbnailSize--}
```
public Dimension getThumbnailSize()
```


生成的缩略图的大小（以像素为单位）。默认为 600x900。

**退货:**
java.awt.Dimension - 相应的 java.awt.Dimension 值。
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




### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean-}
```
public void setGenerateFromFirstPage(boolean value)
```


指定是从文档的第一页还是从第一张图像生成缩略图。默认为 true ，这意味着缩略图将从文档的第一页生成。如果值为 false 并且文档中没有图像，则将从文档的第一页生成缩略图。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension-}
```
public void setThumbnailSize(Dimension value)
```


生成的缩略图的大小（以像素为单位）。默认为 600x900。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Dimension | 对应的java.awt.Dimension值。 |

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
