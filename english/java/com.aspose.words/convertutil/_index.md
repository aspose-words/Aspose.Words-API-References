---
title: ConvertUtil
second_title: Aspose.Words for Java API Reference
description: Provides helper functions to convert between various measurement units.
type: docs
weight: 95
url: /java/com.aspose.words/convertutil/
---

**Inheritance:**
java.lang.Object
```
public class ConvertUtil
```

Provides helper functions to convert between various measurement units.

To learn more, visit the **Convert Between Measurement Units** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [pointToPixel(double points)](#pointToPixel-double-) | Converts points to pixels. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double-) | Converts points to pixels at the specified pixel resolution. |
| [pixelToPoint(double pixels)](#pixelToPoint-double-) | Converts pixels to points. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double-) | Converts pixels to points at the specified pixel resolution. |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double-) | Converts pixels from one resolution to another. |
| [inchToPoint(double inches)](#inchToPoint-double-) | Converts inches to points. |
| [pointToInch(double points)](#pointToInch-double-) | Converts points to inches. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double-) | Converts millimeters to points. |
### pointToPixel(double points) {#pointToPixel-double-}
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
### pointToPixel(double points, double resolution) {#pointToPixel-double-double-}
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
### pixelToPoint(double pixels) {#pixelToPoint-double-}
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
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double-}
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
### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double-}
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
### inchToPoint(double inches) {#inchToPoint-double-}
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
### pointToInch(double points) {#pointToInch-double-}
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
### millimeterToPoint(double millimeters) {#millimeterToPoint-double-}
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
