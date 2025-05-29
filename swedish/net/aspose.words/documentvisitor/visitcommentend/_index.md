---
title: DocumentVisitor.VisitCommentEnd
linktitle: VisitCommentEnd
articleTitle: VisitCommentEnd
second_title: Aspose.Words för .NET
description: Utforska DocumentVisitor VisitCommentEnd-metoden, utformad för att förbättra uppräkningen av kommentartext i dina projekt för sömlös dokumentbehandling.
type: docs
weight: 100
url: /sv/net/aspose.words/documentvisitor/visitcommentend/
---
## DocumentVisitor.VisitCommentEnd method

Anropas när uppräkningen av en kommentartext är avslutad.

```csharp
public virtual VisitorAction VisitCommentEnd(Comment comment)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| comment | Comment | Objektet som besöks. |

### Returvärde

En[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

## Exempel

Visar hur man skriver ut nodstrukturen för varje kommentar och kommentarintervall i ett dokument.

```csharp
public void CommentsToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    CommentStructurePrinter visitor = new CommentStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först-sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av undernoder.
/// Skapar en karta i form av en sträng av alla påträffade Comment/CommentRange-noder och deras undernoder.
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
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet.
    /// En körning registreras endast om den är underordnad noden Comment eller CommentRange.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en CommentRangeStart-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en CommentRangeEnd-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en kommentarnod påträffas i dokumentet.
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
    /// Anropas efter att alla undernoder till en kommentarnod har besökts.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt besökaren befinner sig
    /// i ett kommentar-/kommentarintervalls träd av underordnade noder.
    /// </summary>
    /// <param namn="text"></param>
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

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [Comment](../../comment/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
