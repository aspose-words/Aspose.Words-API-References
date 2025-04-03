---
title: DocumentVisitor.visitCommentEnd method
linktitle: visitCommentEnd method
articleTitle: visitCommentEnd method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitCommentEnd method. Called when enumeration of a comment text has ended."
type: docs
weight: 100
url: /nodejs-net/aspose.words/documentvisitor/visitCommentEnd/
---

## visitCommentEnd(comment) {#comment}

Called when enumeration of a comment text has ended.


```js
visitCommentEnd(comment: Aspose.Words.Comment)
```

| Parameter | Type | Description |
| --- | --- | --- |
| comment | [Comment](../../comment/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every comment and comment range in a document.

```js
test('CommentsToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new CommentStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered Comment/CommentRange nodes and their children.
  /// </summary>
public class CommentStructurePrinter : DocumentVisitor
{
  public CommentStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideComment = false;
  }

  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// A Run is only recorded if it is a child of a Comment or CommentRange node.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

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
    IndentAndAppendLine("[Comment range end]");
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
    /// Called after all the child nodes of a Comment node have been visited.
    /// </summary>
  public override VisitorAction VisitCommentEnd(Comment comment)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Comment end]");
    mVisitorIsInsideComment = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
    /// into a comment/comment range's tree of child nodes.
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

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

