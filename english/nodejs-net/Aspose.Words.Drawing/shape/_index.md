---
title: Shape class
linktitle: Shape class
articleTitle: Shape class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Shape class. Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture"
type: docs
weight: 370
url: /nodejs-net/Aspose.Words.Drawing/shape/
---

## Shape class

Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/nodejs-net/working-with-shapes/) documentation article.




### Remarks

Using the [Shape](./) class you can create or modify shapes in a Microsoft Word document.

An important property of a shape is its [ShapeBase.shapeType](../shapebase/shapeType/). Shapes of different
types can have different capabilities in a Word document. For example, only image and OLE shapes
can have images inside them. Most of the shapes can have text, but not all.

Shapes that can have text, can contain [Paragraph](../../aspose.words/paragraph/) and
[Table](../../aspose.words/table/) nodes as children.




**Inheritance:** [Shape](./) → [ShapeBase](../shapebase/) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [Shape(doc, shapeType)](./constructor/#documentbase_shapetype) | Creates a new shape object. |

### Properties

| Name | Description |
| --- | --- |
| [adjustments](./adjustments/) | Provides access to the adjustment raw values of a shape. For a shape that does not contain any adjustment raw values, it returns an empty collection. |
| [allowOverlap](../shapebase/allowOverlap/) | Gets or sets a value that specifies whether this shape can overlap other shapes.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [alternativeText](../shapebase/alternativeText/) | Defines alternative text to be displayed instead of a graphic.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [anchorLocked](../shapebase/anchorLocked/) | Specifies whether the shape's anchor is locked.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [aspectRatioLocked](../shapebase/aspectRatioLocked/) | Specifies whether the shape's aspect ratio is locked.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [behindText](../shapebase/behindText/) | Specifies whether the shape is below or above text.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [bottom](../shapebase/bottom/) | Gets the position of the bottom edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [canHaveImage](../shapebase/canHaveImage/) | Returns ``true`` if the shape type allows the shape to have an image.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [chart](./chart/) | Provides access to the chart properties if this shape has a [Chart](../chart/). |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [distanceBottom](../shapebase/distanceBottom/) | Returns or sets the distance (in points) between the document text and the bottom edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [distanceLeft](../shapebase/distanceLeft/) | Returns or sets the distance (in points) between the document text and the left edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [distanceRight](../shapebase/distanceRight/) | Returns or sets the distance (in points) between the document text and the right edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [distanceTop](../shapebase/distanceTop/) | Returns or sets the distance (in points) between the document text and the top edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [extrusionEnabled](./extrusionEnabled/) | Returns ``true`` if an extrusion effect is enabled. |
| [fill](../shapebase/fill/) | Gets fill formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [fillColor](./fillColor/) | Defines the brush color that fills the closed path of the shape. |
| [filled](./filled/) | Determines whether the closed path of the shape will be filled. |
| [firstChild](../../aspose.words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [firstParagraph](./firstParagraph/) | Gets the first paragraph in the shape. |
| [flipOrientation](../shapebase/flipOrientation/) | Switches the orientation of a shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [font](../shapebase/font/) | Provides access to the font formatting of this object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [glow](../shapebase/glow/) | Gets glow formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [hasChart](./hasChart/) | Returns ``true`` if this [Shape](./) has a [Chart](../chart/). |
| [hasChildNodes](../../aspose.words/compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [hasImage](./hasImage/) | Returns ``true`` if the shape has image bytes or links an image. |
| [hasSmartArt](./hasSmartArt/) | Returns ``true`` if this [Shape](./) has a SmartArt object. |
| [height](../shapebase/height/) | Gets or sets the height of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [heightRelative](../shapebase/heightRelative/) | Gets or sets the value that represents the percentage of shape's relative height.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [hidden](../shapebase/hidden/) | Gets or sets a boolean value indicating whether the shape is visible.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [horizontalAlignment](../shapebase/horizontalAlignment/) | Specifies how the shape is positioned horizontally.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [horizontalRuleFormat](./horizontalRuleFormat/) | Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns ``null``. |
| [href](../shapebase/href/) | Gets or sets the full hyperlink address for a shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [imageData](./imageData/) | Provides access to the image of the shape. Returns ``null`` if the shape cannot have an image. |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [isDecorative](../shapebase/isDecorative/) | Gets or sets the flag that specifies whether the shape is decorative in the document.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isDeleteRevision](../shapebase/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isGroup](../shapebase/isGroup/) | Returns ``true`` if this is a group shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isHorizontalRule](../shapebase/isHorizontalRule/) | Returns ``true`` if this shape is a horizontal rule.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isImage](../shapebase/isImage/) | Returns ``true`` if this shape is an image shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isInline](../shapebase/isInline/) | A quick way to determine if this shape is positioned inline with text.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isInsertRevision](../shapebase/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isLayoutInCell](../shapebase/isLayoutInCell/) | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isMoveFromRevision](../shapebase/isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isMoveToRevision](../shapebase/isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isSignatureLine](../shapebase/isSignatureLine/) | Indicates that shape is a [SignatureLine](../signatureline/).<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isTopLevel](../shapebase/isTopLevel/) | Returns ``true`` if this shape is not a child of a group shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [isWordArt](../shapebase/isWordArt/) | Returns ``true`` if this shape is a WordArt object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [lastChild](../../aspose.words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [lastParagraph](./lastParagraph/) | Gets the last paragraph in the shape. |
| [left](../shapebase/left/) | Gets or sets the position of the left edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [leftRelative](../shapebase/leftRelative/) | Gets or sets the value that represents shape's relative left position in percent.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [markupLanguage](../shapebase/markupLanguage/) | Gets MarkupLanguage used for this graphic object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [name](../shapebase/name/) | Gets or sets the optional shape name.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.Shape](../../aspose.words/nodetype/#Shape). |
| [oleFormat](./oleFormat/) | Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns ``null``. |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parentParagraph](../shapebase/parentParagraph/) | Returns the immediate parent paragraph.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [reflection](../shapebase/reflection/) | Gets reflection formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [relativeHorizontalPosition](../shapebase/relativeHorizontalPosition/) | Specifies relative to what the shape is positioned horizontally.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [relativeHorizontalSize](../shapebase/relativeHorizontalSize/) | Gets or sets the value of shape's relative size in horizontal direction.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [relativeVerticalPosition](../shapebase/relativeVerticalPosition/) | Specifies relative to what the shape is positioned vertically.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [relativeVerticalSize](../shapebase/relativeVerticalSize/) | Gets or sets the value of shape's relative size in vertical direction.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [right](../shapebase/right/) | Gets the position of the right edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [rotation](../shapebase/rotation/) | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [screenTip](../shapebase/screenTip/) | Defines the text displayed when the mouse pointer moves over the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [shadowEnabled](./shadowEnabled/) | Returns ``true`` if a shadow effect is enabled. |
| [shadowFormat](../shapebase/shadowFormat/) | Gets shadow formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [shapeType](../shapebase/shapeType/) | Gets the shape type.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [signatureLine](./signatureLine/) | Gets [SignatureLine](../signatureline/) object if the shape is a signature line. Returns ``null`` otherwise. |
| [softEdge](../shapebase/softEdge/) | Gets soft edge formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [storyType](./storyType/) | Returns [StoryType.Textbox](../../aspose.words/storytype/#Textbox). |
| [stroke](./stroke/) | Defines a stroke for a shape. |
| [strokeColor](./strokeColor/) | Defines the color of a stroke. |
| [strokeWeight](./strokeWeight/) | Defines the brush thickness that strokes the path of a shape in points. |
| [stroked](./stroked/) | Defines whether the path will be stroked. |
| [target](../shapebase/target/) | Gets or sets the target frame for the shape hyperlink.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [textBox](./textBox/) | Defines attributes that specify how text is displayed in a shape. |
| [textPath](./textPath/) | Defines the text of the text path (of a WordArt object). |
| [title](../shapebase/title/) | Gets or sets the title (caption) of the current shape object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [top](../shapebase/top/) | Gets or sets the position of the top edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [topRelative](../shapebase/topRelative/) | Gets or sets the value that represents shape's relative top position in percent.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [verticalAlignment](../shapebase/verticalAlignment/) | Specifies how the shape is positioned vertically.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [width](../shapebase/width/) | Gets or sets the width of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [widthRelative](../shapebase/widthRelative/) | Gets or sets the value that represents the percentage of shape's relative width.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [wrapSide](../shapebase/wrapSide/) | Specifies how the text is wrapped around the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [wrapType](../shapebase/wrapType/) | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [zorder](../shapebase/zorder/) | Determines the display order of overlapping shapes.<br>(Inherited from [ShapeBase](../shapebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the shape. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the shape. |
|[ adjustWithEffects(source)](../shapebase/adjustWithEffects/#jsrectanglef) | <br>(Inherited from [ShapeBase](../shapebase/)) |
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
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
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
|[ getShapeRenderer()](../shapebase/getShapeRenderer/#default) | Creates and returns an object that can be used to render this shape into an image.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ getSmartTag(index, isDeep)](../../aspose.words/compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getTable(index, isDeep)](../../aspose.words/compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ indexOf(child)](../../aspose.words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../aspose.words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../aspose.words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ localToParent(value)](../shapebase/localToParent/#jspointf) | <br>(Inherited from [ShapeBase](../shapebase/)) |
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
|[ updateSmartArtDrawing()](./updateSmartArtDrawing/#default) | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |

### Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
let nodes = [...doc.getChildNodes(aw.NodeType.Shape, true)];

expect(nodes.filter(s => s.asShape().hasImage).length).toEqual(9);

let imageIndex = 0;
for (let node of nodes)
{
  let shape = node.asShape();
  if (shape.hasImage)
  {
    // The image data of shapes may contain images of many possible image formats. 
    // We can determine a file extension for each image automatically, based on its format.
    let imageFileName =
      `File.ExtractImages.${imageIndex}${aw.FileFormatUtil.imageTypeToExtension(shape.imageData.imageType)}`;
    shape.imageData.save(base.artifactsDir + imageFileName);
    imageIndex++;
  }
}
```

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

Shows how to delete all shapes from a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert two shapes along with a group shape with another shape inside it.
builder.insertShape(aw.Drawing.ShapeType.Rectangle, 400, 200);
builder.insertShape(aw.Drawing.ShapeType.Star, 300, 300);

let group = new aw.Drawing.GroupShape(doc);
group.bounds2 = new aw.JSRectangleF(100, 50, 200, 100);
group.coordOrigin2 = new aw.JSPoint(-1000, -500);

let subShape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Cube);
subShape.width = 500;
subShape.height = 700;
subShape.left = 0;
subShape.top = 0;

group.appendChild(subShape);
builder.insertNode(group);

expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(3);
expect(doc.getChildNodes(aw.NodeType.GroupShape, true).count).toEqual(1);

// Remove all Shape nodes from the document.
let shapes = doc.getChildNodes(aw.NodeType.Shape, true);
shapes.clear();

// All shapes are gone, but the group shape is still in the document.
expect(doc.getChildNodes(aw.NodeType.GroupShape, true).count).toEqual(1);
expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(0);

// Remove all group shapes separately.
let groupShapes = doc.getChildNodes(aw.NodeType.GroupShape, true);
groupShapes.clear();

expect(doc.getChildNodes(aw.NodeType.GroupShape, true).count).toEqual(0);
expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(0);
```

### See Also

* module [Aspose.Words.Drawing](../)
* class [ShapeBase](../shapebase/)
* class [GroupShape](../groupshape/)

