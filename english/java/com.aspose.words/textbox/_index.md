---
title: TextBox
second_title: Aspose.Words for Java API Reference
description: Defines attributes that specify how a text is displayed inside a shape.
type: docs
weight: 558
url: /java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

Defines attributes that specify how a text is displayed inside a shape.

To learn more, visit the **Working with Shapes** documentation article.

Use the [Shape.getTextBox()](../../com.aspose.words/shape\#getTextBox--) property to access text properties of a shape. You do not create instances of the [TextBox](../../com.aspose.words/textbox) class directly.
## Methods

| Method | Description |
| --- | --- |
| [getInternalMarginLeft()](#getInternalMarginLeft--) | Specifies the inner left margin in points for a shape. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double-) | Specifies the inner left margin in points for a shape. |
| [getInternalMarginRight()](#getInternalMarginRight--) | Specifies the inner right margin in points for a shape. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double-) | Specifies the inner right margin in points for a shape. |
| [getInternalMarginTop()](#getInternalMarginTop--) | Specifies the inner top margin in points for a shape. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double-) | Specifies the inner top margin in points for a shape. |
| [getInternalMarginBottom()](#getInternalMarginBottom--) | Specifies the inner bottom margin in points for a shape. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double-) | Specifies the inner bottom margin in points for a shape. |
| [getFitShapeToText()](#getFitShapeToText--) | Determines whether Microsoft Word will grow the shape to fit text. |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean-) | Determines whether Microsoft Word will grow the shape to fit text. |
| [getLayoutFlow()](#getLayoutFlow--) | Determines the flow of the text layout in a shape. |
| [setLayoutFlow(int value)](#setLayoutFlow-int-) | Determines the flow of the text layout in a shape. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode--) | Determines how text wraps inside a shape. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int-) | Determines how text wraps inside a shape. |
| [getVerticalAnchor()](#getVerticalAnchor--) | Specifies the vertical alignment of the text within a shape. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | Specifies the vertical alignment of the text within a shape. |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox-) | Determines whether this TextBox can be linked to the target Textbox. |
| [getNext()](#getNext--) | Gets a TextBox that represents the next TextBox in a sequence of shapes. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox-) | Sets a TextBox that represents the next TextBox in a sequence of shapes. |
| [getPrevious()](#getPrevious--) | Returns a TextBox that represents the previous TextBox in a sequence of shapes. |
| [breakForwardLink()](#breakForwardLink--) | Breaks the link to the next TextBox. |
| [getParent()](#getParent--) | Gets a parent shape for the TextBox. |
### getInternalMarginLeft() {#getInternalMarginLeft--}
```
public double getInternalMarginLeft()
```


Specifies the inner left margin in points for a shape.

The default value is 1/10 inch.

**Returns:**
double - The corresponding  double  value.
### setInternalMarginLeft(double value) {#setInternalMarginLeft-double-}
```
public void setInternalMarginLeft(double value)
```


Specifies the inner left margin in points for a shape.

The default value is 1/10 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getInternalMarginRight() {#getInternalMarginRight--}
```
public double getInternalMarginRight()
```


Specifies the inner right margin in points for a shape.

The default value is 1/10 inch.

**Returns:**
double - The corresponding  double  value.
### setInternalMarginRight(double value) {#setInternalMarginRight-double-}
```
public void setInternalMarginRight(double value)
```


Specifies the inner right margin in points for a shape.

The default value is 1/10 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getInternalMarginTop() {#getInternalMarginTop--}
```
public double getInternalMarginTop()
```


Specifies the inner top margin in points for a shape.

The default value is 1/20 inch.

**Returns:**
double - The corresponding  double  value.
### setInternalMarginTop(double value) {#setInternalMarginTop-double-}
```
public void setInternalMarginTop(double value)
```


Specifies the inner top margin in points for a shape.

The default value is 1/20 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getInternalMarginBottom() {#getInternalMarginBottom--}
```
public double getInternalMarginBottom()
```


Specifies the inner bottom margin in points for a shape.

The default value is 1/20 inch.

**Returns:**
double - The corresponding  double  value.
### setInternalMarginBottom(double value) {#setInternalMarginBottom-double-}
```
public void setInternalMarginBottom(double value)
```


Specifies the inner bottom margin in points for a shape.

The default value is 1/20 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getFitShapeToText() {#getFitShapeToText--}
```
public boolean getFitShapeToText()
```


Determines whether Microsoft Word will grow the shape to fit text.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setFitShapeToText(boolean value) {#setFitShapeToText-boolean-}
```
public void setFitShapeToText(boolean value)
```


Determines whether Microsoft Word will grow the shape to fit text.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLayoutFlow() {#getLayoutFlow--}
```
public int getLayoutFlow()
```


Determines the flow of the text layout in a shape.

The default value is [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow\#HORIZONTAL).

**Returns:**
int - The corresponding  int  value. The returned value is one of [LayoutFlow](../../com.aspose.words/layoutflow) constants.
### setLayoutFlow(int value) {#setLayoutFlow-int-}
```
public void setLayoutFlow(int value)
```


Determines the flow of the text layout in a shape.

The default value is [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow\#HORIZONTAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LayoutFlow](../../com.aspose.words/layoutflow) constants. |

### getTextBoxWrapMode() {#getTextBoxWrapMode--}
```
public int getTextBoxWrapMode()
```


Determines how text wraps inside a shape.

The default value is [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode\#SQUARE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode) constants.
### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int-}
```
public void setTextBoxWrapMode(int value)
```


Determines how text wraps inside a shape.

The default value is [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode\#SQUARE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode) constants. |

### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


Specifies the vertical alignment of the text within a shape.

The default value is [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor\#TOP).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TextBoxAnchor](../../com.aspose.words/textboxanchor) constants.
### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


Specifies the vertical alignment of the text within a shape.

The default value is [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor\#TOP).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextBoxAnchor](../../com.aspose.words/textboxanchor) constants. |

### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox-}
```
public boolean isValidLinkTarget(TextBox target)
```


Determines whether this TextBox can be linked to the target Textbox.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox) |  |

**Returns:**
boolean
### getNext() {#getNext--}
```
public TextBox getNext()
```


Gets a TextBox that represents the next TextBox in a sequence of shapes.

**Returns:**
[TextBox](../../com.aspose.words/textbox) - A TextBox that represents the next TextBox in a sequence of shapes.
### setNext(TextBox value) {#setNext-com.aspose.words.TextBox-}
```
public void setNext(TextBox value)
```


Sets a TextBox that represents the next TextBox in a sequence of shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox) | A TextBox that represents the next TextBox in a sequence of shapes. |

### getPrevious() {#getPrevious--}
```
public TextBox getPrevious()
```


Returns a TextBox that represents the previous TextBox in a sequence of shapes.

**Returns:**
[TextBox](../../com.aspose.words/textbox) - A TextBox that represents the previous TextBox in a sequence of shapes.
### breakForwardLink() {#breakForwardLink--}
```
public void breakForwardLink()
```


Breaks the link to the next TextBox. BreakForwardLink() doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and BreakForwardLink at the 2-nd textbox will create two sequences 1-2, 3-4.

### getParent() {#getParent--}
```
public Shape getParent()
```


Gets a parent shape for the TextBox.

**Returns:**
[Shape](../../com.aspose.words/shape) - A parent shape for the TextBox.
