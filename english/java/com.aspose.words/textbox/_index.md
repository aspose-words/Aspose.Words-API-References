---
title: TextBox
linktitle: TextBox
second_title: Aspose.Words for Java API Reference
description: Defines attributes that specify how a text is displayed inside a shape in Java.
type: docs
weight: 564
url: /java/com.aspose.words/textbox/
---

**Inheritance:**
java.lang.Object
```
public class TextBox
```

Defines attributes that specify how a text is displayed inside a shape.

To learn more, visit the [ Working with Shapes ][Working with Shapes] documentation article.

Use the [Shape.getTextBox()](../../com.aspose.words/shape/\#getTextBox) property to access text properties of a shape. You do not create instances of the [TextBox](../../com.aspose.words/textbox/) class directly.


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Methods

| Method | Description |
| --- | --- |
| [breakForwardLink()](#breakForwardLink) | Breaks the link to the next [TextBox](../../com.aspose.words/textbox/). |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getFitShapeToText()](#getFitShapeToText) | Determines whether Microsoft Word will grow the shape to fit text. |
| [getInternalMarginBottom()](#getInternalMarginBottom) | Specifies the inner bottom margin in points for a shape. |
| [getInternalMarginLeft()](#getInternalMarginLeft) | Specifies the inner left margin in points for a shape. |
| [getInternalMarginRight()](#getInternalMarginRight) | Specifies the inner right margin in points for a shape. |
| [getInternalMarginTop()](#getInternalMarginTop) | Specifies the inner top margin in points for a shape. |
| [getLayoutFlow()](#getLayoutFlow) | Determines the flow of the text layout in a shape. |
| [getNext()](#getNext) | Gets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |
| [getNoTextRotation()](#getNoTextRotation) | Gets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [getParent()](#getParent) | Gets a parent shape for the [TextBox](../../com.aspose.words/textbox/). |
| [getPrevious()](#getPrevious) | Returns a [TextBox](../../com.aspose.words/textbox/) that represents the previous [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode) | Determines how text wraps inside a shape. |
| [getVerticalAnchor()](#getVerticalAnchor) | Specifies the vertical alignment of the text within a shape. |
| [hashCode()](#hashCode) |  |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox) | Determines whether this [TextBox](../../com.aspose.words/textbox/) can be linked to the target [TextBox](../../com.aspose.words/textbox/). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean) | Determines whether Microsoft Word will grow the shape to fit text. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double) | Specifies the inner bottom margin in points for a shape. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double) | Specifies the inner left margin in points for a shape. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double) | Specifies the inner right margin in points for a shape. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double) | Specifies the inner top margin in points for a shape. |
| [setLayoutFlow(int value)](#setLayoutFlow-int) | Determines the flow of the text layout in a shape. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox) | Sets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |
| [setNoTextRotation(boolean value)](#setNoTextRotation-boolean) | Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int) | Determines how text wraps inside a shape. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | Specifies the vertical alignment of the text within a shape. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### breakForwardLink() {#breakForwardLink}
```
public void breakForwardLink()
```


Breaks the link to the next [TextBox](../../com.aspose.words/textbox/). [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) doesn't break all other links in the current sequence of shapes. For example: 1-2-3-4 sequence and [breakForwardLink()](../../com.aspose.words/textbox/\#breakForwardLink) at the 2-nd textbox will create two sequences 1-2, 3-4.

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
### getFitShapeToText() {#getFitShapeToText}
```
public boolean getFitShapeToText()
```


Determines whether Microsoft Word will grow the shape to fit text.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getInternalMarginBottom() {#getInternalMarginBottom}
```
public double getInternalMarginBottom()
```


Specifies the inner bottom margin in points for a shape.

The default value is 1/20 inch.

**Returns:**
double - The corresponding  double  value.
### getInternalMarginLeft() {#getInternalMarginLeft}
```
public double getInternalMarginLeft()
```


Specifies the inner left margin in points for a shape.

The default value is 1/10 inch.

**Returns:**
double - The corresponding  double  value.
### getInternalMarginRight() {#getInternalMarginRight}
```
public double getInternalMarginRight()
```


Specifies the inner right margin in points for a shape.

The default value is 1/10 inch.

**Returns:**
double - The corresponding  double  value.
### getInternalMarginTop() {#getInternalMarginTop}
```
public double getInternalMarginTop()
```


Specifies the inner top margin in points for a shape.

The default value is 1/20 inch.

**Returns:**
double - The corresponding  double  value.
### getLayoutFlow() {#getLayoutFlow}
```
public int getLayoutFlow()
```


Determines the flow of the text layout in a shape.

The default value is [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

**Returns:**
int - The corresponding  int  value. The returned value is one of [LayoutFlow](../../com.aspose.words/layoutflow/) constants.
### getNext() {#getNext}
```
public TextBox getNext()
```


Gets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.

**Returns:**
[TextBox](../../com.aspose.words/textbox/) - A [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.
### getNoTextRotation() {#getNoTextRotation}
```
public boolean getNoTextRotation()
```


Gets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.

The default value is  false 

**Returns:**
boolean - A boolean value indicating either text of the TextBox should not rotate when the shape is rotated.
### getParent() {#getParent}
```
public Shape getParent()
```


Gets a parent shape for the [TextBox](../../com.aspose.words/textbox/).

**Returns:**
[Shape](../../com.aspose.words/shape/) - A parent shape for the [TextBox](../../com.aspose.words/textbox/).
### getPrevious() {#getPrevious}
```
public TextBox getPrevious()
```


Returns a [TextBox](../../com.aspose.words/textbox/) that represents the previous [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.

**Returns:**
[TextBox](../../com.aspose.words/textbox/) - A [TextBox](../../com.aspose.words/textbox/) that represents the previous [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.
### getTextBoxWrapMode() {#getTextBoxWrapMode}
```
public int getTextBoxWrapMode()
```


Determines how text wraps inside a shape.

The default value is [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) constants.
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


Specifies the vertical alignment of the text within a shape.

The default value is [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TextBoxAnchor](../../com.aspose.words/textboxanchor/) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox}
```
public boolean isValidLinkTarget(TextBox target)
```


Determines whether this [TextBox](../../com.aspose.words/textbox/) can be linked to the target [TextBox](../../com.aspose.words/textbox/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox/) |  |

**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setFitShapeToText(boolean value) {#setFitShapeToText-boolean}
```
public void setFitShapeToText(boolean value)
```


Determines whether Microsoft Word will grow the shape to fit text.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double}
```
public void setInternalMarginBottom(double value)
```


Specifies the inner bottom margin in points for a shape.

The default value is 1/20 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double}
```
public void setInternalMarginLeft(double value)
```


Specifies the inner left margin in points for a shape.

The default value is 1/10 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double}
```
public void setInternalMarginRight(double value)
```


Specifies the inner right margin in points for a shape.

The default value is 1/10 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double}
```
public void setInternalMarginTop(double value)
```


Specifies the inner top margin in points for a shape.

The default value is 1/20 inch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setLayoutFlow(int value) {#setLayoutFlow-int}
```
public void setLayoutFlow(int value)
```


Determines the flow of the text layout in a shape.

The default value is [LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow/\#HORIZONTAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LayoutFlow](../../com.aspose.words/layoutflow/) constants. |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox}
```
public void setNext(TextBox value)
```


Sets a [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox/) | A [TextBox](../../com.aspose.words/textbox/) that represents the next [TextBox](../../com.aspose.words/textbox/) in a sequence of shapes. |

### setNoTextRotation(boolean value) {#setNoTextRotation-boolean}
```
public void setNoTextRotation(boolean value)
```


Sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.

The default value is  false 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int}
```
public void setTextBoxWrapMode(int value)
```


Determines how text wraps inside a shape.

The default value is [TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode/\#SQUARE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextBoxWrapMode](../../com.aspose.words/textboxwrapmode/) constants. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


Specifies the vertical alignment of the text within a shape.

The default value is [TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor/\#TOP).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TextBoxAnchor](../../com.aspose.words/textboxanchor/) constants. |

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

