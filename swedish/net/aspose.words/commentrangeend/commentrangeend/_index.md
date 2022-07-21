---
title: CommentRangeEnd
second_title: Aspose.Words för .NET API Referens
description: Initierar en ny instans av den här klassen.
type: docs
weight: 10
url: /sv/net/aspose.words/commentrangeend/commentrangeend/
---
## CommentRangeEnd constructor

Initierar en ny instans av den här klassen.

```csharp
public CommentRangeEnd(DocumentBase doc, int id)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| id | Int32 | Kommentarsidentifieraren som detta objekt är länkat till. |

### Anmärkningar

När[`CommentRangeEnd`](../../commentrangeend) skapas, det tillhör det angivna dokumentet, men är inte ännu en del av dokumentet och[`ParentNode`](../../node/parentnode) är inget.

Att lägga till en[`CommentRangeEnd`](../../commentrangeend) till dokumentet använd InsertAfter eller InsertBefore på stycket där du vill infoga kommentaren.

### Exempel

Visar hur du skriver ut innehållet i alla kommentarer och deras kommentarintervall med hjälp av en dokumentbesökare.

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

    // Lägg till text i dokumentet, förvräng den i ett kommentarsområde och lägg sedan till din kommentar.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Lägg till två svar på kommentaren.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Itererar över varje kommentar på toppnivå och skriver ut dess kommentarintervall, innehåll och svar.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Iterera över alla kommentarer på toppnivå. Till skillnad från kommentarer av svarstyp har kommentarer på toppnivå ingen förfader.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Besök först början av kommentarsintervallet.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Besök sedan kommentaren och eventuella svar som den kan ha.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Slutligen, besök slutet av kommentarsintervallet och skriv sedan ut besökarens textinnehåll.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Skriver ut information och innehåll för alla kommentarer och kommentarintervall som påträffas i dokumentet.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Hämtar vanlig text av dokumentet som samlades av besökaren.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en körnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

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
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en kommentarsnod påträffas i dokumentet.
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
    /// Anropas när besöket av en kommentarsnod avslutas i dokumentet.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt besökaren befinner sig i dokumentträdet.
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

### Se även

* class [DocumentBase](../../documentbase)
* class [CommentRangeEnd](../../commentrangeend)
* namnutrymme [Aspose.Words](../../commentrangeend)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
