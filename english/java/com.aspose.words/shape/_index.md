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
| [adjustWithEffects(Rectangle2D.Float source)](#adjustWithEffects-java.awt.geom.Rectangle2D.Float-) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Adds the specified node to the end of the list of child nodes for this node. |
| [canHaveImage()](#canHaveImage--) | Returns true if the shape type allows the shape to have an image. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShapeAttr(int key)](#fetchInheritedShapeAttr-int-) | Reserved for system use. |
| [fetchShapeAttr(int key)](#fetchShapeAttr-int-) | Reserved for system use. |
| [getAllowOverlap()](#getAllowOverlap--) | Gets a value that specifies whether this shape can overlap other shapes. |
| [getAlternativeText()](#getAlternativeText--) | Defines alternative text to be displayed instead of a graphic. |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Gets the first ancestor of the specified object type. |
| [getAnchorLocked()](#getAnchorLocked--) | Specifies whether the shape's anchor is locked. |
| [getAspectRatioLocked()](#getAspectRatioLocked--) | Specifies whether the shape's aspect ratio is locked. |
| [getBehindText()](#getBehindText--) | Specifies whether the shape is below or above text. |
| [getBottom()](#getBottom--) | Gets the position of the bottom edge of the containing block of the shape. |
| [getBounds()](#getBounds--) | Gets the location and size of the containing block of the shape. |
| [getBoundsInPoints()](#getBoundsInPoints--) | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [getBoundsWithEffects()](#getBoundsWithEffects--) | Gets final extent that this shape object has after applying drawing effects. |
| [getChart()](#getChart--) | Provides access to the chart properties if this shape has a Chart. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCoordOrigin()](#getCoordOrigin--) | The coordinates at the top-left corner of the containing block of this shape. |
| [getCoordSize()](#getCoordSize--) | The width and height of the coordinate space inside the containing block of this shape. |
| [getCount()](#getCount--) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Specifies custom node identifier. |
| [getDashStyle()](#getDashStyle--) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDirectShapeAttr(int key)](#getDirectShapeAttr-int-) | Reserved for system use. |
| [getDistanceBottom()](#getDistanceBottom--) | Gets the distance (in points) between the document text and the bottom edge of the shape. |
| [getDistanceLeft()](#getDistanceLeft--) | Gets the distance (in points) between the document text and the left edge of the shape. |
| [getDistanceRight()](#getDistanceRight--) | Gets the distance (in points) between the document text and the right edge of the shape. |
| [getDistanceTop()](#getDistanceTop--) | Gets the distance (in points) between the document text and the top edge of the shape. |
| [getDocument()](#getDocument--) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getEndArrowLength()](#getEndArrowLength--) |  |
| [getEndArrowType()](#getEndArrowType--) |  |
| [getEndArrowWidth()](#getEndArrowWidth--) |  |
| [getEndCap()](#getEndCap--) |  |
| [getExtrusionEnabled()](#getExtrusionEnabled--) | Returns true if an extrusion effect is enabled. |
| [getFill()](#getFill--) | Gets fill formatting for the shape. |
| [getFillColor()](#getFillColor--) | Defines the brush color that fills the closed path of the shape. |
| [getFillType()](#getFillType--) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [getFilled()](#getFilled--) | Determines whether the closed path of the shape will be filled. |
| [getFilledColor()](#getFilledColor--) |  |
| [getFirstChild()](#getFirstChild--) | Gets the first child of the node. |
| [getFirstParagraph()](#getFirstParagraph--) | Gets the first paragraph in the shape. |
| [getFlipOrientation()](#getFlipOrientation--) | Switches the orientation of a shape. |
| [getFont()](#getFont--) | Provides access to the font formatting of this object. |
| [getGradientAngle()](#getGradientAngle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getHRef()](#getHRef--) | Gets the full hyperlink address for a shape. |
| [getHeight()](#getHeight--) | Gets the height of the containing block of the shape. |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | Specifies how the shape is positioned horizontally. |
| [getHorizontalMargins_ITextBox()](#getHorizontalMargins-ITextBox--) |  |
| [getHorizontalRuleFormat()](#getHorizontalRuleFormat--) | Provides access to the properties of the horizontal rule shape. |
| [getImageData()](#getImageData--) | Provides access to the image of the shape. |
| [getJoinStyle()](#getJoinStyle--) |  |
| [getLastChild()](#getLastChild--) | Gets the last child of the node. |
| [getLastParagraph()](#getLastParagraph--) | Gets the last paragraph in the shape. |
| [getLeft()](#getLeft--) | Gets the position of the left edge of the containing block of the shape. |
| [getLineFillType()](#getLineFillType--) |  |
| [getLineStyle()](#getLineStyle--) |  |
| [getMarkupLanguage()](#getMarkupLanguage--) | Gets MarkupLanguage used for this graphic object. |
| [getMarkupLanguage_ITextBox()](#getMarkupLanguage-ITextBox--) |  |
| [getName()](#getName--) | Gets the optional shape name. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType--) | Returns [NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE). |
| [getOleFormat()](#getOleFormat--) | Provides access to the OLE data of a shape. |
| [getOn()](#getOn--) |  |
| [getOpacity()](#getOpacity--) |  |
| [getParentNode()](#getParentNode--) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph--) | Returns the immediate parent paragraph. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPatternType()](#getPatternType--) |  |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Gets the node immediately preceding this node. |
| [getRange()](#getRange--) | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | Specifies relative to what the shape is positioned horizontally. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | Specifies relative to what the shape is positioned vertically. |
| [getRight()](#getRight--) | Gets the position of the right edge of the containing block of the shape. |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [getRotation()](#getRotation--) | Defines the angle (in degrees) that a shape is rotated. |
| [getScreenTip()](#getScreenTip--) | Defines the text displayed when the mouse pointer moves over the shape. |
| [getShadowEnabled()](#getShadowEnabled--) | Returns true if a shadow effect is enabled. |
| [getShadowFormat()](#getShadowFormat--) | Gets shadow formatting for the shape. |
| [getShapeRenderer()](#getShapeRenderer--) | Creates and returns an object that can be used to render this shape into an image. |
| [getShapeType()](#getShapeType--) | Gets the shape type. |
| [getSignatureLine()](#getSignatureLine--) | Gets [getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--) object if the shape is a signature line. |
| [getSizeInPoints()](#getSizeInPoints--) | Gets the size of the shape in points. |
| [getStartArrowLength()](#getStartArrowLength--) |  |
| [getStartArrowType()](#getStartArrowType--) |  |
| [getStartArrowWidth()](#getStartArrowWidth--) |  |
| [getStoryType()](#getStoryType--) | Returns [StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX). |
| [getStroke()](#getStroke--) | Defines a stroke for a shape. |
| [getStrokeColor()](#getStrokeColor--) | Defines the color of a stroke. |
| [getStrokeImageBytes()](#getStrokeImageBytes--) |  |
| [getStrokeTransparency()](#getStrokeTransparency--) |  |
| [getStrokeVisible()](#getStrokeVisible--) |  |
| [getStrokeWeight()](#getStrokeWeight--) | Defines the brush thickness that strokes the path of a shape in points. |
| [getStroked()](#getStroked--) | Defines whether the path will be stroked. |
| [getTarget()](#getTarget--) | Gets the target frame for the shape hyperlink. |
| [getText()](#getText--) | Gets the text of this node and of all its children. |
| [getTextBox()](#getTextBox--) | Defines attributes that specify how text is displayed in a shape. |
| [getTextBoxWrapMode_ITextBox()](#getTextBoxWrapMode-ITextBox--) |  |
| [getTextPath()](#getTextPath--) | Defines the text of the text path (of a WordArt object). |
| [getTextboxLayoutFlow_ITextBox()](#getTextboxLayoutFlow-ITextBox--) |  |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [getTitle()](#getTitle--) | Gets the title (caption) of the current shape object. |
| [getTop()](#getTop--) | Gets the position of the top edge of the containing block of the shape. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Specifies how the shape is positioned vertically. |
| [getWeight()](#getWeight--) |  |
| [getWidth()](#getWidth--) | Gets the width of the containing block of the shape. |
| [getWrapSide()](#getWrapSide--) | Specifies how the text is wrapped around the shape. |
| [getWrapType()](#getWrapType--) | Defines whether the shape is inline or floating. |
| [getZOrder()](#getZOrder--) | Determines the display order of overlapping shapes. |
| [getZOrder_IShape()](#getZOrder-IShape--) |  |
| [hasChart()](#hasChart--) | Returns true if this Shape has a [getChart()](../../com.aspose.words/shape\#getChart--). |
| [hasChildNodes()](#hasChildNodes--) | Returns true if this node has any child nodes. |
| [hasImage()](#hasImage--) | Returns true if the shape has image bytes or links an image. |
| [hasSmartArt()](#hasSmartArt--) | Returns true if this Shape has a SmartArt object. |
| [hasVerticalTextFlow_ITextBox()](#hasVerticalTextFlow-ITextBox--) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite--) | Returns true as this node can have child nodes. |
| [isDecorative()](#isDecorative--) | Gets the flag that specifies whether the shape is decorative in the document. |
| [isDecorative(boolean value)](#isDecorative-boolean-) | Sets the flag that specifies whether the shape is decorative in the document. |
| [isDeleteRevision()](#isDeleteRevision--) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isGroup()](#isGroup--) | Returns true if this is a group shape. |
| [isHorizontalRule()](#isHorizontalRule--) | Returns true if this shape is a horizontal rule. |
| [isImage()](#isImage--) | Returns true if this shape is an image shape. |
| [isInline()](#isInline--) | A quick way to determine if this shape is positioned inline with text. |
| [isInsertRevision()](#isInsertRevision--) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isLayoutInCell()](#isLayoutInCell--) | Gets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isLayoutInCell(boolean value)](#isLayoutInCell-boolean-) | Sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isMoveFromRevision()](#isMoveFromRevision--) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision--) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [isSignatureLine()](#isSignatureLine--) | Indicates that shape is a SignatureLine. |
| [isTopLevel()](#isTopLevel--) | Returns true if this shape is not a child of a group shape. |
| [isWordArt()](#isWordArt--) | Returns true if this shape is a WordArt object. |
| [iterator()](#iterator--) | Provides support for the for each style iteration over the child nodes of this node. |
| [localToParent(Point2D.Float value)](#localToParent-java.awt.geom.Point2D.Float-) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [patterned(int patternType)](#patterned-int-) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove--) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren--) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Removes the specified child node. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeShapeAttr(int key)](#removeShapeAttr-int-) | Reserved for system use. |
| [removeSmartTags()](#removeSmartTags--) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Selects the first Node that matches the XPath expression. |
| [setAllowOverlap(boolean value)](#setAllowOverlap-boolean-) | Sets a value that specifies whether this shape can overlap other shapes. |
| [setAlternativeText(String value)](#setAlternativeText-java.lang.String-) | Defines alternative text to be displayed instead of a graphic. |
| [setAnchorLocked(boolean value)](#setAnchorLocked-boolean-) | Specifies whether the shape's anchor is locked. |
| [setAspectRatioLocked(boolean value)](#setAspectRatioLocked-boolean-) | Specifies whether the shape's aspect ratio is locked. |
| [setBehindText(boolean value)](#setBehindText-boolean-) | Specifies whether the shape is below or above text. |
| [setBounds(Rectangle2D.Float value)](#setBounds-java.awt.geom.Rectangle2D.Float-) | Sets the location and size of the containing block of the shape. |
| [setCoordOrigin(Point value)](#setCoordOrigin-java.awt.Point-) | The coordinates at the top-left corner of the containing block of this shape. |
| [setCoordSize(Dimension value)](#setCoordSize-java.awt.Dimension-) | The width and height of the coordinate space inside the containing block of this shape. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Specifies custom node identifier. |
| [setDashStyle(int value)](#setDashStyle-int-) |  |
| [setDistanceBottom(double value)](#setDistanceBottom-double-) | Sets the distance (in points) between the document text and the bottom edge of the shape. |
| [setDistanceLeft(double value)](#setDistanceLeft-double-) | Sets the distance (in points) between the document text and the left edge of the shape. |
| [setDistanceRight(double value)](#setDistanceRight-double-) | Sets the distance (in points) between the document text and the right edge of the shape. |
| [setDistanceTop(double value)](#setDistanceTop-double-) | Sets the distance (in points) between the document text and the top edge of the shape. |
| [setEndArrowLength(int value)](#setEndArrowLength-int-) |  |
| [setEndArrowType(int value)](#setEndArrowType-int-) |  |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int-) |  |
| [setEndCap(int value)](#setEndCap-int-) |  |
| [setFillColor(Color value)](#setFillColor-java.awt.Color-) | Defines the brush color that fills the closed path of the shape. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [setFilled(boolean value)](#setFilled-boolean-) | Determines whether the closed path of the shape will be filled. |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [setFlipOrientation(int value)](#setFlipOrientation-int-) | Switches the orientation of a shape. |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [setHRef(String value)](#setHRef-java.lang.String-) | Sets the full hyperlink address for a shape. |
| [setHeight(double value)](#setHeight-double-) | Sets the height of the containing block of the shape. |
| [setHorizontalAlignment(int value)](#setHorizontalAlignment-int-) | Specifies how the shape is positioned horizontally. |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [setJoinStyle(int value)](#setJoinStyle-int-) |  |
| [setLeft(double value)](#setLeft-double-) | Sets the position of the left edge of the containing block of the shape. |
| [setLineFillType(int value)](#setLineFillType-int-) |  |
| [setLineStyle(int value)](#setLineStyle-int-) |  |
| [setName(String value)](#setName-java.lang.String-) | Sets the optional shape name. |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [setRelativeHorizontalPosition(int value)](#setRelativeHorizontalPosition-int-) | Specifies relative to what the shape is positioned horizontally. |
| [setRelativeVerticalPosition(int value)](#setRelativeVerticalPosition-int-) | Specifies relative to what the shape is positioned vertically. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [setRotation(double value)](#setRotation-double-) | Defines the angle (in degrees) that a shape is rotated. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setScreenTip(String value)](#setScreenTip-java.lang.String-) | Defines the text displayed when the mouse pointer moves over the shape. |
| [setShapeAttr(int key, Object value)](#setShapeAttr-int-java.lang.Object-) | Reserved for system use. |
| [setStartArrowLength(int value)](#setStartArrowLength-int-) |  |
| [setStartArrowType(int value)](#setStartArrowType-int-) |  |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int-) |  |
| [setStrokeColor(Color value)](#setStrokeColor-java.awt.Color-) | Defines the color of a stroke. |
| [setStrokeTransparency(double value)](#setStrokeTransparency-double-) |  |
| [setStrokeVisible(boolean value)](#setStrokeVisible-boolean-) |  |
| [setStrokeWeight(double value)](#setStrokeWeight-double-) | Defines the brush thickness that strokes the path of a shape in points. |
| [setStroked(boolean value)](#setStroked-boolean-) | Defines whether the path will be stroked. |
| [setTarget(String value)](#setTarget-java.lang.String-) | Sets the target frame for the shape hyperlink. |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [setTitle(String value)](#setTitle-java.lang.String-) | Sets the title (caption) of the current shape object. |
| [setTop(double value)](#setTop-double-) | Sets the position of the top edge of the containing block of the shape. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Specifies how the shape is positioned vertically. |
| [setWeight(double value)](#setWeight-double-) |  |
| [setWidth(double value)](#setWidth-double-) | Sets the width of the containing block of the shape. |
| [setWrapSide(int value)](#setWrapSide-int-) | Specifies how the text is wrapped around the shape. |
| [setWrapType(int value)](#setWrapType-int-) | Defines whether the shape is inline or floating. |
| [setZOrder(int value)](#setZOrder-int-) | Determines the display order of overlapping shapes. |
| [setZOrder_IShape(int value)](#setZOrder-IShape-int-) |  |
| [solid()](#solid--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int-) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [updateSmartArtDrawing()](#updateSmartArtDrawing--) | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
### canHaveImage() {#canHaveImage--}
```
public boolean canHaveImage()
```


Returns true if the shape type allows the shape to have an image.

Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape except a group shape can have an image, therefore this property returns true for all shapes except [GroupShape](../../com.aspose.words/groupshape).

**Returns:**
boolean - True if the shape type allows the shape to have an image.
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node.
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getAlternativeText() {#getAlternativeText--}
```
public String getAlternativeText()
```


Defines alternative text to be displayed instead of a graphic.

The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or null if no ancestor of this type was found.

The ancestor type matches if it is equal to ancestorType or derived from ancestorType.
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
### getAspectRatioLocked() {#getAspectRatioLocked--}
```
public boolean getAspectRatioLocked()
```


Specifies whether the shape's aspect ratio is locked.

The default value depends on the [getShapeType()](../../com.aspose.words/shapebase\#getShapeType--), for the ShapeType.Image it is **true** but for the other shape types it is **false**.

Has effect for top level shapes only.

**Returns:**
boolean - The corresponding  boolean  value.
### getBehindText() {#getBehindText--}
```
public boolean getBehindText()
```


Specifies whether the shape is below or above text.

Has effect only for top level shapes.

The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### getBottom() {#getBottom--}
```
public double getBottom()
```


Gets the position of the bottom edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Returns:**
double - The position of the bottom edge of the containing block of the shape.
### getBounds() {#getBounds--}
```
public Rectangle2D.Float getBounds()
```


Gets the location and size of the containing block of the shape. Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Returns:**
java.awt.geom.Rectangle2D.Float - The location and size of the containing block of the shape.
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
### getChart() {#getChart--}
```
public Chart getChart()
```


Provides access to the chart properties if this shape has a Chart. This property will return the [getChart()](../../com.aspose.words/shape\#getChart--) object only if [hasChart()](../../com.aspose.words/shape\#hasChart--) property is true for this Shape, and will throw an exception otherwise.

**Returns:**
[Chart](../../com.aspose.words/chart) - The corresponding [Chart](../../com.aspose.words/chart) value.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) is equivalent to calling  GetChildNodes(NodeType.Any, false)  and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All immediate child nodes of this node.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCoordOrigin() {#getCoordOrigin--}
```
public Point getCoordOrigin()
```


The coordinates at the top-left corner of the containing block of this shape.

The default value is (0,0).

**Returns:**
java.awt.Point - The corresponding java.awt.Point value.
### getCoordSize() {#getCoordSize--}
```
public Dimension getCoordSize()
```


The width and height of the coordinate space inside the containing block of this shape.

The default value is (1000, 1000).

**Returns:**
java.awt.Dimension - The corresponding java.awt.Dimension value.
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of immediate children of this node.

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getDashStyle() {#getDashStyle--}
```
public int getDashStyle()
```




**Returns:**
int
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
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


Gets the distance (in points) between the document text and the bottom edge of the shape.

The default value is 0.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the bottom edge of the shape.
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


Gets the distance (in points) between the document text and the left edge of the shape.

The default value is 1/8 inch.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the left edge of the shape.
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


Gets the distance (in points) between the document text and the right edge of the shape.

The default value is 1/8 inch.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the right edge of the shape.
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


Gets the distance (in points) between the document text and the top edge of the shape.

The default value is 0.

Has effect only for top level shapes.

**Returns:**
double - The distance (in points) between the document text and the top edge of the shape.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getEndArrowLength() {#getEndArrowLength--}
```
public int getEndArrowLength()
```




**Returns:**
int
### getEndArrowType() {#getEndArrowType--}
```
public int getEndArrowType()
```




**Returns:**
int
### getEndArrowWidth() {#getEndArrowWidth--}
```
public int getEndArrowWidth()
```




**Returns:**
int
### getEndCap() {#getEndCap--}
```
public int getEndCap()
```




**Returns:**
int
### getExtrusionEnabled() {#getExtrusionEnabled--}
```
public boolean getExtrusionEnabled()
```


Returns true if an extrusion effect is enabled.

**Returns:**
boolean - True if an extrusion effect is enabled.
### getFill() {#getFill--}
```
public Fill getFill()
```


Gets fill formatting for the shape.

**Returns:**
[Fill](../../com.aspose.words/fill) - Fill formatting for the shape.
### getFillColor() {#getFillColor--}
```
public Color getFillColor()
```


Defines the brush color that fills the closed path of the shape.

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-) property.

The default value is .

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getFillType() {#getFillType--}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilled() {#getFilled--}
```
public boolean getFilled()
```


Determines whether the closed path of the shape will be filled.

This is a shortcut to the [Fill.getOn()](../../com.aspose.words/fill\#getOn--) / [Fill.setOn(boolean)](../../com.aspose.words/fill\#setOn-boolean-) property.

The default value is **true**.

**Returns:**
boolean - The corresponding  boolean  value.
### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the shape.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The first paragraph in the shape.
### getFlipOrientation() {#getFlipOrientation--}
```
public int getFlipOrientation()
```


Switches the orientation of a shape.

The default value is [FlipOrientation.NONE](../../com.aspose.words/fliporientation\#NONE).

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [FlipOrientation](../../com.aspose.words/fliporientation) constants.
### getFont() {#getFont--}
```
public Font getFont()
```


Provides access to the font formatting of this object.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**Returns:**
int
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
### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


Specifies how the shape is positioned horizontally.

The default value is [HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment\#NONE).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants.
### getHorizontalMargins_ITextBox() {#getHorizontalMargins-ITextBox--}
```
public float getHorizontalMargins_ITextBox()
```




**Returns:**
float
### getHorizontalRuleFormat() {#getHorizontalRuleFormat--}
```
public HorizontalRuleFormat getHorizontalRuleFormat()
```


Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns null.

**Returns:**
[HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat) - The corresponding [HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat) value.
### getImageData() {#getImageData--}
```
public ImageData getImageData()
```


Provides access to the image of the shape. Returns null if the shape cannot have an image.

**Returns:**
[ImageData](../../com.aspose.words/imagedata) - The corresponding [ImageData](../../com.aspose.words/imagedata) value.
### getJoinStyle() {#getJoinStyle--}
```
public int getJoinStyle()
```




**Returns:**
int
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the shape.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The last paragraph in the shape.
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
### getLineFillType() {#getLineFillType--}
```
public int getLineFillType()
```




**Returns:**
int
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```




**Returns:**
int
### getMarkupLanguage() {#getMarkupLanguage--}
```
public byte getMarkupLanguage()
```


Gets MarkupLanguage used for this graphic object.

**Returns:**
byte - MarkupLanguage used for this graphic object. The returned value is one of [ShapeMarkupLanguage](../../com.aspose.words/shapemarkuplanguage) constants.
### getMarkupLanguage_ITextBox() {#getMarkupLanguage-ITextBox--}
```
public byte getMarkupLanguage_ITextBox()
```




**Returns:**
byte
### getName() {#getName--}
```
public String getName()
```


Gets the optional shape name.

Default is empty string.

Cannot be null, but can be an empty string.

**Returns:**
java.lang.String - The optional shape name.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE).

**Returns:**
int - \{[NodeType.SHAPE](../../com.aspose.words/nodetype\#SHAPE). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getOleFormat() {#getOleFormat--}
```
public OleFormat getOleFormat()
```


Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns null.

**Returns:**
[OleFormat](../../com.aspose.words/oleformat) - The corresponding [OleFormat](../../com.aspose.words/oleformat) value.
### getOn() {#getOn--}
```
public boolean getOn()
```




**Returns:**
boolean
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**Returns:**
double
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


Returns the immediate parent paragraph. For child shapes of a group shape and child shapes of an Office Math object always returns null.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The immediate parent paragraph.
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph)
### getPatternType() {#getPatternType--}
```
public int getPatternType()
```




**Returns:**
int
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**Returns:**
int
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getRange() {#getRange--}
```
public Range getRange()
```


Returns a **Range** object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range) - A **Range** object that represents the portion of a document that is contained in this node.
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


Specifies relative to what the shape is positioned horizontally.

The default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants.
### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


Specifies relative to what the shape is positioned vertically.

The default value is [RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition\#PARAGRAPH).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants.
### getRight() {#getRight--}
```
public double getRight()
```


Gets the position of the right edge of the containing block of the shape.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

**Returns:**
double - The position of the right edge of the containing block of the shape.
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getRotation() {#getRotation--}
```
public double getRotation()
```


Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

The default value is 0.

**Returns:**
double - The corresponding  double  value.
### getScreenTip() {#getScreenTip--}
```
public String getScreenTip()
```


Defines the text displayed when the mouse pointer moves over the shape.

The default value is an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getShadowEnabled() {#getShadowEnabled--}
```
public boolean getShadowEnabled()
```


Returns true if a shadow effect is enabled.

**Returns:**
boolean - True if a shadow effect is enabled.
### getShadowFormat() {#getShadowFormat--}
```
public ShadowFormat getShadowFormat()
```


Gets shadow formatting for the shape.

**Returns:**
[ShadowFormat](../../com.aspose.words/shadowformat) - Shadow formatting for the shape.
### getShapeRenderer() {#getShapeRenderer--}
```
public ShapeRenderer getShapeRenderer()
```


Creates and returns an object that can be used to render this shape into an image.

This method just invokes the [ShapeRenderer](../../com.aspose.words/shaperenderer) constructor and passes this object as a parameter.

**Returns:**
[ShapeRenderer](../../com.aspose.words/shaperenderer) - The renderer object for this shape.
### getShapeType() {#getShapeType--}
```
public int getShapeType()
```


Gets the shape type.

**Returns:**
int - The shape type. The returned value is one of [ShapeType](../../com.aspose.words/shapetype) constants.
### getSignatureLine() {#getSignatureLine--}
```
public SignatureLine getSignatureLine()
```


Gets [getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--) object if the shape is a signature line. Returns **null** otherwise. You can insert new SignatureLines into the document using [DocumentBuilder.insertSignatureLine(com.aspose.words.SignatureLineOptions)](../../com.aspose.words/documentbuilder\#insertSignatureLine-com.aspose.words.SignatureLineOptions-) and **M:Aspose.Words.DocumentBuilder.InsertSignatureLine(Aspose.Words.SignatureLineOptions,Aspose.Words.Drawing.RelativeHorizontalPosition,System.Double,Aspose.Words.Drawing.RelativeVerticalPosition,System.Double,Aspose.Words.Drawing.WrapType)**

**Returns:**
[SignatureLine](../../com.aspose.words/signatureline) - \{[getSignatureLine()](../../com.aspose.words/shape\#getSignatureLine--) object if the shape is a signature line.
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


Gets the size of the shape in points.  Gets the size of the shape in points.

Point2D.Float is used as return type because we need in float dimension values here. One should to assume that Point2D's *x == width* and *y == height*.

**Returns:**
java.awt.geom.Point2D.Float - The size of the shape in points.
### getStartArrowLength() {#getStartArrowLength--}
```
public int getStartArrowLength()
```




**Returns:**
int
### getStartArrowType() {#getStartArrowType--}
```
public int getStartArrowType()
```




**Returns:**
int
### getStartArrowWidth() {#getStartArrowWidth--}
```
public int getStartArrowWidth()
```




**Returns:**
int
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


Returns [StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX).

**Returns:**
int - \{[StoryType.TEXTBOX](../../com.aspose.words/storytype\#TEXTBOX). The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getStroke() {#getStroke--}
```
public Stroke getStroke()
```


Defines a stroke for a shape.

**Returns:**
[Stroke](../../com.aspose.words/stroke) - The corresponding [Stroke](../../com.aspose.words/stroke) value.
### getStrokeColor() {#getStrokeColor--}
```
public Color getStrokeColor()
```


Defines the color of a stroke.

This is a shortcut to the [Stroke.getColor()](../../com.aspose.words/stroke\#getColor--) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke\#setColor-java.awt.Color-) property.

The default value is .

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getStrokeImageBytes() {#getStrokeImageBytes--}
```
public byte[] getStrokeImageBytes()
```




**Returns:**
byte[]
### getStrokeTransparency() {#getStrokeTransparency--}
```
public double getStrokeTransparency()
```




**Returns:**
double
### getStrokeVisible() {#getStrokeVisible--}
```
public boolean getStrokeVisible()
```




**Returns:**
boolean
### getStrokeWeight() {#getStrokeWeight--}
```
public double getStrokeWeight()
```


Defines the brush thickness that strokes the path of a shape in points.

This is a shortcut to the [Stroke.getWeight()](../../com.aspose.words/stroke\#getWeight--) / [Stroke.setWeight(double)](../../com.aspose.words/stroke\#setWeight-double-) property.

The default value is 0.75.

**Returns:**
double - The corresponding  double  value.
### getStroked() {#getStroked--}
```
public boolean getStroked()
```


Defines whether the path will be stroked.

This is a shortcut to the [Stroke.getOn()](../../com.aspose.words/stroke\#getOn--) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke\#setOn-boolean-) property.

The default value is **true**.

**Returns:**
boolean - The corresponding  boolean  value.
### getTarget() {#getTarget--}
```
public String getTarget()
```


Gets the target frame for the shape hyperlink.

The default value is an empty string.

**Returns:**
java.lang.String - The target frame for the shape hyperlink.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getTextBox() {#getTextBox--}
```
public TextBox getTextBox()
```


Defines attributes that specify how text is displayed in a shape.

**Returns:**
[TextBox](../../com.aspose.words/textbox) - The corresponding [TextBox](../../com.aspose.words/textbox) value.
### getTextBoxWrapMode_ITextBox() {#getTextBoxWrapMode-ITextBox--}
```
public int getTextBoxWrapMode_ITextBox()
```




**Returns:**
int
### getTextPath() {#getTextPath--}
```
public TextPath getTextPath()
```


Defines the text of the text path (of a WordArt object).

**Returns:**
[TextPath](../../com.aspose.words/textpath) - The corresponding [TextPath](../../com.aspose.words/textpath) value.
### getTextboxLayoutFlow_ITextBox() {#getTextboxLayoutFlow-ITextBox--}
```
public int getTextboxLayoutFlow_ITextBox()
```




**Returns:**
int
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**Returns:**
int
### getTitle() {#getTitle--}
```
public String getTitle()
```


Gets the title (caption) of the current shape object.

Default is empty string.

Cannot be null, but can be an empty string.

**Returns:**
java.lang.String - The title (caption) of the current shape object.
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
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Specifies how the shape is positioned vertically.

The default value is [VerticalAlignment.NONE](../../com.aspose.words/verticalalignment\#NONE).

Has effect only for top level floating shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants.
### getWeight() {#getWeight--}
```
public double getWeight()
```




**Returns:**
double
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
### getWrapSide() {#getWrapSide--}
```
public int getWrapSide()
```


Specifies how the text is wrapped around the shape.

The default value is [WrapSide.BOTH](../../com.aspose.words/wrapside\#BOTH).

Has effect only for top level shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [WrapSide](../../com.aspose.words/wrapside) constants.
### getWrapType() {#getWrapType--}
```
public int getWrapType()
```


Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.

The default value is [WrapType.NONE](../../com.aspose.words/wraptype\#NONE).

Has effect only for top level shapes.

**Returns:**
int - The corresponding  int  value. The returned value is one of [WrapType](../../com.aspose.words/wraptype) constants.
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
### getZOrder_IShape() {#getZOrder-IShape--}
```
public int getZOrder_IShape()
```




**Returns:**
int
### hasChart() {#hasChart--}
```
public boolean hasChart()
```


Returns true if this Shape has a [getChart()](../../com.aspose.words/shape\#getChart--).

**Returns:**
boolean - True if this Shape has a [getChart()](../../com.aspose.words/shape\#getChart--).
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


Returns true if this node has any child nodes.

**Returns:**
boolean - True if this node has any child nodes.
### hasImage() {#hasImage--}
```
public boolean hasImage()
```


Returns true if the shape has image bytes or links an image.

**Returns:**
boolean - True if the shape has image bytes or links an image.
### hasSmartArt() {#hasSmartArt--}
```
public boolean hasSmartArt()
```


Returns true if this Shape has a SmartArt object.

**Returns:**
boolean - True if this Shape has a SmartArt object.
### hasVerticalTextFlow_ITextBox() {#hasVerticalTextFlow-ITextBox--}
```
public boolean hasVerticalTextFlow_ITextBox()
```




**Returns:**
boolean
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array. Returns -1 if the node is not found in the child nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

If refChild is null, inserts newChild at the beginning of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newNode is placed after the refNode. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

If refChild is null, inserts newChild at the end of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newChild is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Returns true as this node can have child nodes.

**Returns:**
boolean - True as this node can have child nodes.
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

### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isGroup() {#isGroup--}
```
public boolean isGroup()
```


Returns true if this is a group shape.

**Returns:**
boolean - True if this is a group shape.
### isHorizontalRule() {#isHorizontalRule--}
```
public boolean isHorizontalRule()
```


Returns true if this shape is a horizontal rule.

**Returns:**
boolean - True if this shape is a horizontal rule.
### isImage() {#isImage--}
```
public boolean isImage()
```


Returns true if this shape is an image shape.

**Returns:**
boolean - True if this shape is an image shape.
### isInline() {#isInline--}
```
public boolean isInline()
```


A quick way to determine if this shape is positioned inline with text.

Has effect only for top level shapes.

**Returns:**
boolean - The corresponding  boolean  value.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
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
### isSignatureLine() {#isSignatureLine--}
```
public boolean isSignatureLine()
```


Indicates that shape is a SignatureLine.

**Returns:**
boolean - The corresponding  boolean  value.
### isTopLevel() {#isTopLevel--}
```
public boolean isTopLevel()
```


Returns true if this shape is not a child of a group shape.

**Returns:**
boolean - True if this shape is not a child of a group shape.
### isWordArt() {#isWordArt--}
```
public boolean isWordArt()
```


Returns true if this shape is a WordArt object. Works till 2007 compatibility mode. In 2010 and higher compatibility mode WordArt is just a TextBox with fancy fonts.

**Returns:**
boolean - True if this shape is a WordArt object.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
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
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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

### patterned(int patternType) {#patterned-int-}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the rootNode.
### remove() {#remove--}
```
public void remove()
```


Removes itself from the parent.

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of oldChild is set to null after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node) - The removed node.
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeShapeAttr(int key) {#removeShapeAttr-int-}
```
public void removeShapeAttr(int key)
```


Reserved for system use. IShapeAttrSource.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. This method does not remove the content of the smart tags.

### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


Selects the first Node that matches the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node) - The first Node that matches the XPath query or null if no matching node is found.
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

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDashStyle(int value) {#setDashStyle-int-}
```
public void setDashStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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

### setEndArrowLength(int value) {#setEndArrowLength-int-}
```
public void setEndArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowType(int value) {#setEndArrowType-int-}
```
public void setEndArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowWidth(int value) {#setEndArrowWidth-int-}
```
public void setEndArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndCap(int value) {#setEndCap-int-}
```
public void setEndCap(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

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

### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

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

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

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

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setJoinStyle(int value) {#setJoinStyle-int-}
```
public void setJoinStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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

### setLineFillType(int value) {#setLineFillType-int-}
```
public void setLineFillType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

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

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

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

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

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

### setStartArrowLength(int value) {#setStartArrowLength-int-}
```
public void setStartArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStartArrowType(int value) {#setStartArrowType-int-}
```
public void setStartArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStartArrowWidth(int value) {#setStartArrowWidth-int-}
```
public void setStartArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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

### setStrokeTransparency(double value) {#setStrokeTransparency-double-}
```
public void setStrokeTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setStrokeVisible(boolean value) {#setStrokeVisible-boolean-}
```
public void setStrokeVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

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

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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

### setWeight(double value) {#setWeight-double-}
```
public void setWeight(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

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

### setZOrder_IShape(int value) {#setZOrder-IShape-int-}
```
public void setZOrder_IShape(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### solid() {#solid--}
```
public void solid()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### updateSmartArtDrawing() {#updateSmartArtDrawing--}
```
public void updateSmartArtDrawing()
```


Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. Microsoft Word generates and saves the pre-rendered drawing along with SmartArt object. However, if the document is saved by other applications, the pre-rendered SmartArt drawing may be missing or incorrect. If pre-rendered drawing is available then Aspose.Words uses it to render the SmartArt object. If pre-rendered drawing is missing then Aspose.Words uses its own SmartArt cold rendering engine to render the SmartArt object. If pre-rendered drawing is incorrect then it is required to call this method to invoke the SmartArt cold rendering engine.

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

