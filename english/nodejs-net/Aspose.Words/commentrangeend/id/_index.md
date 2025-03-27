---
title: CommentRangeEnd.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for NodeJs
description: "CommentRangeEnd.id property. Specifies the identifier of the comment to which this region is linked to."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/commentrangeend/id/
---

## CommentRangeEnd.id property

Specifies the identifier of the comment to which this region is linked to.


```js
get id(): number
```

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

* module [Aspose.Words](../../)
* class [CommentRangeEnd](../)

