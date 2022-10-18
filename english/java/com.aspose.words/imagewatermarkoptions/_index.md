---
title: ImageWatermarkOptions
second_title: Aspose.Words for Java API Reference
description: Contains options that can be specified when adding a watermark with image.
type: docs
weight: 344
url: /java/com.aspose.words/imagewatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImageWatermarkOptions
```

Contains options that can be specified when adding a watermark with image.

To learn more, visit the **Working with Watermark** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getScale()](#getScale--) | Gets the scale factor expressed as a fraction of the image. |
| [setScale(double value)](#setScale-double-) | Sets the scale factor expressed as a fraction of the image. |
| [isWashout()](#isWashout--) | Gets a boolean value which is responsible for washout effect of the watermark. |
| [isWashout(boolean value)](#isWashout-boolean-) | Sets a boolean value which is responsible for washout effect of the watermark. |
### getScale() {#getScale--}
```
public double getScale()
```


Gets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.

**Returns:**
double - The scale factor expressed as a fraction of the image.
### setScale(double value) {#setScale-double-}
```
public void setScale(double value)
```


Sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The scale factor expressed as a fraction of the image. |

### isWashout() {#isWashout--}
```
public boolean isWashout()
```


Gets a boolean value which is responsible for washout effect of the watermark. The default value is True.

**Returns:**
boolean - A boolean value which is responsible for washout effect of the watermark.
### isWashout(boolean value) {#isWashout-boolean-}
```
public void isWashout(boolean value)
```


Sets a boolean value which is responsible for washout effect of the watermark. The default value is True.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value which is responsible for washout effect of the watermark. |

