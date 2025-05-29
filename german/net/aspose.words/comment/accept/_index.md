---
title: Comment.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: Entdecken Sie die Kommentarakzeptanz-Methode, um die Besucherinteraktion zu verbessern und sinnvolle Interaktionen auf Ihrer Website zu ermöglichen. Stärken Sie noch heute Ihre Online-Community!
type: docs
weight: 130
url: /de/net/aspose.words/comment/accept/
---
## Comment.Accept method

Nimmt einen Besucher auf.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Besucher, der die Knoten besuchen wird. |

### Rückgabewert

Wahr, wenn alle Knoten besucht wurden; falsch, wenn[`DocumentVisitor`](../../documentvisitor/) hat den Vorgang abgebrochen, bevor alle Knoten besucht wurden.

## Bemerkungen

Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft eine entsprechende Methode auf[`DocumentVisitor`](../../documentvisitor/).

Weitere Informationen finden Sie im Besucher-Entwurfsmuster.

Anrufe[`VisitCommentStart`](../../documentvisitor/visitcommentstart/) , dann ruft[`Accept`](../../node/accept/)für alle Kindknoten des Kommentars und der Aufrufe[`VisitCommentEnd`](../../documentvisitor/visitcommentend/) am Ende.

## Beispiele

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

* class [DocumentVisitor](../../documentvisitor/)
* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
