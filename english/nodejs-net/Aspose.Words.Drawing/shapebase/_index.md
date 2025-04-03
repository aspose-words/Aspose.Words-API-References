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

If the shape is a child of a [Paragraph](../../aspose.words/paragraph/) object, then the shape is said to be "top-level".
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




**Inheritance:** [ShapeBase](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [allowOverlap](./allowOverlap/) | Gets or sets a value that specifies whether this shape can overlap other shapes. |
| [alternativeText](./alternativeText/) | Defines alternative text to be displayed instead of a graphic. |
| [anchorLocked](./anchorLocked/) | Specifies whether the shape's anchor is locked. |
| [aspectRatioLocked](./aspectRatioLocked/) | Specifies whether the shape's aspect ratio is locked. |
| [behindText](./behindText/) | Specifies whether the shape is below or above text. |
| [bottom](./bottom/) | Gets the position of the bottom edge of the containing block of the shape. |
| [canHaveImage](./canHaveImage/) | Returns ``true`` if the shape type allows the shape to have an image. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [distanceBottom](./distanceBottom/) | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [distanceLeft](./distanceLeft/) | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [distanceRight](./distanceRight/) | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [distanceTop](./distanceTop/) | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [fill](./fill/) | Gets fill formatting for the shape. |
| [firstChild](../../aspose.words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [flipOrientation](./flipOrientation/) | Switches the orientation of a shape. |
| [font](./font/) | Provides access to the font formatting of this object. |
| [glow](./glow/) | Gets glow formatting for the shape. |
| [hasChildNodes](../../aspose.words/compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [height](./height/) | Gets or sets the height of the containing block of the shape. |
| [heightRelative](./heightRelative/) | Gets or sets the value that represents the percentage of shape's relative height. |
| [hidden](./hidden/) | Gets or sets a boolean value indicating whether the shape is visible. |
| [horizontalAlignment](./horizontalAlignment/) | Specifies how the shape is positioned horizontally. |
| [href](./href/) | Gets or sets the full hyperlink address for a shape. |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [isDecorative](./isDecorative/) | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [isDeleteRevision](./isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isGroup](./isGroup/) | Returns ``true`` if this is a group shape. |
| [isHorizontalRule](./isHorizontalRule/) | Returns ``true`` if this shape is a horizontal rule. |
| [isImage](./isImage/) | Returns ``true`` if this shape is an image shape. |
| [isInline](./isInline/) | A quick way to determine if this shape is positioned inline with text. |
| [isInsertRevision](./isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isLayoutInCell](./isLayoutInCell/) | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [isMoveFromRevision](./isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision](./isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [isSignatureLine](./isSignatureLine/) | Indicates that shape is a [SignatureLine](../signatureline/). |
| [isTopLevel](./isTopLevel/) | Returns ``true`` if this shape is not a child of a group shape. |
| [isWordArt](./isWordArt/) | Returns ``true`` if this shape is a WordArt object. |
| [lastChild](../../aspose.words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [left](./left/) | Gets or sets the position of the left edge of the containing block of the shape. |
| [leftRelative](./leftRelative/) | Gets or sets the value that represents shape's relative left position in percent. |
| [markupLanguage](./markupLanguage/) | Gets MarkupLanguage used for this graphic object. |
| [name](./name/) | Gets or sets the optional shape name. |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](../../aspose.words/node/nodeType/) | Gets the type of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parentParagraph](./parentParagraph/) | Returns the immediate parent paragraph. |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
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
|[ accept(visitor)](../../aspose.words/node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ acceptEnd(visitor)](../../aspose.words/compositenode/acceptEnd/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ acceptStart(visitor)](../../aspose.words/compositenode/acceptStart/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ adjustWithEffects(source)](./adjustWithEffects/#jsrectanglef) |  |
|[ appendChild(newChild)](../../aspose.words/compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ asBody()](../../aspose.words/node/asBody/#default) | Cast node to [Body](../../aspose.words/body/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkEnd()](../../aspose.words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../aspose.words/bookmarkend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkStart()](../../aspose.words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../aspose.words/bookmarkstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBuildingBlock()](../../aspose.words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../aspose.words/buildingblock/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCell()](../../aspose.words/node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asComment()](../../aspose.words/node/asComment/#default) | Cast node to [Comment](../../aspose.words/comment/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeEnd()](../../aspose.words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../aspose.words/commentrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeStart()](../../aspose.words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../aspose.words/commentrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCompositeNode()](../../aspose.words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../aspose.words/compositenode/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asDocument()](../../aspose.words/node/asDocument/#default) | Cast node to [Node.document](../../aspose.words/node/document/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeEnd()](../../aspose.words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../aspose.words/editablerangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeStart()](../../aspose.words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../aspose.words/editablerangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldEnd()](../../aspose.words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldSeparator()](../../aspose.words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldStart()](../../aspose.words/node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFootnote()](../../aspose.words/node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFormField()](../../aspose.words/node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGlossaryDocument()](../../aspose.words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSubDocument()](../../aspose.words/node/asSubDocument/#default) | Cast node to [SubDocument](../../aspose.words/subdocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asTable()](../../aspose.words/node/asTable/#default) | Cast node to [Table](../../aspose.words/table/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ clone(isCloneChildren)](../../aspose.words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getAncestor(ancestorType)](../../aspose.words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getBuildingBlock(index, isDeep)](../../aspose.words/compositenode/getBuildingBlock/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../../aspose.words/compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../../aspose.words/compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getComment(index, isDeep)](../../aspose.words/compositenode/getComment/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../../aspose.words/compositenode/getEditableRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getFootnote(index, isDeep)](../../aspose.words/compositenode/getFootnote/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getGroupShape(index, isDeep)](../../aspose.words/compositenode/getGroupShape/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getOfficeMath(index, isDeep)](../../aspose.words/compositenode/getOfficeMath/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getParagraph(index, isDeep)](../../aspose.words/compositenode/getParagraph/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getRun(index, isDeep)](../../aspose.words/compositenode/getRun/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSdt(index, isDeep)](../../aspose.words/compositenode/getSdt/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../../aspose.words/compositenode/getSdtRangeEnd/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../../aspose.words/compositenode/getSdtRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getShape(index, isDeep)](../../aspose.words/compositenode/getShape/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getShapeRenderer()](./getShapeRenderer/#default) | Creates and returns an object that can be used to render this shape into an image. |
|[ getSmartTag(index, isDeep)](../../aspose.words/compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getTable(index, isDeep)](../../aspose.words/compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ indexOf(child)](../../aspose.words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../aspose.words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../aspose.words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ localToParent(value)](./localToParent/#jspointf) |  |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prependChild(newChild)](../../aspose.words/compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ removeAllChildren()](../../aspose.words/compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ removeChild(oldChild)](../../aspose.words/compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ removeSmartTags()](../../aspose.words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ selectNodes(xpath)](../../aspose.words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ selectSingleNode(xpath)](../../aspose.words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

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
* class [CompositeNode](../../aspose.words/compositenode/)
* class [Shape](../shape/)
* class [GroupShape](../groupshape/)

