---
title: Shape
linktitle: Shape
second_title: Aspose.Words for Java
description: Represents an object in the drawing layer such as an AutoShape textbox freeform OLE object ActiveX control or picture in Java.
type: docs
weight: 604
url: /java/com.aspose.words/shape/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/), [com.aspose.words.ShapeBase](../../com.aspose.words/shapebase/)
```
public class Shape extends ShapeBase
```

Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture.

To learn more, visit the [ Working with Shapes ][Working with Shapes] documentation article.

 **Remarks:** 

Using the [Shape](../../com.aspose.words/shape/) class you can create or modify shapes in a Microsoft Word document.

An important property of a shape is its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType). Shapes of different types can have different capabilities in a Word document. For example, only image and OLE shapes can have images inside them. Most of the shapes can have text, but not all.

Shapes that can have text, can contain [Paragraph](../../com.aspose.words/paragraph/) and [Table](../../com.aspose.words/table/) nodes as children.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

Shows how to extract images from a document, and save them to the local file system as individual files.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Get the collection of shapes from the document,
 // and save the image data of every shape with an image as a file to the local file system.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 int imageIndex = 0;
 for (Shape shape : (Iterable) shapes) {
     if (shape.hasImage()) {
         // The image data of shapes may contain images of many possible image formats.
         // We can determine a file extension for each image automatically, based on its format.
         String imageFileName = MessageFormat.format("File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil.imageTypeToExtension(shape.getImageData().getImageType()));
         shape.getImageData().save(getArtifactsDir() + imageFileName);
         imageIndex++;
     }
 }
 
```

Shows how to delete all shapes from a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two shapes along with a group shape with another shape inside it.
 builder.insertShape(ShapeType.RECTANGLE, 400.0, 200.0);
 builder.insertShape(ShapeType.STAR, 300.0, 300.0);

 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(100f, 50f, 200f, 100f));
 group.setCoordOrigin(new Point(-1000, -500));

 Shape subShape = new Shape(doc, ShapeType.CUBE);
 subShape.setWidth(500.0);
 subShape.setHeight(700.0);
 subShape.setLeft(0.0);
 subShape.setTop(0.0);

 group.appendChild(subShape);
 builder.insertNode(group);

 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 3);
 Assert.assertEquals(doc.getChildNodes(NodeType.GROUP_SHAPE, true).getCount(), 1);

 // Remove all Shape nodes from the document.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);
 shapes.clear();

 // All shapes are gone, but the group shape is still in the document.
 Assert.assertEquals(doc.getChildNodes(NodeType.GROUP_SHAPE, true).getCount(), 1);
 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 0);

 // Remove all group shapes separately.
 NodeCollection groupShapes = doc.getChildNodes(NodeType.GROUP_SHAPE, true);
 groupShapes.clear();

 Assert.assertEquals(doc.getChildNodes(NodeType.GROUP_SHAPE, true).getCount(), 0);
 Assert.assertEquals(doc.getChildNodes(NodeType.SHAPE, true).getCount(), 0);
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Constructors

| Constructor | Description |
| --- | --- |
| [Shape(DocumentBase doc, int shapeType)](#Shape-com.aspose.words.DocumentBase-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the end of the shape. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the start of the shape. |
| [adjustWithEffects(Rectangle2D.Float source)](#adjustWithEffects-java.awt.geom.Rectangle2D.Float) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [canHaveImage()](#canHaveImage) | Returns  true  if the shape type allows the shape to have an image. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [fetchInheritedShapeAttr(int key)](#fetchInheritedShapeAttr-int) |  |
| [fetchShapeAttr(int key)](#fetchShapeAttr-int) |  |
| [getAdjustments()](#getAdjustments) | Provides access to the adjustment raw values of a shape. |
| [getAllowOverlap()](#getAllowOverlap) | Gets a value that specifies whether this shape can overlap other shapes. |
| [getAlternativeText()](#getAlternativeText) | Defines alternative text to be displayed instead of a graphic. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getAnchorLocked()](#getAnchorLocked) | Specifies whether the shape's anchor is locked. |
| [getAspectRatioLocked()](#getAspectRatioLocked) | Specifies whether the shape's aspect ratio is locked. |
| [getBehindText()](#getBehindText) | Specifies whether the shape is below or above text. |
| [getBlur()](#getBlur) |  |
| [getBottom()](#getBottom) | Gets the position of the bottom edge of the containing block of the shape. |
| [getBounds()](#getBounds) | Gets the location and size of the containing block of the shape. |
| [getBoundsInPoints()](#getBoundsInPoints) | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [getBoundsWithEffects()](#getBoundsWithEffects) | Gets final extent that this shape object has after applying drawing effects. |
| [getChart()](#getChart) | Provides access to the chart properties if this shape has a [Chart](../../com.aspose.words/chart/). |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) |  |
| [getContainer()](#getContainer) |  |
| [getCoordOrigin()](#getCoordOrigin) | The coordinates at the top-left corner of the containing block of this shape. |
| [getCoordSize()](#getCoordSize) | The width and height of the coordinate space inside the containing block of this shape. |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDashStyle()](#getDashStyle) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDirectShapeAttr(int key)](#getDirectShapeAttr-int) |  |
| [getDistance()](#getDistance) |  |
| [getDistanceBottom()](#getDistanceBottom) | Gets the distance (in points) between the document text and the bottom edge of the shape. |
| [getDistanceLeft()](#getDistanceLeft) | Gets the distance (in points) between the document text and the left edge of the shape. |
| [getDistanceRight()](#getDistanceRight) | Gets the distance (in points) between the document text and the right edge of the shape. |
| [getDistanceTop()](#getDistanceTop) | Gets the distance (in points) between the document text and the top edge of the shape. |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getEdgeRadius()](#getEdgeRadius) |  |
| [getEndArrowLength()](#getEndArrowLength) |  |
| [getEndArrowType()](#getEndArrowType) |  |
| [getEndArrowWidth()](#getEndArrowWidth) |  |
| [getEndCap()](#getEndCap) |  |
| [getExtrusionEnabled()](#getExtrusionEnabled) | Returns  true  if an extrusion effect is enabled. |
| [getFill()](#getFill) | Gets fill formatting for the shape. |
| [getFillColor()](#getFillColor) | Defines the brush color that fills the closed path of the shape. |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableBaseForeColor()](#getFillableBaseForeColor) |  |
| [getFillableForeColor()](#getFillableForeColor) |  |
| [getFillableForeThemeColor()](#getFillableForeThemeColor) |  |
| [getFillableForeTintAndShade()](#getFillableForeTintAndShade) |  |
| [getFillableImageBytes()](#getFillableImageBytes) |  |
| [getFillableTransparency()](#getFillableTransparency) |  |
| [getFillableVisible()](#getFillableVisible) |  |
| [getFilled()](#getFilled) | Determines whether the closed path of the shape will be filled. |
| [getFilledColor()](#getFilledColor) |  |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFirstParagraph()](#getFirstParagraph) | Gets the first paragraph in the shape. |
| [getFlipOrientation()](#getFlipOrientation) | Switches the orientation of a shape. |
| [getFont()](#getFont) | Provides access to the font formatting of this object. |
| [getGlow()](#getGlow) | Gets glow formatting for the shape. |
| [getGradientAngle()](#getGradientAngle) |  |
| [getGradientStops()](#getGradientStops) |  |
| [getGradientStyle()](#getGradientStyle) |  |
| [getGradientVariant()](#getGradientVariant) |  |
| [getHRef()](#getHRef) | Gets the full hyperlink address for a shape. |
| [getHeight()](#getHeight) | Gets the height of the containing block of the shape. |
| [getHeightRelative()](#getHeightRelative) | Gets the value that represents the percentage of shape's relative height. |
| [getHidden()](#getHidden) | Gets a boolean value indicating whether the shape is visible. |
| [getHorizontalAlignment()](#getHorizontalAlignment) | Specifies how the shape is positioned horizontally. |
| [getHorizontalMargins_ITextBox()](#getHorizontalMargins-ITextBox) |  |
| [getHorizontalRuleFormat()](#getHorizontalRuleFormat) | Provides access to the properties of the horizontal rule shape. |
| [getImageData()](#getImageData) | Provides access to the image of the shape. |
| [getJoinStyle()](#getJoinStyle) |  |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLastParagraph()](#getLastParagraph) | Gets the last paragraph in the shape. |
| [getLeft()](#getLeft) | Gets the position of the left edge of the containing block of the shape. |
| [getLeftRelative()](#getLeftRelative) | Gets the value that represents shape's relative left position in percent. |
| [getLineFillType()](#getLineFillType) |  |
| [getLineStyle()](#getLineStyle) |  |
| [getMarkupLanguage()](#getMarkupLanguage) | Gets MarkupLanguage used for this graphic object. |
| [getMarkupLanguage_ITextBox()](#getMarkupLanguage-ITextBox) |  |
| [getName()](#getName) | Gets the optional shape name. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.SHAPE](../../com.aspose.words/nodetype/\#SHAPE). |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOleFormat()](#getOleFormat) | Provides access to the OLE data of a shape. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph) | Returns the immediate parent paragraph. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPatternType()](#getPatternType) |  |
| [getPresetTexture()](#getPresetTexture) |  |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRadius()](#getRadius) |  |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getReflection()](#getReflection) | Gets reflection formatting for the shape. |
| [getReflectionSize()](#getReflectionSize) |  |
| [getReflectionTransparency()](#getReflectionTransparency) |  |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition) | Specifies relative to what the shape is positioned horizontally. |
| [getRelativeHorizontalSize()](#getRelativeHorizontalSize) | Gets the value of shape's relative size in horizontal direction. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition) | Specifies relative to what the shape is positioned vertically. |
| [getRelativeVerticalSize()](#getRelativeVerticalSize) | Gets the value of shape's relative size in vertical direction. |
| [getRight()](#getRight) | Gets the position of the right edge of the containing block of the shape. |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getRotation()](#getRotation) | Defines the angle (in degrees) that a shape is rotated. |
| [getScreenTip()](#getScreenTip) | Defines the text displayed when the mouse pointer moves over the shape. |
| [getShadowColors()](#getShadowColors) |  |
| [getShadowEnabled()](#getShadowEnabled) | Returns  true  if a shadow effect is enabled. |
| [getShadowFormat()](#getShadowFormat) | Gets shadow formatting for the shape. |
| [getShadowType()](#getShadowType) |  |
| [getShapeRenderer()](#getShapeRenderer) | Creates and returns an object that can be used to render this shape into an image. |
| [getShapeType()](#getShapeType) | Gets the shape type. |
| [getSignatureLine()](#getSignatureLine) | Gets [SignatureLine](../../com.aspose.words/signatureline/) object if the shape is a signature line. |
| [getSizeInPoints()](#getSizeInPoints) | Gets the size of the shape in points. |
| [getSoftEdge()](#getSoftEdge) | Gets soft edge formatting for the shape. |
| [getStartArrowLength()](#getStartArrowLength) |  |
| [getStartArrowType()](#getStartArrowType) |  |
| [getStartArrowWidth()](#getStartArrowWidth) |  |
| [getStoryType()](#getStoryType) | Returns [StoryType.TEXTBOX](../../com.aspose.words/storytype/\#TEXTBOX). |
| [getStroke()](#getStroke) | Defines a stroke for a shape. |
| [getStrokeBackThemeColor()](#getStrokeBackThemeColor) |  |
| [getStrokeBackTintAndShade()](#getStrokeBackTintAndShade) |  |
| [getStrokeColor()](#getStrokeColor) | Defines the color of a stroke. |
| [getStrokeForeThemeColor()](#getStrokeForeThemeColor) |  |
| [getStrokeForeTintAndShade()](#getStrokeForeTintAndShade) |  |
| [getStrokeImageBytes()](#getStrokeImageBytes) |  |
| [getStrokeTransparency()](#getStrokeTransparency) |  |
| [getStrokeVisible()](#getStrokeVisible) |  |
| [getStrokeWeight()](#getStrokeWeight) | Defines the brush thickness that strokes the path of a shape in points. |
| [getStroked()](#getStroked) | Defines whether the path will be stroked. |
| [getTarget()](#getTarget) | Gets the target frame for the shape hyperlink. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [getTextBox()](#getTextBox) | Defines attributes that specify how text is displayed in a shape. |
| [getTextBoxWrapMode_ITextBox()](#getTextBoxWrapMode-ITextBox) |  |
| [getTextPath()](#getTextPath) | Defines the text of the text path (of a WordArt object). |
| [getTextboxLayoutFlow_ITextBox()](#getTextboxLayoutFlow-ITextBox) |  |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getTitle()](#getTitle) | Gets the title (caption) of the current shape object. |
| [getTop()](#getTop) | Gets the position of the top edge of the containing block of the shape. |
| [getTopRelative()](#getTopRelative) | Gets the value that represents shape's relative top position in percent. |
| [getTransparency()](#getTransparency) |  |
| [getVerticalAlignment()](#getVerticalAlignment) | Specifies how the shape is positioned vertically. |
| [getVisible()](#getVisible) |  |
| [getWeight()](#getWeight) |  |
| [getWidth()](#getWidth) | Gets the width of the containing block of the shape. |
| [getWidthRelative()](#getWidthRelative) | Gets the value that represents the percentage of shape's relative width. |
| [getWrapSide()](#getWrapSide) | Specifies how the text is wrapped around the shape. |
| [getWrapType()](#getWrapType) | Defines whether the shape is inline or floating. |
| [getZOrder()](#getZOrder) | Determines the display order of overlapping shapes. |
| [getZOrder_IShape()](#getZOrder-IShape) |  |
| [hasChart()](#hasChart) | Returns  true  if this [Shape](../../com.aspose.words/shape/) has a [Chart](../../com.aspose.words/chart/). |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hasImage()](#hasImage) | Returns  true  if the shape has image bytes or links an image. |
| [hasSmartArt()](#hasSmartArt) | Returns  true  if this [Shape](../../com.aspose.words/shape/) has a SmartArt object. |
| [hasVerticalTextFlow_ITextBox()](#hasVerticalTextFlow-ITextBox) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [isDecorative()](#isDecorative) | Gets the flag that specifies whether the shape is decorative in the document. |
| [isDecorative(boolean value)](#isDecorative-boolean) | Sets the flag that specifies whether the shape is decorative in the document. |
| [isDeleteRevision()](#isDeleteRevision) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isGroup()](#isGroup) | Returns  true  if this is a group shape. |
| [isHorizontalRule()](#isHorizontalRule) | Returns  true  if this shape is a horizontal rule. |
| [isImage()](#isImage) | Returns  true  if this shape is an image shape. |
| [isInline()](#isInline) | A quick way to determine if this shape is positioned inline with text. |
| [isInsertRevision()](#isInsertRevision) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isLayoutInCell()](#isLayoutInCell) | Gets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isLayoutInCell(boolean value)](#isLayoutInCell-boolean) | Sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isMoveFromRevision()](#isMoveFromRevision) | Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision) | Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [isSignatureLine()](#isSignatureLine) | Indicates that shape is a [SignatureLine](../../com.aspose.words/signatureline/). |
| [isTopLevel()](#isTopLevel) | Returns  true  if this shape is not a child of a group shape. |
| [isWordArt()](#isWordArt) | Returns  true  if this shape is a WordArt object. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [localToParent(Point2D.Float value)](#localToParent-java.awt.geom.Point2D.Float) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeGlow()](#removeGlow) |  |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeReflection()](#removeReflection) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeShadow()](#removeShadow) |  |
| [removeShapeAttr(int key)](#removeShapeAttr-int) |  |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [removeSoftEdge()](#removeSoftEdge) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setAllowOverlap(boolean value)](#setAllowOverlap-boolean) | Sets a value that specifies whether this shape can overlap other shapes. |
| [setAlternativeText(String value)](#setAlternativeText-java.lang.String) | Defines alternative text to be displayed instead of a graphic. |
| [setAnchorLocked(boolean value)](#setAnchorLocked-boolean) | Specifies whether the shape's anchor is locked. |
| [setAspectRatioLocked(boolean value)](#setAspectRatioLocked-boolean) | Specifies whether the shape's aspect ratio is locked. |
| [setBehindText(boolean value)](#setBehindText-boolean) | Specifies whether the shape is below or above text. |
| [setBlur(double value)](#setBlur-double) |  |
| [setBounds(Rectangle2D.Float value)](#setBounds-java.awt.geom.Rectangle2D.Float) | Sets the location and size of the containing block of the shape. |
| [setColor(Color value)](#setColor-java.awt.Color) |  |
| [setCoordOrigin(Point value)](#setCoordOrigin-java.awt.Point) | The coordinates at the top-left corner of the containing block of this shape. |
| [setCoordSize(Dimension value)](#setCoordSize-java.awt.Dimension) | The width and height of the coordinate space inside the containing block of this shape. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setDashStyle(int value)](#setDashStyle-int) |  |
| [setDistance(double value)](#setDistance-double) |  |
| [setDistanceBottom(double value)](#setDistanceBottom-double) | Sets the distance (in points) between the document text and the bottom edge of the shape. |
| [setDistanceLeft(double value)](#setDistanceLeft-double) | Sets the distance (in points) between the document text and the left edge of the shape. |
| [setDistanceRight(double value)](#setDistanceRight-double) | Sets the distance (in points) between the document text and the right edge of the shape. |
| [setDistanceTop(double value)](#setDistanceTop-double) | Sets the distance (in points) between the document text and the top edge of the shape. |
| [setEdgeRadius(double value)](#setEdgeRadius-double) |  |
| [setEndArrowLength(int value)](#setEndArrowLength-int) |  |
| [setEndArrowType(int value)](#setEndArrowType-int) |  |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int) |  |
| [setEndCap(int value)](#setEndCap-int) |  |
| [setFillColor(Color value)](#setFillColor-java.awt.Color) | Defines the brush color that fills the closed path of the shape. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color) |  |
| [setFillableBackThemeColor(int value)](#setFillableBackThemeColor-int) |  |
| [setFillableBackTintAndShade(double value)](#setFillableBackTintAndShade-double) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color) |  |
| [setFillableForeThemeColor(int value)](#setFillableForeThemeColor-int) |  |
| [setFillableForeTintAndShade(double value)](#setFillableForeTintAndShade-double) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean) |  |
| [setFilled(boolean value)](#setFilled-boolean) | Determines whether the closed path of the shape will be filled. |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color) |  |
| [setFlipOrientation(int value)](#setFlipOrientation-int) | Switches the orientation of a shape. |
| [setGradientAngle(double value)](#setGradientAngle-double) |  |
| [setHRef(String value)](#setHRef-java.lang.String) | Sets the full hyperlink address for a shape. |
| [setHeight(double value)](#setHeight-double) | Sets the height of the containing block of the shape. |
| [setHeightRelative(float value)](#setHeightRelative-float) | Sets the value that represents the percentage of shape's relative height. |
| [setHidden(boolean value)](#setHidden-boolean) | Sets a boolean value indicating whether the shape is visible. |
| [setHorizontalAlignment(int value)](#setHorizontalAlignment-int) | Specifies how the shape is positioned horizontally. |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setJoinStyle(int value)](#setJoinStyle-int) |  |
| [setLeft(double value)](#setLeft-double) | Sets the position of the left edge of the containing block of the shape. |
| [setLeftRelative(float value)](#setLeftRelative-float) | Sets the value that represents shape's relative left position in percent. |
| [setLineFillType(int value)](#setLineFillType-int) |  |
| [setLineStyle(int value)](#setLineStyle-int) |  |
| [setName(String value)](#setName-java.lang.String) | Sets the optional shape name. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setRadius(double value)](#setRadius-double) |  |
| [setReflectionSize(double value)](#setReflectionSize-double) |  |
| [setReflectionTransparency(double value)](#setReflectionTransparency-double) |  |
| [setRelativeHorizontalPosition(int value)](#setRelativeHorizontalPosition-int) | Specifies relative to what the shape is positioned horizontally. |
| [setRelativeHorizontalSize(int value)](#setRelativeHorizontalSize-int) | Sets the value of shape's relative size in horizontal direction. |
| [setRelativeVerticalPosition(int value)](#setRelativeVerticalPosition-int) | Specifies relative to what the shape is positioned vertically. |
| [setRelativeVerticalSize(int value)](#setRelativeVerticalSize-int) | Sets the value of shape's relative size in vertical direction. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setRotation(double value)](#setRotation-double) | Defines the angle (in degrees) that a shape is rotated. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setScreenTip(String value)](#setScreenTip-java.lang.String) | Defines the text displayed when the mouse pointer moves over the shape. |
| [setShadowType(int value)](#setShadowType-int) |  |
| [setShapeAttr(int key, Object value)](#setShapeAttr-int-java.lang.Object) |  |
| [setStartArrowLength(int value)](#setStartArrowLength-int) |  |
| [setStartArrowType(int value)](#setStartArrowType-int) |  |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int) |  |
| [setStrokeBackThemeColor(int value)](#setStrokeBackThemeColor-int) |  |
| [setStrokeBackTintAndShade(double value)](#setStrokeBackTintAndShade-double) |  |
| [setStrokeColor(Color value)](#setStrokeColor-java.awt.Color) | Defines the color of a stroke. |
| [setStrokeForeThemeColor(int value)](#setStrokeForeThemeColor-int) |  |
| [setStrokeForeTintAndShade(double value)](#setStrokeForeTintAndShade-double) |  |
| [setStrokeTransparency(double value)](#setStrokeTransparency-double) |  |
| [setStrokeVisible(boolean value)](#setStrokeVisible-boolean) |  |
| [setStrokeWeight(double value)](#setStrokeWeight-double) | Defines the brush thickness that strokes the path of a shape in points. |
| [setStroked(boolean value)](#setStroked-boolean) | Defines whether the path will be stroked. |
| [setTarget(String value)](#setTarget-java.lang.String) | Sets the target frame for the shape hyperlink. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setTitle(String value)](#setTitle-java.lang.String) | Sets the title (caption) of the current shape object. |
| [setTop(double value)](#setTop-double) | Sets the position of the top edge of the containing block of the shape. |
| [setTopRelative(float value)](#setTopRelative-float) | Sets the value that represents shape's relative top position in percent. |
| [setTransparency(double value)](#setTransparency-double) |  |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Specifies how the shape is positioned vertically. |
| [setWeight(double value)](#setWeight-double) |  |
| [setWidth(double value)](#setWidth-double) | Sets the width of the containing block of the shape. |
| [setWidthRelative(float value)](#setWidthRelative-float) | Sets the value that represents the percentage of shape's relative width. |
| [setWrapSide(int value)](#setWrapSide-int) | Specifies how the text is wrapped around the shape. |
| [setWrapType(int value)](#setWrapType-int) | Defines whether the shape is inline or floating. |
| [setZOrder(int value)](#setZOrder-int) | Determines the display order of overlapping shapes. |
| [setZOrder_IShape(int value)](#setZOrder-IShape-int) |  |
| [solid()](#solid) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [updateSmartArtDrawing()](#updateSmartArtDrawing) | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |
### Shape(DocumentBase doc, int shapeType) {#Shape-com.aspose.words.DocumentBase-int}
```
public Shape(DocumentBase doc, int shapeType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| shapeType | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

 **Remarks:** 

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

Calls [DocumentVisitor.visitShapeStart(com.aspose.words.Shape)](../../com.aspose.words/documentvisitor/\#visitShapeStart-com.aspose.words.Shape), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the shape and calls [DocumentVisitor.visitShapeEnd(com.aspose.words.Shape)](../../com.aspose.words/documentvisitor/\#visitShapeEnd-com.aspose.words.Shape) at the end.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Accepts a visitor for visiting the end of the shape.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Accepts a visitor for visiting the start of the shape.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### adjustWithEffects(Rectangle2D.Float source) {#adjustWithEffects-java.awt.geom.Rectangle2D.Float}
```
public Rectangle2D.Float adjustWithEffects(Rectangle2D.Float source)
```


Adds to the source rectangle values of the effect extent and returns the final rectangle.

 **Examples:** 

Shows how to check how a shape's bounds are affected by shape effects.

```

 Document doc = new Document(getMyDir() + "Shape shadow effect.docx");
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());
 Assert.assertEquals(shapeList.size(), 2);

 Shape firstShape = shapeList.get(0);
 Shape secondShape = shapeList.get(1);

 // The two shapes are identical in terms of dimensions and shape type.
 Assert.assertEquals(firstShape.getWidth(), secondShape.getWidth());
 Assert.assertEquals(firstShape.getHeight(), secondShape.getHeight());
 Assert.assertEquals(firstShape.getShapeType(), secondShape.getShapeType());

 // The first shape has no effects, and the second one has a shadow and thick outline.
 // These effects make the size of the second shape's silhouette bigger than that of the first.
 // Even though the rectangle's size shows up when we click on these shapes in Microsoft Word,
 // the visible outer bounds of the second shape are affected by the shadow and outline and thus are bigger.
 // We can use the "AdjustWithEffects" method to see the true size of the shape.
 Assert.assertEquals(0.0, firstShape.getStrokeWeight());
 Assert.assertEquals(20.0, secondShape.getStrokeWeight());
 Assert.assertFalse(firstShape.getShadowEnabled());
 Assert.assertTrue(secondShape.getShadowEnabled());

 Shape shape = firstShape;

 // Run this method to get the size of the rectangle adjusted for all our shape effects.
 Rectangle2D.Float rectangleFOut = shape.adjustWithEffects(new Rectangle2D.Float(200f, 200f, 1000f, 1000f));

 // Since the shape has no border-changing effects, its boundary dimensions are unaffected.
 Assert.assertEquals(200.0, rectangleFOut.getX());
 Assert.assertEquals(200.0, rectangleFOut.getY());
 Assert.assertEquals(1000.0, rectangleFOut.getWidth());
 Assert.assertEquals(1000.0, rectangleFOut.getHeight());

 // Verify the final extent of the first shape, in points.
 Assert.assertEquals(0.0, shape.getBoundsWithEffects().getX());
 Assert.assertEquals(0.0, shape.getBoundsWithEffects().getY());
 Assert.assertEquals(147.0, shape.getBoundsWithEffects().getWidth());
 Assert.assertEquals(147.0, shape.getBoundsWithEffects().getHeight());

 shape = secondShape;
 rectangleFOut = shape.adjustWithEffects(new Rectangle2D.Float(200f, 200f, 1000f, 1000f));

 // The shape effects have moved the apparent top left corner of the shape slightly.
 Assert.assertEquals(171.5, rectangleFOut.getX());
 Assert.assertEquals(167.0, rectangleFOut.getY());

 // The effects have also affected the visible dimensions of the shape.
 Assert.assertEquals(1045.0, rectangleFOut.getWidth());
 Assert.assertEquals(1133.5, rectangleFOut.getHeight());

 // The effects have also affected the visible bounds of the shape.
 Assert.assertEquals(-28.5, shape.getBoundsWithEffects().getX());
 Assert.assertEquals(-33.0, shape.getBoundsWithEffects().getY());
 Assert.assertEquals(192.0, shape.getBoundsWithEffects().getWidth());
 Assert.assertEquals(280.5, shape.getBoundsWithEffects().getHeight());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| source | java.awt.geom.Rectangle2D.Float |  |

**Returns:**
java.awt.geom.Rectangle2D.Float
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### canHaveImage() {#canHaveImage}
```
public boolean canHaveImage()
```


Returns  true  if the shape type allows the shape to have an image.

 **Remarks:** 

Although Microsoft Word has a special shape type for images, it appears that in Microsoft Word documents any shape except a group shape can have an image, therefore this property returns  true  for all shapes except [GroupShape](../../com.aspose.words/groupshape/).

 **Examples:** 

Shows how to insert and rotate an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape with an image.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 Assert.assertTrue(shape.canHaveImage());
 Assert.assertTrue(shape.hasImage());

 // Rotate the image 45 degrees clockwise.
 shape.setRotation(45.0);

 doc.save(getArtifactsDir() + "Shape.Rotate.docx");
 
```

**Returns:**
boolean -  true  if the shape type allows the shape to have an image.
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

 **Remarks:** 

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

 **Examples:** 

Shows how to clone a composite node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShapeAttr(int key) {#fetchInheritedShapeAttr-int}
```
public Object fetchInheritedShapeAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchShapeAttr(int key) {#fetchShapeAttr-int}
```
public Object fetchShapeAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAdjustments() {#getAdjustments}
```
public AdjustmentCollection getAdjustments()
```


Provides access to the adjustment raw values of a shape. For a shape that does not contain any adjustment raw values, it returns an empty collection.

 **Examples:** 

Shows how to work with adjustment raw values.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Returns:**
[AdjustmentCollection](../../com.aspose.words/adjustmentcollection/) - The corresponding [AdjustmentCollection](../../com.aspose.words/adjustmentcollection/) value.
### getAllowOverlap() {#getAllowOverlap}
```
public boolean getAllowOverlap()
```


Gets a value that specifies whether this shape can overlap other shapes.

 **Remarks:** 

This property affects behavior of the shape in Microsoft Word. Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is  true .

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Returns:**
boolean - A value that specifies whether this shape can overlap other shapes.
### getAlternativeText() {#getAlternativeText}
```
public String getAlternativeText()
```


Defines alternative text to be displayed instead of a graphic.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to use a shape's alternative text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertShape(ShapeType.CUBE, 150.0, 150.0);
 shape.setName("MyCube");

 shape.setAlternativeText("Alt text for MyCube.");

 // We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
 doc.save(getArtifactsDir() + "Shape.AltText.docx");

 // Save the document to HTML, and then delete the linked image that belongs to our shape.
 // The browser that is reading our HTML will display the alt text in place of the missing image.
 doc.save(getArtifactsDir() + "Shape.AltText.html");
 new File(getArtifactsDir() + "Shape.AltText.001.png").delete();
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

 **Remarks:** 

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .

 **Examples:** 

Shows how to find out if a tables are nested.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getAnchorLocked() {#getAnchorLocked}
```
public boolean getAnchorLocked()
```


Specifies whether the shape's anchor is locked.

 **Remarks:** 

The default value is  false .

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word. When the anchor is not locked, moving the shape in Microsoft Word can move the shape's anchor too.

 **Examples:** 

Shows how to lock or unlock a shape's paragraph anchor.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 builder.write("Our shape will have an anchor attached to this paragraph.");
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 160.0);
 shape.setWrapType(WrapType.NONE);
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 builder.writeln("Hello again!");

 // Set the "AnchorLocked" property to "true" to prevent the shape's anchor
 // from moving when moving the shape in Microsoft Word.
 // Set the "AnchorLocked" property to "false" to allow any movement of the shape
 // to also move its anchor to any other paragraph that the shape ends up close to.
 shape.setAnchorLocked(anchorLocked);

 // If the shape does not have a visible anchor symbol to its left,
 // we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
 doc.save(getArtifactsDir() + "Shape.AnchorLocked.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getAspectRatioLocked() {#getAspectRatioLocked}
```
public boolean getAspectRatioLocked()
```


Specifies whether the shape's aspect ratio is locked.

 **Remarks:** 

The default value depends on the [ShapeType](../../com.aspose.words/shapetype/), for the [ShapeType.IMAGE](../../com.aspose.words/shapetype/\#IMAGE) it is  true  but for the other shape types it is  false .

Has effect for top level shapes only.

 **Examples:** 

Shows how to lock/unlock a shape's aspect ratio.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
 // eight sizing handles around its perimeter, which we can click and drag to change its size.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
 // when using any of the four diagonal sizing handles, which change both the image's height and width.
 // Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
 // Set the "AspectRatioLocked" property to "false" to allow us to
 // freely change the image's aspect ratio with all sizing handles.
 shape.setAspectRatioLocked(lockAspectRatio);

 doc.save(getArtifactsDir() + "Shape.AspectRatio.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getBehindText() {#getBehindText}
```
public boolean getBehindText()
```


Specifies whether the shape is below or above text.

 **Remarks:** 

Has effect only for top level shapes.

The default value is  false .

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getBlur() {#getBlur}
```
public double getBlur()
```




**Returns:**
double
### getBottom() {#getBottom}
```
public double getBottom()
```


Gets the position of the bottom edge of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - The position of the bottom edge of the containing block of the shape.
### getBounds() {#getBounds}
```
public Rectangle2D.Float getBounds()
```


Gets the location and size of the containing block of the shape.

 **Remarks:** 

Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

 **Examples:** 

Shows how to verify shape containing block boundaries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.LINE, RelativeHorizontalPosition.LEFT_MARGIN, 50.0,
         RelativeVerticalPosition.TOP_MARGIN, 50.0, 100.0, 100.0, WrapType.NONE);
 shape.setStrokeColor(Color.ORANGE);

 // Even though the line itself takes up little space on the document page,
 // it occupies a rectangular containing block, the size of which we can determine using the "Bounds" properties.
 Assert.assertEquals(new Rectangle2D.Float(50f, 50f, 100f, 100f), shape.getBounds());
 Assert.assertEquals(new Rectangle2D.Float(50f, 50f, 100f, 100f), shape.getBoundsInPoints());

 // Create a group shape, and then set the size of its containing block using the "Bounds" property.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(0f, 100f, 250f, 250f));

 Assert.assertEquals(new Rectangle2D.Float(0f, 100f, 250f, 250f), group.getBoundsInPoints());

 // Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
 shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 Assert.assertEquals(new Rectangle2D.Float(700f, 700f, 100f, 100f), shape.getBoundsInPoints());

 group.appendChild(shape);

 // The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
 // and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
 // Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
 // translates to 1pt in the document body's coordinate plane.
 // Every shape that we insert will also shrink in size by a factor of 4.
 // The change in the shape's "BoundsInPoints" property will reflect this.
 Assert.assertEquals(new Rectangle2D.Float(175f, 275f, 25f, 25f), shape.getBoundsInPoints());

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 // Insert a shape and place it outside of the bounds of the group shape's containing block.
 shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(1000.0);
     shape.setTop(1000.0);
 }

 group.appendChild(shape);

 // The group shape's footprint in the document body has increased, but the containing block remains the same.
 Assert.assertEquals(new Rectangle2D.Float(0f, 100f, 250f, 250f), group.getBoundsInPoints());
 Assert.assertEquals(new Rectangle2D.Float(250f, 350f, 25f, 25f), shape.getBoundsInPoints());

 doc.save(getArtifactsDir() + "Shape.Bounds.docx");
 
```

Shows how to create and populate a group shape.

```

 Document doc = new Document();

 // Create a group shape. A group shape can display a collection of child shape nodes.
 // In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
 // select all the other child shapes within this group and allow us to scale and move all the shapes at once.
 GroupShape group = new GroupShape(doc);

 Assert.assertEquals(WrapType.NONE, group.getWrapType());

 // Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
 group.setBounds(new Rectangle2D.Float(0f, 0f, 400f, 400f));

 // Set the group's internal coordinate plane size to 500 x 500pt.
 // The top left corner of the group will have an x and y coordinate of (0, 0),
 // and the bottom right corner will have an x and y coordinate of (500, 500).
 group.setCoordSize(new Dimension(500, 500));

 // Set the coordinates of the top left corner of the group to (-250, -250).
 // The group's center will now have an x and y coordinate value of (0, 0),
 // and the bottom right corner will be at (250, 250).
 group.setCoordOrigin(new Point(-250, -250));

 Shape rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(group.getCoordSize().width);
 rectangleShape.setHeight(group.getCoordSize().height);
 rectangleShape.setLeft(group.getCoordOrigin().x);
 rectangleShape.setTop(group.getCoordOrigin().y);

 // Create a rectangle that will display the boundary of this group shape and add it to the group.
 group.appendChild(rectangleShape);

 // Once a shape is a part of a group shape, we can access it as a child node and then modify it.
 ((Shape) group.getChild(NodeType.SHAPE, 0, true)).getStroke().setDashStyle(DashStyle.DASH);

 Shape starShape = new Shape(doc, ShapeType.STAR);
 starShape.setWidth(20.0);
 starShape.setHeight(20.0);
 starShape.setLeft(-10);
 starShape.setTop(-10);
 starShape.setFillColor(Color.RED);

 // Create a small red star and insert it into the group.
 // Line up the shape with the group's coordinate origin, which we have moved to the center.
 group.appendChild(starShape);

 rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(250.0);
 rectangleShape.setHeight(250.0);
 rectangleShape.setLeft(-250);
 rectangleShape.setTop(-250);
 rectangleShape.setFillColor(Color.BLUE);

 // Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
 // Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
 // and then the shape with the image will overlap the light blue rectangle, using it as a frame.
 // We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
 group.appendChild(rectangleShape);

 Shape imageShape = new Shape(doc, ShapeType.IMAGE);
 imageShape.setWidth(200.0);
 imageShape.setHeight(200.0);
 imageShape.setLeft(-225);
 imageShape.setTop(-225);

 group.appendChild(imageShape);

 ((Shape) group.getChild(NodeType.SHAPE, 3, true)).getImageData().setImage(getImageDir() + "Logo.jpg");

 Shape textboxShape = new Shape(doc, ShapeType.TEXT_BOX);
 textboxShape.setWidth(200.0);
 textboxShape.setHeight(50.0);
 textboxShape.setLeft(group.getCoordSize().width + new Point(group.getCoordOrigin()).x - 200);
 textboxShape.setTop(group.getCoordSize().height + new Point(group.getCoordOrigin()).y);

 // Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
 // touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
 // the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
 group.appendChild(textboxShape);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(group);
 builder.moveTo(((Shape) group.getChild(NodeType.SHAPE, 4, true)).appendChild(new Paragraph(doc)));
 builder.write("Hello world!");

 doc.save(getArtifactsDir() + "Shape.GroupShape.docx");
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - The location and size of the containing block of the shape.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.

 **Remarks:** 

The returned bounds do not include the rotation of this shape or the rotation of the parent group shape, if any.

 **Examples:** 

Shows how to verify shape containing block boundaries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.LINE, RelativeHorizontalPosition.LEFT_MARGIN, 50.0,
         RelativeVerticalPosition.TOP_MARGIN, 50.0, 100.0, 100.0, WrapType.NONE);
 shape.setStrokeColor(Color.ORANGE);

 // Even though the line itself takes up little space on the document page,
 // it occupies a rectangular containing block, the size of which we can determine using the "Bounds" properties.
 Assert.assertEquals(new Rectangle2D.Float(50f, 50f, 100f, 100f), shape.getBounds());
 Assert.assertEquals(new Rectangle2D.Float(50f, 50f, 100f, 100f), shape.getBoundsInPoints());

 // Create a group shape, and then set the size of its containing block using the "Bounds" property.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(0f, 100f, 250f, 250f));

 Assert.assertEquals(new Rectangle2D.Float(0f, 100f, 250f, 250f), group.getBoundsInPoints());

 // Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
 shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 Assert.assertEquals(new Rectangle2D.Float(700f, 700f, 100f, 100f), shape.getBoundsInPoints());

 group.appendChild(shape);

 // The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
 // and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
 // Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
 // translates to 1pt in the document body's coordinate plane.
 // Every shape that we insert will also shrink in size by a factor of 4.
 // The change in the shape's "BoundsInPoints" property will reflect this.
 Assert.assertEquals(new Rectangle2D.Float(175f, 275f, 25f, 25f), shape.getBoundsInPoints());

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 // Insert a shape and place it outside of the bounds of the group shape's containing block.
 shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(1000.0);
     shape.setTop(1000.0);
 }

 group.appendChild(shape);

 // The group shape's footprint in the document body has increased, but the containing block remains the same.
 Assert.assertEquals(new Rectangle2D.Float(0f, 100f, 250f, 250f), group.getBoundsInPoints());
 Assert.assertEquals(new Rectangle2D.Float(250f, 350f, 25f, 25f), shape.getBoundsInPoints());

 doc.save(getArtifactsDir() + "Shape.Bounds.docx");
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - The location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.
### getBoundsWithEffects() {#getBoundsWithEffects}
```
public Rectangle2D.Float getBoundsWithEffects()
```


Gets final extent that this shape object has after applying drawing effects. Value is measured in points.

 **Examples:** 

Shows how to check how a shape's bounds are affected by shape effects.

```

 Document doc = new Document(getMyDir() + "Shape shadow effect.docx");
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());
 Assert.assertEquals(shapeList.size(), 2);

 Shape firstShape = shapeList.get(0);
 Shape secondShape = shapeList.get(1);

 // The two shapes are identical in terms of dimensions and shape type.
 Assert.assertEquals(firstShape.getWidth(), secondShape.getWidth());
 Assert.assertEquals(firstShape.getHeight(), secondShape.getHeight());
 Assert.assertEquals(firstShape.getShapeType(), secondShape.getShapeType());

 // The first shape has no effects, and the second one has a shadow and thick outline.
 // These effects make the size of the second shape's silhouette bigger than that of the first.
 // Even though the rectangle's size shows up when we click on these shapes in Microsoft Word,
 // the visible outer bounds of the second shape are affected by the shadow and outline and thus are bigger.
 // We can use the "AdjustWithEffects" method to see the true size of the shape.
 Assert.assertEquals(0.0, firstShape.getStrokeWeight());
 Assert.assertEquals(20.0, secondShape.getStrokeWeight());
 Assert.assertFalse(firstShape.getShadowEnabled());
 Assert.assertTrue(secondShape.getShadowEnabled());

 Shape shape = firstShape;

 // Run this method to get the size of the rectangle adjusted for all our shape effects.
 Rectangle2D.Float rectangleFOut = shape.adjustWithEffects(new Rectangle2D.Float(200f, 200f, 1000f, 1000f));

 // Since the shape has no border-changing effects, its boundary dimensions are unaffected.
 Assert.assertEquals(200.0, rectangleFOut.getX());
 Assert.assertEquals(200.0, rectangleFOut.getY());
 Assert.assertEquals(1000.0, rectangleFOut.getWidth());
 Assert.assertEquals(1000.0, rectangleFOut.getHeight());

 // Verify the final extent of the first shape, in points.
 Assert.assertEquals(0.0, shape.getBoundsWithEffects().getX());
 Assert.assertEquals(0.0, shape.getBoundsWithEffects().getY());
 Assert.assertEquals(147.0, shape.getBoundsWithEffects().getWidth());
 Assert.assertEquals(147.0, shape.getBoundsWithEffects().getHeight());

 shape = secondShape;
 rectangleFOut = shape.adjustWithEffects(new Rectangle2D.Float(200f, 200f, 1000f, 1000f));

 // The shape effects have moved the apparent top left corner of the shape slightly.
 Assert.assertEquals(171.5, rectangleFOut.getX());
 Assert.assertEquals(167.0, rectangleFOut.getY());

 // The effects have also affected the visible dimensions of the shape.
 Assert.assertEquals(1045.0, rectangleFOut.getWidth());
 Assert.assertEquals(1133.5, rectangleFOut.getHeight());

 // The effects have also affected the visible bounds of the shape.
 Assert.assertEquals(-28.5, shape.getBoundsWithEffects().getX());
 Assert.assertEquals(-33.0, shape.getBoundsWithEffects().getY());
 Assert.assertEquals(192.0, shape.getBoundsWithEffects().getWidth());
 Assert.assertEquals(280.5, shape.getBoundsWithEffects().getHeight());
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - Final extent that this shape object has after applying drawing effects.
### getChart() {#getChart}
```
public Chart getChart()
```


Provides access to the chart properties if this shape has a [Chart](../../com.aspose.words/chart/).

 **Remarks:** 

This property will return the [Chart](../../com.aspose.words/chart/) object only if [hasChart()](../../com.aspose.words/shape/\#hasChart) property is  true  for this [Shape](../../com.aspose.words/shape/), and will throw an exception otherwise.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
[Chart](../../com.aspose.words/chart/) - The corresponding [Chart](../../com.aspose.words/chart/) value.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
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
[Node](../../com.aspose.words/node/)
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public Color getColor()
```




**Returns:**
java.awt.Color
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCoordOrigin() {#getCoordOrigin}
```
public Point getCoordOrigin()
```


The coordinates at the top-left corner of the containing block of this shape.

 **Remarks:** 

The default value is (0,0).

 **Examples:** 

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```

 Document doc = new Document();

 // Insert a group shape, and place it 100 points below and to the right of
 // the document's x and Y coordinate origin point.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(100f, 100f, 500f, 500f));

 // Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
 // lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
 Assert.assertEquals(new Point2D.Float(100f, 100f), group.localToParent(new Point2D.Float(0f, 0f)));

 // By default, a shape's internal coordinate plane has the top left corner at (0, 0),
 // and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
 // in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
 // to a movement of 2pts on the group shape's coordinate plane.
 Assert.assertEquals(new Point2D.Float(150f, 150f), group.localToParent(new Point2D.Float(100f, 100f)));
 Assert.assertEquals(new Point2D.Float(200f, 200f), group.localToParent(new Point2D.Float(200f, 200f)));
 Assert.assertEquals(new Point2D.Float(250f, 250f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Move the group shape's x and y axis origin from the top left corner to the center.
 // This will offset the group's internal coordinates relative to the document's coordinates even further.
 group.setCoordOrigin(new Point(-250, -250));

 Assert.assertEquals(new Point2D.Float(375f, 375f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Changing the scale of the coordinate plane will also affect relative locations.
 group.setCoordSize(new Dimension(500, 500));

 Assert.assertEquals(new Point2D.Float(650f, 650f), group.localToParent(new Point2D.Float(300f, 300f)));

 // If we wish to add a shape to this group while defining its location based on a location in the document,
 // we will need to first confirm a location in the group shape that will match the document's location.
 Assert.assertEquals(new Point2D.Float(700f, 700f), group.localToParent(new Point2D.Float(350f, 350f)));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 group.appendChild(shape);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 doc.save(getArtifactsDir() + "Shape.LocalToParent.docx");
 
```

Shows how to create and populate a group shape.

```

 Document doc = new Document();

 // Create a group shape. A group shape can display a collection of child shape nodes.
 // In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
 // select all the other child shapes within this group and allow us to scale and move all the shapes at once.
 GroupShape group = new GroupShape(doc);

 Assert.assertEquals(WrapType.NONE, group.getWrapType());

 // Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
 group.setBounds(new Rectangle2D.Float(0f, 0f, 400f, 400f));

 // Set the group's internal coordinate plane size to 500 x 500pt.
 // The top left corner of the group will have an x and y coordinate of (0, 0),
 // and the bottom right corner will have an x and y coordinate of (500, 500).
 group.setCoordSize(new Dimension(500, 500));

 // Set the coordinates of the top left corner of the group to (-250, -250).
 // The group's center will now have an x and y coordinate value of (0, 0),
 // and the bottom right corner will be at (250, 250).
 group.setCoordOrigin(new Point(-250, -250));

 Shape rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(group.getCoordSize().width);
 rectangleShape.setHeight(group.getCoordSize().height);
 rectangleShape.setLeft(group.getCoordOrigin().x);
 rectangleShape.setTop(group.getCoordOrigin().y);

 // Create a rectangle that will display the boundary of this group shape and add it to the group.
 group.appendChild(rectangleShape);

 // Once a shape is a part of a group shape, we can access it as a child node and then modify it.
 ((Shape) group.getChild(NodeType.SHAPE, 0, true)).getStroke().setDashStyle(DashStyle.DASH);

 Shape starShape = new Shape(doc, ShapeType.STAR);
 starShape.setWidth(20.0);
 starShape.setHeight(20.0);
 starShape.setLeft(-10);
 starShape.setTop(-10);
 starShape.setFillColor(Color.RED);

 // Create a small red star and insert it into the group.
 // Line up the shape with the group's coordinate origin, which we have moved to the center.
 group.appendChild(starShape);

 rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(250.0);
 rectangleShape.setHeight(250.0);
 rectangleShape.setLeft(-250);
 rectangleShape.setTop(-250);
 rectangleShape.setFillColor(Color.BLUE);

 // Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
 // Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
 // and then the shape with the image will overlap the light blue rectangle, using it as a frame.
 // We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
 group.appendChild(rectangleShape);

 Shape imageShape = new Shape(doc, ShapeType.IMAGE);
 imageShape.setWidth(200.0);
 imageShape.setHeight(200.0);
 imageShape.setLeft(-225);
 imageShape.setTop(-225);

 group.appendChild(imageShape);

 ((Shape) group.getChild(NodeType.SHAPE, 3, true)).getImageData().setImage(getImageDir() + "Logo.jpg");

 Shape textboxShape = new Shape(doc, ShapeType.TEXT_BOX);
 textboxShape.setWidth(200.0);
 textboxShape.setHeight(50.0);
 textboxShape.setLeft(group.getCoordSize().width + new Point(group.getCoordOrigin()).x - 200);
 textboxShape.setTop(group.getCoordSize().height + new Point(group.getCoordOrigin()).y);

 // Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
 // touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
 // the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
 group.appendChild(textboxShape);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(group);
 builder.moveTo(((Shape) group.getChild(NodeType.SHAPE, 4, true)).appendChild(new Paragraph(doc)));
 builder.write("Hello world!");

 doc.save(getArtifactsDir() + "Shape.GroupShape.docx");
 
```

**Returns:**
java.awt.Point - The corresponding java.awt.Point value.
### getCoordSize() {#getCoordSize}
```
public Dimension getCoordSize()
```


The width and height of the coordinate space inside the containing block of this shape.

 **Remarks:** 

The default value is (1000, 1000).

 **Examples:** 

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```

 Document doc = new Document();

 // Insert a group shape, and place it 100 points below and to the right of
 // the document's x and Y coordinate origin point.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(100f, 100f, 500f, 500f));

 // Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
 // lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
 Assert.assertEquals(new Point2D.Float(100f, 100f), group.localToParent(new Point2D.Float(0f, 0f)));

 // By default, a shape's internal coordinate plane has the top left corner at (0, 0),
 // and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
 // in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
 // to a movement of 2pts on the group shape's coordinate plane.
 Assert.assertEquals(new Point2D.Float(150f, 150f), group.localToParent(new Point2D.Float(100f, 100f)));
 Assert.assertEquals(new Point2D.Float(200f, 200f), group.localToParent(new Point2D.Float(200f, 200f)));
 Assert.assertEquals(new Point2D.Float(250f, 250f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Move the group shape's x and y axis origin from the top left corner to the center.
 // This will offset the group's internal coordinates relative to the document's coordinates even further.
 group.setCoordOrigin(new Point(-250, -250));

 Assert.assertEquals(new Point2D.Float(375f, 375f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Changing the scale of the coordinate plane will also affect relative locations.
 group.setCoordSize(new Dimension(500, 500));

 Assert.assertEquals(new Point2D.Float(650f, 650f), group.localToParent(new Point2D.Float(300f, 300f)));

 // If we wish to add a shape to this group while defining its location based on a location in the document,
 // we will need to first confirm a location in the group shape that will match the document's location.
 Assert.assertEquals(new Point2D.Float(700f, 700f), group.localToParent(new Point2D.Float(350f, 350f)));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 group.appendChild(shape);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 doc.save(getArtifactsDir() + "Shape.LocalToParent.docx");
 
```

Shows how to create and populate a group shape.

```

 Document doc = new Document();

 // Create a group shape. A group shape can display a collection of child shape nodes.
 // In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
 // select all the other child shapes within this group and allow us to scale and move all the shapes at once.
 GroupShape group = new GroupShape(doc);

 Assert.assertEquals(WrapType.NONE, group.getWrapType());

 // Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
 group.setBounds(new Rectangle2D.Float(0f, 0f, 400f, 400f));

 // Set the group's internal coordinate plane size to 500 x 500pt.
 // The top left corner of the group will have an x and y coordinate of (0, 0),
 // and the bottom right corner will have an x and y coordinate of (500, 500).
 group.setCoordSize(new Dimension(500, 500));

 // Set the coordinates of the top left corner of the group to (-250, -250).
 // The group's center will now have an x and y coordinate value of (0, 0),
 // and the bottom right corner will be at (250, 250).
 group.setCoordOrigin(new Point(-250, -250));

 Shape rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(group.getCoordSize().width);
 rectangleShape.setHeight(group.getCoordSize().height);
 rectangleShape.setLeft(group.getCoordOrigin().x);
 rectangleShape.setTop(group.getCoordOrigin().y);

 // Create a rectangle that will display the boundary of this group shape and add it to the group.
 group.appendChild(rectangleShape);

 // Once a shape is a part of a group shape, we can access it as a child node and then modify it.
 ((Shape) group.getChild(NodeType.SHAPE, 0, true)).getStroke().setDashStyle(DashStyle.DASH);

 Shape starShape = new Shape(doc, ShapeType.STAR);
 starShape.setWidth(20.0);
 starShape.setHeight(20.0);
 starShape.setLeft(-10);
 starShape.setTop(-10);
 starShape.setFillColor(Color.RED);

 // Create a small red star and insert it into the group.
 // Line up the shape with the group's coordinate origin, which we have moved to the center.
 group.appendChild(starShape);

 rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(250.0);
 rectangleShape.setHeight(250.0);
 rectangleShape.setLeft(-250);
 rectangleShape.setTop(-250);
 rectangleShape.setFillColor(Color.BLUE);

 // Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
 // Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
 // and then the shape with the image will overlap the light blue rectangle, using it as a frame.
 // We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
 group.appendChild(rectangleShape);

 Shape imageShape = new Shape(doc, ShapeType.IMAGE);
 imageShape.setWidth(200.0);
 imageShape.setHeight(200.0);
 imageShape.setLeft(-225);
 imageShape.setTop(-225);

 group.appendChild(imageShape);

 ((Shape) group.getChild(NodeType.SHAPE, 3, true)).getImageData().setImage(getImageDir() + "Logo.jpg");

 Shape textboxShape = new Shape(doc, ShapeType.TEXT_BOX);
 textboxShape.setWidth(200.0);
 textboxShape.setHeight(50.0);
 textboxShape.setLeft(group.getCoordSize().width + new Point(group.getCoordOrigin()).x - 200);
 textboxShape.setTop(group.getCoordSize().height + new Point(group.getCoordOrigin()).y);

 // Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
 // touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
 // the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
 group.appendChild(textboxShape);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(group);
 builder.moveTo(((Shape) group.getChild(NodeType.SHAPE, 4, true)).appendChild(new Paragraph(doc)));
 builder.write("Hello world!");

 doc.save(getArtifactsDir() + "Shape.GroupShape.docx");
 
```

**Returns:**
java.awt.Dimension - The corresponding java.awt.Dimension value.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of immediate children of this node.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Returns:**
int - The corresponding  int  value.
### getDashStyle() {#getDashStyle}
```
public int getDashStyle()
```




**Returns:**
int
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectShapeAttr(int key) {#getDirectShapeAttr-int}
```
public Object getDirectShapeAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDistance() {#getDistance}
```
public double getDistance()
```




**Returns:**
double
### getDistanceBottom() {#getDistanceBottom}
```
public double getDistanceBottom()
```


Gets the distance (in points) between the document text and the bottom edge of the shape.

 **Remarks:** 

The default value is 0.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Returns:**
double - The distance (in points) between the document text and the bottom edge of the shape.
### getDistanceLeft() {#getDistanceLeft}
```
public double getDistanceLeft()
```


Gets the distance (in points) between the document text and the left edge of the shape.

 **Remarks:** 

The default value is 1/8 inch.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Returns:**
double - The distance (in points) between the document text and the left edge of the shape.
### getDistanceRight() {#getDistanceRight}
```
public double getDistanceRight()
```


Gets the distance (in points) between the document text and the right edge of the shape.

 **Remarks:** 

The default value is 1/8 inch.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Returns:**
double - The distance (in points) between the document text and the right edge of the shape.
### getDistanceTop() {#getDistanceTop}
```
public double getDistanceTop()
```


Gets the distance (in points) between the document text and the top edge of the shape.

 **Remarks:** 

The default value is 0.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Returns:**
double - The distance (in points) between the document text and the top edge of the shape.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

 **Remarks:** 

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

 **Examples:** 

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/)
### getEdgeRadius() {#getEdgeRadius}
```
public double getEdgeRadius()
```




**Returns:**
double
### getEndArrowLength() {#getEndArrowLength}
```
public int getEndArrowLength()
```




**Returns:**
int
### getEndArrowType() {#getEndArrowType}
```
public int getEndArrowType()
```




**Returns:**
int
### getEndArrowWidth() {#getEndArrowWidth}
```
public int getEndArrowWidth()
```




**Returns:**
int
### getEndCap() {#getEndCap}
```
public int getEndCap()
```




**Returns:**
int
### getExtrusionEnabled() {#getExtrusionEnabled}
```
public boolean getExtrusionEnabled()
```


Returns  true  if an extrusion effect is enabled.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
boolean -  true  if an extrusion effect is enabled.
### getFill() {#getFill}
```
public Fill getFill()
```


Gets fill formatting for the shape.

 **Examples:** 

Shows how to fill a shape with a solid color.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the shape.
### getFillColor() {#getFillColor}
```
public Color getFillColor()
```


Defines the brush color that fills the closed path of the shape.

 **Remarks:** 

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) property.

The default value is java.awt.Color\#getWhite().getWhite().

 **Examples:** 

Shows how to fill a shape with a solid color.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getFillType() {#getFillType}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableBackThemeColor() {#getFillableBackThemeColor}
```
public int getFillableBackThemeColor()
```




**Returns:**
int
### getFillableBackTintAndShade() {#getFillableBackTintAndShade}
```
public double getFillableBackTintAndShade()
```




**Returns:**
double
### getFillableBaseForeColor() {#getFillableBaseForeColor}
```
public Color getFillableBaseForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeThemeColor() {#getFillableForeThemeColor}
```
public int getFillableForeThemeColor()
```




**Returns:**
int
### getFillableForeTintAndShade() {#getFillableForeTintAndShade}
```
public double getFillableForeTintAndShade()
```




**Returns:**
double
### getFillableImageBytes() {#getFillableImageBytes}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilled() {#getFilled}
```
public boolean getFilled()
```


Determines whether the closed path of the shape will be filled.

 **Remarks:** 

This is a shortcut to the [Fill.getVisible()](../../com.aspose.words/fill/\#getVisible) / [Fill.setVisible(boolean)](../../com.aspose.words/fill/\#setVisible-boolean) property.

The default value is  true .

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getFilledColor() {#getFilledColor}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node.

 **Remarks:** 

If there is no first child node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFirstParagraph() {#getFirstParagraph}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the shape.

 **Examples:** 

Shows how to create and format a text box.

```

 Document doc = new Document();

 // Create a floating text box.
 Shape textBox = new Shape(doc, ShapeType.TEXT_BOX);
 textBox.setWrapType(WrapType.NONE);
 textBox.setHeight(50.0);
 textBox.setWidth(200.0);

 // Set the horizontal, and vertical alignment of the text inside the shape.
 textBox.setHorizontalAlignment(HorizontalAlignment.CENTER);
 textBox.setVerticalAlignment(VerticalAlignment.TOP);

 // Add a paragraph to the text box and add a run of text that the text box will display.
 textBox.appendChild(new Paragraph(doc));
 Paragraph para = textBox.getFirstParagraph();
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 Run run = new Run(doc);
 run.setText("Hello world!");
 para.appendChild(run);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(textBox);

 doc.save(getArtifactsDir() + "Shape.CreateTextBox.docx");
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The first paragraph in the shape.
### getFlipOrientation() {#getFlipOrientation}
```
public int getFlipOrientation()
```


Switches the orientation of a shape.

 **Remarks:** 

The default value is [FlipOrientation.NONE](../../com.aspose.words/fliporientation/\#NONE).

 **Examples:** 

Shows how to flip a shape on an axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert an image shape and leave its orientation in its default state.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 Assert.assertEquals(FlipOrientation.NONE, shape.getFlipOrientation());

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 250.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
 // making it into a horizontal mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.HORIZONTAL);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 250.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
 // making it into a vertical mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.VERTICAL);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 250.0,
         RelativeVerticalPosition.TOP_MARGIN, 250.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
 // making it into a horizontal and vertical mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.BOTH);

 doc.save(getArtifactsDir() + "Shape.FlipShapeOrientation.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [FlipOrientation](../../com.aspose.words/fliporientation/) constants.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of this object.

 **Examples:** 

Shows how to insert a text box, and set the font of its contents.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 50.0);
 builder.moveTo(shape.getLastParagraph());
 builder.write("This text is inside the text box.");

 // Set the "Hidden" property of the shape's "Font" object to "true" to hide the text box from sight
 // and collapse the space that it would normally occupy.
 // Set the "Hidden" property of the shape's "Font" object to "false" to leave the text box visible.
 shape.getFont().setHidden(hideShape);

 // If the shape is visible, we will modify its appearance via the font object.
 if (!hideShape) {
     shape.getFont().setHighlightColor(Color.LIGHT_GRAY);
     shape.getFont().setColor(Color.RED);
     shape.getFont().setUnderline(Underline.DASH);
 }

 // Move the builder out of the text box back into the main document.
 builder.moveTo(shape.getParentParagraph());

 builder.writeln("\nThis text is outside the text box.");

 doc.save(getArtifactsDir() + "Shape.Font.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getGlow() {#getGlow}
```
public GlowFormat getGlow()
```


Gets glow formatting for the shape.

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
[GlowFormat](../../com.aspose.words/glowformat/) - Glow formatting for the shape.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/)
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```




**Returns:**
int
### getHRef() {#getHRef}
```
public String getHRef()
```


Gets the full hyperlink address for a shape.

 **Remarks:** 

The default value is an empty string.

Below are examples of valid values for this property:

Full URI:  https://www.aspose.com/ .

Full file name:  C:\\\\My Documents\\\\SalesReport.doc .

Relative URI:  ../../../resource.txt 

Relative file name:  ..\\\\My Documents\\\\SalesReport.doc .

Bookmark within another document:  https://www.aspose.com/Products/Default.aspx\#Suites 

Bookmark within this document:  \#BookmakName .

 **Examples:** 

Shows how to insert a shape which contains an image, and is also a hyperlink.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setHRef("https://forum.aspose.com/");
 shape.setTarget("New Window");
 shape.setScreenTip("Aspose.Words Support Forums");

 // Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
 // and take us to the hyperlink in the "HRef" property.
 doc.save(getArtifactsDir() + "Image.InsertImageWithHyperlink.docx");
 
```

**Returns:**
java.lang.String - The full hyperlink address for a shape.
### getHeight() {#getHeight}
```
public double getHeight()
```


Gets the height of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

Shows how to resize a shape with an image.

```

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```

**Returns:**
double - The height of the containing block of the shape.
### getHeightRelative() {#getHeightRelative}
```
public float getHeightRelative()
```


Gets the value that represents the percentage of shape's relative height.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Returns:**
float - The value that represents the percentage of shape's relative height.
### getHidden() {#getHidden}
```
public boolean getHidden()
```


Gets a boolean value indicating whether the shape is visible.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to hide the shape.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 if (!shape.getHidden())
     shape.setHidden(true);

 doc.save(getArtifactsDir() + "Shape.Hidden.docx");
 
```

**Returns:**
boolean - A boolean value indicating whether the shape is visible.
### getHorizontalAlignment() {#getHorizontalAlignment}
```
public int getHorizontalAlignment()
```


Specifies how the shape is positioned horizontally.

 **Remarks:** 

The default value is [HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment/\#NONE).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) constants.
### getHorizontalMargins_ITextBox() {#getHorizontalMargins-ITextBox}
```
public float getHorizontalMargins_ITextBox()
```




**Returns:**
float
### getHorizontalRuleFormat() {#getHorizontalRuleFormat}
```
public HorizontalRuleFormat getHorizontalRuleFormat()
```


Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns  null .

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
[HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat/) - The corresponding [HorizontalRuleFormat](../../com.aspose.words/horizontalruleformat/) value.
### getImageData() {#getImageData}
```
public ImageData getImageData()
```


Provides access to the image of the shape. Returns  null  if the shape cannot have an image.

 **Examples:** 

Shows how to extract images from a document, and save them to the local file system as individual files.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Get the collection of shapes from the document,
 // and save the image data of every shape with an image as a file to the local file system.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 int imageIndex = 0;
 for (Shape shape : (Iterable) shapes) {
     if (shape.hasImage()) {
         // The image data of shapes may contain images of many possible image formats.
         // We can determine a file extension for each image automatically, based on its format.
         String imageFileName = MessageFormat.format("File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil.imageTypeToExtension(shape.getImageData().getImageType()));
         shape.getImageData().save(getArtifactsDir() + imageFileName);
         imageIndex++;
     }
 }
 
```

Shows how to insert a linked image into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Returns:**
[ImageData](../../com.aspose.words/imagedata/) - The corresponding [ImageData](../../com.aspose.words/imagedata/) value.
### getJoinStyle() {#getJoinStyle}
```
public int getJoinStyle()
```




**Returns:**
int
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node.

 **Remarks:** 

If there is no last child node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLastParagraph() {#getLastParagraph}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the shape.

 **Examples:** 

Shows how to set the orientation of text inside a text box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Move the document builder to inside the TextBox and add text.
 builder.moveTo(textBoxShape.getLastParagraph());
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 // Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
 textBox.setLayoutFlow(layoutFlow);

 doc.save(getArtifactsDir() + "Shape.TextBoxLayoutFlow.docx");
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The last paragraph in the shape.
### getLeft() {#getLeft}
```
public double getLeft()
```


Gets the position of the left edge of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - The position of the left edge of the containing block of the shape.
### getLeftRelative() {#getLeftRelative}
```
public float getLeftRelative()
```


Gets the value that represents shape's relative left position in percent.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Returns:**
float - The value that represents shape's relative left position in percent.
### getLineFillType() {#getLineFillType}
```
public int getLineFillType()
```




**Returns:**
int
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```




**Returns:**
int
### getMarkupLanguage() {#getMarkupLanguage}
```
public byte getMarkupLanguage()
```


Gets MarkupLanguage used for this graphic object.

 **Examples:** 

Shows how to verify a shape's size and markup language.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");

 Assert.assertEquals(ShapeMarkupLanguage.DML, shape.getMarkupLanguage());
 Assert.assertEquals(new Point2D.Float(300f, 300f), shape.getSizeInPoints());
 
```

**Returns:**
byte - MarkupLanguage used for this graphic object. The returned value is one of [ShapeMarkupLanguage](../../com.aspose.words/shapemarkuplanguage/) constants.
### getMarkupLanguage_ITextBox() {#getMarkupLanguage-ITextBox}
```
public byte getMarkupLanguage_ITextBox()
```




**Returns:**
byte
### getName() {#getName}
```
public String getName()
```


Gets the optional shape name.

 **Remarks:** 

Default is empty string.

Cannot be  null , but can be an empty string.

 **Examples:** 

Shows how to use a shape's alternative text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertShape(ShapeType.CUBE, 150.0, 150.0);
 shape.setName("MyCube");

 shape.setAlternativeText("Alt text for MyCube.");

 // We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
 doc.save(getArtifactsDir() + "Shape.AltText.docx");

 // Save the document to HTML, and then delete the linked image that belongs to our shape.
 // The browser that is reading our HTML will display the alt text in place of the missing image.
 doc.save(getArtifactsDir() + "Shape.AltText.html");
 new File(getArtifactsDir() + "Shape.AltText.001.png").delete();
 
```

**Returns:**
java.lang.String - The optional shape name.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node.

 **Remarks:** 

If there is no next node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.SHAPE](../../com.aspose.words/nodetype/\#SHAPE).

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
int - [NodeType.SHAPE](../../com.aspose.words/nodetype/\#SHAPE). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getOldOn() {#getOldOn}
```
public boolean getOldOn()
```




**Returns:**
boolean
### getOldOpacity() {#getOldOpacity}
```
public double getOldOpacity()
```




**Returns:**
double
### getOleFormat() {#getOleFormat}
```
public OleFormat getOleFormat()
```


Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns  null .

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
[OleFormat](../../com.aspose.words/oleformat/) - The corresponding [OleFormat](../../com.aspose.words/oleformat/) value.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

 **Remarks:** 

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

 **Examples:** 

Shows how to access a node's parent node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Returns the immediate parent paragraph.

 **Remarks:** 

For child shapes of a group shape and child shapes of an Office Math object always returns  null .

 **Examples:** 

Shows how to insert a text box, and set the font of its contents.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 50.0);
 builder.moveTo(shape.getLastParagraph());
 builder.write("This text is inside the text box.");

 // Set the "Hidden" property of the shape's "Font" object to "true" to hide the text box from sight
 // and collapse the space that it would normally occupy.
 // Set the "Hidden" property of the shape's "Font" object to "false" to leave the text box visible.
 shape.getFont().setHidden(hideShape);

 // If the shape is visible, we will modify its appearance via the font object.
 if (!hideShape) {
     shape.getFont().setHighlightColor(Color.LIGHT_GRAY);
     shape.getFont().setColor(Color.RED);
     shape.getFont().setUnderline(Underline.DASH);
 }

 // Move the builder out of the text box back into the main document.
 builder.moveTo(shape.getParentParagraph());

 builder.writeln("\nThis text is outside the text box.");

 doc.save(getArtifactsDir() + "Shape.Font.docx");
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The immediate parent paragraph.
### getParentParagraph_IInline() {#getParentParagraph-IInline}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph/)
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```




**Returns:**
int
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node.

 **Remarks:** 

If there is no preceding node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRadius() {#getRadius}
```
public double getRadius()
```




**Returns:**
double
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

 **Examples:** 

Shows how to delete all the nodes from a range.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getReflection() {#getReflection}
```
public ReflectionFormat getReflection()
```


Gets reflection formatting for the shape.

 **Examples:** 

Shows how to interact with reflection shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
[ReflectionFormat](../../com.aspose.words/reflectionformat/) - Reflection formatting for the shape.
### getReflectionSize() {#getReflectionSize}
```
public double getReflectionSize()
```




**Returns:**
double
### getReflectionTransparency() {#getReflectionTransparency}
```
public double getReflectionTransparency()
```




**Returns:**
double
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition}
```
public int getRelativeHorizontalPosition()
```


Specifies relative to what the shape is positioned horizontally.

 **Remarks:** 

The default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/) constants.
### getRelativeHorizontalSize() {#getRelativeHorizontalSize}
```
public int getRelativeHorizontalSize()
```


Gets the value of shape's relative size in horizontal direction.

 **Remarks:** 

The default value is [RelativeHorizontalSize](../../com.aspose.words/relativehorizontalsize/).

Has effect only if [getWidthRelative()](../../com.aspose.words/shapebase/\#getWidthRelative) / [setWidthRelative(float)](../../com.aspose.words/shapebase/\#setWidthRelative-float) is set.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Returns:**
int - The value of shape's relative size in horizontal direction. The returned value is one of [RelativeHorizontalSize](../../com.aspose.words/relativehorizontalsize/) constants.
### getRelativeVerticalPosition() {#getRelativeVerticalPosition}
```
public int getRelativeVerticalPosition()
```


Specifies relative to what the shape is positioned vertically.

 **Remarks:** 

The default value is [RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/) constants.
### getRelativeVerticalSize() {#getRelativeVerticalSize}
```
public int getRelativeVerticalSize()
```


Gets the value of shape's relative size in vertical direction.

 **Remarks:** 

The default value is [RelativeVerticalSize.MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

Has effect only if [getHeightRelative()](../../com.aspose.words/shapebase/\#getHeightRelative) / [setHeightRelative(float)](../../com.aspose.words/shapebase/\#setHeightRelative-float) is set.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Returns:**
int - The value of shape's relative size in vertical direction. The returned value is one of [RelativeVerticalSize](../../com.aspose.words/relativeverticalsize/) constants.
### getRight() {#getRight}
```
public double getRight()
```


Gets the position of the right edge of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - The position of the right edge of the containing block of the shape.
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getRotation() {#getRotation}
```
public double getRotation()
```


Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

 **Remarks:** 

The default value is 0.

 **Examples:** 

Shows how to insert and rotate an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape with an image.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 Assert.assertTrue(shape.canHaveImage());
 Assert.assertTrue(shape.hasImage());

 // Rotate the image 45 degrees clockwise.
 shape.setRotation(45.0);

 doc.save(getArtifactsDir() + "Shape.Rotate.docx");
 
```

**Returns:**
double - The corresponding  double  value.
### getScreenTip() {#getScreenTip}
```
public String getScreenTip()
```


Defines the text displayed when the mouse pointer moves over the shape.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to insert a shape which contains an image, and is also a hyperlink.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setHRef("https://forum.aspose.com/");
 shape.setTarget("New Window");
 shape.setScreenTip("Aspose.Words Support Forums");

 // Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
 // and take us to the hyperlink in the "HRef" property.
 doc.save(getArtifactsDir() + "Image.InsertImageWithHyperlink.docx");
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getShadowColors() {#getShadowColors}
```
public Color getShadowColors()
```




**Returns:**
java.awt.Color
### getShadowEnabled() {#getShadowEnabled}
```
public boolean getShadowEnabled()
```


Returns  true  if a shadow effect is enabled.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
boolean -  true  if a shadow effect is enabled.
### getShadowFormat() {#getShadowFormat}
```
public ShadowFormat getShadowFormat()
```


Gets shadow formatting for the shape.

 **Examples:** 

Shows how to get shadow color.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
[ShadowFormat](../../com.aspose.words/shadowformat/) - Shadow formatting for the shape.
### getShadowType() {#getShadowType}
```
public int getShadowType()
```




**Returns:**
int
### getShapeRenderer() {#getShapeRenderer}
```
public ShapeRenderer getShapeRenderer()
```


Creates and returns an object that can be used to render this shape into an image.

 **Remarks:** 

This method just invokes the [ShapeRenderer](../../com.aspose.words/shaperenderer/) constructor and passes this object as a parameter.

 **Examples:** 

Shows how to use a shape renderer to export shapes to files in the local file system.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 Assert.assertEquals(7, shapes.getCount());

 // There are 7 shapes in the document, including one group shape with 2 child shapes.
 // We will render every shape to an image file in the local file system
 // while ignoring the group shapes since they have no appearance.
 // This will produce 6 image files.
 for (Shape shape : (Iterable) doc.getChildNodes(NodeType.SHAPE, true)) {
     ShapeRenderer renderer = shape.getShapeRenderer();
     ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
     renderer.save(getArtifactsDir() + MessageFormat.format("Shape.RenderAllShapes.{0}.png", shape.getName()), options);
 }
 
```

**Returns:**
[ShapeRenderer](../../com.aspose.words/shaperenderer/) - The renderer object for this shape.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```


Gets the shape type.

 **Examples:** 

Shows how to create a group of shapes, and print its contents using a document visitor.

```

 public void groupOfShapes() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
     // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
     // please use DocumentBuilder.InsertShape methods.
     Shape balloon = new Shape(doc, ShapeType.BALLOON);
     balloon.setWidth(200.0);
     balloon.setHeight(200.0);
     balloon.setStrokeColor(Color.RED);

     Shape cube = new Shape(doc, ShapeType.CUBE);
     cube.setWidth(100.0);
     cube.setHeight(100.0);
     cube.setStrokeColor(Color.BLUE);

     GroupShape group = new GroupShape(doc);
     group.appendChild(balloon);
     group.appendChild(cube);

     Assert.assertTrue(group.isGroup());
     builder.insertNode(group);

     ShapeInfoPrinter printer = new ShapeInfoPrinter();
     group.accept(printer);

     System.out.println(printer.getText());
 }

 /// 
 /// Prints the contents of a visited shape group to the console.
 /// 
 public static class ShapeInfoPrinter extends DocumentVisitor {
     public ShapeInfoPrinter() {
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public int visitGroupShapeStart(final GroupShape groupShape) {
         mBuilder.append("Shape group started:\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGroupShapeEnd(final GroupShape groupShape) {
         mBuilder.append("End of shape group\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeStart(final Shape shape) {
         mBuilder.append("\tShape - " + shape.getShapeType() + ":\r\n");
         mBuilder.append("\t\tWidth: " + shape.getWidth() + "\r\n");
         mBuilder.append("\t\tHeight: " + shape.getHeight() + "\r\n");
         mBuilder.append("\t\tStroke color: " + shape.getStroke().getColor() + "\r\n");
         mBuilder.append("\t\tFill color: " + shape.getFill().getForeColor() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeEnd(final Shape shape) {
         mBuilder.append("\tEnd of shape\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
int - The shape type. The returned value is one of [ShapeType](../../com.aspose.words/shapetype/) constants.
### getSignatureLine() {#getSignatureLine}
```
public SignatureLine getSignatureLine()
```


Gets [SignatureLine](../../com.aspose.words/signatureline/) object if the shape is a signature line. Returns  null  otherwise.

 **Remarks:** 

You can insert new [SignatureLine](../../com.aspose.words/signatureline/) into the document using [DocumentBuilder.insertSignatureLine(com.aspose.words.SignatureLineOptions)](../../com.aspose.words/documentbuilder/\#insertSignatureLine-com.aspose.words.SignatureLineOptions) and

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**M:Aspose.Words.DocumentBuilder.InsertSignatureLine(Aspose.Words.SignatureLineOptions,Aspose.Words.Drawing.RelativeHorizontalPosition,System.Double,Aspose.Words.Drawing.RelativeVerticalPosition,System.Double,Aspose.Words.Drawing.WrapType)**

**Returns:**
[SignatureLine](../../com.aspose.words/signatureline/) - [SignatureLine](../../com.aspose.words/signatureline/) object if the shape is a signature line.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Gets the size of the shape in points.  Gets the size of the shape in points.

 **Remarks:** 

Point2D.Float is used as return type because we need in float dimension values here. One should to assume that Point2D's *x == width* and *y == height*.

 **Examples:** 

Shows how to verify a shape's size and markup language.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");

 Assert.assertEquals(ShapeMarkupLanguage.DML, shape.getMarkupLanguage());
 Assert.assertEquals(new Point2D.Float(300f, 300f), shape.getSizeInPoints());
 
```

**Returns:**
java.awt.geom.Point2D.Float - The size of the shape in points.
### getSoftEdge() {#getSoftEdge}
```
public SoftEdgeFormat getSoftEdge()
```


Gets soft edge formatting for the shape.

 **Examples:** 

Shows how to set limit for image resolution.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

Shows how to work with soft edge formatting.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

**Returns:**
[SoftEdgeFormat](../../com.aspose.words/softedgeformat/) - Soft edge formatting for the shape.
### getStartArrowLength() {#getStartArrowLength}
```
public int getStartArrowLength()
```




**Returns:**
int
### getStartArrowType() {#getStartArrowType}
```
public int getStartArrowType()
```




**Returns:**
int
### getStartArrowWidth() {#getStartArrowWidth}
```
public int getStartArrowWidth()
```




**Returns:**
int
### getStoryType() {#getStoryType}
```
public int getStoryType()
```


Returns [StoryType.TEXTBOX](../../com.aspose.words/storytype/\#TEXTBOX).

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
int - [StoryType.TEXTBOX](../../com.aspose.words/storytype/\#TEXTBOX). The returned value is one of [StoryType](../../com.aspose.words/storytype/) constants.
### getStroke() {#getStroke}
```
public Stroke getStroke()
```


Defines a stroke for a shape.

 **Examples:** 

Shows to create a variety of shapes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are four examples of shapes that we can insert into our documents.
 // 1 -  Dotted, horizontal, half-transparent red line
 // with an arrow on the left end and a diamond on the right end:
 Shape arrow = new Shape(doc, ShapeType.LINE);
 arrow.setWidth(200.0);
 arrow.getStroke().setColor(Color.RED);
 arrow.getStroke().setStartArrowType(ArrowType.ARROW);
 arrow.getStroke().setStartArrowLength(ArrowLength.LONG);
 arrow.getStroke().setStartArrowWidth(ArrowWidth.WIDE);
 arrow.getStroke().setEndArrowType(ArrowType.DIAMOND);
 arrow.getStroke().setEndArrowLength(ArrowLength.LONG);
 arrow.getStroke().setEndArrowWidth(ArrowWidth.WIDE);
 arrow.getStroke().setDashStyle(DashStyle.DASH);
 arrow.getStroke().setOpacity(0.5);

 Assert.assertEquals(arrow.getStroke().getJoinStyle(), JoinStyle.MITER);

 builder.insertNode(arrow);

 // 2 -  Thick black diagonal line with rounded ends:
 Shape line = new Shape(doc, ShapeType.LINE);
 line.setTop(40.0);
 line.setWidth(200.0);
 line.setHeight(20.0);
 line.setStrokeWeight(5.0);
 line.getStroke().setEndCap(EndCap.ROUND);

 builder.insertNode(line);

 // 3 -  Arrow with a green fill:
 Shape filledInArrow = new Shape(doc, ShapeType.ARROW);
 filledInArrow.setWidth(200.0);
 filledInArrow.setHeight(40.0);
 filledInArrow.setTop(100.0);
 filledInArrow.getFill().setForeColor(Color.GREEN);
 filledInArrow.getFill().setVisible(true);

 builder.insertNode(filledInArrow);

 // 4 -  Arrow with a flipped orientation filled in with the Aspose logo:
 Shape filledInArrowImg = new Shape(doc, ShapeType.ARROW);
 filledInArrowImg.setWidth(200.0);
 filledInArrowImg.setHeight(40.0);
 filledInArrowImg.setTop(160.0);
 filledInArrowImg.setFlipOrientation(FlipOrientation.BOTH);

 BufferedImage image = ImageIO.read(getAsposelogoUri().toURL().openStream());
 Graphics2D graphics2D = image.createGraphics();

 // When we flip the orientation of our arrow, we also flip the image that the arrow contains.
 // Flip the image the other way to cancel this out before getting the shape to display it.
 AffineTransform at = new AffineTransform();
 at.concatenate(AffineTransform.getScaleInstance(1, -1));
 at.concatenate(AffineTransform.getTranslateInstance(0, -image.getHeight()));
 graphics2D.transform(at);
 graphics2D.drawImage(image, 0, 0, null);
 graphics2D.dispose();

 filledInArrowImg.getImageData().setImage(image);
 builder.insertNode(filledInArrowImg);

 doc.save(getArtifactsDir() + "Drawing.VariousShapes.docx");
 
```

**Returns:**
[Stroke](../../com.aspose.words/stroke/) - The corresponding [Stroke](../../com.aspose.words/stroke/) value.
### getStrokeBackThemeColor() {#getStrokeBackThemeColor}
```
public int getStrokeBackThemeColor()
```




**Returns:**
int
### getStrokeBackTintAndShade() {#getStrokeBackTintAndShade}
```
public double getStrokeBackTintAndShade()
```




**Returns:**
double
### getStrokeColor() {#getStrokeColor}
```
public Color getStrokeColor()
```


Defines the color of a stroke.

 **Remarks:** 

This is a shortcut to the [Stroke.getColor()](../../com.aspose.words/stroke/\#getColor) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke/\#setColor-java.awt.Color) property.

The default value is java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Shows how to fill a shape with a solid color.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getStrokeForeThemeColor() {#getStrokeForeThemeColor}
```
public int getStrokeForeThemeColor()
```




**Returns:**
int
### getStrokeForeTintAndShade() {#getStrokeForeTintAndShade}
```
public double getStrokeForeTintAndShade()
```




**Returns:**
double
### getStrokeImageBytes() {#getStrokeImageBytes}
```
public byte[] getStrokeImageBytes()
```




**Returns:**
byte[]
### getStrokeTransparency() {#getStrokeTransparency}
```
public double getStrokeTransparency()
```




**Returns:**
double
### getStrokeVisible() {#getStrokeVisible}
```
public boolean getStrokeVisible()
```




**Returns:**
boolean
### getStrokeWeight() {#getStrokeWeight}
```
public double getStrokeWeight()
```


Defines the brush thickness that strokes the path of a shape in points.

 **Remarks:** 

This is a shortcut to the [Stroke.getWeight()](../../com.aspose.words/stroke/\#getWeight) / [Stroke.setWeight(double)](../../com.aspose.words/stroke/\#setWeight-double) property.

The default value is 0.75.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
double - The corresponding  double  value.
### getStroked() {#getStroked}
```
public boolean getStroked()
```


Defines whether the path will be stroked.

 **Remarks:** 

This is a shortcut to the [Stroke.getOn()](../../com.aspose.words/stroke/\#getOn) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke/\#setOn-boolean) property.

The default value is  true .

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getTarget() {#getTarget}
```
public String getTarget()
```


Gets the target frame for the shape hyperlink.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to insert a shape which contains an image, and is also a hyperlink.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setHRef("https://forum.aspose.com/");
 shape.setTarget("New Window");
 shape.setScreenTip("Aspose.Words Support Forums");

 // Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
 // and take us to the hyperlink in the "HRef" property.
 doc.save(getArtifactsDir() + "Image.InsertImageWithHyperlink.docx");
 
```

**Returns:**
java.lang.String - The target frame for the shape hyperlink.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

 **Remarks:** 

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Shows the difference between calling the GetText and ToString methods on a node.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD Field");

 // GetText will retrieve the visible text as well as field codes and special characters.
 Assert.assertEquals("MERGEFIELD Field«Field»\f", doc.getText());

 // ToString will give us the document's appearance if saved to a passed save format.
 Assert.assertEquals("«Field»\r\n", doc.toString(SaveFormat.TEXT));
 
```

Shows how to output all paragraphs in a document that are list items.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
java.lang.String
### getTextBox() {#getTextBox}
```
public TextBox getTextBox()
```


Defines attributes that specify how text is displayed in a shape.

 **Examples:** 

Shows how to set the orientation of text inside a text box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 100.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Move the document builder to inside the TextBox and add text.
 builder.moveTo(textBoxShape.getLastParagraph());
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 // Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
 textBox.setLayoutFlow(layoutFlow);

 doc.save(getArtifactsDir() + "Shape.TextBoxLayoutFlow.docx");
 
```

**Returns:**
[TextBox](../../com.aspose.words/textbox/) - The corresponding [TextBox](../../com.aspose.words/textbox/) value.
### getTextBoxWrapMode_ITextBox() {#getTextBoxWrapMode-ITextBox}
```
public int getTextBoxWrapMode_ITextBox()
```




**Returns:**
int
### getTextPath() {#getTextPath}
```
public TextPath getTextPath()
```


Defines the text of the text path (of a WordArt object).

 **Examples:** 

Shows how to work with WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
[TextPath](../../com.aspose.words/textpath/) - The corresponding [TextPath](../../com.aspose.words/textpath/) value.
### getTextboxLayoutFlow_ITextBox() {#getTextboxLayoutFlow-ITextBox}
```
public int getTextboxLayoutFlow_ITextBox()
```




**Returns:**
int
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getTitle() {#getTitle}
```
public String getTitle()
```


Gets the title (caption) of the current shape object.

 **Remarks:** 

Default is empty string.

Cannot be  null , but can be an empty string.

 **Examples:** 

Shows how to set the title of a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a shape, give it a title, and then add it to the document.
 Shape shape = new Shape(doc, ShapeType.CUBE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 shape.setTitle("My cube");

 builder.insertNode(shape);

 // When we save a document with a shape that has a title,
 // Aspose.Words will store that title in the shape's Alt Text.
 doc.save(getArtifactsDir() + "Shape.Title.docx");

 doc = new Document(getArtifactsDir() + "Shape.Title.docx");
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("", shape.getTitle());
 Assert.assertEquals("Title: My cube", shape.getAlternativeText());
 
```

**Returns:**
java.lang.String - The title (caption) of the current shape object.
### getTop() {#getTop}
```
public double getTop()
```


Gets the position of the top edge of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - The position of the top edge of the containing block of the shape.
### getTopRelative() {#getTopRelative}
```
public float getTopRelative()
```


Gets the value that represents shape's relative top position in percent.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Returns:**
float - The value that represents shape's relative top position in percent.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```




**Returns:**
double
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Specifies how the shape is positioned vertically.

 **Remarks:** 

The default value is [VerticalAlignment.NONE](../../com.aspose.words/verticalalignment/\#NONE).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment/) constants.
### getVisible() {#getVisible}
```
public boolean getVisible()
```




**Returns:**
boolean
### getWeight() {#getWeight}
```
public double getWeight()
```




**Returns:**
double
### getWidth() {#getWidth}
```
public double getWidth()
```


Gets the width of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

Shows how to resize a shape with an image.

```

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```

**Returns:**
double - The width of the containing block of the shape.
### getWidthRelative() {#getWidthRelative}
```
public float getWidthRelative()
```


Gets the value that represents the percentage of shape's relative width.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Returns:**
float - The value that represents the percentage of shape's relative width.
### getWrapSide() {#getWrapSide}
```
public int getWrapSide()
```


Specifies how the text is wrapped around the shape.

 **Remarks:** 

The default value is [WrapSide.BOTH](../../com.aspose.words/wrapside/\#BOTH).

Has effect only for top level shapes.

 **Examples:** 

Shows how to replace all textbox shapes with image shapes.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [WrapSide](../../com.aspose.words/wrapside/) constants.
### getWrapType() {#getWrapType}
```
public int getWrapType()
```


Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.

 **Remarks:** 

The default value is [WrapType.NONE](../../com.aspose.words/wraptype/\#NONE).

Has effect only for top level shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

Shows how to create and format a text box.

```

 Document doc = new Document();

 // Create a floating text box.
 Shape textBox = new Shape(doc, ShapeType.TEXT_BOX);
 textBox.setWrapType(WrapType.NONE);
 textBox.setHeight(50.0);
 textBox.setWidth(200.0);

 // Set the horizontal, and vertical alignment of the text inside the shape.
 textBox.setHorizontalAlignment(HorizontalAlignment.CENTER);
 textBox.setVerticalAlignment(VerticalAlignment.TOP);

 // Add a paragraph to the text box and add a run of text that the text box will display.
 textBox.appendChild(new Paragraph(doc));
 Paragraph para = textBox.getFirstParagraph();
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 Run run = new Run(doc);
 run.setText("Hello world!");
 para.appendChild(run);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(textBox);

 doc.save(getArtifactsDir() + "Shape.CreateTextBox.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [WrapType](../../com.aspose.words/wraptype/) constants.
### getZOrder() {#getZOrder}
```
public int getZOrder()
```


Determines the display order of overlapping shapes.

 **Remarks:** 

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main text of the document.

The display order of child shapes in a group shape is determined by their order inside the group shape.

 **Examples:** 

Shows how to manipulate the order of shapes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert three different colored rectangles that partially overlap each other.
 // When we insert a shape that overlaps another shape, Aspose.Words places the newer shape on top of the old one.
 // The light green rectangle will overlap the light blue rectangle and partially obscure it,
 // and the light blue rectangle will obscure the orange rectangle.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);
 shape.setFillColor(Color.ORANGE);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 150.0,
         RelativeVerticalPosition.TOP_MARGIN, 150.0, 200.0, 200.0, WrapType.NONE);
 shape.setFillColor(Color.BLUE);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 200.0,
         RelativeVerticalPosition.TOP_MARGIN, 200.0, 200.0, 200.0, WrapType.NONE);
 shape.setFillColor(Color.GREEN);

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 // The "ZOrder" property of a shape determines its stacking priority among other overlapping shapes.
 // If two overlapping shapes have different "ZOrder" values,
 // Microsoft Word will place the shape with a higher value over the shape with the lower value.
 // Set the "ZOrder" values of our shapes to place the first orange rectangle over the second light blue one
 // and the second light blue rectangle over the third light green rectangle.
 // This will reverse their original stacking order.
 shapeList.get(0).setZOrder(3);
 shapeList.get(1).setZOrder(2);
 shapeList.get(2).setZOrder(1);

 doc.save(getArtifactsDir() + "Shape.ZOrder.docx");
 
```

**Returns:**
int - The corresponding  int  value.
### getZOrder_IShape() {#getZOrder-IShape}
```
public int getZOrder_IShape()
```




**Returns:**
int
### hasChart() {#hasChart}
```
public boolean hasChart()
```


Returns  true  if this [Shape](../../com.aspose.words/shape/) has a [Chart](../../com.aspose.words/chart/).

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Returns:**
boolean -  true  if this [Shape](../../com.aspose.words/shape/) has a [Chart](../../com.aspose.words/chart/).
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

 **Examples:** 

Shows how to combine the rows from two tables into one.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
boolean -  true  if this node has any child nodes.
### hasImage() {#hasImage}
```
public boolean hasImage()
```


Returns  true  if the shape has image bytes or links an image.

 **Examples:** 

Shows how to delete all shapes with images from a document.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

Shows how to extract images from a document, and save them to the local file system as individual files.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Get the collection of shapes from the document,
 // and save the image data of every shape with an image as a file to the local file system.
 NodeCollection shapes = doc.getChildNodes(NodeType.SHAPE, true);

 int imageIndex = 0;
 for (Shape shape : (Iterable) shapes) {
     if (shape.hasImage()) {
         // The image data of shapes may contain images of many possible image formats.
         // We can determine a file extension for each image automatically, based on its format.
         String imageFileName = MessageFormat.format("File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil.imageTypeToExtension(shape.getImageData().getImageType()));
         shape.getImageData().save(getArtifactsDir() + imageFileName);
         imageIndex++;
     }
 }
 
```

**Returns:**
boolean -  true  if the shape has image bytes or links an image.
### hasSmartArt() {#hasSmartArt}
```
public boolean hasSmartArt()
```


Returns  true  if this [Shape](../../com.aspose.words/shape/) has a SmartArt object.

 **Examples:** 

Shows how to count the number of shapes in a document with SmartArt objects.

```

 Document doc = new Document(getMyDir() + "SmartArt.docx");

 int count = 0;
 for (Shape shape : (Iterable) doc.getChildNodes(NodeType.SHAPE, true)) {
     if (shape.hasSmartArt())
         count++;
 }

 Assert.assertEquals(2, count);
 
```

**Returns:**
boolean -  true  if this [Shape](../../com.aspose.words/shape/) has a SmartArt object.
### hasVerticalTextFlow_ITextBox() {#hasVerticalTextFlow-ITextBox}
```
public boolean hasVerticalTextFlow_ITextBox()
```




**Returns:**
boolean
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array.

 **Remarks:** 

Returns -1 if the node is not found in the child nodes.

 **Examples:** 

Shows how to get the index of a given child node from its parent.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

 **Remarks:** 

If  refChild  is  null , inserts  newChild  at the beginning of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to replace all textbox shapes with image shapes.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed after the  refChild . |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

 **Remarks:** 

If  refChild  is  null , inserts  newChild  at the end of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  as this node can have child nodes.
### isDecorative() {#isDecorative}
```
public boolean isDecorative()
```


Gets the flag that specifies whether the shape is decorative in the document.

 **Remarks:** 

Note that shape having not empty [getAlternativeText()](../../com.aspose.words/shapebase/\#getAlternativeText) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase/\#setAlternativeText-java.lang.String) cannot be decorative.

 **Examples:** 

Shows how to set that the shape is decorative.

```

 Document doc = new Document(getMyDir() + "Decorative shapes.docx");

 Shape shape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(shape.isDecorative());

 // If "AlternativeText" is not empty, the shape cannot be decorative.
 // That's why our value has changed to 'false'.
 shape.setAlternativeText("Alternative text.");
 Assert.assertFalse(shape.isDecorative());

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.moveToDocumentEnd();
 // Create a new shape as decorative.
 shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 100.0);
 shape.isDecorative(true);

 doc.save(getArtifactsDir() + "Shape.IsDecorative.docx");
 
```

**Returns:**
boolean - The flag that specifies whether the shape is decorative in the document.
### isDecorative(boolean value) {#isDecorative-boolean}
```
public void isDecorative(boolean value)
```


Sets the flag that specifies whether the shape is decorative in the document.

 **Remarks:** 

Note that shape having not empty [getAlternativeText()](../../com.aspose.words/shapebase/\#getAlternativeText) / [setAlternativeText(java.lang.String)](../../com.aspose.words/shapebase/\#setAlternativeText-java.lang.String) cannot be decorative.

 **Examples:** 

Shows how to set that the shape is decorative.

```

 Document doc = new Document(getMyDir() + "Decorative shapes.docx");

 Shape shape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(shape.isDecorative());

 // If "AlternativeText" is not empty, the shape cannot be decorative.
 // That's why our value has changed to 'false'.
 shape.setAlternativeText("Alternative text.");
 Assert.assertFalse(shape.isDecorative());

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.moveToDocumentEnd();
 // Create a new shape as decorative.
 shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 100.0);
 shape.isDecorative(true);

 doc.save(getArtifactsDir() + "Shape.IsDecorative.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The flag that specifies whether the shape is decorative in the document. |

### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to work with revision shapes.

```

 Document doc = new Document();

 Assert.assertFalse(doc.getTrackRevisions());

 // Insert an inline shape without tracking revisions, which will make this shape not a revision of any kind.
 Shape shape = new Shape(doc, ShapeType.CUBE);
 shape.setWrapType(WrapType.INLINE);
 shape.setWidth(100.0);
 shape.setHeight(100.0);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 // Start tracking revisions and then insert another shape, which will be a revision.
 doc.startTrackRevisions("John Doe");

 shape = new Shape(doc, ShapeType.SUN);
 shape.setWrapType(WrapType.INLINE);
 shape.setWidth(100.0);
 shape.setHeight(100.0);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());
 Assert.assertEquals(shapeList.size(), 2);

 Shape firstShape = shapeList.get(0);
 firstShape.remove();

 // Since we removed that shape while we were tracking changes,
 // the shape persists in the document and counts as a delete revision.
 // Accepting this revision will remove the shape permanently, and rejecting it will keep it in the document.
 Assert.assertEquals(ShapeType.CUBE, shapeList.get(0).getShapeType());
 Assert.assertTrue(shapeList.get(0).isDeleteRevision());

 // And we inserted another shape while tracking changes, so that shape will count as an insert revision.
 // Accepting this revision will assimilate this shape into the document as a non-revision,
 // and rejecting the revision will remove this shape permanently.
 Assert.assertEquals(ShapeType.SUN, shapeList.get(1).getShapeType());
 Assert.assertTrue(shapeList.get(1).isInsertRevision());
 
```

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isGroup() {#isGroup}
```
public boolean isGroup()
```


Returns  true  if this is a group shape.

 **Examples:** 

Shows how to create a group of shapes, and print its contents using a document visitor.

```

 public void groupOfShapes() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
     // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
     // please use DocumentBuilder.InsertShape methods.
     Shape balloon = new Shape(doc, ShapeType.BALLOON);
     balloon.setWidth(200.0);
     balloon.setHeight(200.0);
     balloon.setStrokeColor(Color.RED);

     Shape cube = new Shape(doc, ShapeType.CUBE);
     cube.setWidth(100.0);
     cube.setHeight(100.0);
     cube.setStrokeColor(Color.BLUE);

     GroupShape group = new GroupShape(doc);
     group.appendChild(balloon);
     group.appendChild(cube);

     Assert.assertTrue(group.isGroup());
     builder.insertNode(group);

     ShapeInfoPrinter printer = new ShapeInfoPrinter();
     group.accept(printer);

     System.out.println(printer.getText());
 }

 /// 
 /// Prints the contents of a visited shape group to the console.
 /// 
 public static class ShapeInfoPrinter extends DocumentVisitor {
     public ShapeInfoPrinter() {
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public int visitGroupShapeStart(final GroupShape groupShape) {
         mBuilder.append("Shape group started:\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGroupShapeEnd(final GroupShape groupShape) {
         mBuilder.append("End of shape group\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeStart(final Shape shape) {
         mBuilder.append("\tShape - " + shape.getShapeType() + ":\r\n");
         mBuilder.append("\t\tWidth: " + shape.getWidth() + "\r\n");
         mBuilder.append("\t\tHeight: " + shape.getHeight() + "\r\n");
         mBuilder.append("\t\tStroke color: " + shape.getStroke().getColor() + "\r\n");
         mBuilder.append("\t\tFill color: " + shape.getFill().getForeColor() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeEnd(final Shape shape) {
         mBuilder.append("\tEnd of shape\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
boolean -  true  if this is a group shape.
### isHorizontalRule() {#isHorizontalRule}
```
public boolean isHorizontalRule()
```


Returns  true  if this shape is a horizontal rule.

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean -  true  if this shape is a horizontal rule.
### isImage() {#isImage}
```
public boolean isImage()
```


Returns  true  if this shape is an image shape.

 **Examples:** 

Shows how to open an HTML document with images from a stream using a base URI.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Returns:**
boolean -  true  if this shape is an image shape.
### isInline() {#isInline}
```
public boolean isInline()
```


A quick way to determine if this shape is positioned inline with text.

 **Remarks:** 

Has effect only for top level shapes.

 **Examples:** 

Shows how to determine whether a shape is inline or floating.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two wrapping types that shapes may have.
 // 1 -  Inline:
 builder.write("Hello world! ");
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 100.0);
 shape.setFillColor(Color.BLUE);
 builder.write(" Hello again.");

 // An inline shape sits inside a paragraph among other paragraph elements, such as runs of text.
 // In Microsoft Word, we may click and drag the shape to any paragraph as if it is a character.
 // If the shape is large, it will affect vertical paragraph spacing.
 // We cannot move this shape to a place with no paragraph.
 Assert.assertEquals(WrapType.INLINE, shape.getWrapType());
 Assert.assertTrue(shape.isInline());

 // 2 -  Floating:
 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 200.0,
         RelativeVerticalPosition.TOP_MARGIN, 200.0, 100.0, 100.0, WrapType.NONE);
 shape.setFillColor(Color.ORANGE);

 // A floating shape belongs to the paragraph that we insert it into,
 // which we can determine by an anchor symbol that appears when we click the shape.
 // If the shape does not have a visible anchor symbol to its left,
 // we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
 // In Microsoft Word, we may left click and drag this shape freely to any location.
 Assert.assertEquals(WrapType.NONE, shape.getWrapType());
 Assert.assertFalse(shape.isInline());

 doc.save(getArtifactsDir() + "Shape.IsInline.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to work with revision shapes.

```

 Document doc = new Document();

 Assert.assertFalse(doc.getTrackRevisions());

 // Insert an inline shape without tracking revisions, which will make this shape not a revision of any kind.
 Shape shape = new Shape(doc, ShapeType.CUBE);
 shape.setWrapType(WrapType.INLINE);
 shape.setWidth(100.0);
 shape.setHeight(100.0);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 // Start tracking revisions and then insert another shape, which will be a revision.
 doc.startTrackRevisions("John Doe");

 shape = new Shape(doc, ShapeType.SUN);
 shape.setWrapType(WrapType.INLINE);
 shape.setWidth(100.0);
 shape.setHeight(100.0);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());
 Assert.assertEquals(shapeList.size(), 2);

 Shape firstShape = shapeList.get(0);
 firstShape.remove();

 // Since we removed that shape while we were tracking changes,
 // the shape persists in the document and counts as a delete revision.
 // Accepting this revision will remove the shape permanently, and rejecting it will keep it in the document.
 Assert.assertEquals(ShapeType.CUBE, shapeList.get(0).getShapeType());
 Assert.assertTrue(shapeList.get(0).isDeleteRevision());

 // And we inserted another shape while tracking changes, so that shape will count as an insert revision.
 // Accepting this revision will assimilate this shape into the document as a non-revision,
 // and rejecting the revision will remove this shape permanently.
 Assert.assertEquals(ShapeType.SUN, shapeList.get(1).getShapeType());
 Assert.assertTrue(shapeList.get(1).isInsertRevision());
 
```

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isLayoutInCell() {#isLayoutInCell}
```
public boolean isLayoutInCell()
```


Gets a flag indicating whether the shape is displayed inside a table or outside of it.

 **Remarks:** 

The default value is  true .

Has effect only for top level shapes, the property [getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) of which is set to value other than [Inline](../../com.aspose.words/inline/).

 **Examples:** 

Shows how to determine how to display a shape in a table cell.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(10.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table.setStyle(tableStyle);

 builder.moveTo(table.getFirstRow().getFirstCell().getFirstParagraph());

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 50.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);

 // Set the "IsLayoutInCell" property to "true" to display the shape as an inline element inside the cell's paragraph.
 // The coordinate origin that will determine the shape's location will be the top left corner of the shape's cell.
 // If we re-size the cell, the shape will move to maintain the same position starting from the cell's top left.
 // Set the "IsLayoutInCell" property to "false" to display the shape as an independent floating shape.
 // The coordinate origin that will determine the shape's location will be the top left corner of the page,
 // and the shape will not respond to any re-sizing of its cell.
 shape.isLayoutInCell(isLayoutInCell);

 // We can only apply the "IsLayoutInCell" property to floating shapes.
 shape.setWrapType(WrapType.NONE);

 doc.save(getArtifactsDir() + "Shape.LayoutInTableCell.docx");
 
```

**Returns:**
boolean - A flag indicating whether the shape is displayed inside a table or outside of it.
### isLayoutInCell(boolean value) {#isLayoutInCell-boolean}
```
public void isLayoutInCell(boolean value)
```


Sets a flag indicating whether the shape is displayed inside a table or outside of it.

 **Remarks:** 

The default value is  true .

Has effect only for top level shapes, the property [getWrapType()](../../com.aspose.words/shapebase/\#getWrapType) / [setWrapType(int)](../../com.aspose.words/shapebase/\#setWrapType-int) of which is set to value other than [Inline](../../com.aspose.words/inline/).

 **Examples:** 

Shows how to determine how to display a shape in a table cell.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(10.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table.setStyle(tableStyle);

 builder.moveTo(table.getFirstRow().getFirstCell().getFirstParagraph());

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 50.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);

 // Set the "IsLayoutInCell" property to "true" to display the shape as an inline element inside the cell's paragraph.
 // The coordinate origin that will determine the shape's location will be the top left corner of the shape's cell.
 // If we re-size the cell, the shape will move to maintain the same position starting from the cell's top left.
 // Set the "IsLayoutInCell" property to "false" to display the shape as an independent floating shape.
 // The coordinate origin that will determine the shape's location will be the top left corner of the page,
 // and the shape will not respond to any re-sizing of its cell.
 shape.isLayoutInCell(isLayoutInCell);

 // We can only apply the "IsLayoutInCell" property to floating shapes.
 shape.setWrapType(WrapType.NONE);

 doc.save(getArtifactsDir() + "Shape.LayoutInTableCell.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the shape is displayed inside a table or outside of it. |

### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to identify move revision shapes.

```

 // A move revision is when we move an element in the document body by cut-and-pasting it in Microsoft Word while
 // tracking changes. If we involve an inline shape in such a text movement, that shape will also be a revision.
 // Copying-and-pasting or moving floating shapes do not create move revisions.
 Document doc = new Document(getMyDir() + "Revision shape.docx");

 // Move revisions consist of pairs of "Move from", and "Move to" revisions. We moved in this document in one shape,
 // but until we accept or reject the move revision, there will be two instances of that shape.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());
 Assert.assertEquals(shapeList.size(), 2);

 Shape firstShape = shapeList.get(0);

 // This is the "Move to" revision, which is the shape at its arrival destination.
 // If we accept the revision, this "Move to" revision shape will disappear,
 // and the "Move from" revision shape will remain.
 Assert.assertFalse(shapeList.get(0).isMoveFromRevision());
 Assert.assertTrue(shapeList.get(0).isMoveToRevision());

 // This is the "Move from" revision, which is the shape at its original location.
 // If we accept the revision, this "Move from" revision shape will disappear,
 // and the "Move to" revision shape will remain.
 Assert.assertTrue(shapeList.get(1).isMoveFromRevision());
 Assert.assertFalse(shapeList.get(1).isMoveToRevision());
 
```

**Returns:**
boolean -  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to identify move revision shapes.

```

 // A move revision is when we move an element in the document body by cut-and-pasting it in Microsoft Word while
 // tracking changes. If we involve an inline shape in such a text movement, that shape will also be a revision.
 // Copying-and-pasting or moving floating shapes do not create move revisions.
 Document doc = new Document(getMyDir() + "Revision shape.docx");

 // Move revisions consist of pairs of "Move from", and "Move to" revisions. We moved in this document in one shape,
 // but until we accept or reject the move revision, there will be two instances of that shape.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());
 Assert.assertEquals(shapeList.size(), 2);

 Shape firstShape = shapeList.get(0);

 // This is the "Move to" revision, which is the shape at its arrival destination.
 // If we accept the revision, this "Move to" revision shape will disappear,
 // and the "Move from" revision shape will remain.
 Assert.assertFalse(shapeList.get(0).isMoveFromRevision());
 Assert.assertTrue(shapeList.get(0).isMoveToRevision());

 // This is the "Move from" revision, which is the shape at its original location.
 // If we accept the revision, this "Move from" revision shape will disappear,
 // and the "Move to" revision shape will remain.
 Assert.assertTrue(shapeList.get(1).isMoveFromRevision());
 Assert.assertFalse(shapeList.get(1).isMoveToRevision());
 
```

**Returns:**
boolean -  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### isSignatureLine() {#isSignatureLine}
```
public boolean isSignatureLine()
```


Indicates that shape is a [SignatureLine](../../com.aspose.words/signatureline/).

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isTopLevel() {#isTopLevel}
```
public boolean isTopLevel()
```


Returns  true  if this shape is not a child of a group shape.

 **Examples:** 

Shows how to tell whether a shape is a part of a group shape.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 shape.setWrapType(WrapType.NONE);

 // A shape by default is not part of any group shape, and therefore has the "IsTopLevel" property set to "true".
 Assert.assertTrue(shape.isTopLevel());

 GroupShape group = new GroupShape(doc);
 group.appendChild(shape);

 // Once we assimilate a shape into a group shape, the "IsTopLevel" property changes to "false".
 Assert.assertFalse(shape.isTopLevel());
 
```

**Returns:**
boolean -  true  if this shape is not a child of a group shape.
### isWordArt() {#isWordArt}
```
public boolean isWordArt()
```


Returns  true  if this shape is a WordArt object.

 **Remarks:** 

Works till 2007 compatibility mode. In 2010 and higher compatibility mode WordArt is just a TextBox with fancy fonts.

 **Examples:** 

Shows how to work with WordArt.

```

 public void insertTextPaths() throws Exception {
     Document doc = new Document();

     // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
     // Provide a "ShapeType" as an argument to set a shape for the WordArt.
     Shape shape = appendWordArt(doc, "Hello World! This text is bold, and italic.",
             "Arial", 480.0, 24.0, Color.WHITE, Color.BLACK, ShapeType.TEXT_PLAIN_TEXT);

     // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
     shape.getTextPath().setBold(true);
     shape.getTextPath().setItalic(true);

     // Below are various other text formatting-related properties.
     Assert.assertFalse(shape.getTextPath().getUnderline());
     Assert.assertFalse(shape.getTextPath().getShadow());
     Assert.assertFalse(shape.getTextPath().getStrikeThrough());
     Assert.assertFalse(shape.getTextPath().getReverseRows());
     Assert.assertFalse(shape.getTextPath().getXScale());
     Assert.assertFalse(shape.getTextPath().getTrim());
     Assert.assertFalse(shape.getTextPath().getSmallCaps());

     Assert.assertEquals(36.0, shape.getTextPath().getSize());
     Assert.assertEquals("Hello World! This text is bold, and italic.", shape.getTextPath().getText());
     Assert.assertEquals(ShapeType.TEXT_PLAIN_TEXT, shape.getShapeType());

     // Use the "On" property to show/hide the text.
     shape = appendWordArt(doc, "On set to \"true\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(true);

     shape = appendWordArt(doc, "On set to \"false\"", "Calibri", 150.0, 24.0, Color.YELLOW, Color.pink, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setOn(false);

     // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
     shape = appendWordArt(doc, "Kerning: VAV", "Times New Roman", 90.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(true);

     shape = appendWordArt(doc, "No kerning: VAV", "Times New Roman", 100.0, 24.0, Color.ORANGE, Color.RED, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setKerning(false);

     // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
     shape = appendWordArt(doc, "Spacing set to 0.1", "Calibri", 120.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_CASCADE_DOWN);
     shape.getTextPath().setSpacing(0.1);

     // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
     shape = appendWordArt(doc, "RotateLetters", "Calibri", 200.0, 36.0, Color.YELLOW, Color.GREEN, ShapeType.TEXT_WAVE);
     shape.getTextPath().setRotateLetters(true);

     // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
     shape = appendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_SLANT_UP);
     shape.getTextPath().setSameLetterHeights(true);

     // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
     shape = appendWordArt(doc, "FitShape on", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     Assert.assertTrue(shape.getTextPath().getFitShape());
     shape.getTextPath().setSize(24.0);

     // If we set the "FitShape: property to "false", the text will keep the size
     // which the "Size" property specifies regardless of the size of the shape.
     // Use the "TextPathAlignment" property also to align the text to a side of the shape.
     shape = appendWordArt(doc, "FitShape off", "Calibri", 160.0, 24.0, Color.BLUE, Color.BLUE, ShapeType.TEXT_PLAIN_TEXT);
     shape.getTextPath().setFitShape(false);
     shape.getTextPath().setSize(24.0);
     shape.getTextPath().setTextPathAlignment(TextPathAlignment.RIGHT);

     doc.save(getArtifactsDir() + "Shape.InsertTextPaths.docx");
 }

 /// 
 /// Insert a new paragraph with a WordArt shape inside it.
 /// 
 private static Shape appendWordArt(Document doc, String text, String textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, int wordArtShapeType) throws Exception {
     // Create an inline Shape, which will serve as a container for our WordArt.
     // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
     // These types will have "WordArt object" in the description,
     // and their enumerator constant names will all start with "Text".
     Shape shape = new Shape(doc, wordArtShapeType);
     {
         shape.setWrapType(WrapType.INLINE);
         shape.setWidth(shapeWidth);
         shape.setHeight(shapeHeight);
         shape.setFillColor(wordArtFill);
         shape.setStrokeColor(line);
     }

     shape.getTextPath().setText(text);
     shape.getTextPath().setFontFamily(textFontFamily);

     Paragraph para = (Paragraph) doc.getFirstSection().getBody().appendChild(new Paragraph(doc));
     para.appendChild(shape);
     return shape;
 }
 
```

**Returns:**
boolean -  true  if this shape is a WordArt object.
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

 **Examples:** 

Shows how to print all of a document's comments and their replies.

```

 Document doc = new Document(getMyDir() + "Comments.docx");

 NodeCollection comments = doc.getChildNodes(NodeType.COMMENT, true);
 // If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
 // Print all top-level comments along with any replies they may have.
 for (Comment comment : (Iterable) comments) {
     if (comment.getAncestor() == null) {
         System.out.println("Top-level comment:");
         System.out.println("\t\"{comment.GetText().Trim()}\", by {comment.Author}");
         System.out.println("Has {comment.Replies.Count} replies");
         for (Comment commentReply : comment.getReplies()) {
             System.out.println("\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
         }
         System.out.println();
     }
 }
 
```

**Returns:**
java.util.Iterator
### localToParent(Point2D.Float value) {#localToParent-java.awt.geom.Point2D.Float}
```
public Point2D.Float localToParent(Point2D.Float value)
```


Converts a value from the local coordinate space into the coordinate space of the parent shape.

 **Examples:** 

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```

 Document doc = new Document();

 // Insert a group shape, and place it 100 points below and to the right of
 // the document's x and Y coordinate origin point.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(100f, 100f, 500f, 500f));

 // Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
 // lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
 Assert.assertEquals(new Point2D.Float(100f, 100f), group.localToParent(new Point2D.Float(0f, 0f)));

 // By default, a shape's internal coordinate plane has the top left corner at (0, 0),
 // and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
 // in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
 // to a movement of 2pts on the group shape's coordinate plane.
 Assert.assertEquals(new Point2D.Float(150f, 150f), group.localToParent(new Point2D.Float(100f, 100f)));
 Assert.assertEquals(new Point2D.Float(200f, 200f), group.localToParent(new Point2D.Float(200f, 200f)));
 Assert.assertEquals(new Point2D.Float(250f, 250f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Move the group shape's x and y axis origin from the top left corner to the center.
 // This will offset the group's internal coordinates relative to the document's coordinates even further.
 group.setCoordOrigin(new Point(-250, -250));

 Assert.assertEquals(new Point2D.Float(375f, 375f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Changing the scale of the coordinate plane will also affect relative locations.
 group.setCoordSize(new Dimension(500, 500));

 Assert.assertEquals(new Point2D.Float(650f, 650f), group.localToParent(new Point2D.Float(300f, 300f)));

 // If we wish to add a shape to this group while defining its location based on a location in the document,
 // we will need to first confirm a location in the group shape that will match the document's location.
 Assert.assertEquals(new Point2D.Float(700f, 700f), group.localToParent(new Point2D.Float(350f, 350f)));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 group.appendChild(shape);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 doc.save(getArtifactsDir() + "Shape.LocalToParent.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.geom.Point2D.Float |  |

**Returns:**
java.awt.geom.Point2D.Float
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

 **Examples:** 

Shows how to remove all child nodes of a specific type from a composite node.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

Shows how to delete all shapes with images from a document.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

 **Remarks:** 

The parent of  oldChild  is set to  null  after the node is removed.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.
### removeGlow() {#removeGlow}
```
public void removeGlow()
```




### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeReflection() {#removeReflection}
```
public void removeReflection()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeShadow() {#removeShadow}
```
public void removeShadow()
```




### removeShapeAttr(int key) {#removeShapeAttr-int}
```
public void removeShapeAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node.

 **Remarks:** 

This method does not remove the content of the smart tags.

 **Examples:** 

Removes all smart tags from descendant nodes of a composite node.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Shows how to create smart tags.

```

 public void create() throws Exception {
     Document doc = new Document();

     // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
     // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
     SmartTag smartTag = new SmartTag(doc);

     // Smart tags are composite nodes that contain their recognized text in its entirety.
     // Add contents to this smart tag manually.
     smartTag.appendChild(new Run(doc, "May 29, 2019"));

     // Microsoft Word may recognize the above contents as being a date.
     // Smart tags use the "Element" property to reflect the type of data they contain.
     smartTag.setElement("date");

     // Some smart tag types process their contents further into custom XML properties.
     smartTag.getProperties().add(new CustomXmlProperty("Day", "", "29"));
     smartTag.getProperties().add(new CustomXmlProperty("Month", "", "5"));
     smartTag.getProperties().add(new CustomXmlProperty("Year", "", "2019"));

     // Set the smart tag's URI to the default value.
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a date. "));

     // Create another smart tag for a stock ticker.
     smartTag = new SmartTag(doc);
     smartTag.setElement("stockticker");
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     smartTag.appendChild(new Run(doc, "MSFT"));

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a stock ticker."));

     // Print all the smart tags in our document using a document visitor.
     doc.accept(new SmartTagPrinter());

     // Older versions of Microsoft Word support smart tags.
     doc.save(getArtifactsDir() + "SmartTag.Create.doc");

     // Use the "RemoveSmartTags" method to remove all smart tags from a document.
     Assert.assertEquals(2, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

     doc.removeSmartTags();

     Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 }

 /// 
 /// Prints visited smart tags and their contents.
 /// 
 private static class SmartTagPrinter extends DocumentVisitor {
     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(SmartTag smartTag) {
         System.out.println("Smart tag type: {smartTag.Element}");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a SmartTag node is ended.
     /// 
     public int visitSmartTagEnd(SmartTag smartTag) {
         System.out.println("\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

         if (smartTag.getProperties().getCount() == 0) {
             System.out.println("\tContains no properties");
         } else {
             System.out.println("\tProperties: ");
             String[] properties = new String[smartTag.getProperties().getCount()];
             int index = 0;

             for (CustomXmlProperty cxp : smartTag.getProperties())
                 properties[index++] = MessageFormat.format("\"{0}\" = \"{1}\"", cxp.getName(), cxp.getValue());

             System.out.println(StringUtils.join(properties, ", "));
         }

         return VisitorAction.CONTINUE;
     }
 }
 
```

### removeSoftEdge() {#removeSoftEdge}
```
public void removeSoftEdge()
```




### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to use an XPath expression to test whether a node is inside a field.

```

 Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

 // The NodeList that results from this XPath expression will contain all nodes we find inside a field.
 // However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
 // Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
 NodeList resultList =
         doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");
 Run[] runs = Arrays.stream(resultList.toArray()).filter(n -> n.getNodeType() == NodeType.RUN).toArray(Run[]::new);
 Run run = runs[0];

 // Check if the specified run is one of the nodes that are inside the field.
 System.out.println(MessageFormat.format("Contents of the first Run node that''s part of a field: {0}", run.getText().trim()));
 
```

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setAllowOverlap(boolean value) {#setAllowOverlap-boolean}
```
public void setAllowOverlap(boolean value)
```


Sets a value that specifies whether this shape can overlap other shapes.

 **Remarks:** 

This property affects behavior of the shape in Microsoft Word. Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is  true .

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value that specifies whether this shape can overlap other shapes. |

### setAlternativeText(String value) {#setAlternativeText-java.lang.String}
```
public void setAlternativeText(String value)
```


Defines alternative text to be displayed instead of a graphic.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to use a shape's alternative text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertShape(ShapeType.CUBE, 150.0, 150.0);
 shape.setName("MyCube");

 shape.setAlternativeText("Alt text for MyCube.");

 // We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
 doc.save(getArtifactsDir() + "Shape.AltText.docx");

 // Save the document to HTML, and then delete the linked image that belongs to our shape.
 // The browser that is reading our HTML will display the alt text in place of the missing image.
 doc.save(getArtifactsDir() + "Shape.AltText.html");
 new File(getArtifactsDir() + "Shape.AltText.001.png").delete();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setAnchorLocked(boolean value) {#setAnchorLocked-boolean}
```
public void setAnchorLocked(boolean value)
```


Specifies whether the shape's anchor is locked.

 **Remarks:** 

The default value is  false .

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word. When the anchor is not locked, moving the shape in Microsoft Word can move the shape's anchor too.

 **Examples:** 

Shows how to lock or unlock a shape's paragraph anchor.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 builder.write("Our shape will have an anchor attached to this paragraph.");
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 160.0);
 shape.setWrapType(WrapType.NONE);
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 builder.writeln("Hello again!");

 // Set the "AnchorLocked" property to "true" to prevent the shape's anchor
 // from moving when moving the shape in Microsoft Word.
 // Set the "AnchorLocked" property to "false" to allow any movement of the shape
 // to also move its anchor to any other paragraph that the shape ends up close to.
 shape.setAnchorLocked(anchorLocked);

 // If the shape does not have a visible anchor symbol to its left,
 // we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
 doc.save(getArtifactsDir() + "Shape.AnchorLocked.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setAspectRatioLocked(boolean value) {#setAspectRatioLocked-boolean}
```
public void setAspectRatioLocked(boolean value)
```


Specifies whether the shape's aspect ratio is locked.

 **Remarks:** 

The default value depends on the [ShapeType](../../com.aspose.words/shapetype/), for the [ShapeType.IMAGE](../../com.aspose.words/shapetype/\#IMAGE) it is  true  but for the other shape types it is  false .

Has effect for top level shapes only.

 **Examples:** 

Shows how to lock/unlock a shape's aspect ratio.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
 // eight sizing handles around its perimeter, which we can click and drag to change its size.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
 // when using any of the four diagonal sizing handles, which change both the image's height and width.
 // Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
 // Set the "AspectRatioLocked" property to "false" to allow us to
 // freely change the image's aspect ratio with all sizing handles.
 shape.setAspectRatioLocked(lockAspectRatio);

 doc.save(getArtifactsDir() + "Shape.AspectRatio.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBehindText(boolean value) {#setBehindText-boolean}
```
public void setBehindText(boolean value)
```


Specifies whether the shape is below or above text.

 **Remarks:** 

Has effect only for top level shapes.

The default value is  false .

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBlur(double value) {#setBlur-double}
```
public void setBlur(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setBounds(Rectangle2D.Float value) {#setBounds-java.awt.geom.Rectangle2D.Float}
```
public void setBounds(Rectangle2D.Float value)
```


Sets the location and size of the containing block of the shape.

 **Remarks:** 

Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

 **Examples:** 

Shows how to verify shape containing block boundaries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.LINE, RelativeHorizontalPosition.LEFT_MARGIN, 50.0,
         RelativeVerticalPosition.TOP_MARGIN, 50.0, 100.0, 100.0, WrapType.NONE);
 shape.setStrokeColor(Color.ORANGE);

 // Even though the line itself takes up little space on the document page,
 // it occupies a rectangular containing block, the size of which we can determine using the "Bounds" properties.
 Assert.assertEquals(new Rectangle2D.Float(50f, 50f, 100f, 100f), shape.getBounds());
 Assert.assertEquals(new Rectangle2D.Float(50f, 50f, 100f, 100f), shape.getBoundsInPoints());

 // Create a group shape, and then set the size of its containing block using the "Bounds" property.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(0f, 100f, 250f, 250f));

 Assert.assertEquals(new Rectangle2D.Float(0f, 100f, 250f, 250f), group.getBoundsInPoints());

 // Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
 shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 Assert.assertEquals(new Rectangle2D.Float(700f, 700f, 100f, 100f), shape.getBoundsInPoints());

 group.appendChild(shape);

 // The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
 // and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
 // Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
 // translates to 1pt in the document body's coordinate plane.
 // Every shape that we insert will also shrink in size by a factor of 4.
 // The change in the shape's "BoundsInPoints" property will reflect this.
 Assert.assertEquals(new Rectangle2D.Float(175f, 275f, 25f, 25f), shape.getBoundsInPoints());

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 // Insert a shape and place it outside of the bounds of the group shape's containing block.
 shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(1000.0);
     shape.setTop(1000.0);
 }

 group.appendChild(shape);

 // The group shape's footprint in the document body has increased, but the containing block remains the same.
 Assert.assertEquals(new Rectangle2D.Float(0f, 100f, 250f, 250f), group.getBoundsInPoints());
 Assert.assertEquals(new Rectangle2D.Float(250f, 350f, 25f, 25f), shape.getBoundsInPoints());

 doc.save(getArtifactsDir() + "Shape.Bounds.docx");
 
```

Shows how to create and populate a group shape.

```

 Document doc = new Document();

 // Create a group shape. A group shape can display a collection of child shape nodes.
 // In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
 // select all the other child shapes within this group and allow us to scale and move all the shapes at once.
 GroupShape group = new GroupShape(doc);

 Assert.assertEquals(WrapType.NONE, group.getWrapType());

 // Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
 group.setBounds(new Rectangle2D.Float(0f, 0f, 400f, 400f));

 // Set the group's internal coordinate plane size to 500 x 500pt.
 // The top left corner of the group will have an x and y coordinate of (0, 0),
 // and the bottom right corner will have an x and y coordinate of (500, 500).
 group.setCoordSize(new Dimension(500, 500));

 // Set the coordinates of the top left corner of the group to (-250, -250).
 // The group's center will now have an x and y coordinate value of (0, 0),
 // and the bottom right corner will be at (250, 250).
 group.setCoordOrigin(new Point(-250, -250));

 Shape rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(group.getCoordSize().width);
 rectangleShape.setHeight(group.getCoordSize().height);
 rectangleShape.setLeft(group.getCoordOrigin().x);
 rectangleShape.setTop(group.getCoordOrigin().y);

 // Create a rectangle that will display the boundary of this group shape and add it to the group.
 group.appendChild(rectangleShape);

 // Once a shape is a part of a group shape, we can access it as a child node and then modify it.
 ((Shape) group.getChild(NodeType.SHAPE, 0, true)).getStroke().setDashStyle(DashStyle.DASH);

 Shape starShape = new Shape(doc, ShapeType.STAR);
 starShape.setWidth(20.0);
 starShape.setHeight(20.0);
 starShape.setLeft(-10);
 starShape.setTop(-10);
 starShape.setFillColor(Color.RED);

 // Create a small red star and insert it into the group.
 // Line up the shape with the group's coordinate origin, which we have moved to the center.
 group.appendChild(starShape);

 rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(250.0);
 rectangleShape.setHeight(250.0);
 rectangleShape.setLeft(-250);
 rectangleShape.setTop(-250);
 rectangleShape.setFillColor(Color.BLUE);

 // Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
 // Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
 // and then the shape with the image will overlap the light blue rectangle, using it as a frame.
 // We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
 group.appendChild(rectangleShape);

 Shape imageShape = new Shape(doc, ShapeType.IMAGE);
 imageShape.setWidth(200.0);
 imageShape.setHeight(200.0);
 imageShape.setLeft(-225);
 imageShape.setTop(-225);

 group.appendChild(imageShape);

 ((Shape) group.getChild(NodeType.SHAPE, 3, true)).getImageData().setImage(getImageDir() + "Logo.jpg");

 Shape textboxShape = new Shape(doc, ShapeType.TEXT_BOX);
 textboxShape.setWidth(200.0);
 textboxShape.setHeight(50.0);
 textboxShape.setLeft(group.getCoordSize().width + new Point(group.getCoordOrigin()).x - 200);
 textboxShape.setTop(group.getCoordSize().height + new Point(group.getCoordOrigin()).y);

 // Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
 // touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
 // the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
 group.appendChild(textboxShape);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(group);
 builder.moveTo(((Shape) group.getChild(NodeType.SHAPE, 4, true)).appendChild(new Paragraph(doc)));
 builder.write("Hello world!");

 doc.save(getArtifactsDir() + "Shape.GroupShape.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.geom.Rectangle2D.Float | The location and size of the containing block of the shape. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setCoordOrigin(Point value) {#setCoordOrigin-java.awt.Point}
```
public void setCoordOrigin(Point value)
```


The coordinates at the top-left corner of the containing block of this shape.

 **Remarks:** 

The default value is (0,0).

 **Examples:** 

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```

 Document doc = new Document();

 // Insert a group shape, and place it 100 points below and to the right of
 // the document's x and Y coordinate origin point.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(100f, 100f, 500f, 500f));

 // Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
 // lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
 Assert.assertEquals(new Point2D.Float(100f, 100f), group.localToParent(new Point2D.Float(0f, 0f)));

 // By default, a shape's internal coordinate plane has the top left corner at (0, 0),
 // and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
 // in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
 // to a movement of 2pts on the group shape's coordinate plane.
 Assert.assertEquals(new Point2D.Float(150f, 150f), group.localToParent(new Point2D.Float(100f, 100f)));
 Assert.assertEquals(new Point2D.Float(200f, 200f), group.localToParent(new Point2D.Float(200f, 200f)));
 Assert.assertEquals(new Point2D.Float(250f, 250f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Move the group shape's x and y axis origin from the top left corner to the center.
 // This will offset the group's internal coordinates relative to the document's coordinates even further.
 group.setCoordOrigin(new Point(-250, -250));

 Assert.assertEquals(new Point2D.Float(375f, 375f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Changing the scale of the coordinate plane will also affect relative locations.
 group.setCoordSize(new Dimension(500, 500));

 Assert.assertEquals(new Point2D.Float(650f, 650f), group.localToParent(new Point2D.Float(300f, 300f)));

 // If we wish to add a shape to this group while defining its location based on a location in the document,
 // we will need to first confirm a location in the group shape that will match the document's location.
 Assert.assertEquals(new Point2D.Float(700f, 700f), group.localToParent(new Point2D.Float(350f, 350f)));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 group.appendChild(shape);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 doc.save(getArtifactsDir() + "Shape.LocalToParent.docx");
 
```

Shows how to create and populate a group shape.

```

 Document doc = new Document();

 // Create a group shape. A group shape can display a collection of child shape nodes.
 // In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
 // select all the other child shapes within this group and allow us to scale and move all the shapes at once.
 GroupShape group = new GroupShape(doc);

 Assert.assertEquals(WrapType.NONE, group.getWrapType());

 // Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
 group.setBounds(new Rectangle2D.Float(0f, 0f, 400f, 400f));

 // Set the group's internal coordinate plane size to 500 x 500pt.
 // The top left corner of the group will have an x and y coordinate of (0, 0),
 // and the bottom right corner will have an x and y coordinate of (500, 500).
 group.setCoordSize(new Dimension(500, 500));

 // Set the coordinates of the top left corner of the group to (-250, -250).
 // The group's center will now have an x and y coordinate value of (0, 0),
 // and the bottom right corner will be at (250, 250).
 group.setCoordOrigin(new Point(-250, -250));

 Shape rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(group.getCoordSize().width);
 rectangleShape.setHeight(group.getCoordSize().height);
 rectangleShape.setLeft(group.getCoordOrigin().x);
 rectangleShape.setTop(group.getCoordOrigin().y);

 // Create a rectangle that will display the boundary of this group shape and add it to the group.
 group.appendChild(rectangleShape);

 // Once a shape is a part of a group shape, we can access it as a child node and then modify it.
 ((Shape) group.getChild(NodeType.SHAPE, 0, true)).getStroke().setDashStyle(DashStyle.DASH);

 Shape starShape = new Shape(doc, ShapeType.STAR);
 starShape.setWidth(20.0);
 starShape.setHeight(20.0);
 starShape.setLeft(-10);
 starShape.setTop(-10);
 starShape.setFillColor(Color.RED);

 // Create a small red star and insert it into the group.
 // Line up the shape with the group's coordinate origin, which we have moved to the center.
 group.appendChild(starShape);

 rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(250.0);
 rectangleShape.setHeight(250.0);
 rectangleShape.setLeft(-250);
 rectangleShape.setTop(-250);
 rectangleShape.setFillColor(Color.BLUE);

 // Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
 // Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
 // and then the shape with the image will overlap the light blue rectangle, using it as a frame.
 // We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
 group.appendChild(rectangleShape);

 Shape imageShape = new Shape(doc, ShapeType.IMAGE);
 imageShape.setWidth(200.0);
 imageShape.setHeight(200.0);
 imageShape.setLeft(-225);
 imageShape.setTop(-225);

 group.appendChild(imageShape);

 ((Shape) group.getChild(NodeType.SHAPE, 3, true)).getImageData().setImage(getImageDir() + "Logo.jpg");

 Shape textboxShape = new Shape(doc, ShapeType.TEXT_BOX);
 textboxShape.setWidth(200.0);
 textboxShape.setHeight(50.0);
 textboxShape.setLeft(group.getCoordSize().width + new Point(group.getCoordOrigin()).x - 200);
 textboxShape.setTop(group.getCoordSize().height + new Point(group.getCoordOrigin()).y);

 // Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
 // touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
 // the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
 group.appendChild(textboxShape);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(group);
 builder.moveTo(((Shape) group.getChild(NodeType.SHAPE, 4, true)).appendChild(new Paragraph(doc)));
 builder.write("Hello world!");

 doc.save(getArtifactsDir() + "Shape.GroupShape.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Point | The corresponding java.awt.Point value. |

### setCoordSize(Dimension value) {#setCoordSize-java.awt.Dimension}
```
public void setCoordSize(Dimension value)
```


The width and height of the coordinate space inside the containing block of this shape.

 **Remarks:** 

The default value is (1000, 1000).

 **Examples:** 

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```

 Document doc = new Document();

 // Insert a group shape, and place it 100 points below and to the right of
 // the document's x and Y coordinate origin point.
 GroupShape group = new GroupShape(doc);
 group.setBounds(new Rectangle2D.Float(100f, 100f, 500f, 500f));

 // Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
 // lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
 Assert.assertEquals(new Point2D.Float(100f, 100f), group.localToParent(new Point2D.Float(0f, 0f)));

 // By default, a shape's internal coordinate plane has the top left corner at (0, 0),
 // and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
 // in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
 // to a movement of 2pts on the group shape's coordinate plane.
 Assert.assertEquals(new Point2D.Float(150f, 150f), group.localToParent(new Point2D.Float(100f, 100f)));
 Assert.assertEquals(new Point2D.Float(200f, 200f), group.localToParent(new Point2D.Float(200f, 200f)));
 Assert.assertEquals(new Point2D.Float(250f, 250f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Move the group shape's x and y axis origin from the top left corner to the center.
 // This will offset the group's internal coordinates relative to the document's coordinates even further.
 group.setCoordOrigin(new Point(-250, -250));

 Assert.assertEquals(new Point2D.Float(375f, 375f), group.localToParent(new Point2D.Float(300f, 300f)));

 // Changing the scale of the coordinate plane will also affect relative locations.
 group.setCoordSize(new Dimension(500, 500));

 Assert.assertEquals(new Point2D.Float(650f, 650f), group.localToParent(new Point2D.Float(300f, 300f)));

 // If we wish to add a shape to this group while defining its location based on a location in the document,
 // we will need to first confirm a location in the group shape that will match the document's location.
 Assert.assertEquals(new Point2D.Float(700f, 700f), group.localToParent(new Point2D.Float(350f, 350f)));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 {
     shape.setWidth(100.0);
     shape.setHeight(100.0);
     shape.setLeft(700.0);
     shape.setTop(700.0);
 }

 group.appendChild(shape);
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(group);

 doc.save(getArtifactsDir() + "Shape.LocalToParent.docx");
 
```

Shows how to create and populate a group shape.

```

 Document doc = new Document();

 // Create a group shape. A group shape can display a collection of child shape nodes.
 // In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
 // select all the other child shapes within this group and allow us to scale and move all the shapes at once.
 GroupShape group = new GroupShape(doc);

 Assert.assertEquals(WrapType.NONE, group.getWrapType());

 // Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
 group.setBounds(new Rectangle2D.Float(0f, 0f, 400f, 400f));

 // Set the group's internal coordinate plane size to 500 x 500pt.
 // The top left corner of the group will have an x and y coordinate of (0, 0),
 // and the bottom right corner will have an x and y coordinate of (500, 500).
 group.setCoordSize(new Dimension(500, 500));

 // Set the coordinates of the top left corner of the group to (-250, -250).
 // The group's center will now have an x and y coordinate value of (0, 0),
 // and the bottom right corner will be at (250, 250).
 group.setCoordOrigin(new Point(-250, -250));

 Shape rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(group.getCoordSize().width);
 rectangleShape.setHeight(group.getCoordSize().height);
 rectangleShape.setLeft(group.getCoordOrigin().x);
 rectangleShape.setTop(group.getCoordOrigin().y);

 // Create a rectangle that will display the boundary of this group shape and add it to the group.
 group.appendChild(rectangleShape);

 // Once a shape is a part of a group shape, we can access it as a child node and then modify it.
 ((Shape) group.getChild(NodeType.SHAPE, 0, true)).getStroke().setDashStyle(DashStyle.DASH);

 Shape starShape = new Shape(doc, ShapeType.STAR);
 starShape.setWidth(20.0);
 starShape.setHeight(20.0);
 starShape.setLeft(-10);
 starShape.setTop(-10);
 starShape.setFillColor(Color.RED);

 // Create a small red star and insert it into the group.
 // Line up the shape with the group's coordinate origin, which we have moved to the center.
 group.appendChild(starShape);

 rectangleShape = new Shape(doc, ShapeType.RECTANGLE);
 rectangleShape.setWidth(250.0);
 rectangleShape.setHeight(250.0);
 rectangleShape.setLeft(-250);
 rectangleShape.setTop(-250);
 rectangleShape.setFillColor(Color.BLUE);

 // Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
 // Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
 // and then the shape with the image will overlap the light blue rectangle, using it as a frame.
 // We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
 group.appendChild(rectangleShape);

 Shape imageShape = new Shape(doc, ShapeType.IMAGE);
 imageShape.setWidth(200.0);
 imageShape.setHeight(200.0);
 imageShape.setLeft(-225);
 imageShape.setTop(-225);

 group.appendChild(imageShape);

 ((Shape) group.getChild(NodeType.SHAPE, 3, true)).getImageData().setImage(getImageDir() + "Logo.jpg");

 Shape textboxShape = new Shape(doc, ShapeType.TEXT_BOX);
 textboxShape.setWidth(200.0);
 textboxShape.setHeight(50.0);
 textboxShape.setLeft(group.getCoordSize().width + new Point(group.getCoordOrigin()).x - 200);
 textboxShape.setTop(group.getCoordSize().height + new Point(group.getCoordOrigin()).y);

 // Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
 // touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
 // the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
 group.appendChild(textboxShape);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(group);
 builder.moveTo(((Shape) group.getChild(NodeType.SHAPE, 4, true)).appendChild(new Paragraph(doc)));
 builder.write("Hello world!");

 doc.save(getArtifactsDir() + "Shape.GroupShape.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Dimension | The corresponding java.awt.Dimension value. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDashStyle(int value) {#setDashStyle-int}
```
public void setDashStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setDistanceBottom(double value) {#setDistanceBottom-double}
```
public void setDistanceBottom(double value)
```


Sets the distance (in points) between the document text and the bottom edge of the shape.

 **Remarks:** 

The default value is 0.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the bottom edge of the shape. |

### setDistanceLeft(double value) {#setDistanceLeft-double}
```
public void setDistanceLeft(double value)
```


Sets the distance (in points) between the document text and the left edge of the shape.

 **Remarks:** 

The default value is 1/8 inch.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the left edge of the shape. |

### setDistanceRight(double value) {#setDistanceRight-double}
```
public void setDistanceRight(double value)
```


Sets the distance (in points) between the document text and the right edge of the shape.

 **Remarks:** 

The default value is 1/8 inch.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the right edge of the shape. |

### setDistanceTop(double value) {#setDistanceTop-double}
```
public void setDistanceTop(double value)
```


Sets the distance (in points) between the document text and the top edge of the shape.

 **Remarks:** 

The default value is 0.

Has effect only for top level shapes.

 **Examples:** 

Shows how to set the wrapping distance for a text that surrounds a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a rectangle and, get the text to wrap tightly around its bounds.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 150.0, 150.0);
 shape.setWrapType(WrapType.TIGHT);

 // Set the minimum distance between the shape and surrounding text to 40pt from all sides.
 shape.setDistanceTop(40.0);
 shape.setDistanceBottom(40.0);
 shape.setDistanceLeft(40.0);
 shape.setDistanceRight(40.0);

 // Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
 shape.setTop(75.0);
 shape.setLeft(150.0);
 shape.setRotation(60.0);

 // Add text that will wrap around the shape.
 builder.getFont().setSize(24.0d);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
         "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 doc.save(getArtifactsDir() + "Shape.Coordinates.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance (in points) between the document text and the top edge of the shape. |

### setEdgeRadius(double value) {#setEdgeRadius-double}
```
public void setEdgeRadius(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setEndArrowLength(int value) {#setEndArrowLength-int}
```
public void setEndArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowType(int value) {#setEndArrowType-int}
```
public void setEndArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowWidth(int value) {#setEndArrowWidth-int}
```
public void setEndArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndCap(int value) {#setEndCap-int}
```
public void setEndCap(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillColor(Color value) {#setFillColor-java.awt.Color}
```
public void setFillColor(Color value)
```


Defines the brush color that fills the closed path of the shape.

 **Remarks:** 

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) property.

The default value is java.awt.Color\#getWhite().getWhite().

 **Examples:** 

Shows how to fill a shape with a solid color.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setFilled(boolean value) {#setFilled-boolean}
```
public void setFilled(boolean value)
```


Determines whether the closed path of the shape will be filled.

 **Remarks:** 

This is a shortcut to the [Fill.getVisible()](../../com.aspose.words/fill/\#getVisible) / [Fill.setVisible(boolean)](../../com.aspose.words/fill/\#setVisible-boolean) property.

The default value is  true .

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFlipOrientation(int value) {#setFlipOrientation-int}
```
public void setFlipOrientation(int value)
```


Switches the orientation of a shape.

 **Remarks:** 

The default value is [FlipOrientation.NONE](../../com.aspose.words/fliporientation/\#NONE).

 **Examples:** 

Shows how to flip a shape on an axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert an image shape and leave its orientation in its default state.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 Assert.assertEquals(FlipOrientation.NONE, shape.getFlipOrientation());

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 250.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
 // making it into a horizontal mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.HORIZONTAL);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 250.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
 // making it into a vertical mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.VERTICAL);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 250.0,
         RelativeVerticalPosition.TOP_MARGIN, 250.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
 // making it into a horizontal and vertical mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.BOTH);

 doc.save(getArtifactsDir() + "Shape.FlipShapeOrientation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [FlipOrientation](../../com.aspose.words/fliporientation/) constants. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setHRef(String value) {#setHRef-java.lang.String}
```
public void setHRef(String value)
```


Sets the full hyperlink address for a shape.

 **Remarks:** 

The default value is an empty string.

Below are examples of valid values for this property:

Full URI:  https://www.aspose.com/ .

Full file name:  C:\\\\My Documents\\\\SalesReport.doc .

Relative URI:  ../../../resource.txt 

Relative file name:  ..\\\\My Documents\\\\SalesReport.doc .

Bookmark within another document:  https://www.aspose.com/Products/Default.aspx\#Suites 

Bookmark within this document:  \#BookmakName .

 **Examples:** 

Shows how to insert a shape which contains an image, and is also a hyperlink.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setHRef("https://forum.aspose.com/");
 shape.setTarget("New Window");
 shape.setScreenTip("Aspose.Words Support Forums");

 // Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
 // and take us to the hyperlink in the "HRef" property.
 doc.save(getArtifactsDir() + "Image.InsertImageWithHyperlink.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The full hyperlink address for a shape. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Sets the height of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

Shows how to resize a shape with an image.

```

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The height of the containing block of the shape. |

### setHeightRelative(float value) {#setHeightRelative-float}
```
public void setHeightRelative(float value)
```


Sets the value that represents the percentage of shape's relative height.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The value that represents the percentage of shape's relative height. |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Sets a boolean value indicating whether the shape is visible.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to hide the shape.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 if (!shape.getHidden())
     shape.setHidden(true);

 doc.save(getArtifactsDir() + "Shape.Hidden.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether the shape is visible. |

### setHorizontalAlignment(int value) {#setHorizontalAlignment-int}
```
public void setHorizontalAlignment(int value)
```


Specifies how the shape is positioned horizontally.

 **Remarks:** 

The default value is [HorizontalAlignment.NONE](../../com.aspose.words/horizontalalignment/\#NONE).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) constants. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setJoinStyle(int value) {#setJoinStyle-int}
```
public void setJoinStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setLeft(double value) {#setLeft-double}
```
public void setLeft(double value)
```


Sets the position of the left edge of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position of the left edge of the containing block of the shape. |

### setLeftRelative(float value) {#setLeftRelative-float}
```
public void setLeftRelative(float value)
```


Sets the value that represents shape's relative left position in percent.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The value that represents shape's relative left position in percent. |

### setLineFillType(int value) {#setLineFillType-int}
```
public void setLineFillType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Sets the optional shape name.

 **Remarks:** 

Default is empty string.

Cannot be  null , but can be an empty string.

 **Examples:** 

Shows how to use a shape's alternative text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertShape(ShapeType.CUBE, 150.0, 150.0);
 shape.setName("MyCube");

 shape.setAlternativeText("Alt text for MyCube.");

 // We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
 doc.save(getArtifactsDir() + "Shape.AltText.docx");

 // Save the document to HTML, and then delete the linked image that belongs to our shape.
 // The browser that is reading our HTML will display the alt text in place of the missing image.
 doc.save(getArtifactsDir() + "Shape.AltText.html");
 new File(getArtifactsDir() + "Shape.AltText.001.png").delete();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The optional shape name. |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setReflectionSize(double value) {#setReflectionSize-double}
```
public void setReflectionSize(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setReflectionTransparency(double value) {#setReflectionTransparency-double}
```
public void setReflectionTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setRelativeHorizontalPosition(int value) {#setRelativeHorizontalPosition-int}
```
public void setRelativeHorizontalPosition(int value)
```


Specifies relative to what the shape is positioned horizontally.

 **Remarks:** 

The default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/) constants. |

### setRelativeHorizontalSize(int value) {#setRelativeHorizontalSize-int}
```
public void setRelativeHorizontalSize(int value)
```


Sets the value of shape's relative size in horizontal direction.

 **Remarks:** 

The default value is [RelativeHorizontalSize](../../com.aspose.words/relativehorizontalsize/).

Has effect only if [getWidthRelative()](../../com.aspose.words/shapebase/\#getWidthRelative) / [setWidthRelative(float)](../../com.aspose.words/shapebase/\#setWidthRelative-float) is set.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The value of shape's relative size in horizontal direction. The value must be one of [RelativeHorizontalSize](../../com.aspose.words/relativehorizontalsize/) constants. |

### setRelativeVerticalPosition(int value) {#setRelativeVerticalPosition-int}
```
public void setRelativeVerticalPosition(int value)
```


Specifies relative to what the shape is positioned vertically.

 **Remarks:** 

The default value is [RelativeVerticalPosition.PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/) constants. |

### setRelativeVerticalSize(int value) {#setRelativeVerticalSize-int}
```
public void setRelativeVerticalSize(int value)
```


Sets the value of shape's relative size in vertical direction.

 **Remarks:** 

The default value is [RelativeVerticalSize.MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

Has effect only if [getHeightRelative()](../../com.aspose.words/shapebase/\#getHeightRelative) / [setHeightRelative(float)](../../com.aspose.words/shapebase/\#setHeightRelative-float) is set.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The value of shape's relative size in vertical direction. The value must be one of [RelativeVerticalSize](../../com.aspose.words/relativeverticalsize/) constants. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setRotation(double value) {#setRotation-double}
```
public void setRotation(double value)
```


Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.

 **Remarks:** 

The default value is 0.

 **Examples:** 

Shows how to insert and rotate an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape with an image.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 Assert.assertTrue(shape.canHaveImage());
 Assert.assertTrue(shape.hasImage());

 // Rotate the image 45 degrees clockwise.
 shape.setRotation(45.0);

 doc.save(getArtifactsDir() + "Shape.Rotate.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setScreenTip(String value) {#setScreenTip-java.lang.String}
```
public void setScreenTip(String value)
```


Defines the text displayed when the mouse pointer moves over the shape.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to insert a shape which contains an image, and is also a hyperlink.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setHRef("https://forum.aspose.com/");
 shape.setTarget("New Window");
 shape.setScreenTip("Aspose.Words Support Forums");

 // Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
 // and take us to the hyperlink in the "HRef" property.
 doc.save(getArtifactsDir() + "Image.InsertImageWithHyperlink.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setShadowType(int value) {#setShadowType-int}
```
public void setShadowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setShapeAttr(int key, Object value) {#setShapeAttr-int-java.lang.Object}
```
public void setShapeAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStartArrowLength(int value) {#setStartArrowLength-int}
```
public void setStartArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStartArrowType(int value) {#setStartArrowType-int}
```
public void setStartArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStartArrowWidth(int value) {#setStartArrowWidth-int}
```
public void setStartArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStrokeBackThemeColor(int value) {#setStrokeBackThemeColor-int}
```
public void setStrokeBackThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStrokeBackTintAndShade(double value) {#setStrokeBackTintAndShade-double}
```
public void setStrokeBackTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setStrokeColor(Color value) {#setStrokeColor-java.awt.Color}
```
public void setStrokeColor(Color value)
```


Defines the color of a stroke.

 **Remarks:** 

This is a shortcut to the [Stroke.getColor()](../../com.aspose.words/stroke/\#getColor) / [Stroke.setColor(java.awt.Color)](../../com.aspose.words/stroke/\#setColor-java.awt.Color) property.

The default value is java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Shows how to fill a shape with a solid color.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Write some text, and then cover it with a floating shape.
 builder.getFont().setSize(32.0);
 builder.writeln("Hello world!");

 Shape shape = builder.insertShape(ShapeType.CLOUD_CALLOUT, RelativeHorizontalPosition.LEFT_MARGIN, 25.0,
         RelativeVerticalPosition.TOP_MARGIN, 25.0, 250.0, 150.0, WrapType.NONE);

 // Use the "StrokeColor" property to set the color of the outline of the shape.
 shape.setStrokeColor(Color.BLACK);

 // Use the "FillColor" property to set the color of the inside area of the shape.
 shape.setFillColor(Color.BLUE);

 // The "Opacity" property determines how transparent the color is on a 0-1 scale,
 // with 1 being fully opaque, and 0 being invisible.
 // The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
 Assert.assertEquals(1.0d, shape.getFill().getOpacity());

 // Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
 shape.getFill().setOpacity(0.3);

 doc.save(getArtifactsDir() + "Shape.Fill.docx");
 
```

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### setStrokeForeThemeColor(int value) {#setStrokeForeThemeColor-int}
```
public void setStrokeForeThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStrokeForeTintAndShade(double value) {#setStrokeForeTintAndShade-double}
```
public void setStrokeForeTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setStrokeTransparency(double value) {#setStrokeTransparency-double}
```
public void setStrokeTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setStrokeVisible(boolean value) {#setStrokeVisible-boolean}
```
public void setStrokeVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setStrokeWeight(double value) {#setStrokeWeight-double}
```
public void setStrokeWeight(double value)
```


Defines the brush thickness that strokes the path of a shape in points.

 **Remarks:** 

This is a shortcut to the [Stroke.getWeight()](../../com.aspose.words/stroke/\#getWeight) / [Stroke.setWeight(double)](../../com.aspose.words/stroke/\#setWeight-double) property.

The default value is 0.75.

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setStroked(boolean value) {#setStroked-boolean}
```
public void setStroked(boolean value)
```


Defines whether the path will be stroked.

 **Remarks:** 

This is a shortcut to the [Stroke.getOn()](../../com.aspose.words/stroke/\#getOn) / [Stroke.setOn(boolean)](../../com.aspose.words/stroke/\#setOn-boolean) property.

The default value is  true .

 **Examples:** 

Shows how to iterate over all the shapes in a document.

```

 public void visitShapes() throws Exception {
     Document doc = new Document(getMyDir() + "Revision shape.docx");
     ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Logs appearance-related information about visited shapes.
 /// 
 private static class ShapeAppearancePrinter extends DocumentVisitor {
     public ShapeAppearancePrinter() {
         mShapesVisited = 0;
         mTextIndentLevel = 0;
         mStringBuilder = new StringBuilder();
     }

     /// 
     /// Appends a line to the StringBuilder with one prepended tab character for each indent level.
     /// 
     private void appendLine(String text) {
         for (int i = 0; i < mTextIndentLevel; i++) {
             mStringBuilder.append('\t');
         }

         mStringBuilder.append(text + "\n");
     }

     /// 
     /// Return all the text that the StringBuilder has accumulated.
     /// 
     public String getText() {
         return MessageFormat.format("Shapes visited: {0}\n{1}", mShapesVisited, mStringBuilder);
     }

     /// 
     /// Called when this visitor visits the start of a Shape node.
     /// 
     public int visitShapeStart(Shape shape) {
         appendLine(MessageFormat.format("Shape found: {0}", shape.getShapeType()));

         mTextIndentLevel++;

         if (shape.hasChart())
             appendLine(MessageFormat.format("Has chart: {0}", shape.getChart().getTitle().getText()));

         appendLine(MessageFormat.format("Extrusion enabled: {0}", shape.getExtrusionEnabled()));
         appendLine(MessageFormat.format("Shadow enabled: {0}", shape.getShadowEnabled()));
         appendLine(MessageFormat.format("StoryType: {0}", shape.getStoryType()));

         if (shape.getStroked()) {
             Assert.assertEquals(shape.getStrokeColor(), shape.getStroke().getColor());
             appendLine(MessageFormat.format("Stroke colors: {0}, {1}", shape.getStroke().getColor(), shape.getStroke().getColor2()));
             appendLine(MessageFormat.format("Stroke weight: {0}", shape.getStrokeWeight()));
         }

         if (shape.getFilled())
             appendLine(MessageFormat.format("Filled: {0}", shape.getFillColor()));

         if (shape.getOleFormat() != null)
             appendLine(MessageFormat.format("Ole found of type: {0}", shape.getOleFormat().getProgId()));

         if (shape.getSignatureLine() != null)
             appendLine(MessageFormat.format("Found signature line for: {0}, {1}", shape.getSignatureLine().getSigner(), shape.getSignatureLine().getSignerTitle()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a Shape node.
     /// 
     public int visitShapeEnd(Shape shape) {
         mTextIndentLevel--;
         mShapesVisited++;
         appendLine(MessageFormat.format("End of {0}", shape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the start of a GroupShape node.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         appendLine(MessageFormat.format("Shape group found: {0}", groupShape.getShapeType()));
         mTextIndentLevel++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when this visitor visits the end of a GroupShape node.
     /// 
     public int visitGroupShapeEnd(GroupShape groupShape) {
         mTextIndentLevel--;
         appendLine(MessageFormat.format("End of {0}", groupShape.getShapeType()));

         return VisitorAction.CONTINUE;
     }

     private int mShapesVisited;
     private int mTextIndentLevel;
     private final StringBuilder mStringBuilder;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setTarget(String value) {#setTarget-java.lang.String}
```
public void setTarget(String value)
```


Sets the target frame for the shape hyperlink.

 **Remarks:** 

The default value is an empty string.

 **Examples:** 

Shows how to insert a shape which contains an image, and is also a hyperlink.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setHRef("https://forum.aspose.com/");
 shape.setTarget("New Window");
 shape.setScreenTip("Aspose.Words Support Forums");

 // Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
 // and take us to the hyperlink in the "HRef" property.
 doc.save(getArtifactsDir() + "Image.InsertImageWithHyperlink.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The target frame for the shape hyperlink. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Sets the title (caption) of the current shape object.

 **Remarks:** 

Default is empty string.

Cannot be  null , but can be an empty string.

 **Examples:** 

Shows how to set the title of a shape.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a shape, give it a title, and then add it to the document.
 Shape shape = new Shape(doc, ShapeType.CUBE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 shape.setTitle("My cube");

 builder.insertNode(shape);

 // When we save a document with a shape that has a title,
 // Aspose.Words will store that title in the shape's Alt Text.
 doc.save(getArtifactsDir() + "Shape.Title.docx");

 doc = new Document(getArtifactsDir() + "Shape.Title.docx");
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("", shape.getTitle());
 Assert.assertEquals("Title: My cube", shape.getAlternativeText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The title (caption) of the current shape object. |

### setTop(double value) {#setTop-double}
```
public void setTop(double value)
```


Sets the position of the top edge of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position of the top edge of the containing block of the shape. |

### setTopRelative(float value) {#setTopRelative-float}
```
public void setTopRelative(float value)
```


Sets the value that represents shape's relative top position in percent.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The value that represents shape's relative top position in percent. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Specifies how the shape is positioned vertically.

 **Remarks:** 

The default value is [VerticalAlignment.NONE](../../com.aspose.words/verticalalignment/\#NONE).

Has effect only for top level floating shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [VerticalAlignment](../../com.aspose.words/verticalalignment/) constants. |

### setWeight(double value) {#setWeight-double}
```
public void setWeight(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Sets the width of the containing block of the shape.

 **Remarks:** 

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

 **Examples:** 

Shows how to insert a floating image, and specify its position and size.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

Shows how to resize a shape with an image.

```

 // When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
 // when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");

 // A 400x400 image will create an ImageData object with an image size of 300x300pt.
 ImageSize imageSize = shape.getImageData().getImageSize();

 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // If a shape's dimensions match the image data's dimensions,
 // then the shape is displaying the image in its original size.
 Assert.assertEquals(300.0d, shape.getWidth());
 Assert.assertEquals(300.0d, shape.getHeight());

 // Reduce the overall size of the shape by 50%.
 shape.setWidth(shape.getWidth() * 0.5);

 // Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
 Assert.assertEquals(150.0d, shape.getWidth());
 Assert.assertEquals(150.0d, shape.getHeight());

 // When we resize the shape, the size of the image data remains the same.
 Assert.assertEquals(300.0d, imageSize.getWidthPoints());
 Assert.assertEquals(300.0d, imageSize.getHeightPoints());

 // We can reference the image data dimensions to apply a scaling based on the size of the image.
 shape.setWidth(imageSize.getWidthPoints() * 1.1);

 Assert.assertEquals(330.0d, shape.getWidth());
 Assert.assertEquals(330.0d, shape.getHeight());

 doc.save(getArtifactsDir() + "Image.ScaleImage.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the containing block of the shape. |

### setWidthRelative(float value) {#setWidthRelative-float}
```
public void setWidthRelative(float value)
```


Sets the value that represents the percentage of shape's relative width.

 **Examples:** 

Shows how to set relative size and position.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The value that represents the percentage of shape's relative width. |

### setWrapSide(int value) {#setWrapSide-int}
```
public void setWrapSide(int value)
```


Specifies how the text is wrapped around the shape.

 **Remarks:** 

The default value is [WrapSide.BOTH](../../com.aspose.words/wrapside/\#BOTH).

Has effect only for top level shapes.

 **Examples:** 

Shows how to replace all textbox shapes with image shapes.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [WrapSide](../../com.aspose.words/wrapside/) constants. |

### setWrapType(int value) {#setWrapType-int}
```
public void setWrapType(int value)
```


Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.

 **Remarks:** 

The default value is [WrapType.NONE](../../com.aspose.words/wraptype/\#NONE).

Has effect only for top level shapes.

 **Examples:** 

Shows how to insert a floating image to the center of a page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

Shows how to create and format a text box.

```

 Document doc = new Document();

 // Create a floating text box.
 Shape textBox = new Shape(doc, ShapeType.TEXT_BOX);
 textBox.setWrapType(WrapType.NONE);
 textBox.setHeight(50.0);
 textBox.setWidth(200.0);

 // Set the horizontal, and vertical alignment of the text inside the shape.
 textBox.setHorizontalAlignment(HorizontalAlignment.CENTER);
 textBox.setVerticalAlignment(VerticalAlignment.TOP);

 // Add a paragraph to the text box and add a run of text that the text box will display.
 textBox.appendChild(new Paragraph(doc));
 Paragraph para = textBox.getFirstParagraph();
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 Run run = new Run(doc);
 run.setText("Hello world!");
 para.appendChild(run);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(textBox);

 doc.save(getArtifactsDir() + "Shape.CreateTextBox.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [WrapType](../../com.aspose.words/wraptype/) constants. |

### setZOrder(int value) {#setZOrder-int}
```
public void setZOrder(int value)
```


Determines the display order of overlapping shapes.

 **Remarks:** 

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main text of the document.

The display order of child shapes in a group shape is determined by their order inside the group shape.

 **Examples:** 

Shows how to manipulate the order of shapes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert three different colored rectangles that partially overlap each other.
 // When we insert a shape that overlaps another shape, Aspose.Words places the newer shape on top of the old one.
 // The light green rectangle will overlap the light blue rectangle and partially obscure it,
 // and the light blue rectangle will obscure the orange rectangle.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);
 shape.setFillColor(Color.ORANGE);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 150.0,
         RelativeVerticalPosition.TOP_MARGIN, 150.0, 200.0, 200.0, WrapType.NONE);
 shape.setFillColor(Color.BLUE);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 200.0,
         RelativeVerticalPosition.TOP_MARGIN, 200.0, 200.0, 200.0, WrapType.NONE);
 shape.setFillColor(Color.GREEN);

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 // The "ZOrder" property of a shape determines its stacking priority among other overlapping shapes.
 // If two overlapping shapes have different "ZOrder" values,
 // Microsoft Word will place the shape with a higher value over the shape with the lower value.
 // Set the "ZOrder" values of our shapes to place the first orange rectangle over the second light blue one
 // and the second light blue rectangle over the third light green rectangle.
 // This will reverse their original stacking order.
 shapeList.get(0).setZOrder(3);
 shapeList.get(1).setZOrder(2);
 shapeList.get(2).setZOrder(1);

 doc.save(getArtifactsDir() + "Shape.ZOrder.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setZOrder_IShape(int value) {#setZOrder-IShape-int}
```
public void setZOrder_IShape(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### solid() {#solid}
```
public void solid()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

 **Examples:** 

Exports the content of a node to String in HTML format.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### updateSmartArtDrawing() {#updateSmartArtDrawing}
```
public void updateSmartArtDrawing()
```


Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine.

 **Remarks:** 

Microsoft Word generates and saves the pre-rendered drawing along with SmartArt object. However, if the document is saved by other applications, the pre-rendered SmartArt drawing may be missing or incorrect. If pre-rendered drawing is available then Aspose.Words uses it to render the SmartArt object. If pre-rendered drawing is missing then Aspose.Words uses its own SmartArt cold rendering engine to render the SmartArt object. If pre-rendered drawing is incorrect then it is required to call this method to invoke the SmartArt cold rendering engine.

