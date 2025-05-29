---
title: Comment.Done
linktitle: Done
articleTitle: Done
second_title: Aspose.Words für .NET
description: Markieren Sie Kommentare mit der Eigenschaft „Erledigt“ als abgeschlossen. Verwalten Sie Ihre Aufgaben ganz einfach und verbessern Sie die Workflow-Effizienz mit dieser einfachen Kennzeichnungsfunktion.
type: docs
weight: 60
url: /de/net/aspose.words/comment/done/
---
## Comment.Done property

Ruft ein Flag ab oder legt es fest, das angibt, dass der Kommentar als erledigt markiert wurde.

```csharp
public bool Done { get; set; }
```

## Beispiele

Zeigt, wie ein Kommentar als „erledigt“ markiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

    // Fügen Sie einen Kommentar ein, um auf einen Fehler hinzuweisen.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

    // Kommentare haben ein „Erledigt“-Flag, das standardmäßig auf „false“ gesetzt ist.
// Wenn ein Kommentar vorschlägt, dass wir eine Änderung im Dokument vornehmen,
// wir können die Änderung anwenden und anschließend auch das Flag „Erledigt“ setzen, um die Korrektur anzuzeigen.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Kommentare, die "fertig" sind, werden sich unterscheiden
// von denen, die nicht „fertig“ sind, mit einer verblassten Textfarbe.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

Zeigt, wie der Inhalt aller Kommentare und deren Kommentarbereiche mithilfe eines Dokumentbetrachters gedruckt werden.

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

    // Fügen Sie dem Dokument Text hinzu, verzerren Sie ihn in einem Kommentarbereich und fügen Sie dann Ihren Kommentar hinzu.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Fügen Sie dem Kommentar zwei Antworten hinzu.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Durchläuft jeden Kommentar der obersten Ebene und druckt seinen Kommentarbereich, Inhalt und seine Antworten.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Durchlaufe alle Kommentare der obersten Ebene. Im Gegensatz zu Kommentaren vom Typ „Antwort“ haben Kommentare der obersten Ebene keinen Vorgänger.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // Besuchen Sie zuerst den Anfang des Kommentarbereichs.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Sehen Sie sich dann den Kommentar und alle Antworten an, die er möglicherweise enthält.
        comment.Accept(commentVisitor);
        // Besuchen Sie nur den Anfang des Kommentars.
        comment.AcceptStart(commentVisitor);
        // Besuchen Sie nur das Ende des Kommentars.
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Besuchen Sie abschließend das Ende des Kommentarbereichs und drucken Sie dann den Textinhalt des Besuchers.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Druckt Informationen und Inhalte aller im Dokument vorkommenden Kommentare und Kommentarbereiche.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Ruft den Klartext des vom Besucher gesammelten Dokuments ab.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein CommentRangeStart-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein CommentRangeEnd-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Kommentarknoten gefunden wird.
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
    /// Wird aufgerufen, wenn der Besuch eines Kommentarknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Fügen Sie dem StringBuilder eine Zeile hinzu und rücken Sie sie ein, je nachdem, wie tief der Besucher im Dokumentbaum ist.
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

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
