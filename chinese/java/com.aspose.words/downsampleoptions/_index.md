---
title: DownsampleOptions
second_title: Aspose.Words for Java API 参考
description:允许指定下采样选项。
type: docs
weight: 133
url: /zh/java/com.aspose.words/downsampleoptions/
---

**遗产:**
java.lang.Object
```
public class DownsampleOptions
```

允许指定下采样选项。

要了解更多信息，请访问**Save a Document**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDownsampleImages()](#getDownsampleImages--) | 指定是否应该对图像进行下采样。 |
| [getResolution()](#getResolution--) | 指定图像应该被下采样到的分辨率（以每英寸像素为单位）。 |
| [getResolutionThreshold()](#getResolutionThreshold--) | 以每英寸像素数指定阈值分辨率。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean-) | 指定是否应该对图像进行下采样。 |
| [setResolution(int value)](#setResolution-int-) | 指定图像应该被下采样到的分辨率（以每英寸像素为单位）。 |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int-) | 以每英寸像素数指定阈值分辨率。 |
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
### getDownsampleImages() {#getDownsampleImages--}
```
public boolean getDownsampleImages()
```


指定是否应该对图像进行下采样。默认值是true 。

**退货:**
boolean - 对应的布尔值。
### getResolution() {#getResolution--}
```
public int getResolution()
```


指定图像应该被下采样到的分辨率（以每英寸像素为单位）。默认值为 220 ppi。

**退货:**
int - 对应的 int 值。
### getResolutionThreshold() {#getResolutionThreshold--}
```
public int getResolutionThreshold()
```


以每英寸像素数指定阈值分辨率。如果文档中图像的分辨率小于阈值，则不会应用下采样算法。值 0 表示不使用阈值检查，并且对所有可以缩小尺寸的图像进行下采样。默认值为 0。

**退货:**
int - 对应的 int 值。
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




### setDownsampleImages(boolean value) {#setDownsampleImages-boolean-}
```
public void setDownsampleImages(boolean value)
```


指定是否应该对图像进行下采样。默认值是true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setResolution(int value) {#setResolution-int-}
```
public void setResolution(int value)
```


指定图像应该被下采样到的分辨率（以每英寸像素为单位）。默认值为 220 ppi。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setResolutionThreshold(int value) {#setResolutionThreshold-int-}
```
public void setResolutionThreshold(int value)
```


以每英寸像素数指定阈值分辨率。如果文档中图像的分辨率小于阈值，则不会应用下采样算法。值 0 表示不使用阈值检查，并且对所有可以缩小尺寸的图像进行下采样。默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

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
