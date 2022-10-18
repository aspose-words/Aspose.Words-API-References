---
title: ImageSize
second_title: Aspose.Words for Java API Reference
description: Contains information about image size and resolution.
type: docs
weight: 342
url: /java/com.aspose.words/imagesize/
---

**Inheritance:**
java.lang.Object
```
public class ImageSize
```

Contains information about image size and resolution.

To learn more, visit the **Working with Images** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int-) | Initializes width and height to the given values in pixels. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double-) | Initializes width, height and resolution to the given values. |
## Methods

| Method | Description |
| --- | --- |
| [getWidthPixels()](#getWidthPixels--) | Gets the width of the image in pixels. |
| [getHeightPixels()](#getHeightPixels--) | Gets the height of the image in pixels. |
| [getHorizontalResolution()](#getHorizontalResolution--) | Gets the horizontal resolution in DPI. |
| [getVerticalResolution()](#getVerticalResolution--) | Gets the vertical resolution in DPI. |
| [getWidthPoints()](#getWidthPoints--) | Gets the width of the image in points. |
| [getHeightPoints()](#getHeightPoints--) | Gets the height of the image in points. |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int-}
```
public ImageSize(int widthPixels, int heightPixels)
```


Initializes width and height to the given values in pixels. Initializes resolution to 96 dpi.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| widthPixels | int | Width in pixels. |
| heightPixels | int | Height in pixels. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double-}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


Initializes width, height and resolution to the given values.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| widthPixels | int | Width in pixels. |
| heightPixels | int | Height in pixels. |
| horizontalResolution | double | Horizontal resolution in DPI. |
| verticalResolution | double | Vertical resolution in DPI. |

### getWidthPixels() {#getWidthPixels--}
```
public int getWidthPixels()
```


Gets the width of the image in pixels.

**Returns:**
int - The width of the image in pixels.
### getHeightPixels() {#getHeightPixels--}
```
public int getHeightPixels()
```


Gets the height of the image in pixels.

**Returns:**
int - The height of the image in pixels.
### getHorizontalResolution() {#getHorizontalResolution--}
```
public double getHorizontalResolution()
```


Gets the horizontal resolution in DPI.

**Returns:**
double - The horizontal resolution in DPI.
### getVerticalResolution() {#getVerticalResolution--}
```
public double getVerticalResolution()
```


Gets the vertical resolution in DPI.

**Returns:**
double - The vertical resolution in DPI.
### getWidthPoints() {#getWidthPoints--}
```
public double getWidthPoints()
```


Gets the width of the image in points. 1 point is 1/72 inch.

**Returns:**
double - The width of the image in points.
### getHeightPoints() {#getHeightPoints--}
```
public double getHeightPoints()
```


Gets the height of the image in points. 1 point is 1/72 inch.

**Returns:**
double - The height of the image in points.
