---
title: FieldStart class
linktitle: FieldStart class
articleTitle: FieldStart class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fields.FieldStart class. Represents a start of a Word field in a document"
type: docs
weight: 960
url: /nodejs-net/aspose.words.fields/fieldstart/
---

## FieldStart class

Represents a start of a Word field in a document.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Remarks

[FieldStart](./) is an inline-level node and represented by the
Aspose.Words.ControlChar.FieldStartChar control character in the document.

[FieldStart](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of
a field start character, field code, field separator character, field result
and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField()](../../aspose.words/documentbuilder/insertField/#string)
method.




**Inheritance:** [FieldStart](./) → [FieldChar](../fieldchar/) → [SpecialChar](../../aspose.words/specialchar/) → [Inline](../../aspose.words/inline/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [fieldData](./fieldData/) | Gets custom field data which is associated with the field. |
| [fieldType](../fieldchar/fieldType/) | Returns the type of the field.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [font](../../aspose.words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [isDeleteRevision](../../aspose.words/inline/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isDirty](../fieldchar/isDirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [isFormatRevision](../../aspose.words/inline/isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isInsertRevision](../../aspose.words/inline/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isLocked](../fieldchar/isLocked/) | Gets or sets whether the parent field is locked (should not recalculate its result).<br>(Inherited from [FieldChar](../fieldchar/)) |
| [isMoveFromRevision](../../aspose.words/inline/isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isMoveToRevision](../../aspose.words/inline/isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.FieldStart](../../aspose.words/nodetype/#FieldStart). |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parentParagraph](../../aspose.words/inline/parentParagraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
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
|[ asFieldEnd()](../../aspose.words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../fieldend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldSeparator()](../../aspose.words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../fieldseparator/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldStart()](../../aspose.words/node/asFieldStart/#default) | Cast node to [FieldStart](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFootnote()](../../aspose.words/node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFormField()](../../aspose.words/node/asFormField/#default) | Cast node to [FormField](../formfield/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGlossaryDocument()](../../aspose.words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSubDocument()](../../aspose.words/node/asSubDocument/#default) | Cast node to [SubDocument](../../aspose.words/subdocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asTable()](../../aspose.words/node/asTable/#default) | Cast node to [Table](../../aspose.words/table/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ clone(isCloneChildren)](../../aspose.words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getAncestor(ancestorType)](../../aspose.words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getField()](../fieldchar/getField/#default) | Returns a field for the field char.<br>(Inherited from [FieldChar](../fieldchar/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to find all hyperlinks in a Word document, and then change their URLs and display names.

```js
describe("ExReplaceHyperlinks", () => {
  test('Fields', () => {
    let doc = new aw.Document(base.myDir + "Hyperlinks.docx");

    // Hyperlinks in a Word documents are fields. To begin looking for hyperlinks, we must first find all the fields.
    // Use the "SelectNodes" method to find all the fields in the document via an XPath.
    let fieldStarts = doc.selectNodes("//FieldStart");

    foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
    {
      if (fieldStart.fieldType == aw.Fields.FieldType.FieldHyperlink)
      {
        let hyperlink = new aw.RW.OfficeShared.Hyperlink(fieldStart);

        // Hyperlinks that link to bookmarks do not have URLs.
        if (hyperlink.IsLocal)
          continue;

        // Give each URL hyperlink a new URL and name.
        hyperlink.target = NewUrl;
        hyperlink.name = NewName;
      }
    }

    doc.save(base.artifactsDir + "ReplaceHyperlinks.fields.docx");
  });


  private const string NewUrl = @"http://www.aspose.com";
  private const string NewName = "Aspose - The .NET & Java Component Publisher";

  /// <summary>
  /// HYPERLINK fields contain and display hyperlinks in the document body. A field in Aspose.Words 
  /// consists of several nodes, and it might be difficult to work with all those nodes directly. 
  /// This implementation will work only if the hyperlink code and name each consist of only one Run node.
  ///
  /// The node structure for fields is as follows:
  /// 
  /// [FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
  /// 
  /// Below are two example field codes of HYPERLINK fields:
  /// HYPERLINK "url"
  /// HYPERLINK \l "bookmark name"
  /// 
  /// A field's "Result" property contains text that the field displays in the document body to the user.
  /// </summary>
  internal class Hyperlink
  internal Hyperlink(FieldStart fieldStart)
  {
    if (fieldStart == null)
      throw new ArgumentNullException("fieldStart");
    if (fieldStart.fieldType != aw.Fields.FieldType.FieldHyperlink)
      throw new ArgumentException("Field start type must be FieldHyperlink.");

    mFieldStart = fieldStart;

      // Find the field separator node.
    mFieldSeparator = FindNextSibling(mFieldStart, aw.NodeType.FieldSeparator);
    if (mFieldSeparator == null)
      throw new InvalidOperationException("Cannot find field separator.");

      // Normally, we can always find the field's end node, but the example document 
      // contains a paragraph break inside a hyperlink, which puts the field end 
      // in the next paragraph. It will be much more complicated to handle fields which span several 
      // paragraphs correctly. In this case allowing field end to be null is enough.
    mFieldEnd = FindNextSibling(mFieldSeparator, aw.NodeType.FieldEnd);

      // Field code looks something like "HYPERLINK "http:\\www.myurl.com"", but it can consist of several runs.
    string fieldCode = GetTextSameParent(mFieldStart.nextSibling, mFieldSeparator);
    Match match = gRegex.match(fieldCode.trim());

      // The hyperlink is local if \l is present in the field code.
    mIsLocal = match.groups.at(1).length > 0; 
    mTarget = match.groups.at(2).value;
  }

    /// <summary>
    /// Gets or sets the display name of the hyperlink.
    /// </summary>
  internal string Name
  {
    get
    {
      return GetTextSameParent(mFieldSeparator, mFieldEnd);
    }
    set
    {
        // Hyperlink display name is stored in the field result, which is a Run 
        // node between field separator and field end.
      let fieldResult = (Run) mFieldSeparator.nextSibling;
      fieldResult.text = value;

        // If the field result consists of more than one run, delete these runs.
      RemoveSameParent(fieldResult.nextSibling, mFieldEnd);
    }
  }

    /// <summary>
    /// Gets or sets the target URL or bookmark name of the hyperlink.
    /// </summary>
  internal string Target
  {
    get
    {
      return mTarget;
    }
    set
    {
      mTarget = value;
      UpdateFieldCode();
    }
  }

    /// <summary>
    /// True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
    /// </summary>
  internal bool IsLocal
  {
    get
    {
      return mIsLocal;
    }
    set
    {
      mIsLocal = value;
      UpdateFieldCode();
    }
  }

  private void UpdateFieldCode()
  {
      // A field's field code is in a Run node between the field's start node and field separator.
    let fieldCode = (Run) mFieldStart.nextSibling;
    fieldCode.text = string.format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

      // If the field code consists of more than one run, delete these runs.
    RemoveSameParent(fieldCode.nextSibling, mFieldSeparator);
  }

    /// <summary>
    /// Goes through siblings starting from the start node until it finds a node of the specified type or null.
    /// </summary>
  private static Node FindNextSibling(Node startNode, NodeType nodeType)
  {
    for (let node = startNode; node != null; node = node.nextSibling)
    {
      if (node.nodeType == nodeType)
        return node;
    }

    return null;
  }

    /// <summary>
    /// Retrieves text from start up to but not including the end node.
    /// </summary>
  private static string GetTextSameParent(Node startNode, Node endNode)
  {
    if ((endNode != null) && (startNode.parentNode != endNode.parentNode))
      throw new ArgumentException("Start and end nodes are expected to have the same parent.");

    let builder = new StringBuilder();
    for (let child = startNode; !child.equals(endNode); child = child.nextSibling)
      builder.append(child.getText());

    return builder.toString();
  }

    /// <summary>
    /// Removes nodes from start up to but not including the end node.
    /// Assumes that the start and end nodes have the same parent.
    /// </summary>
  private static void RemoveSameParent(Node startNode, Node endNode)
  {
    if (endNode != null && startNode.parentNode != endNode.parentNode)
      throw new ArgumentException("Start and end nodes are expected to have the same parent.");

    let curChild = startNode;
    while ((curChild != null) && (curChild != endNode))
    {
      let nextChild = curChild.nextSibling;
      curChild.remove();
      curChild = nextChild;
    }
  }

  private readonly Node mFieldStart;
  private readonly Node mFieldSeparator;
  private readonly Node mFieldEnd;
  private bool mIsLocal;
  private string mTarget;

  private static readonly Regex gRegex = new Regex(
    "\\S+" + // One or more non spaces HYPERLINK or other word in other languages.
    "\\s+" + // One or more spaces.
    "(?:\"\"\\s+)?" + // Non-capturing optional "" and one or more spaces.
    "(\\\\l\\s+)?" + // Optional \l flag followed by one or more spaces.
    "\"" + // One apostrophe.	
    "([^\"]+)" + // One or more characters, excluding the apostrophe (hyperlink target).
    "\"" // One closing apostrophe.
  );
```

### See Also

* module [Aspose.Words.Fields](../)
* class [FieldChar](../fieldchar/)

