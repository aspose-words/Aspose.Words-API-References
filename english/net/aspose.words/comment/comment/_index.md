---
title: Comment
linktitle: Comment
second_title: Aspose.Words for .NET API Reference
description: Comment constructor. Initializes a new instance of the Comment class in C#.
type: docs
weight: 10
url: /net/aspose.words/comment/comment/
---
## Comment(*[DocumentBase](../../documentbase/)*) {#constructor}

Initializes a new instance of the [`Comment`](../) class.

```csharp
public Comment(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When [`Comment`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To append [`Comment`](../) to the document use [`InsertAfter`](../../compositenode/insertafter/) or [`InsertBefore`](../../compositenode/insertbefore/) on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [`Author`](../author/), [`Initial`](../initial/) and [`DateTime`](../datetime/) properties.

## Examples

Shows how print the contents of all comments and their comment ranges using a document visitor.

```csharp
public void CreateCommentsAndPrintAllInfo()
{
    Document doc = new Document();

    Comment newComment = new Comment(doc)
    {
        Author = "VDeryushev",
        Initial = "VD",
        DateTime = DateTime.Now
    };

    newComment.SetText("Comment regarding text.");

    // Add text to the document, warp it in a comment range, and then add your comment.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Add two replies to the comment.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Iterates over every top-level comment and prints its comment range, contents, and replies.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // First, visit the start of the comment range.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Then, visit the comment, and any replies that it may have.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Finally, visit the end of the comment range, and then print the visitor's text contents.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
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
        return mBuilder.ToString();
    }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a CommentRangeStart node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a CommentRangeEnd node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Comment node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        IndentAndAppendLine(
            $"[Comment start] For comment range ID {comment.Id}, By {comment.Author} on {comment.DateTime}");
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when the visiting of a Comment node is ended in the document.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideComment;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### See Also

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* namespace [Aspose.Words](../../comment/)
* assembly [Aspose.Words](../../../)

---

## Comment(*[DocumentBase](../../documentbase/), string, string, DateTime*) {#constructor_1}

Initializes a new instance of the [`Comment`](../) class.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |
| author | String | The author name for the comment. Cannot be `null`. |
| initial | String | The author initials for the comment. Cannot be `null`. |
| dateTime | DateTime | The date and time for the comment. |

## Examples

Shows how to add a comment to a paragraph.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### See Also

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* namespace [Aspose.Words](../../comment/)
* assembly [Aspose.Words](../../../)
