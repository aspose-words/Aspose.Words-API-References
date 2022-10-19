---
title: ShapeBase
second_title: Aspose.Words for Java API Reference
description: Base class for objects in the drawing layer such as an AutoShape freeform OLE object ActiveX control or picture.
type: docs
weight: 517
url: /java/com.aspose.words/shapebase/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class ShapeBase extends CompositeNode
```

Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture.

To learn more, visit the **Working with Shapes** documentation article.

This is an abstract class. The two derived classes that you can instantiate are [Shape](../../com.aspose.words/shape) and [GroupShape](../../com.aspose.words/groupshape).

A shape is a node in the document tree.

If the shape is a child of a [Paragraph](../../com.aspose.words/paragraph) object, then the shape is said to be "top-level". Top-level shapes are measured and positioned in points.

A shape can also occur as a child of a [GroupShape](../../com.aspose.words/groupshape) object when several shapes are grouped. Child shapes of a group shape are positioned in the coordinate space and units defined by the [getCoordSize()](../../com.aspose.words/shapebase\#getCoordSize--) / [setCoordSize(java.awt.Dimension)](../../com.aspose.words/shapebase\#setCoordSize-java.awt.Dimension-) and [getCoordOrigin()](../../com.aspose.words/shapebase\#getCoordOrigin--) / [setCoordOrigin(java.awt.Point)](../../com.aspose.words/shapebase\#setCoordOrigin-java.awt.Point-) properties of the parent group shape.

A shape can be positioned inline with text or floating. The positioning method is controlled using the [getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) property.

When a shape is floating, it is positioned relative to something (e.g the current paragraph, the margin or the page). The relative positioning of the shape is specified using the [getRelativeHorizontalPosition()](../../com.aspose.words/shapebase\#getRelativeHorizontalPosition--) / [setRelativeHorizontalPosition(int)](../../com.aspose.words/shapebase\#setRelativeHorizontalPosition-int-) and [getRelativeVerticalPosition()](../../com.aspose.words/shapebase\#getRelativeVerticalPosition--) / [setRelativeVerticalPosition(int)](../../com.aspose.words/shapebase\#setRelativeVerticalPosition-int-) properties.

A floating shape be positioned explicitly using the [getLeft()](../../com.aspose.words/shapebase\#getLeft--) / [setLeft(double)](../../com.aspose.words/shapebase\#setLeft-double-) and [getTop()](../../com.aspose.words/shapebase\#getTop--) / [setTop(double)](../../com.aspose.words/shapebase\#setTop-double-) properties or aligned relative to some other object using the [getHorizontalAlignment()](../../com.aspose.words/shapebase\#getHorizontalAlignment--) / [setHorizontalAlignment(int)](../../com.aspose.words/shapebase\#setHorizontalAlignment-int-) and [getVerticalAlignment()](../../com.aspose.words/shapebase\#getVerticalAlignment--) / [setVerticalAlignment(int)](../../com.aspose.words/shapebase\#setVerticalAlignment-int-) properties.
## Methods

| Method | Description |
| --- | --- |
| [getShapeRenderer()](#getShapeRenderer--) | Creates and returns an object that can be used to render this shape into an image. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getZOrder_IShape()](#getZOrder-IShape--) |  |
| [setZOrder_IShape(int value)](#setZOrder-IShape-int-) |  |
| [getDirectShapeAttr(int key)](#getDirectShapeAttr-int-) | Reserved for system use. |
| [fetchInheritedShapeAttr(int key)](#fetchInheritedShapeAttr-int-) | Reserved for system use. |
| [fetchShapeAttr(int key)](#fetchShapeAttr-int-) | Reserved for system use. |
| [setShapeAttr(int key, Object value)](#setShapeAttr-int-java.lang.Object-) | Reserved for system use. |
| [removeShapeAttr(int key)](#removeShapeAttr-int-) | Reserved for system use. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [solid()](#solid--) |  |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getPatternType()](#getPatternType--) |  |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [patterned(int patternType)](#patterned-int-) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [getFilledColor()](#getFilledColor--) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [getOn()](#getOn--) |  |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [getOpacity()](#getOpacity--) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [getFillType()](#getFillType--) |  |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [getGradientAngle()](#getGradientAngle--) |  |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [localToParent(Point2D.Float value)](#localToParent-java.awt.geom.Point2D.Float-) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [getFill()](#getFill--) | Gets fill formatting for the shape. |
| [getShadowFormat()](#getShadowFormat--) | Gets shadow formatting for the shape. |
| [getScreenTip()](#getScreenTip--) | Defines the text displayed when the mouse pointer moves over the shape. |
| [setScreenTip(String value)](#setScreenTip-java.lang.String-) | Defines the text displayed when the mouse pointer moves over the shape. |
| [getHRef()](#getHRef--) | Gets the full hyperlink address for a shape. |
| [setHRef(String value)](#setHRef-java.lang.String-) | Sets the full hyperlink address for a shape. |
| [getTarget()](#getTarget--) | Gets the target frame for the shape hyperlink. |
| [setTarget(String value)](#setTarget-java.lang.String-) | Sets the target frame for the shape hyperlink. |
| [getAlternativeText()](#getAlternativeText--) | Defines alternative text to be displayed instead of a graphic. |
| [setAlternativeText(String value)](#setAlternativeText-java.lang.String-) | Defines alternative text to be displayed instead of a graphic. |
| [isDecorative()](#isDecorative--) | Gets the flag that specifies whether the shape is decorative in the document. |
| [isDecorative(boolean value)](#isDecorative-boolean-) | Sets the flag that specifies whether the shape is decorative in the document. |
| [getTitle()](#getTitle--) | Gets the title (caption) of the current shape object. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Sets the title (caption) of the current shape object. |
| [getName()](#getName--) | Gets the optional shape name. |
| [setName(String value)](#setName-java.lang.String-) | Sets the optional shape name. |
| [isInsertRevision()](#isInsertRevision--) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isDeleteRevision()](#isDeleteRevision--) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision()](#isMoveFromRevision--) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision--) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [isTopLevel()](#isTopLevel--) | Returns true if this shape is not a child of a group shape. |
| [isGroup()](#isGroup--) | Returns true if this is a group shape. |
| [isImage()](#isImage--) | Returns true if this shape is an image shape. |
| [isHorizontalRule()](#isHorizontalRule--) | Returns true if this shape is a horizontal rule. |
| [isWordArt()](#isWordArt--) | Returns true if this shape is a WordArt object. |
| [canHaveImage()](#canHaveImage--) | Returns true if the shape type allows the shape to have an image. |
| [getAnchorLocked()](#getAnchorLocked--) | Specifies whether the shape's anchor is locked. |
| [setAnchorLocked(boolean value)](#setAnchorLocked-boolean-) | Specifies whether the shape's anchor is locked. |
| [getAspectRatioLocked()](#getAspectRatioLocked--) | Specifies whether the shape's aspect ratio is locked. |
| [setAspectRatioLocked(boolean value)](#setAspectRatioLocked-boolean-) | Specifies whether the shape's aspect ratio is locked. |
| [getAllowOverlap()](#getAllowOverlap--) | Gets a value that specifies whether this shape can overlap other shapes. |
| [setAllowOverlap(boolean value)](#setAllowOverlap-boolean-) | Sets a value that specifies whether this shape can overlap other shapes. |
| [getBehindText()](#getBehindText--) | Specifies whether the shape is below or above text. |
| [setBehindText(boolean value)](#setBehindText-boolean-) | Specifies whether the shape is below or above text. |
| [isInline()](#isInline--) | A quick way to determine if this shape is positioned inline with text. |
| [getLeft()](#getLeft--) | Gets the position of the left edge of the containing block of the shape. |
| [setLeft(double value)](#setLeft-double-) | Sets the position of the left edge of the containing block of the shape. |
| [getTop()](#getTop--) | Gets the position of the top edge of the containing block of the shape. |
| [setTop(double value)](#setTop-double-) | Sets the position of the top edge of the containing block of the shape. |
| [getRight()](#getRight--) | Gets the position of the right edge of the containing block of the shape. |
| [getBottom()](#getBottom--) | Gets the position of the bottom edge of the containing block of the shape. |
| [getWidth()](#getWidth--) | Gets the width of the containing block of the shape. |
| [setWidth(double value)](#setWidth-double-) | Sets the width of the containing block of the shape. |
| [getHeight()](#getHeight--) | Gets the height of the containing block of the shape. |
| [setHeight(double value)](#setHeight-double-) | Sets the height of the containing block of the shape. |
| [getDistanceTop()](#getDistanceTop--) | Gets the distance (in points) between the document text and the top edge of the shape. |
| [setDistanceTop(double value)](#setDistanceTop-double-) | Sets the distance (in points) between the document text and the top edge of the shape. |
| [getDistanceBottom()](#getDistanceBottom--) | Gets the distance (in points) between the document text and the bottom edge of the shape. |
| [setDistanceBottom(double value)](#setDistanceBottom-double-) | Sets the distance (in points) between the document text and the bottom edge of the shape. |
| [getDistanceLeft()](#getDistanceLeft--) | Gets the distance (in points) between the document text and the left edge of the shape. |
| [setDistanceLeft(double value)](#setDistanceLeft-double-) | Sets the distance (in points) between the document text and the left edge of the shape. |
| [getDistanceRight()](#getDistanceRight--) | Gets the distance (in points) between the document text and the right edge of the shape. |
| [setDistanceRight(double value)](#setDistanceRight-double-) | Sets the distance (in points) between the document text and the right edge of the shape. |
| [getRotation()](#getRotation--) | Defines the angle (in degrees) that a shape is rotated. |
| [setRotation(double value)](#setRotation-double-) | Defines the angle (in degrees) that a shape is rotated. |
| [getZOrder()](#getZOrder--) | Determines the display order of overlapping shapes. |
| [setZOrder(int value)](#setZOrder-int-) | Determines the display order of overlapping shapes. |
| [getParentParagraph()](#getParentParagraph--) | Returns the immediate parent paragraph. |
| [getBounds()](#getBounds--) | Gets the location and size of the containing block of the shape. |
| [setBounds(Rectangle2D.Float value)](#setBounds-java.awt.geom.Rectangle2D.Float-) | Sets the location and size of the containing block of the shape. |
| [getBoundsInPoints()](#getBoundsInPoints--) | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [getBoundsWithEffects()](#getBoundsWithEffects--) | Gets final extent that this shape object has after applying drawing effects. |
| [adjustWithEffects(Rectangle2D.Float source)](#adjustWithEffects-java.awt.geom.Rectangle2D.Float-) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [getShapeType()](#getShapeType--) | Gets the shape type. |
| [getMarkupLanguage()](#getMarkupLanguage--) | Gets MarkupLanguage used for this graphic object. |
| [getSizeInPoints()](#getSizeInPoints--) | Gets the size of the shape in points. |
| [getFlipOrientation()](#getFlipOrientation--) | Switches the orientation of a shape. |
| [setFlipOrientation(int value)](#setFlipOrientation-int-) | Switches the orientation of a shape. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | Specifies relative to what the shape is positioned horizontally. |
| [setRelativeHorizontalPosition(int value)](#setRelativeHorizontalPosition-int-) | Specifies relative to what the shape is positioned horizontally. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | Specifies relative to what the shape is positioned vertically. |
| [setRelativeVerticalPosition(int value)](#setRelativeVerticalPosition-int-) | Specifies relative to what the shape is positioned vertically. |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | Specifies how the shape is positioned horizontally. |
| [setHorizontalAlignment(int value)](#setHorizontalAlignment-int-) | Specifies how the shape is positioned horizontally. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Specifies how the shape is positioned vertically. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Specifies how the shape is positioned vertically. |
| [getWrapType()](#getWrapType--) | Defines whether the shape is inline or floating. |
| [setWrapType(int value)](#setWrapType-int-) | Defines whether the shape is inline or floating. |
| [getWrapSide()](#getWrapSide--) | Specifies how the text is wrapped around the shape. |
| [setWrapSide(int value)](#setWrapSide-int-) | Specifies how the text is wrapped around the shape. |
| [getCoordOrigin()](#getCoordOrigin--) | The coordinates at the top-left corner of the containing block of this shape. |
| [setCoordOrigin(Point value)](#setCoordOrigin-java.awt.Point-) | The coordinates at the top-left corner of the containing block of this shape. |
| [getCoordSize()](#getCoordSize--) | The width and height of the coordinate space inside the containing block of this shape. |
| [setCoordSize(Dimension value)](#setCoordSize-java.awt.Dimension-) | The width and height of the coordinate space inside the containing block of this shape. |
| [getFont()](#getFont--) | Provides access to the font formatting of this object. |
| [isSignatureLine()](#isSignatureLine--) | Indicates that shape is a SignatureLine. |
| [isLayoutInCell()](#isLayoutInCell--) | Gets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isLayoutInCell(boolean value)](#isLayoutInCell-boolean-) | Sets a flag indicating whether the shape is displayed inside a table or outside of it. |
### getShapeRenderer() {#getShapeRenderer--}
```
public ShapeRenderer getShapeRenderer()
```


Creates and returns an object that can be used to render this shape into an image.

This method just invokes the [ShapeRenderer](../../com.aspose.words/shaperenderer) constructor and passes this object as a parameter.

**Returns:**
[ShapeRenderer](../../com.aspose.words/shaperenderer) - The renderer object for this shape.
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph)
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getZOrder_IShape() {#getZOrder-IShape--}
```
public int getZOrder_IShape()
```




**Returns:**
int
### setZOrder_IShape(int value) {#setZOrder-IShape-int-}
```
public void setZOrder_IShape(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getDirectShapeAttr(int key) {#getDirectShapeAttr-int-}
```
public Object getDirectShapeAttr(int key)
```


Reserved for system use. IShapeAttrSource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShapeAttr(int key) {#fetchInheritedShapeAttr-int-}
```
public Object fetchInheritedShapeAttr(int key)
```


Reserved for system use. IShapeAttrSource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchShapeAttr(int key) {#fetchShapeAttr-int-}
```
public Object fetchShapeAttr(int key)
```


Reserved for system use. IShapeAttrSource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setShapeAttr(int key, Object value) {#setShapeAttr-int-java.lang.Object-}
```
public void setShapeAttr(int key, Object value)
```


Reserved for system use. IShapeAttrSource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeShapeAttr(int key) {#removeShapeAttr-int-}
```
public void removeShapeAttr(int key)
```


Reserved for system use. IShapeAttrSource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### solid() {#solid--}
```
public void solid()
```




### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**Returns:**
int
### getPatternType() {#getPatternType--}
```
public int getPatternType()
```




**Returns:**
int
### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### patterned(int patternType) {#patterned-int-}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double-}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |

### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### getOn() {#getOn--}
```
public boolean getOn()
```




**Returns:**
boolean
### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**Returns:**
double
### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**Returns:**
double
### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getFillType() {#getFillType--}
```
public int getFillType()
```




**Returns:**
int
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**Returns:**
int
### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**Returns:**
double
### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**Returns:**
int
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### localToParent(Point2D.Float value) {#localToParent-java.awt.geom.Point2D.Float-}
```
public Point2D.Float localToParent(Point2D.Float value)
```


Converts a value from the local coordinate space into the coordinate space of the parent shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.geom.Point2D.Float |  |

**Returns:**
java.awt.geom.Point2D.Float
### getFill() {#getFill--}
```
public Fill getFill()
```


Gets fill formatting for the shape.

**Returns:**
[Fill](../../com.aspose.words/fill) - Fill formatting for the shape.
### getShadowFormat() {#getShadowFormat--}
```
public ShadowFormat getShadowFormat()
```


Gets shadow formatting for the shape.

**Returns:**
[ShadowFormat](../../com.aspose.words/shadowformat) - Shadow formatting for the shape.
### getScreenTip() {#getScreenTip--}
```
public String getScreenTip()
```


Defines the text displayed when the mouse pointer moves over the shape.

The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setScreenTip(String value) {#setScreenTip-java.lang.String-}
```
public void setScreenTip(String value)
```


Defines the text displayed when the mouse pointer moves over the shape.

The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getHRef() {#getHRef--}
```
public String getHRef()
```


Gets the full hyperlink address for a shape.

The default value is an empty string.

Below are examples of valid values for this property:

Full URI:  https://www.aspose.com/ .

Full file name:  C:\\\\My Documents\\\\SalesReport.doc .

Relative URI:  ../../../resource.txt 

Relative file name:  ..\\\\My Documents\\\\SalesReport.doc .

Bookmark within another document:  https://www.aspose.com/Products/Default.aspx\#Suites 

Bookmark within this document:  \#BookmakName .

**Returns:**
java.lang.String - The full hyperlink address for a shape.
### setHRef(String value) {#setHRef-java.lang.String-}
```
public void setHRef(String value)
```


Sets the full hyperlink address for a shape.

The default value is an empty string.

Below are examples of valid values for this property:

Full URI:  https://www.aspose.com/ .

Full file name:  C:\\\\My Documents\\\\SalesReport.doc .

Relative URI:  ../../../resource.txt 

Relative file name:  ..\\\\My Documents\\\\SalesReport.doc .

Bookmark within another document:  https://www.aspose.com/Products/Default.aspx\#Suites 

Bookmark within this document:  \#BookmakName .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The full hyperlink address for a shape. |

### getTarget() {#getTarget--}
```
public String getTarget()
```


Gets the target frame for the shape hyperlink.

The default value is an empty string.

**Returns:**
java.lang.String - The target frame for the shape hyperlink.
### setTarget(String value) {#setTarget-java.lang.String-}
```
public void setTarget(String value)
```


Sets the target frame for the shape hyperlink.

The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The target frame for the shape hyperlink. |

### getAlternativeText() {#getAlternativeText--}
```
public String getAlternativeText()
```


Defines alternative text to be displayed instead of a graphic.

The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setAlternativeText(String value) {#setAlternativeText-java.lang.String-}
```
public void setAlternativeText(String value)
```


Defines alternative text to be displayed instead of a graphic.

The default value is an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### isDecorative() {#isDecorative--}
```
public boolean isDecorative()
```


Gets the flag that specifies whether the shape is decorative in the document. Note that shape having not empty [getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-) cannot be decorative.

**Returns:**
boolean - The flag that specifies whether the shape is decorative in the document.
### isDecorative(boolean value) {#isDecorative-boolean-}
```
public void isDecorative(boolean value)
```


Sets the flag that specifies whether the shape is decorative in the document. Note that shape having not empty [getAlternativeText()](../../com.aspose.words/shapebase\#getAlternativeText--) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase\#setAlternativeText-java.lang.String-) cannot be decorative.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The flag that specifies whether the shape is decorative in the document. |

### getTitle() {#getTitle--}
```
public String getTitle()
```


Gets the title (caption) of the current shape object.

Default is empty string.

Cannot be null, but can be an empty string.

**Returns:**
java.lang.String - The title (caption) of the current shape object.
### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Sets the title (caption) of the current shape object.

Default is empty string.

Cannot be null, but can be an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The title (caption) of the current shape object. |

### getName() {#getName--}
```
public String getName()
```


Gets the optional shape name.

Default is empty string.

Cannot be null, but can be an empty string.

**Returns:**
java.lang.String - The optional shape name.
### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the optional shape name.

Default is empty string.

Cannot be null, but can be an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The optional shape name. |

### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### isTopLevel() {#isTopLevel--}
```
public boolean isTopLevel()
```


Returns true if this shape is not a child of a group shape.

**Returns:**
boolean - True if this shape is not a child of a group shape.
### isGroup() {#isGroup--}
```
public boolean isGroup()
```


Returns true if this is a group shape.

**Returns:**
boolean - True if this is a group shape.
### isImage() {#isImage--}
```
public boolean isImage()
```


Returns true if this shape is an image shape.

**Returns:**
boolean - True if this shape is an image shape.
### isHorizontalRule() {#isHorizontalRule--}
```
public boolean isHorizontalRule()
```


Returns true if this shape is a horizontal rule.

**Returns:**
boolean - True if this shape is a horizontal rule.
### isWordArt() {#isWordArt--}
```
public boolean isWordArt()
```


Returns true if this shape is a WordArt object. Works till 2007 compatibility mode. In 2010 and higher compatibility mode WordArt is just a TextBox with fancy fonts.

**Returns:**
boolean - True if this shape is a WordArt object.
### canHaveImage() {#canHaveImage--}
```
public boolean canHaveImage()
```


Returns true if the shape type allows the shape to have an image.

Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape except a group shape can have an image, therefore this property returns true for all shapes except [GroupShape](../../com.aspose.words/groupshape).

**Returns:**
boolean - True if the shape type allows the shape to have an image.
### getAnchorLocked() {#getAnchorLocked--}
```
public boolean getAnchorLocked()
```


Specifies whether the shape's anchor is locked.

The default value is **false**.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word. When the anchor is not locked, moving the shape in Microsoft Word can move the shape's anchor too.

**Returns:**
boolean - The corresponding  boolean  value.
### setAnchorLocked(boolean value) {#setAnchorLocked-boolean-}
```
public void setAnchorLocked(boolean value)
```


Specifies whether the shape's anchor is locked.

The default value is **false**.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word. When the anchor is not locked, moving the shape in Microsoft Word can move the shape's anchor too.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAspectRatioLocked() {#getAspectRatioLocked--}
```
public boolean getAspectRatioLocked()
```


Specifies whether the shape's aspect ratio is locked.

The default value depends on the [getShapeType()](../../com.aspose.words/shapebase\#getShapeType--), for the ShapeType.Image it is **true** but for the other shape types it is **false**.

Has effect for top level shapes only.

**Returns:**
boolean - The corresponding  boolean  value.
### setAspectRatioLocked(boolean value) {#setAspectRatioLocked-boolean-}
```
public void setAspectRatioLocked(boolean value)
```


Specifies whether the shape's aspect ratio is locked.

The default value depends on the [getShapeType()](../../com.aspose.words/shapebase\#getShapeType--), for the ShapeType.Image it is **true** but for the other shape types it is **false**.

Has effect for top level shapes only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


Gets a value that specifies whether this shape can overlap other shapes.

This property affects behavior of the shape in Microsoft Word. Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is **true**.

**Returns:**
boolean - A value that specifies whether this shape can overlap other shapes.
### setAllowOverlap(boolean value) {#setAllowOverlap-boolean-}
```
public void setAllowOverlap(boolean value)
```


Sets a value that specifies whether this shape can overlap other shapes.

This property affects behavior of the shape in Microsoft Word. Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value that specifies whether this shape can overlap other shapes. |

### getBehindText() {#getBehindText--}
```
public boolean getBehindText()
```


Specifies whether the shape is below or above text.

Has effect only for top level shapes.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### setBehindText(boolean value) {#setBehindText-boolean-}
```
public void setBehindText(boolean value)
```


Specifies whether the shape is below or above text.

Has effect only for top level shapes.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isInline() {#isInline--}
```
public boolean isInline()
```


A quick way to determine if this shape is positioned inline with text.

Has effect only for top level shapes.

**Returns:**
boolean - The corresponding  boolean  value.
### getLeft() {#getLeft--}
```
public double getLeft()
```


Gets the position of the left edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

**Returns:**
double - The position of the left edge of the containing block of the shape.
### setLeft(double value) {#setLeft-double-}
```
public void setLeft(double value)
```


Sets the position of the left edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position of the left edge of the containing block of the shape. |

### getTop() {#getTop--}
```
public double getTop()
```


Gets the position of the top edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

**Returns:**
double - The position of the top edge of the containing block of the shape.
### setTop(double value) {#setTop-double-}
```
public void setTop(double value)
```


Sets the position of the top edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position of the top edge of the containing block of the shape. |

### getRight() {#getRight--}
```
public double getRight()
```


Gets the position of the right edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Returns:**
double - The position of the right edge of the containing block of the shape.
### getBottom() {#getBottom--}
```
public double getBottom()
```


Gets the position of the bottom edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Returns:**
double - The position of the bottom edge of the containing block of the shape.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Gets the width of the containing block of the shape.

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

**Returns:**
double - The width of the containing block of the shape.
### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


Sets the width of the containing block of the shape.

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the containing block of the shape. |

### getHeight() {#getHeight--}
```
public double getHeight()
```


Gets the height of the containing block of the shape.

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

**Returns:**
double - The height of the containing block of the shape.
### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


Sets the height of the containing block of the shape.

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The height of the containing block of the shape. |

### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


Gets the distance (in points) between the document text and the top edge of the shape.

The default value is 0.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the top edge of the shape.
### setDistanceTop(double value) {#setDistanceTop-double-}
```
public void setDistanceTop(double value)
```


Sets the distance (in points) between the document text and the top edge of the shape.

The default value is 0.

Has effect only for top level shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the top edge of the shape. |

### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


Gets the distance (in points) between the document text and the bottom edge of the shape.

The default value is 0.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the bottom edge of the shape.
### setDistanceBottom(double value) {#setDistanceBottom-double-}
```
public void setDistanceBottom(double value)
```


Sets the distance (in points) between the document text and the bottom edge of the shape.

The default value is 0.

Has effect only for top level shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the bottom edge of the shape. |

### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


Gets the distance (in points) between the document text and the left edge of the shape.

The default value is 1/8 inch.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the left edge of the shape.
### setDistanceLeft(double value) {#setDistanceLeft-double-}
```
public void setDistanceLeft(double value)
```


Sets the distance (in points) between the document text and the left edge of the shape.

The default value is 1/8 inch.

Has effect only for top level shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the left edge of the shape. |

### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


Gets the distance (in points) between the document text and the right edge of the shape.

The default value is 1/8 inch.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the right edge of the shape.
### setDistanceRight(double value) {#setDistanceRight-double-}
```
public void setDistanceRight(double value)
```


Sets the distance (in points) between the document text and the right edge of the shape.

The default value is 1/8 inch.

Has effect only for top level shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the right edge of the shape. |

### getRotation() {#getRotation--}
```
public double getRotation()
```


Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

The default value is 0.

**Returns:**
double - The corresponding  double  value.
### setRotation(double value) {#setRotation-double-}
```
public void setRotation(double value)
```


Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getZOrder() {#getZOrder--}
```
public int getZOrder()
```


Determines the display order of overlapping shapes.

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main text of the document.

The display order of child shapes in a group shape is determined by their order inside the group shape.

**Returns:**
int - The corresponding  int  value.
### setZOrder(int value) {#setZOrder-int-}
```
public void setZOrder(int value)
```


Determines the display order of overlapping shapes.

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main text of the document.

The display order of child shapes in a group shape is determined by their order inside the group shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


Returns the immediate parent paragraph. For child shapes of a group shape and child shapes of an Office Math object always returns null.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The immediate parent paragraph.
### getBounds() {#getBounds--}
```
public Rectangle2D.Float getBounds()
```


Gets the location and size of the containing block of the shape. Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Returns:**
java.awt.geom.Rectangle2D.Float - The location and size of the containing block of the shape.
### setBounds(Rectangle2D.Float value) {#setBounds-java.awt.geom.Rectangle2D.Float-}
```
public void setBounds(Rectangle2D.Float value)
```


Sets the location and size of the containing block of the shape. Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.geom.Rectangle2D.Float | The location and size of the containing block of the shape. |

### getBoundsInPoints() {#getBoundsInPoints--}
```
public Rectangle2D.Float getBoundsInPoints()
```


Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.

**Returns:**
java.awt.geom.Rectangle2D.Float - The location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.
### getBoundsWithEffects() {#getBoundsWithEffects--}
```
public Rectangle2D.Float getBoundsWithEffects()
```


Gets final extent that this shape object has after applying drawing effects. Value is measured in points.

**Returns:**
java.awt.geom.Rectangle2D.Float - Final extent that this shape object has after applying drawing effects.
### adjustWithEffects(Rectangle2D.Float source) {#adjustWithEffects-java.awt.geom.Rectangle2D.Float-}
```
public Rectangle2D.Float adjustWithEffects(Rectangle2D.Float source)
```


Adds to the source rectangle values of the effect extent and returns the final rectangle.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| source | java.awt.geom.Rectangle2D.Float |  |

**Returns:**
java.awt.geom.Rectangle2D.Float
### getShapeType() {#getShapeType--}
```
public int getShapeType()
```


Gets the shape type.

**Returns:**
int - The shape type. The returned value is one of [ShapeType](../../com.aspose.words/shapetype) constants.
### getMarkupLanguage() {#getMarkupLanguage--}
```
public byte getMarkupLanguage()
```


Gets MarkupLanguage used for this graphic object.

**Returns:**
byte - MarkupLanguage used for this graphic object. The returned value is one of [ShapeMarkupLanguage](../../com.aspose.words/shapemarkuplanguage) constants.
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


Gets the size of the shape in points.  Gets the size of the shape in points.

Point2D.Float is used as return type because we need in float dimension values here. One should to assume that Point2D's *x == width* and *y == height*.

**Returns:**
java.awt.geom.Point2D.Float - The size of the shape in points.
### getFlipOrientation() {#getFlipOrientation--}
```
public int getFlipOrientation()
```


Switches the orientation of a shape.

The default value is [FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [FlipOrientation](../../com.aspose.words/fliporientation) constants.
### setFlipOrientation(int value) {#setFlipOrientation-int-}
```
public void setFlipOrientation(int value)
```


Switches the orientation of a shape.

The default value is [FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [FlipOrientation](../../com.aspose.words/fliporientation) constants. |

### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


Specifies relative to what the shape is positioned horizontally.

The default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants.
### setRelativeHorizontalPosition(int value) {#setRelativeHorizontalPosition-int-}
```
public void setRelativeHorizontalPosition(int value)
```


Specifies relative to what the shape is positioned horizontally.

The default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

Has effect only for top level floating shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants. |

### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


Specifies relative to what the shape is positioned vertically.

The default value is [RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants.
### setRelativeVerticalPosition(int value) {#setRelativeVerticalPosition-int-}
```
public void setRelativeVerticalPosition(int value)
```


Specifies relative to what the shape is positioned vertically.

The default value is [RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

Has effect only for top level floating shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants. |

### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


Specifies how the shape is positioned horizontally.

The default value is [HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants.
### setHorizontalAlignment(int value) {#setHorizontalAlignment-int-}
```
public void setHorizontalAlignment(int value)
```


Specifies how the shape is positioned horizontally.

The default value is [HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

Has effect only for top level floating shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants. |

### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Specifies how the shape is positioned vertically.

The default value is [VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants.
### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


Specifies how the shape is positioned vertically.

The default value is [VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

Has effect only for top level floating shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants. |

### getWrapType() {#getWrapType--}
```
public int getWrapType()
```


Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.

The default value is [WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

Has effect only for top level shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [WrapType](../../com.aspose.words/wraptype) constants.
### setWrapType(int value) {#setWrapType-int-}
```
public void setWrapType(int value)
```


Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.

The default value is [WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

Has effect only for top level shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [WrapType](../../com.aspose.words/wraptype) constants. |

### getWrapSide() {#getWrapSide--}
```
public int getWrapSide()
```


Specifies how the text is wrapped around the shape.

The default value is [WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

Has effect only for top level shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [WrapSide](../../com.aspose.words/wrapside) constants.
### setWrapSide(int value) {#setWrapSide-int-}
```
public void setWrapSide(int value)
```


Specifies how the text is wrapped around the shape.

The default value is [WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

Has effect only for top level shapes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [WrapSide](../../com.aspose.words/wrapside) constants. |

### getCoordOrigin() {#getCoordOrigin--}
```
public Point getCoordOrigin()
```


The coordinates at the top-left corner of the containing block of this shape.

The default value is (0,0).

**Returns:**
java.awt.Point - The corresponding java.awt.Point value.
### setCoordOrigin(Point value) {#setCoordOrigin-java.awt.Point-}
```
public void setCoordOrigin(Point value)
```


The coordinates at the top-left corner of the containing block of this shape.

The default value is (0,0).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Point | The corresponding java.awt.Point value. |

### getCoordSize() {#getCoordSize--}
```
public Dimension getCoordSize()
```


The width and height of the coordinate space inside the containing block of this shape.

The default value is (1000, 1000).

**Returns:**
java.awt.Dimension - The corresponding java.awt.Dimension value.
### setCoordSize(Dimension value) {#setCoordSize-java.awt.Dimension-}
```
public void setCoordSize(Dimension value)
```


The width and height of the coordinate space inside the containing block of this shape.

The default value is (1000, 1000).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Dimension | The corresponding java.awt.Dimension value. |

### getFont() {#getFont--}
```
public Font getFont()
```


Provides access to the font formatting of this object.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### isSignatureLine() {#isSignatureLine--}
```
public boolean isSignatureLine()
```


Indicates that shape is a SignatureLine.

**Returns:**
boolean - The corresponding  boolean  value.
### isLayoutInCell() {#isLayoutInCell--}
```
public boolean isLayoutInCell()
```


Gets a flag indicating whether the shape is displayed inside a table or outside of it.

The default value is **true**.

Has effect only for top level shapes, the property [getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) of which is set to value other than [Inline](../../com.aspose.words/inline).

**Returns:**
boolean - A flag indicating whether the shape is displayed inside a table or outside of it.
### isLayoutInCell(boolean value) {#isLayoutInCell-boolean-}
```
public void isLayoutInCell(boolean value)
```


Sets a flag indicating whether the shape is displayed inside a table or outside of it.

The default value is **true**.

Has effect only for top level shapes, the property [getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) of which is set to value other than [Inline](../../com.aspose.words/inline).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the shape is displayed inside a table or outside of it. |

