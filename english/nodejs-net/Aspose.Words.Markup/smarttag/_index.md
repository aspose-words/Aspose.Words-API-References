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

[SmartTag](./) can be a child of a [Paragraph](../../Aspose.Words/paragraph/) or
another [SmartTag](./) node.

The complete list of child nodes that can occur inside a smart tag consists of
[BookmarkStart](../../Aspose.Words/bookmarkstart/), [BookmarkEnd](../../Aspose.Words/bookmarkend/),
[FieldStart](../../Aspose.Words.Fields/fieldstart/), [FieldSeparator](../../Aspose.Words.Fields/fieldseparator/), [FieldEnd](../../Aspose.Words.Fields/fieldend/), [FormField](../../Aspose.Words.Fields/formfield/),
[Comment](../../Aspose.Words/comment/), [Footnote](../../Aspose.Words.Notes/footnote/),
[Run](../../Aspose.Words/run/), [SpecialChar](../../Aspose.Words/specialchar/),
[Shape](../../Aspose.Words.Drawing/shape/), [GroupShape](../../Aspose.Words.Drawing/groupshape/),
[CommentRangeStart](../../Aspose.Words/commentrangestart/),
[CommentRangeEnd](../../Aspose.Words/commentrangeend/),
[SmartTag](./).




**Inheritance:** [SmartTag](./) → [CompositeNode](../../Aspose.Words/compositenode/) → [Node](../../Aspose.Words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [SmartTag(doc)](./SmartTag/#documentbase) | Initializes a new instance of the [SmartTag](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [count](../../Aspose.Words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [element](./element/) | Specifies the name of the smart tag within the document. |
| [firstChild](../../Aspose.Words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [hasChildNodes](../../Aspose.Words/compositenode/hasChildNodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [lastChild](../../Aspose.Words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.SmartTag](../../Aspose.Words/nodetype/#SmartTag). |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [properties](./properties/) | A collection of the smart tag properties. |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [uri](./uri/) | Specifies the namespace URI of the smart tag. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the SmartTag. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the SmartTag. |
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
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](./).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../structureddocumenttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
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
|[ getSmartTag(index, isDeep)](../../Aspose.Words/compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getTable(index, isDeep)](../../Aspose.Words/compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getText()](../../Aspose.Words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ indexOf(child)](../../Aspose.Words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../Aspose.Words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../Aspose.Words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ nextPreOrder(rootNode)](../../Aspose.Words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nodeTypeToString(nodeType)](../../Aspose.Words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ prependChild(newChild)](../../Aspose.Words/compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ previousPreOrder(rootNode)](../../Aspose.Words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ referenceEquals(other)](../../Aspose.Words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ remove()](../../Aspose.Words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ removeAllChildren()](../../Aspose.Words/compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ removeChild(oldChild)](../../Aspose.Words/compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ removeSmartTags()](../../Aspose.Words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](./) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectNodes(xpath)](../../Aspose.Words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectSingleNode(xpath)](../../Aspose.Words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../Aspose.Words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

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
* class [CompositeNode](../../Aspose.Words/compositenode/)

