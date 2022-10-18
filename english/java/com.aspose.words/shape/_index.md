---
title: Shape
second_title: Aspose.Words for Java API Reference
description: Represents an object in the drawing layer such as an AutoShape textbox freeform OLE object ActiveX control or picture.
type: docs
weight: 516
url: /java/com.aspose.words/shape/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.ShapeBase](../../com.aspose.words/shapebase)
```
public class Shape extends ShapeBase
```

Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture.

To learn more, visit the **Working with Shapes** documentation article.

Using the [Shape](../../com.aspose.words/shape) class you can create or modify shapes in a Microsoft Word document.

An important property of a shape is its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--). Shapes of different types can have different capabilities in a Word document. For example, only image and OLE shapes can have images inside them. Most of the shapes can have text, but not all.

Shapes that can have text, can contain [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes as children.
## Constructors

| Constructor | Description |
| --- | --- |
| [Shape(DocumentBase doc, int shapeType)](#Shape-com.aspose.words.DocumentBase-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getHorizontalMargins_ITextBox()](#getHorizontalMargins-ITextBox--) |  |
| [getStrokeVisible()](#getStrokeVisible--) |  |
| [setStrokeVisible(boolean value)](#setStrokeVisible-boolean-) |  |
| [getStrokeTransparency()](#getStrokeTransparency--) |  |
| [setStrokeTransparency(double value)](#setStrokeTransparency-double-) |  |
| [getWeight()](#getWeight--) |  |
| [setWeight(double value)](#setWeight-double-) |  |
| [getDashStyle()](#getDashStyle--) |  |
| [setDashStyle(int value)](#setDashStyle-int-) |  |
| [getJoinStyle()](#getJoinStyle--) |  |
| [setJoinStyle(int value)](#setJoinStyle-int-) |  |
| [getEndCap()](#getEndCap--) |  |
| [setEndCap(int value)](#setEndCap-int-) |  |
| [getLineStyle()](#getLineStyle--) |  |
| [setLineStyle(int value)](#setLineStyle-int-) |  |
| [getStartArrowType()](#getStartArrowType--) |  |
| [setStartArrowType(int value)](#setStartArrowType-int-) |  |
| [getEndArrowType()](#getEndArrowType--) |  |
| [setEndArrowType(int value)](#setEndArrowType-int-) |  |
| [getStartArrowWidth()](#getStartArrowWidth--) |  |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int-) |  |
| [getStartArrowLength()](#getStartArrowLength--) |  |
| [setStartArrowLength(int value)](#setStartArrowLength-int-) |  |
| [getEndArrowWidth()](#getEndArrowWidth--) |  |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int-) |  |
| [getEndArrowLength()](#getEndArrowLength--) |  |
| [setEndArrowLength(int value)](#setEndArrowLength-int-) |  |
| [getLineFillType()](#getLineFillType--) |  |
| [setLineFillType(int value)](#setLineFillType-int-) |  |
| [getStrokeImageBytes()](#getStrokeImageBytes--) |  |
| [getNodeType()](#getNodeType--) | Returns [NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE). |
| [getStoryType()](#getStoryType--) | Returns [StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX). |
| [getExtrusionEnabled()](#getExtrusionEnabled--) | Returns true if an extrusion effect is enabled. |
| [getShadowEnabled()](#getShadowEnabled--) | Returns true if a shadow effect is enabled. |
| [getStroke()](#getStroke--) | Defines a stroke for a shape. |
| [getStroked()](#getStroked--) | Defines whether the path will be stroked. |
| [setStroked(boolean value)](#setStroked-boolean-) | Defines whether the path will be stroked. |
| [getStrokeWeight()](#getStrokeWeight--) | Defines the brush thickness that strokes the path of a shape in points. |
| [setStrokeWeight(double value)](#setStrokeWeight-double-) | Defines the brush thickness that strokes the path of a shape in points. |
| [getStrokeColor()](#getStrokeColor--) | Defines the color of a stroke. |
| [setStrokeColor(Color value)](#setStrokeColor-java.awt.Color-) | Defines the color of a stroke. |
| [getFilled()](#getFilled--) | Determines whether the closed path of the shape will be filled. |
| [setFilled(boolean value)](#setFilled-boolean-) | Determines whether the closed path of the shape will be filled. |
| [getFillColor()](#getFillColor--) | Defines the brush color that fills the closed path of the shape. |
| [setFillColor(Color value)](#setFillColor-java.awt.Color-) | Defines the brush color that fills the closed path of the shape. |
| [hasImage()](#hasImage--) | Returns true if the shape has image bytes or links an image. |
| [getImageData()](#getImageData--) | Provides access to the image of the shape. |
| [getOleFormat()](#getOleFormat--) | Provides access to the OLE data of a shape. |
| [getTextBox()](#getTextBox--) | Defines attributes that specify how text is displayed in a shape. |
| [getTextPath()](#getTextPath--) | Defines the text of the text path (of a WordArt object). |
| [getFirstParagraph()](#getFirstParagraph--) | Gets the first paragraph in the shape. |
| [getLastParagraph()](#getLastParagraph--) | Gets the last paragraph in the shape. |
| [getHorizontalRuleFormat()](#getHorizontalRuleFormat--) | Provides access to the properties of the horizontal rule shape. |
| [getSignatureLine()](#getSignatureLine--) | Gets [getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--) object if the shape is a signature line. |
| [getTextBoxWrapMode_ITextBox()](#getTextBoxWrapMode-ITextBox--) |  |
| [getTextboxLayoutFlow_ITextBox()](#getTextboxLayoutFlow-ITextBox--) |  |
| [hasVerticalTextFlow_ITextBox()](#hasVerticalTextFlow-ITextBox--) |  |
| [getMarkupLanguage_ITextBox()](#getMarkupLanguage-ITextBox--) |  |
| [hasChart()](#hasChart--) | Returns true if this Shape has a [getChart()](../../com.aspose.words/shape\#getChart--). |
| [hasSmartArt()](#hasSmartArt--) | Returns true if this Shape has a SmartArt object. |
| [updateSmartArtDrawing()](#updateSmartArtDrawing--) | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |
| [getChart()](#getChart--) | Provides access to the chart properties if this shape has a Chart. |
### Shape(DocumentBase doc, int shapeType) {#Shape-com.aspose.words.DocumentBase-int-}
```
public Shape(DocumentBase doc, int shapeType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| shapeType | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitShapeStart(com.aspose.words.Shape)](../../com.aspose.words/documentvisitor\#visitShapeStart-com.aspose.words.Shape-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of the shape and calls [DocumentVisitor.visitShapeEnd(com.aspose.words.Shape)](../../com.aspose.words/documentvisitor\#visitShapeEnd-com.aspose.words.Shape-) at the end.
### getHorizontalMargins_ITextBox() {#getHorizontalMargins-ITextBox--}
```
public float getHorizontalMargins_ITextBox()
```




**Returns:**
float
### getStrokeVisible() {#getStrokeVisible--}
```
public boolean getStrokeVisible()
```




**Returns:**
boolean
### setStrokeVisible(boolean value) {#setStrokeVisible-boolean-}
```
public void setStrokeVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getStrokeTransparency() {#getStrokeTransparency--}
```
public double getStrokeTransparency()
```




**Returns:**
double
### setStrokeTransparency(double value) {#setStrokeTransparency-double-}
```
public void setStrokeTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### getWeight() {#getWeight--}
```
public double getWeight()
```




**Returns:**
double
### setWeight(double value) {#setWeight-double-}
```
public void setWeight(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### getDashStyle() {#getDashStyle--}
```
public int getDashStyle()
```




**Returns:**
int
### setDashStyle(int value) {#setDashStyle-int-}
```
public void setDashStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getJoinStyle() {#getJoinStyle--}
```
public int getJoinStyle()
```




**Returns:**
int
### setJoinStyle(int value) {#setJoinStyle-int-}
```
public void setJoinStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getEndCap() {#getEndCap--}
```
public int getEndCap()
```




**Returns:**
int
### setEndCap(int value) {#setEndCap-int-}
```
public void setEndCap(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```




**Returns:**
int
### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getStartArrowType() {#getStartArrowType--}
```
public int getStartArrowType()
```




**Returns:**
int
### setStartArrowType(int value) {#setStartArrowType-int-}
```
public void setStartArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getEndArrowType() {#getEndArrowType--}
```
public int getEndArrowType()
```




**Returns:**
int
### setEndArrowType(int value) {#setEndArrowType-int-}
```
public void setEndArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getStartArrowWidth() {#getStartArrowWidth--}
```
public int getStartArrowWidth()
```




**Returns:**
int
### setStartArrowWidth(int value) {#setStartArrowWidth-int-}
```
public void setStartArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getStartArrowLength() {#getStartArrowLength--}
```
public int getStartArrowLength()
```




**Returns:**
int
### setStartArrowLength(int value) {#setStartArrowLength-int-}
```
public void setStartArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getEndArrowWidth() {#getEndArrowWidth--}
```
public int getEndArrowWidth()
```




**Returns:**
int
### setEndArrowWidth(int value) {#setEndArrowWidth-int-}
```
public void setEndArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getEndArrowLength() {#getEndArrowLength--}
```
public int getEndArrowLength()
```




**Returns:**
int
### setEndArrowLength(int value) {#setEndArrowLength-int-}
```
public void setEndArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getLineFillType() {#getLineFillType--}
```
public int getLineFillType()
```




**Returns:**
int
### setLineFillType(int value) {#setLineFillType-int-}
```
public void setLineFillType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getStrokeImageBytes() {#getStrokeImageBytes--}
```
public byte[] getStrokeImageBytes()
```




**Returns:**
byte[]
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE).

**Returns:**
int - \{[NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


Returns [StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX).

**Returns:**
int - \{[StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX). The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getExtrusionEnabled() {#getExtrusionEnabled--}
```
public boolean getExtrusionEnabled()
```


Returns true if an extrusion effect is enabled.

**Returns:**
boolean - True if an extrusion effect is enabled.
### getShadowEnabled() {#getShadowEnabled--}
```
public boolean getShadowEnabled()
```


Returns true if a shadow effect is enabled.

**Returns:**
boolean - True if a shadow effect is enabled.
### getStroke() {#getStroke--}
```
public Stroke getStroke()
```


Defines a stroke for a shape.

**Returns:**
[Stroke](../../com.aspose.words/stroke) - The corresponding [Stroke](../../com.aspose.words/stroke) value.
### getStroked() {#getStroked--}
```
public boolean getStroked()
```


Defines whether the path will be stroked.

This is a shortcut to the [Stroke.getOn()](../../com.aspose.words/stroke\#getOn--) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke\#setOn-boolean-) property.

The default value is **true**.

**Returns:**
boolean - The corresponding  boolean  value.
### setStroked(boolean value) {#setStroked-boolean-}
```
public void setStroked(boolean value)
```


Defines whether the path will be stroked.

This is a shortcut to the [Stroke.getOn()](../../com.aspose.words/stroke\#getOn--) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke\#setOn-boolean-) property.

The default value is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getStrokeWeight() {#getStrokeWeight--}
```
public double getStrokeWeight()
```


Defines the brush thickness that strokes the path of a shape in points.

This is a shortcut to the [Stroke.getWeight()](../../com.aspose.words/stroke\#getWeight--) / [Stroke.setWeight(double)](../../com.aspose.words/stroke\#setWeight-double-) property.

The default value is 0.75.

**Returns:**
double - The corresponding  double  value.
### setStrokeWeight(double value) {#setStrokeWeight-double-}
```
public void setStrokeWeight(double value)
```


Defines the brush thickness that strokes the path of a shape in points.

This is a shortcut to the [Stroke.getWeight()](../../com.aspose.words/stroke\#getWeight--) / [Stroke.setWeight(double)](../../com.aspose.words/stroke\#setWeight-double-) property.

The default value is 0.75.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getStrokeColor() {#getStrokeColor--}
```
public Color getStrokeColor()
```


Defines the color of a stroke.

This is a shortcut to the [Stroke.getColor()](../../com.aspose.words/stroke\#getColor--) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke\#setColor-java.awt.Color-) property.

The default value is .

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### setStrokeColor(Color value) {#setStrokeColor-java.awt.Color-}
```
public void setStrokeColor(Color value)
```


Defines the color of a stroke.

This is a shortcut to the [Stroke.getColor()](../../com.aspose.words/stroke\#getColor--) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke\#setColor-java.awt.Color-) property.

The default value is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### getFilled() {#getFilled--}
```
public boolean getFilled()
```


Determines whether the closed path of the shape will be filled.

This is a shortcut to the [Fill.getOn()](../../com.aspose.words/fill\#getOn--) / [Fill.setOn(boolean)](../../com.aspose.words/fill\#setOn-boolean-) property.

The default value is **true**.

**Returns:**
boolean - The corresponding  boolean  value.
### setFilled(boolean value) {#setFilled-boolean-}
```
public void setFilled(boolean value)
```


Determines whether the closed path of the shape will be filled.

This is a shortcut to the [Fill.getOn()](../../com.aspose.words/fill\#getOn--) / [Fill.setOn(boolean)](../../com.aspose.words/fill\#setOn-boolean-) property.

The default value is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFillColor() {#getFillColor--}
```
public Color getFillColor()
```


Defines the brush color that fills the closed path of the shape.

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-) property.

The default value is .

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### setFillColor(Color value) {#setFillColor-java.awt.Color-}
```
public void setFillColor(Color value)
```


Defines the brush color that fills the closed path of the shape.

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-) property.

The default value is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### hasImage() {#hasImage--}
```
public boolean hasImage()
```


Returns true if the shape has image bytes or links an image.

**Returns:**
boolean - True if the shape has image bytes or links an image.
### getImageData() {#getImageData--}
```
public ImageData getImageData()
```


Provides access to the image of the shape. Returns null if the shape cannot have an image.

**Returns:**
[ImageData](../../com.aspose.words/imagedata) - The corresponding [ImageData](../../com.aspose.words/imagedata) value.
### getOleFormat() {#getOleFormat--}
```
public OleFormat getOleFormat()
```


Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns null.

**Returns:**
[OleFormat](../../com.aspose.words/oleformat) - The corresponding [OleFormat](../../com.aspose.words/oleformat) value.
### getTextBox() {#getTextBox--}
```
public TextBox getTextBox()
```


Defines attributes that specify how text is displayed in a shape.

**Returns:**
[TextBox](../../com.aspose.words/textbox) - The corresponding [TextBox](../../com.aspose.words/textbox) value.
### getTextPath() {#getTextPath--}
```
public TextPath getTextPath()
```


Defines the text of the text path (of a WordArt object).

**Returns:**
[TextPath](../../com.aspose.words/textpath) - The corresponding [TextPath](../../com.aspose.words/textpath) value.
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the shape.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The first paragraph in the shape.
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the shape.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The last paragraph in the shape.
### getHorizontalRuleFormat() {#getHorizontalRuleFormat--}
```
public HorizontalRuleFormat getHorizontalRuleFormat()
```


Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns null.

**Returns:**
[HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat) - The corresponding [HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat) value.
### getSignatureLine() {#getSignatureLine--}
```
public SignatureLine getSignatureLine()
```


Gets [getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--) object if the shape is a signature line. Returns **null** otherwise. You can insert new SignatureLines into the document using [DocumentBuilder.insertSignatureLine(com.aspose.words.SignatureLineOptions)](../../com.aspose.words/documentbuilder\#insertSignatureLine-com.aspose.words.SignatureLineOptions-) and **M:Aspose.Words.DocumentBuilder.InsertSignatureLine(Aspose.Words.SignatureLineOptions,Aspose.Words.Drawing.RelativeHorizontalPosition,System.Double,Aspose.Words.Drawing.RelativeVerticalPosition,System.Double,Aspose.Words.Drawing.WrapType)**

**Returns:**
[SignatureLine](../../com.aspose.words/signatureline) - \{[getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--) object if the shape is a signature line.
### getTextBoxWrapMode_ITextBox() {#getTextBoxWrapMode-ITextBox--}
```
public int getTextBoxWrapMode_ITextBox()
```




**Returns:**
int
### getTextboxLayoutFlow_ITextBox() {#getTextboxLayoutFlow-ITextBox--}
```
public int getTextboxLayoutFlow_ITextBox()
```




**Returns:**
int
### hasVerticalTextFlow_ITextBox() {#hasVerticalTextFlow-ITextBox--}
```
public boolean hasVerticalTextFlow_ITextBox()
```




**Returns:**
boolean
### getMarkupLanguage_ITextBox() {#getMarkupLanguage-ITextBox--}
```
public byte getMarkupLanguage_ITextBox()
```




**Returns:**
byte
### hasChart() {#hasChart--}
```
public boolean hasChart()
```


Returns true if this Shape has a [getChart()](../../com.aspose.words/shape\#getChart--).

**Returns:**
boolean - True if this Shape has a [getChart()](../../com.aspose.words/shape\#getChart--).
### hasSmartArt() {#hasSmartArt--}
```
public boolean hasSmartArt()
```


Returns true if this Shape has a SmartArt object.

**Returns:**
boolean - True if this Shape has a SmartArt object.
### updateSmartArtDrawing() {#updateSmartArtDrawing--}
```
public void updateSmartArtDrawing()
```


Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. Microsoft Word generates and saves the pre-rendered drawing along with SmartArt object. However, if the document is saved by other applications, the pre-rendered SmartArt drawing may be missing or incorrect. If pre-rendered drawing is available then Aspose.Words uses it to render the SmartArt object. If pre-rendered drawing is missing then Aspose.Words uses its own SmartArt cold rendering engine to render the SmartArt object. If pre-rendered drawing is incorrect then it is required to call this method to invoke the SmartArt cold rendering engine.

### getChart() {#getChart--}
```
public Chart getChart()
```


Provides access to the chart properties if this shape has a Chart. This property will return the [getChart()](../../com.aspose.words/shape\#getChart--) object only if [hasChart()](../../com.aspose.words/shape\#hasChart--) property is true for this Shape, and will throw an exception otherwise.

**Returns:**
[Chart](../../com.aspose.words/chart) - The corresponding [Chart](../../com.aspose.words/chart) value.
