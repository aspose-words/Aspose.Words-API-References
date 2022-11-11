---
title: Watermark
second_title: Aspose.Words for Java API Reference
description: 表示使用文档水印的类。
type: docs
weight: 608
url: /zh/java/com.aspose.words/watermark/
---

**遗产:**
java.lang.Object
```
public class Watermark
```

表示使用文档水印的类。

要了解更多信息，请访问**Working with Watermark**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [get类型()](#get类型--) | 获取水印类型。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 去除水印。 |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage-) | 将图像水印添加到文档中。 |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions-) | 将图像水印添加到文档中。 |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions-) | 将图像水印添加到文档中。 |
| [setText(String text)](#setText-java.lang.String-) | 将文本水印添加到文档中。 |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions-) | 将文本水印添加到文档中。 |
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
### get类型() {#get类型--}
```
public int get类型()
```


获取水印类型。

**退货:**
 int - 水印类型。返回值是以下之一[Watermark类型](../../com.aspose.words/watermarktype)常数。
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




### remove() {#remove--}
```
public void remove()
```


去除水印。

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage image)
```


将图像水印添加到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | 显示为水印的图像。 |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions-}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


将图像水印添加到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | 显示为水印的图像。 |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions) | 定义图像水印的附加选项。 |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions-}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


将图像水印添加到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imagePath | java.lang.String | 显示为水印的图像文件的路径。 |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions) | 定义图像水印的附加选项。 |

### setText(String text) {#setText-java.lang.String-}
```
public void setText(String text)
```


将文本水印添加到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | java.lang.String | 显示为水印的文本。文本长度必须在 1 到 200 的范围内。文本不能为空或仅包含空格。 |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions-}
```
public void setText(String text, TextWatermarkOptions options)
```


将文本水印添加到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | java.lang.String | 显示为水印的文本。 |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions) | 定义文本水印的附加选项。文本长度必须在 1 到 200 的范围内。文本不能为空或仅包含空格。 |

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
