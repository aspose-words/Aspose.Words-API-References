---
title: ShapeBase class
linktitle: ShapeBase class
articleTitle: ShapeBase class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.ShapeBase class. Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture"
type: docs
weight: 380
url: /nodejs-net/Aspose.Words.Drawing/shapebase/
---

## ShapeBase class

Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/nodejs-net/working-with-shapes/) documentation article.




### Remarks

This is an abstract class. The two derived classes that you can instantiate
are [Shape](../shape/) and [GroupShape](../groupshape/).

A shape is a node in the document tree.

If the shape is a child of a [Paragraph](../../Aspose.Words/paragraph/) object, then the shape is said to be "top-level".
Top-level shapes are measured and positioned in points.

A shape can also occur as a child of a [GroupShape](../groupshape/) object when several shapes
are grouped. Child shapes of a group shape are positioned in the coordinate space and units
defined by the Aspose.Words.Drawing.ShapeBase.CoordSize and Aspose.Words.Drawing.ShapeBase.CoordOrigin properties of the parent
group shape.

A shape can be positioned inline with text or floating. The positioning method is controlled
using the [ShapeBase.wrapType](./wrapType/) property.

When a shape is floating, it is positioned relative to something (e.g the current paragraph,
the margin or the page). The relative positioning of the shape is specified using the
[ShapeBase.relativeHorizontalPosition](./relativeHorizontalPosition/) and [ShapeBase.relativeVerticalPosition](./relativeVerticalPosition/) properties.

A floating shape be positioned explicitly using the [ShapeBase.left](./left/) and [ShapeBase.top](./top/)
properties or aligned relative to some other object using the [ShapeBase.horizontalAlignment](./horizontalAlignment/)
and [ShapeBase.verticalAlignment](./verticalAlignment/) properties.




**Inheritance:** [ShapeBase](./) → [CompositeNode](../../Aspose.Words/compositenode/) → [Node](../../Aspose.Words/node/)

### Properties

