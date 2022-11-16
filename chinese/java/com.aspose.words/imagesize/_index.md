---
title: ImageSize
second_title: Aspose.Words for Java API 参考
description: 包含有关图像大小和分辨率的信息。
type: docs
weight: 342
url: /zh/java/com.aspose.words/imagesize/
---

**遗产：**
java.lang.Object
```
public class ImageSize
```

包含有关图像大小和分辨率的信息。

要了解更多信息，请访问**Working with Images**文档文章。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int-) | 将宽度和高度初始化为给定的像素值。 |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double-) | 将宽度、高度和分辨率初始化为给定值。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getHeightPixels()](#getHeightPixels--) | 获取图像的高度（以像素为单位）。 |
| [getHeightPoints()](#getHeightPoints--) | 获取图像的高度（以磅为单位）。 |
| [getHorizontalResolution()](#getHorizontalResolution--) | 获取以 DPI 为单位的水平分辨率。 |
| [getVerticalResolution()](#getVerticalResolution--) | 获取 DPI 中的垂直分辨率。 |
| [getWidthPixels()](#getWidthPixels--) | 获取图像的宽度（以像素为单位）。 |
| [getWidthPoints()](#getWidthPoints--) | 以点为单位获取图像的宽度。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int-}
```
public ImageSize(int widthPixels, int heightPixels)
```


将宽度和高度初始化为给定的像素值。将分辨率初始化为 96 dpi。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| widthPixels | int | 以像素为单位的宽度。 |
| heightPixels | int | 以像素为单位的高度。 |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double-}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


将宽度、高度和分辨率初始化为给定值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| widthPixels | int | 以像素为单位的宽度。 |
| heightPixels | int | 以像素为单位的高度。 |
| horizontalResolution | double | DPI 中的水平分辨率。 |
| verticalResolution | double | DPI 中的垂直分辨率。 |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getHeightPixels() {#getHeightPixels--}
```
public int getHeightPixels()
```


获取图像的高度（以像素为单位）。

**退货：**
int - 图像的高度（以像素为单位）。
### getHeightPoints() {#getHeightPoints--}
```
public double getHeightPoints()
```


获取图像的高度（以磅为单位）。 1 点是 1/72 英寸。

**退货：**
double - 图像的高度（以磅为单位）。
### getHorizontalResolution() {#getHorizontalResolution--}
```
public double getHorizontalResolution()
```


获取以 DPI 为单位的水平分辨率。

**退货：**
double - DPI 中的水平分辨率。
### getVerticalResolution() {#getVerticalResolution--}
```
public double getVerticalResolution()
```


获取 DPI 中的垂直分辨率。

**退货：**
double - DPI 中的垂直分辨率。
### getWidthPixels() {#getWidthPixels--}
```
public int getWidthPixels()
```


获取图像的宽度（以像素为单位）。

**退货：**
int - 图像的宽度（以像素为单位）。
### getWidthPoints() {#getWidthPoints--}
```
public double getWidthPoints()
```


以点为单位获取图像的宽度。 1 点是 1/72 英寸。

**退货：**
double - 图像的宽度（以磅为单位）。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
