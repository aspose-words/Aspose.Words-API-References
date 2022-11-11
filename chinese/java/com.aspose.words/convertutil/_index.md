---
title: ConvertUtil
second_title: Aspose.Words for Java API Reference
description: 提供帮助函数以在各种测量单位之间进行转换。
type: docs
weight: 95
url: /zh/java/com.aspose.words/convertutil/
---

**遗产:**
java.lang.Object
```
public class ConvertUtil
```

提供帮助函数以在各种测量单位之间进行转换。

要了解更多信息，请访问**Convert Between Measurement Units**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [inchToPoint(double inches)](#inchToPoint-double-) | 将英寸转换为磅。 |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double-) | 将毫米转换为磅。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double-) | 将像素从一种分辨率转换为另一种分辨率。 |
| [pixelToPoint(double pixels)](#pixelToPoint-double-) | 将像素转换为点。 |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double-) | 将像素转换为指定像素分辨率的点。 |
| [pointToInch(double points)](#pointToInch-double-) | 将点转换为英寸。 |
| [pointToPixel(double points)](#pointToPixel-double-) | 将点转换为像素。 |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double-) | 将点转换为指定像素分辨率的像素。 |
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
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### inchToPoint(double inches) {#inchToPoint-double-}
```
public static double inchToPoint(double inches)
```


将英寸转换为磅。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inches | double | 要转换的值。 1 英寸等于 72 分。 |

**退货:**
双倍的
### millimeterToPoint(double millimeters) {#millimeterToPoint-double-}
```
public static double millimeterToPoint(double millimeters)
```


将毫米转换为磅。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| millimeters | double | 要转换的值。 1 英寸等于 25.4 毫米。 1 英寸等于 72 分。 |

**退货:**
双倍的
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double-}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


将像素从一种分辨率转换为另一种分辨率。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pixels | double | 要转换的值。 |
| oldDpi | double | 当前的 dpi（每英寸点数）分辨率。 |
| newDpi | double | 新的 dpi（每英寸点数）分辨率。 |

**退货:**
整数
### pixelToPoint(double pixels) {#pixelToPoint-double-}
```
public static double pixelToPoint(double pixels)
```


将像素转换为点。将像素转换为 96 dpi 的点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pixels | double | 要转换的值。 1 英寸等于 72 分。 |

**退货:**
双倍的
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double-}
```
public static double pixelToPoint(double pixels, double resolution)
```


将像素转换为指定像素分辨率的点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pixels | double | 要转换的值。 |
| resolution | double | dpi（每英寸点数）分辨率。 1 英寸等于 72 分。 |

**退货:**
双倍的
### pointToInch(double points) {#pointToInch-double-}
```
public static double pointToInch(double points)
```


将点转换为英寸。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| points | double | 要转换的值。 1 英寸等于 72 分。 |

**退货:**
双倍的
### pointToPixel(double points) {#pointToPixel-double-}
```
public static double pointToPixel(double points)
```


将点转换为像素。将点转换为 96 dpi 的像素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| points | double | 要转换的值。 1 英寸等于 72 分。 |

**退货:**
双倍的
### pointToPixel(double points, double resolution) {#pointToPixel-double-double-}
```
public static double pointToPixel(double points, double resolution)
```


将点转换为指定像素分辨率的像素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| points | double | 要转换的值。 |
| resolution | double | dpi（每英寸点数）分辨率。 1 英寸等于 72 分。 |

**退货:**
双倍的
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
