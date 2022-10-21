---
title: FrameFormat
second_title: Aspose.Words for Java API Reference
description: Represents frame related formatting for a paragraph.
type: docs
weight: 301
url: /java/com.aspose.words/frameformat/
---

**Inheritance:**
java.lang.Object
```
public class FrameFormat
```

Represents frame related formatting for a paragraph.

This object is always created. If a paragraph is a frame, then all properties will contain respective values, otherwise all properties are set to their defaults.

Use [isFrame()](../../com.aspose.words/frameformat\#isFrame--) to check whether paragraph is a frame.
## Methods

| Method | Description |
| --- | --- |
| [getHeightRule()](#getHeightRule--) | Gets the rule for determining the height of the specified frame. |
| [getHeight()](#getHeight--) | Gets the height of the specified frame. |
| [getHorizontalDistanceFromText()](#getHorizontalDistanceFromText--) | Gets horizontal distance between a frame and the surrounding text, in points. |
| [getHorizontalPosition()](#getHorizontalPosition--) | Gets horizontal distance between the edge of the frame and the item specified by the [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat\#getRelativeHorizontalPosition--) property. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | Gets the relative horizontal position of a frame. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | Gets the relative vertical position of a frame. |
| [getVerticalDistanceFromText()](#getVerticalDistanceFromText--) | Specifies vertical distance (in points) between a frame and the surrounding text. |
| [getVerticalPosition()](#getVerticalPosition--) | Gets vertical distance between the edge of the frame and the item specified by the [getRelativeVerticalPosition()](../../com.aspose.words/frameformat\#getRelativeVerticalPosition--) property. |
| [getWidth()](#getWidth--) | Gets the width of the specified frame, in points. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Gets vertical alignment of the specified frame. |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | Gets horizontal alignment of the specified frame. |
| [isFrame()](#isFrame--) | Returns true if the paragraph is a frame. |
### getHeightRule() {#getHeightRule--}
```
public int getHeightRule()
```


Gets the rule for determining the height of the specified frame.

**Returns:**
int - The rule for determining the height of the specified frame. The returned value is one of [HeightRule](../../com.aspose.words/heightrule) constants.
### getHeight() {#getHeight--}
```
public double getHeight()
```


Gets the height of the specified frame.

**Returns:**
double - The height of the specified frame.
### getHorizontalDistanceFromText() {#getHorizontalDistanceFromText--}
```
public double getHorizontalDistanceFromText()
```


Gets horizontal distance between a frame and the surrounding text, in points.

**Returns:**
double - Horizontal distance between a frame and the surrounding text, in points.
### getHorizontalPosition() {#getHorizontalPosition--}
```
public double getHorizontalPosition()
```


Gets horizontal distance between the edge of the frame and the item specified by the [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat\#getRelativeHorizontalPosition--) property.

**Returns:**
double - Horizontal distance between the edge of the frame and the item specified by the [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat\#getRelativeHorizontalPosition--) property.
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


Gets the relative horizontal position of a frame.

**Returns:**
int - The relative horizontal position of a frame. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants.
### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


Gets the relative vertical position of a frame.

**Returns:**
int - The relative vertical position of a frame. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants.
### getVerticalDistanceFromText() {#getVerticalDistanceFromText--}
```
public double getVerticalDistanceFromText()
```


Specifies vertical distance (in points) between a frame and the surrounding text.

**Returns:**
double - The corresponding  double  value.
### getVerticalPosition() {#getVerticalPosition--}
```
public double getVerticalPosition()
```


Gets vertical distance between the edge of the frame and the item specified by the [getRelativeVerticalPosition()](../../com.aspose.words/frameformat\#getRelativeVerticalPosition--) property.

**Returns:**
double - Vertical distance between the edge of the frame and the item specified by the [getRelativeVerticalPosition()](../../com.aspose.words/frameformat\#getRelativeVerticalPosition--) property.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Gets the width of the specified frame, in points.

**Returns:**
double - The width of the specified frame, in points.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Gets vertical alignment of the specified frame.

**Returns:**
int - Vertical alignment of the specified frame. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants.
### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


Gets horizontal alignment of the specified frame.

**Returns:**
int - Horizontal alignment of the specified frame. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants.
### isFrame() {#isFrame--}
```
public boolean isFrame()
```


Returns true if the paragraph is a frame.

**Returns:**
boolean - True if the paragraph is a frame.
