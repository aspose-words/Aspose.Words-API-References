---
title: SmartTag class
linktitle: SmartTag class
articleTitle: SmartTag class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.SmartTag class. This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph"
type: docs
weight: 160
url: /nodejs-net/Aspose.Words.Markup/smarttag/
---

## SmartTag class

This element specifies the presence of a smart tag around one or more inline structures
(runs, images, fields,etc.) within a paragraph.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Remarks

Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding
customer-defined semantics into the document via the ability to provide a basic namespace/name
for a run or set of runs within a document.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or
another [SmartTag](./) node.

The complete list of child nodes that can occur inside a smart tag consists of
[BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/),
[FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/),
[Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/),
[Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/),
[Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/),
[CommentRangeStart](../../aspose.words/commentrangestart/),
[CommentRangeEnd](../../aspose.words/commentrangeend/),
[SmartTag](./).




**Inheritance:** [SmartTag](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [SmartTag(doc)](./constructor/#documentbase) | Initializes a new instance of the [SmartTag](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [element](./element/) | Specifies the name of the smart tag within the document. |
| [firstChild](../../aspose.words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [hasChildNodes](../../aspose.words/compositenode/hasChildNodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [lastChild](../../aspose.words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.SmartTag](../../aspose.words/nodetype/#SmartTag). |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [properties](./properties/) | A collection of the smart tag properties. |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [uri](./uri/) | Specifies the namespace URI of the smart tag. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the SmartTag. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the SmartTag. |
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
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
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
|[ getSmartTag(index, isDeep)](../../aspose.words/compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getTable(index, isDeep)](../../aspose.words/compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ indexOf(child)](../../aspose.words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../aspose.words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../aspose.words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prependChild(newChild)](../../aspose.words/compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ removeAllChildren()](../../aspose.words/compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ removeChild(oldChild)](../../aspose.words/compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ removeSmartTags()](../../aspose.words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](./) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ selectNodes(xpath)](../../aspose.words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ selectSingleNode(xpath)](../../aspose.words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to create smart tags.

```js
test('Create', () => {
  let doc = new aw.Document();

  // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
  // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
  let smartTag = new aw.Markup.SmartTag(doc);

  // Smart tags are composite nodes that contain their recognized text in its entirety.
  // Add contents to this smart tag manually.
  smartTag.appendChild(new aw.Run(doc, "May 29, 2019"));

  // Microsoft Word may recognize the above contents as being a date.
  // Smart tags use the "Element" property to reflect the type of data they contain.
  smartTag.element = "date";

  // Some smart tag types process their contents further into custom XML properties.
  smartTag.properties.add(new aw.Markup.CustomXmlProperty("Day", '', "29"));
  smartTag.properties.add(new aw.Markup.CustomXmlProperty("Month", '', "5"));
  smartTag.properties.add(new aw.Markup.CustomXmlProperty("Year", '', "2019"));

  // Set the smart tag's URI to the default value.
  smartTag.uri = "urn:schemas-microsoft-com:office:smarttags";

  doc.firstSection.body.firstParagraph.appendChild(smartTag);
  doc.firstSection.body.firstParagraph.appendChild(new aw.Run(doc, " is a date. "));

  // Create another smart tag for a stock ticker.
  smartTag = new aw.Markup.SmartTag(doc);
  smartTag.element = "stockticker";
  smartTag.uri = "urn:schemas-microsoft-com:office:smarttags";

  smartTag.appendChild(new aw.Run(doc, "MSFT"));

  doc.firstSection.body.firstParagraph.appendChild(smartTag);
  doc.firstSection.body.firstParagraph.appendChild(new aw.Run(doc, " is a stock ticker."));

  // Print all the smart tags in our document using a document visitor.
  doc.accept(new SmartTagPrinter());

  // Older versions of Microsoft Word support smart tags.
  doc.save(base.artifactsDir + "SmartTag.create.doc");

  // Use the "RemoveSmartTags" method to remove all smart tags from a document.
  expect(doc.getChildNodes(aw.NodeType.SmartTag, true).Count).toEqual(2);

  doc.removeSmartTags();

  expect(doc.getChildNodes(aw.NodeType.SmartTag, true).Count).toEqual(0);
});


  /// <summary>
  /// Prints visited smart tags and their contents.
  /// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Called when a SmartTag node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
  {
    console.log(`Smart tag type: ${smartTag.element}`);
    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when the visiting of a SmartTag node is ended.
    /// </summary>
  public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
  {
    console.log(`\tContents: \"${smartTag.toString(aw.SaveFormat.Text)}\"`);

    if (smartTag.properties.count == 0)
    {
      console.log("\tContains no properties");
    }
    else
    {
      Console.write("\tProperties: ");
      string.at(] properties = new string[smartTag.properties.count);
      int index = 0;

      for (let cxp of smartTag.properties)
        properties.at(index++) = `\"${cxp.name}\" = \"${cxp.value}\"`;

      console.log(string.Join(", ", properties));
    }

    return aw.VisitorAction.Continue;
  }
}
```

### See Also

* module [Aspose.Words.Markup](../)
* class [CompositeNode](../../aspose.words/compositenode/)