| Name | Description |
| --- | --- |
| [allowOverlap](./allowOverlap/) | Gets or sets a value that specifies whether this shape can overlap other shapes. |
| [alternativeText](./alternativeText/) | Defines alternative text to be displayed instead of a graphic. |
| [anchorLocked](./anchorLocked/) | Specifies whether the shape's anchor is locked. |
| [aspectRatioLocked](./aspectRatioLocked/) | Specifies whether the shape's aspect ratio is locked. |
| [behindText](./behindText/) | Specifies whether the shape is below or above text. |
| [bottom](./bottom/) | Gets the position of the bottom edge of the containing block of the shape. |
| [canHaveImage](./canHaveImage/) | Returns ``True`` if the shape type allows the shape to have an image. |
| [count](../../Aspose.Words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [distanceBottom](./distanceBottom/) | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [distanceLeft](./distanceLeft/) | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [distanceRight](./distanceRight/) | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [distanceTop](./distanceTop/) | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [fill](./fill/) | Gets fill formatting for the shape. |
| [firstChild](../../Aspose.Words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [flipOrientation](./flipOrientation/) | Switches the orientation of a shape. |
| [font](./font/) | Provides access to the font formatting of this object. |
| [glow](./glow/) | Gets glow formatting for the shape. |
| [hasChildNodes](../../Aspose.Words/compositenode/hasChildNodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [height](./height/) | Gets or sets the height of the containing block of the shape. |
| [heightRelative](./heightRelative/) | Gets or sets the value that represents the percentage of shape's relative height. |
| [hidden](./hidden/) | Gets or sets a boolean value indicating whether the shape is visible. |
| [horizontalAlignment](./horizontalAlignment/) | Specifies how the shape is positioned horizontally. |
| [href](./href/) | Gets or sets the full hyperlink address for a shape. |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [isDecorative](./isDecorative/) | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [isDeleteRevision](./isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isGroup](./isGroup/) | Returns ``True`` if this is a group shape. |
| [isHorizontalRule](./isHorizontalRule/) | Returns ``True`` if this shape is a horizontal rule. |
| [isImage](./isImage/) | Returns ``True`` if this shape is an image shape. |
| [isInline](./isInline/) | A quick way to determine if this shape is positioned inline with text. |
| [isInsertRevision](./isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isLayoutInCell](./isLayoutInCell/) | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isMoveFromRevision](./isMoveFromRevision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision](./isMoveToRevision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [isSignatureLine](./isSignatureLine/) | Indicates that shape is a [SignatureLine](../signatureline/). |
| [isTopLevel](./isTopLevel/) | Returns ``True`` if this shape is not a child of a group shape. |
| [isWordArt](./isWordArt/) | Returns ``True`` if this shape is a WordArt object. |
| [lastChild](../../Aspose.Words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [left](./left/) | Gets or sets the position of the left edge of the containing block of the shape. |
| [leftRelative](./leftRelative/) | Gets or sets the value that represents shape's relative left position in percent. |
| [markupLanguage](./markupLanguage/) | Gets MarkupLanguage used for this graphic object. |
| [name](./name/) | Gets or sets the optional shape name. |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeType](../../Aspose.Words/node/nodeType/) | Gets the type of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [parentParagraph](./parentParagraph/) | Returns the immediate parent paragraph. |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [reflection](./reflection/) | Gets reflection formatting for the shape. |
| [relativeHorizontalPosition](./relativeHorizontalPosition/) | Specifies relative to what the shape is positioned horizontally. |
| [relativeHorizontalSize](./relativeHorizontalSize/) | Gets or sets the value of shape's relative size in horizontal direction. |
| [relativeVerticalPosition](./relativeVerticalPosition/) | Specifies relative to what the shape is positioned vertically. |
| [relativeVerticalSize](./relativeVerticalSize/) | Gets or sets the value of shape's relative size in vertical direction. |
| [right](./right/) | Gets the position of the right edge of the containing block of the shape. |
| [rotation](./rotation/) | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [screenTip](./screenTip/) | Defines the text displayed when the mouse pointer moves over the shape. |
| [shadowFormat](./shadowFormat/) | Gets shadow formatting for the shape. |
| [shapeType](./shapeType/) | Gets the shape type. |
| [softEdge](./softEdge/) | Gets soft edge formatting for the shape. |
| [target](./target/) | Gets or sets the target frame for the shape hyperlink. |
| [title](./title/) | Gets or sets the title (caption) of the current shape object. |
| [top](./top/) | Gets or sets the position of the top edge of the containing block of the shape. |
| [topRelative](./topRelative/) | Gets or sets the value that represents shape's relative top position in percent. |
| [verticalAlignment](./verticalAlignment/) | Specifies how the shape is positioned vertically. |
| [width](./width/) | Gets or sets the width of the containing block of the shape. |
| [widthRelative](./widthRelative/) | Gets or sets the value that represents the percentage of shape's relative width. |
| [wrapSide](./wrapSide/) | Specifies how the text is wrapped around the shape. |
| [wrapType](./wrapType/) | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [zorder](./zorder/) | Determines the display order of overlapping shapes. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../../Aspose.Words/node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ acceptEnd(visitor)](../../Aspose.Words/compositenode/acceptEnd/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ acceptStart(visitor)](../../Aspose.Words/compositenode/acceptStart/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ adjustWithEffects(source)](./adjustWithEffects/#jsrectanglef) |  |
|[ appendChild(newChild)](../../Aspose.Words/compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ asBody()](../../Aspose.Words/node/asBody/#default) | Cast node to [Body](../../Aspose.Words/body/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkEnd()](../../Aspose.Words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../Aspose.Words/bookmarkend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkStart()](../../Aspose.Words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../Aspose.Words/bookmarkstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBuildingBlock()](../../Aspose.Words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../Aspose.Words/buildingblock/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCell()](../../Aspose.Words/node/asCell/#default) | Cast node to [Cell](../../Aspose.Words.Tables/cell/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asComment()](../../Aspose.Words/node/asComment/#default) | Cast node to [Comment](../../Aspose.Words/comment/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeEnd()](../../Aspose.Words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../Aspose.Words/commentrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeStart()](../../Aspose.Words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../Aspose.Words/commentrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCompositeNode()](../../Aspose.Words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../Aspose.Words/compositenode/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asDocument()](../../Aspose.Words/node/asDocument/#default) | Cast node to [Node.document](../../Aspose.Words/node/document/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeEnd()](../../Aspose.Words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../Aspose.Words/editablerangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeStart()](../../Aspose.Words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../Aspose.Words/editablerangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldEnd()](../../Aspose.Words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../../Aspose.Words.Fields/fieldend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldSeparator()](../../Aspose.Words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../Aspose.Words.Fields/fieldseparator/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldStart()](../../Aspose.Words/node/asFieldStart/#default) | Cast node to [FieldStart](../../Aspose.Words.Fields/fieldstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFootnote()](../../Aspose.Words/node/asFootnote/#default) | Cast node to [Footnote](../../Aspose.Words.Notes/footnote/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFormField()](../../Aspose.Words/node/asFormField/#default) | Cast node to [FormField](../../Aspose.Words.Fields/formfield/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGlossaryDocument()](../../Aspose.Words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../Aspose.Words.BuildingBlocks/glossarydocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](../../Aspose.Words.Markup/smarttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../Aspose.Words.Markup/structureddocumenttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../Aspose.Words.Markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../Aspose.Words.Markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSubDocument()](../../Aspose.Words/node/asSubDocument/#default) | Cast node to [SubDocument](../../Aspose.Words/subdocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asTable()](../../Aspose.Words/node/asTable/#default) | Cast node to [Table](../../Aspose.Words/table/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ clone(isCloneChildren)](../../Aspose.Words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getAncestor(ancestorType)](../../Aspose.Words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../Aspose.Words/nodetype/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getBuildingBlock(index, isDeep)](../../Aspose.Words/compositenode/getBuildingBlock/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../../Aspose.Words/compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../../Aspose.Words/compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getComment(index, isDeep)](../../Aspose.Words/compositenode/getComment/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../../Aspose.Words/compositenode/getEditableRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getFootnote(index, isDeep)](../../Aspose.Words/compositenode/getFootnote/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getGroupShape(index, isDeep)](../../Aspose.Words/compositenode/getGroupShape/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getOfficeMath(index, isDeep)](../../Aspose.Words/compositenode/getOfficeMath/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getParagraph(index, isDeep)](../../Aspose.Words/compositenode/getParagraph/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getRun(index, isDeep)](../../Aspose.Words/compositenode/getRun/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSdt(index, isDeep)](../../Aspose.Words/compositenode/getSdt/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../../Aspose.Words/compositenode/getSdtRangeEnd/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../../Aspose.Words/compositenode/getSdtRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getShape(index, isDeep)](../../Aspose.Words/compositenode/getShape/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getShapeRenderer()](./getShapeRenderer/#default) | Creates and returns an object that can be used to render this shape into an image. |
|[ getSmartTag(index, isDeep)](../../Aspose.Words/compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getTable(index, isDeep)](../../Aspose.Words/compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getText()](../../Aspose.Words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ indexOf(child)](../../Aspose.Words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../Aspose.Words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../Aspose.Words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ localToParent(value)](./localToParent/#jspointf) |  |
|[ nextPreOrder(rootNode)](../../Aspose.Words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nodeTypeToString(nodeType)](../../Aspose.Words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ prependChild(newChild)](../../Aspose.Words/compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ previousPreOrder(rootNode)](../../Aspose.Words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ referenceEquals(other)](../../Aspose.Words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ remove()](../../Aspose.Words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ removeAllChildren()](../../Aspose.Words/compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ removeChild(oldChild)](../../Aspose.Words/compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ removeSmartTags()](../../Aspose.Words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../Aspose.Words.Markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectNodes(xpath)](../../Aspose.Words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectSingleNode(xpath)](../../Aspose.Words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../Aspose.Words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

### Examples

Shows how to insert a floating image to the center of a page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.wrapType = aw.Drawing.WrapType.None;
shape.behindText = true;
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.horizontalAlignment = aw.Drawing.HorizontalAlignment.Center;
shape.verticalAlignment = aw.Drawing.VerticalAlignment.Center;

doc.save(base.artifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### See Also

* module [Aspose.Words.Drawing](../)
* class [CompositeNode](../../Aspose.Words/compositenode/)
* class [Shape](../shape/)
* class [GroupShape](../groupshape/)

