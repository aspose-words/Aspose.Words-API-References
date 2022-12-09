---
title: ConvertUtil
second_title: Aspose.Words for Java API Reference
description: Provides helper functions to convert between various measurement units.
type: docs
weight: 96
url: /java/com.aspose.words/convertutil/
---

**Inheritance:**
java.lang.Object
```
public class ConvertUtil
```

Provides helper functions to convert between various measurement units.

To learn more, visit the [ Convert Between Measurement Units ][Convert Between Measurement Units] documentation article.


[Convert Between Measurement Units]: https://docs.aspose.com/words/java/convert-between-measurement-units/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [inchToPoint(double inches)](#inchToPoint-double) | Converts inches to points. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double) | Converts millimeters to points. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double) | Converts pixels from one resolution to another. |
| [pixelToPoint(double pixels)](#pixelToPoint-double) | Converts pixels to points. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double) | Converts pixels to points at the specified pixel resolution. |
| [pointToInch(double points)](#pointToInch-double) | Converts points to inches. |
| [pointToPixel(double points)](#pointToPixel-double) | Converts points to pixels. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double) | Converts points to pixels at the specified pixel resolution. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### inchToPoint(double inches) {#inchToPoint-double}
```
public static double inchToPoint(double inches)
```


Converts inches to points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inches | double | The value to convert. 1 inch equals 72 points. |

**Returns:**
double
### millimeterToPoint(double millimeters) {#millimeterToPoint-double}
```
public static double millimeterToPoint(double millimeters)
```


Converts millimeters to points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | double | The value to convert. 1 inch equals 25.4 millimeters. 1 inch equals 72 points. |

**Returns:**
double
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


Converts pixels from one resolution to another.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |
| oldDpi | double | The current dpi (dots per inch) resolution. |
| newDpi | double | The new dpi (dots per inch) resolution. |

**Returns:**
int
### pixelToPoint(double pixels) {#pixelToPoint-double}
```
public static double pixelToPoint(double pixels)
```


Converts pixels to points.  Converts pixels to points at 96 dpi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. 1 inch equals 72 points. |

**Returns:**
double
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double}
```
public static double pixelToPoint(double pixels, double resolution)
```


Converts pixels to points at the specified pixel resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |
| resolution | double | The dpi (dots per inch) resolution. 1 inch equals 72 points. |

**Returns:**
double
### pointToInch(double points) {#pointToInch-double}
```
public static double pointToInch(double points)
```


Converts points to inches.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. 1 inch equals 72 points. |

**Returns:**
double
### pointToPixel(double points) {#pointToPixel-double}
```
public static double pointToPixel(double points)
```


Converts points to pixels.  Converts points to pixels at 96 dpi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. 1 inch equals 72 points. |

**Returns:**
double
### pointToPixel(double points, double resolution) {#pointToPixel-double-double}
```
public static double pointToPixel(double points, double resolution)
```


Converts points to pixels at the specified pixel resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. |
| resolution | double | The dpi (dots per inch) resolution. 1 inch equals 72 points. |

**Returns:**
double
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

