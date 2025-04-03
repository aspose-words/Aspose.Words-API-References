---
title: CommentRangeEnd class
linktitle: CommentRangeEnd class
articleTitle: CommentRangeEnd class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.CommentRangeEnd class. Denotes the end of a region of text that has a comment associated with it"
type: docs
weight: 210
url: /nodejs-net/aspose.words/commentrangeend/
---

## CommentRangeEnd class

Denotes the end of a region of text that has a comment associated with it.
To learn more, visit the [Working with Comments](https://docs.aspose.com/words/nodejs-net/working-with-comments/) documentation article.




### Remarks

To create a comment anchored to a region of text, you need to create a [Comment](../comment/) and
then create [CommentRangeStart](../commentrangestart/) and [CommentRangeEnd](./) and set their identifiers 
to the same [Comment.id](../comment/id/) value.

[CommentRangeEnd](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).




**Inheritance:** [CommentRangeEnd](./) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [CommentRangeEnd(doc, id)](./constructor/#documentbase_number) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [id](./id/) | Specifies the identifier of the comment to which this region is linked to. |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.CommentRangeEnd](../nodetype/#CommentRangeEnd). |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ asBody()](../node/asBody/#default) | Cast node to [Body](../body/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkEnd()](../node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkStart()](../node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/).<br>(Inherited from [Node](../node/)) |
|[ asBuildingBlock()](../node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/).<br>(Inherited from [Node](../node/)) |
|[ asCell()](../node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../node/)) |
|[ asComment()](../node/asComment/#default) | Cast node to [Comment](../comment/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeEnd()](../node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](./).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeStart()](../node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asCompositeNode()](../node/asCompositeNode/#default) | Cast node to [CompositeNode](../compositenode/).<br>(Inherited from [Node](../node/)) |
|[ asDocument()](../node/asDocument/#default) | Cast node to [Node.document](../node/document/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeEnd()](../node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../editablerangeend/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeStart()](../node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../editablerangestart/).<br>(Inherited from [Node](../node/)) |
|[ asFieldEnd()](../node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../node/)) |
|[ asFieldSeparator()](../node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../node/)) |
|[ asFieldStart()](../node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../node/)) |
|[ asFootnote()](../node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../node/)) |
|[ asFormField()](../node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../node/)) |
|[ asGlossaryDocument()](../node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../node/)) |
|[ asGroupShape()](../node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../node/)) |
|[ asHeaderFooter()](../node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../headerfooter/).<br>(Inherited from [Node](../node/)) |
|[ asOfficeMath()](../node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../node/)) |
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](../paragraph/).<br>(Inherited from [Node](../node/)) |
|[ asRow()](../node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../node/)) |
|[ asRun()](../node/asRun/#default) | Cast node to [Run](../run/).<br>(Inherited from [Node](../node/)) |
|[ asSection()](../node/asSection/#default) | Cast node to [Section](../section/).<br>(Inherited from [Node](../node/)) |
|[ asShape()](../node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../node/)) |
|[ asSmartTag()](../node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../node/)) |
|[ asSpecialChar()](../node/asSpecialChar/#default) | Cast node to [SpecialChar](../specialchar/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTag()](../node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeEnd()](../node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeStart()](../node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asSubDocument()](../node/asSubDocument/#default) | Cast node to [SubDocument](../subdocument/).<br>(Inherited from [Node](../node/)) |
|[ asTable()](../node/asTable/#default) | Cast node to [Table](../table/).<br>(Inherited from [Node](../node/)) |
|[ clone(isCloneChildren)](../node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getText()](../node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how print the contents of all comments and their comment ranges using a document visitor.

```js
test('CreateCommentsAndPrintAllInfo', () => {
  let doc = new aw.Document();

  let newComment = new aw.Comment(doc);
  newComment.author = "VDeryushev";
  newComment.initial = "VD",
  newComment.dateTime = Date.now();

  newComment.setText("Comment regarding text.");

  // Add text to the document, warp it in a comment range, and then add your comment.
  let para = doc.firstSection.body.firstParagraph;
  para.appendChild(new aw.CommentRangeStart(doc, newComment.id));
  para.appendChild(new aw.Run(doc, "Commented text."));
  para.appendChild(new aw.CommentRangeEnd(doc, newComment.id));
  para.appendChild(newComment); 

  // Add two replies to the comment.
  newComment.addReply("John Doe", "JD", Date.now(), "New reply.");
  newComment.addReply("John Doe", "JD", Date.now(), "Another reply.");

  printAllCommentInfo(doc.getChildNodes(aw.NodeType.Comment, true));
});


/// <summary>
/// Iterates over every top-level comment and prints its comment range, contents, and replies.
/// </summary>
function printAllCommentInfo(comments)
{
  let commentVisitor = new CommentInfoPrinter();

    // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
  foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
  {
      // First, visit the start of the comment range.
    let commentRangeStart = (CommentRangeStart)comment.previousSibling.previousSibling.previousSibling;
    commentRangeStart.accept(commentVisitor);

      // Then, visit the comment, and any replies that it may have.
    comment.accept(commentVisitor);

    for (let reply of comment.replies)
      reply.accept(commentVisitor);

      // Finally, visit the end of the comment range, and then print the visitor's text contents.
    let commentRangeEnd = (CommentRangeEnd)comment.previousSibling;
    commentRangeEnd.accept(commentVisitor);

    console.log(commentVisitor.getText());
  }
}

  /// <summary>
  /// Prints information and contents of all comments and comment ranges encountered in the document.
  /// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
  public CommentInfoPrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideComment = false;
  }

    /// <summary>
    /// Gets the plain text of the document that was accumulated by the visitor.
    /// </summary>
  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.text + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a CommentRangeStart node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
  {
    IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.id);
    mDocTraversalDepth++;
    mVisitorIsInsideComment = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a CommentRangeEnd node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.id + "\n");
    mVisitorIsInsideComment = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Comment node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitCommentStart(Comment comment)
  {
    IndentAndAppendLine(
      `[Comment start] For comment range ID ${comment.id}, By ${comment.author} on ${comment.dateTime}`);
    mDocTraversalDepth++;
    mVisitorIsInsideComment = true;


    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when the visiting of a Comment node is ended in the document.
    /// </summary>
  public override VisitorAction VisitCommentEnd(Comment comment)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Comment end]");
    mVisitorIsInsideComment = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++)
    {
      mBuilder.append("|  ");
    }

    mBuilder.AppendLine(text);
  }

  private bool mVisitorIsInsideComment;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words](../)
* class [Node](../node/)
* class [Comment](../comment/)
* class [CommentRangeStart](../commentrangestart/)

