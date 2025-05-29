---
title: HeaderFooter.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words för .NET
description: Förbättra användarupplevelsen på din webbplats med HeaderFooter AcceptEnd-metoden, utformad för att sömlöst hantera besökarinteraktioner i slutet av rubriken.
type: docs
weight: 80
url: /sv/net/aspose.words/headerfooter/acceptend/
---
## HeaderFooter.AcceptEnd method

Accepterar en besökare för att besöka slutet av rubriken.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Dokumentbesökaren. |

### Returvärde

Den åtgärd som besökaren ska vidta.

## Exempel

Visar hur man skriver ut nodstrukturen för varje sidhuvud och sidfot i ett dokument.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först-sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Ett alternativt sätt att komma åt ett dokuments sidhuvud/sidfot sektion för sektion är genom att öppna samlingen.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Går igenom en nods icke-binära träd av undernoder.
/// Skapar en karta i form av en sträng av alla påträffade HeaderFooter-noder och deras undernoder.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en HeaderFooter-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder till en HeaderFooter-nod har besökts.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt inne i dokumentträdet besökaren befinner sig.
    /// </summary>
    /// <param namn="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
