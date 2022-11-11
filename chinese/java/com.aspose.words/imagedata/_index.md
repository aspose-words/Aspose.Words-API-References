---
title: ImageData
second_title: Aspose.Words for Java API 参考
description:定义形状的图像。
type: docs
weight: 337
url: /zh/java/com.aspose.words/imagedata/
---

**遗产:**
java.lang.Object
```
public class ImageData
```

定义形状的图像。

要了解更多信息，请访问**Working with Images**文档文章。

使用[Shape.getImageData()](../../com.aspose.words/shape\#getImageData--)属性来访问和修改形状内的图像。您不创建的实例[ImageData](../../com.aspose.words/imagedata)直接上课。

图像可以存储在形状内，链接到外部文件或两者（链接并存储在文档中）。

无论图像是存储在形状内还是链接在一起，您始终可以使用[toByteArray()](../../com.aspose.words/imagedata\#toByteArray--), [toImage()](../../com.aspose.words/imagedata\#toImage--)或者[save(java.lang.String)](../../com.aspose.words/imagedata\#save-java.lang.String-)方法。如果图像存储在形状内，您也可以使用[getImageBytes()](../../com.aspose.words/imagedata\#getImageBytes--) / [setImageBytes(byte[])](../../com.aspose.words/imagedata\#setImageBytes-byte---)财产。

要将图像存储在形状中，请使用[setImage(java.lang.String)](../../com.aspose.words/imagedata\#setImage-java.lang.String-)方法。要将图像链接到形状，请将[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)财产。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getBiLevel()](#getBiLevel--) | 确定图像是否以黑白显示。 |
| [getBorders()](#getBorders--) | 获取图像边框的集合。 |
| [getBrightness()](#getBrightness--) | 获取图片的亮度。 |
| [getChromaKey()](#getChromaKey--) | 定义将被视为透明的图像的颜色值。 |
| [get班级()](#get班级--) |  |
| [getContrast()](#getContrast--) | 获取指定图片的对比度。 |
| [getCropBottom()](#getCropBottom--) | 定义从底部移除图片的比例。 |
| [getCropLeft()](#getCropLeft--) | 定义从左侧删除图片的比例。 |
| [getCropRight()](#getCropRight--) | 定义从右侧移除图片的比例。 |
| [getCropTop()](#getCropTop--) | 定义从顶部移除图片的比例。 |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getGrayScale()](#getGrayScale--) | 确定图片是否以灰度模式显示。 |
| [getImageBytes()](#getImageBytes--) | 获取存储在形状中的图像的原始字节。 |
| [getImageSize()](#getImageSize--) | 获取有关图像大小和分辨率的信息。 |
| [getImage类型()](#getImage类型--) | 获取图像的类型。 |
| [getSourceFullName()](#getSourceFullName--) | 获取链接图像的源文件的路径和名称。 |
| [getTitle()](#getTitle--) | 定义图像的标题。 |
| [hasImage()](#hasImage--) | 如果形状具有图像字节或链接图像，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [isLink()](#isLink--) | 如果图像链接到形状，则返回 true（当[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)已指定）。 |
| [isLinkOnly()](#isLinkOnly--) | 如果图像已链接且未存储在文档中，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream stream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | 将图像保存到文件中。 |
| [setBiLevel(boolean value)](#setBiLevel-boolean-) | 确定图像是否以黑白显示。 |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBrightness(double value)](#setBrightness-double-) | 设置图像的亮度。 |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color-) | 定义将被视为透明的图像的颜色值。 |
| [setContrast(double value)](#setContrast-double-) | 设置指定图片的对比度。 |
| [setCropBottom(double value)](#setCropBottom-double-) | 定义从底部移除图片的比例。 |
| [setCropLeft(double value)](#setCropLeft-double-) | 定义从左侧删除图片的比例。 |
| [setCropRight(double value)](#setCropRight-double-) | 定义从右侧移除图片的比例。 |
| [setCropTop(double value)](#setCropTop-double-) | 定义从顶部移除图片的比例。 |
| [setGrayScale(boolean value)](#setGrayScale-boolean-) | 确定图片是否以灰度模式显示。 |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage-) | 设置形状显示的图像。 |
| [setImage(InputStream stream)](#setImage-java.io.InputStream-) |  |
| [setImage(String fileName)](#setImage-java.lang.String-) | 设置形状显示的图像。 |
| [setImageBytes(byte[] value)](#setImageBytes-byte---) | 设置存储在形状中的图像的原始字节。 |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | 设置链接图像的源文件的路径和名称。 |
| [setTitle(String value)](#setTitle-java.lang.String-) | 定义图像的标题。 |
| [toByteArray()](#toByteArray--) | 返回任何图像的图像字节，无论图像是存储还是链接。 |
| [toImage()](#toImage--) | 获取作为 java BufferedImage 对象存储在形状中的图像。 |
| [toStream()](#toStream--) | 创建并返回包含图像字节的流。 |
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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getBiLevel() {#getBiLevel--}
```
public boolean getBiLevel()
```


确定图像是否以黑白显示。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取图像边框的集合。边框仅对内联图像有效。

**退货:**
[BorderCollection](../../com.aspose.words/bordercollection) - 图像边框的集合。
### getBrightness() {#getBrightness--}
```
public double getBrightness()
```


获取图片的亮度。此属性的值必须是从 0.0（最暗）到 1.0（最亮）的数字。

默认值为 0.5。

**退货:**
double - 图片的亮度。
### getChromaKey() {#getChromaKey--}
```
public Color getChromaKey()
```


定义将被视为透明的图像的颜色值。

默认值为 0。

**退货:**
java.awt.Color - 对应的 java.awt.Color 值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getContrast() {#getContrast--}
```
public double getContrast()
```


获取指定图片的对比度。此属性的值必须是从 0.0（最小对比度）到 1.0（最大对比度）的数字。

默认值为 0.5。

**退货:**
double - 指定图片的对比度。
### getCropBottom() {#getCropBottom--}
```
public double getCropBottom()
```


定义从底部移除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**退货:**
double - 对应的双精度值。
### getCropLeft() {#getCropLeft--}
```
public double getCropLeft()
```


定义从左侧删除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**退货:**
double - 对应的双精度值。
### getCropRight() {#getCropRight--}
```
public double getCropRight()
```


定义从右侧移除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**退货:**
double - 对应的双精度值。
### getCropTop() {#getCropTop--}
```
public double getCropTop()
```


定义从顶部移除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**退货:**
double - 对应的双精度值。
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getGrayScale() {#getGrayScale--}
```
public boolean getGrayScale()
```


确定图片是否以灰度模式显示。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getImageBytes() {#getImageBytes--}
```
public byte[] getImageBytes()
```


获取存储在形状中的图像的原始字节。

将值设置为 null 或空数组将从形状中删除图像。

如果图像未存储在文档中，则返回 null（例如，在这种情况下，图像可能是链接的）。

**退货:**
字节[] - 存储在形状中的图像的原始字节。
### getImageSize() {#getImageSize--}
```
public ImageSize getImageSize()
```


获取有关图像大小和分辨率的信息。 (4661,6)

如果图像仅链接而不存储在文档中，则返回零大小。

**退货:**
[ImageSize](../../com.aspose.words/imagesize) - 有关图像大小和分辨率的信息。
### getImage类型() {#getImage类型--}
```
public int getImage类型()
```


获取图像的类型。 (4671,6)

**退货:**
 int - 图像的类型。返回值是以下之一[Image类型](../../com.aspose.words/imagetype)常数。
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


获取链接图像的源文件的路径和名称。

默认值为空字符串。

如果[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)不是空字符串，图像是链接的。

**退货:**
java.lang.String - 链接图像的源文件的路径和名称。
### getTitle() {#getTitle--}
```
public String getTitle()
```


定义图像的标题。

默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### hasImage() {#hasImage--}
```
public boolean hasImage()
```


如果形状具有图像字节或链接图像，则返回 true。 (4654,6)

**退货:**
boolean - 如果形状具有图像字节或链接图像，则为真。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isLink() {#isLink--}
```
public boolean isLink()
```


如果图像链接到形状，则返回 true（当[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)已指定）。 (4678,6)

**退货:**
 boolean - 如果图像链接到形状则为真（当[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)已指定）。
### isLinkOnly() {#isLinkOnly--}
```
public boolean isLinkOnly()
```


如果图像已链接且未存储在文档中，则返回 true。 (4685,6)

**退货:**
boolean - 如果图像已链接且未存储在文档中，则为真。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream stream) {#save-java.io.OutputStream-}
```
public void save(OutputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


将图像保存到文件中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 保存图像的文件名。 |

### setBiLevel(boolean value) {#setBiLevel-boolean-}
```
public void setBiLevel(boolean value)
```


确定图像是否以黑白显示。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double-}
```
public void setBrightness(double value)
```


设置图像的亮度。此属性的值必须是从 0.0（最暗）到 1.0（最亮）的数字。

默认值为 0.5。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 图片的亮度。 |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color-}
```
public void setChromaKey(Color value)
```


定义将被视为透明的图像的颜色值。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 对应的 java.awt.Color 值。 |

### setContrast(double value) {#setContrast-double-}
```
public void setContrast(double value)
```


设置指定图片的对比度。此属性的值必须是从 0.0（最小对比度）到 1.0（最大对比度）的数字。

默认值为 0.5。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 指定图片的对比度。 |

### setCropBottom(double value) {#setCropBottom-double-}
```
public void setCropBottom(double value)
```


定义从底部移除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setCropLeft(double value) {#setCropLeft-double-}
```
public void setCropLeft(double value)
```


定义从左侧删除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setCropRight(double value) {#setCropRight-double-}
```
public void setCropRight(double value)
```


定义从右侧移除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setCropTop(double value) {#setCropTop-double-}
```
public void setCropTop(double value)
```


定义从顶部移除图片的比例。

裁剪量的范围可以从 -1.0 到 1.0。默认值为 0。请注意，值为 1 将根本不显示图片。负值将导致图片从被裁剪的边缘向内挤压（图片和裁剪边缘之间的空白空间将被形状的填充颜色填充）。小于 1 的正值将导致剩余的图片被拉伸以适应形状。

默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setGrayScale(boolean value) {#setGrayScale-boolean-}
```
public void setGrayScale(boolean value)
```


确定图片是否以灰度模式显示。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage image)
```


设置形状显示的图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | 图像对象。 |

### setImage(InputStream stream) {#setImage-java.io.InputStream-}
```
public void setImage(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String-}
```
public void setImage(String fileName)
```


设置形状显示的图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 图像文件。可以是文件名或 URL。 |

### setImageBytes(byte[] value) {#setImageBytes-byte---}
```
public void setImageBytes(byte[] value)
```


设置存储在形状中的图像的原始字节。

将值设置为 null 或空数组将从形状中删除图像。

如果图像未存储在文档中，则返回 null（例如，在这种情况下，图像可能是链接的）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | 存储在形状中的图像的原始字节。 |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


设置链接图像的源文件的路径和名称。

默认值为空字符串。

如果[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)不是空字符串，图像是链接的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 链接图像的源文件的路径和名称。 |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


定义图像的标题。

默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### toByteArray() {#toByteArray--}
```
public byte[] toByteArray()
```


返回任何图像的图像字节，无论图像是存储还是链接。

**退货:**
字节[] - 如果图像已链接，则每次调用时都会下载图像。
### toImage() {#toImage--}
```
public BufferedImage toImage()
```


获取作为 java BufferedImage 对象存储在形状中的图像。

**退货:**
java.awt.image.BufferedImage - 每次调用此方法时尝试从图像字节创建一个新的 java.awt.image.BufferedImage 对象。如果 javax.imageio.ImageReader 无法读取图像字节（emf、wmf、tiff 等），则该方法返回 null。

调用者负责处理图像对象。
### toStream() {#toStream--}
```
public InputStream toStream()
```


创建并返回包含图像字节的流。

如果图像字节存储在形状中，则创建并返回一个对象。

如果图像被链接并存储在文件中，则打开文件并返回一个对象。

如果图像被链接并存储在外部 URL 中，则打开 URL 并返回一个对象。

调用者是否有责任处置流对象。

这还没有移植到Java。

**退货:**
java.io.InputStream
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
