---
title: DocumentVisitor.VisitFootnoteEnd
second_title: Aspose.Words för .NET API Referens
description: DocumentVisitor metod. Anropas när uppräkningen av en fotnot eller slutnotstext har avslutats.
type: docs
weight: 210
url: /sv/net/aspose.words/documentvisitor/visitfootnoteend/
---
## DocumentVisitor.VisitFootnoteEnd method

Anropas när uppräkningen av en fotnot eller slutnotstext har avslutats.

```csharp
public virtual VisitorAction VisitFootnoteEnd(Footnote footnote)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| footnote | Footnote | Objektet som besöks. |

### Returvärde

A[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

### Exempel

Visar hur man skriver ut nodstrukturen för varje fotnot i ett dokument.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av underordnade noder.
/// Skapar en karta i form av en sträng av alla påträffade fotnotsnoder och deras barn.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// Hämtar vanlig text av dokumentet som samlades av besökaren.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en fotnotsnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Kallas efter att alla undernoder i en fotnotsnod har besökts.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en körnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt besökaren befinner sig i dokumentträdet.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [Footnote](../../../aspose.words.notes/footnote/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../documentvisitor/)
* hopsättning [Aspose.Words](../../../)


