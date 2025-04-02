---
title: FieldStart class
linktitle: FieldStart class
articleTitle: FieldStart class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.FieldStart class. Represents a start of a Word field in a document"
type: docs
weight: 960
url: /nodejs-net/Aspose.Words.Fields/fieldstart/
---

## FieldStart class

Represents a start of a Word field in a document.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Remarks

[FieldStart](./) is an inline-level node and represented by the
Aspose.Words.ControlChar.FieldStartChar control character in the document.

[FieldStart](./) can only be a child of [Paragraph](../../Aspose.Words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of
a field start character, field code, field separator character, field result
and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField()](../../Aspose.Words/documentbuilder/insertField/#string)
method.




**Inheritance:** [FieldStart](./) → [FieldChar](../fieldchar/) → [SpecialChar](../../Aspose.Words/specialchar/) → [Inline](../../Aspose.Words/inline/) → [Node](../../Aspose.Words/node/)

### Properties

| Name | Description |
| --- | --- |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [fieldData](./fieldData/) | Gets custom field data which is associated with the field. |
| [fieldType](../fieldchar/fieldType/) | Returns the type of the field.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [font](../../Aspose.Words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [isDeleteRevision](../../Aspose.Words/inline/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isDirty](../fieldchar/isDirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [isFormatRevision](../../Aspose.Words/inline/isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isInsertRevision](../../Aspose.Words/inline/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isLocked](../fieldchar/isLocked/) | Gets or sets whether the parent field is locked (should not recalculate its result).<br>(Inherited from [FieldChar](../fieldchar/)) |
| [isMoveFromRevision](../../Aspose.Words/inline/isMoveFromRevision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [isMoveToRevision](../../Aspose.Words/inline/isMoveToRevision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.FieldStart](../../Aspose.Words/nodetype/#FieldStart). |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [parentParagraph](../../Aspose.Words/inline/parentParagraph/) | Retrieves the parent [Paragraph](../../Aspose.Words/paragraph/) of this node.<br>(Inherited from [Inline](../../Aspose.Words/inline/)) |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
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
|[ asFieldEnd()](../../Aspose.Words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../fieldend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldSeparator()](../../Aspose.Words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../fieldseparator/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldStart()](../../Aspose.Words/node/asFieldStart/#default) | Cast node to [FieldStart](./).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFootnote()](../../Aspose.Words/node/asFootnote/#default) | Cast node to [Footnote](../../Aspose.Words.Notes/footnote/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFormField()](../../Aspose.Words/node/asFormField/#default) | Cast node to [FormField](../formfield/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGlossaryDocument()](../../Aspose.Words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../Aspose.Words.BuildingBlocks/glossarydocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](../../Aspose.Words.Markup/smarttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../Aspose.Words.Markup/structureddocumenttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../Aspose.Words.Markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../Aspose.Words.Markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSubDocument()](../../Aspose.Words/node/asSubDocument/#default) | Cast node to [SubDocument](../../Aspose.Words/subdocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asTable()](../../Aspose.Words/node/asTable/#default) | Cast node to [Table](../../Aspose.Words/table/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ clone(isCloneChildren)](../../Aspose.Words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getAncestor(ancestorType)](../../Aspose.Words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../Aspose.Words/nodetype/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getField()](../fieldchar/getField/#default) | Returns a field for the field char.<br>(Inherited from [FieldChar](../fieldchar/)) |
|[ getText()](../../Aspose.Words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nextPreOrder(rootNode)](../../Aspose.Words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nodeTypeToString(nodeType)](../../Aspose.Words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ previousPreOrder(rootNode)](../../Aspose.Words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ referenceEquals(other)](../../Aspose.Words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ remove()](../../Aspose.Words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

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

