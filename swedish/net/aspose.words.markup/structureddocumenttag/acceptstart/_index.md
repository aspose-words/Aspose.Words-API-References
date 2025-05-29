---
title: StructuredDocumentTag.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words för .NET
description: Upptäck StructuredDocumentTag AcceptStart-metoden för att förbättra din dokumenthantering. Effektivisera besökarinteraktioner för optimal prestanda!
type: docs
weight: 350
url: /sv/net/aspose.words.markup/structureddocumenttag/acceptstart/
---
## StructuredDocumentTag.AcceptStart method

Accepterar en besökare för att besöka början av StructuredDocumentTag.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Dokumentbesökaren. |

### Returvärde

Den åtgärd som besökaren ska vidta.

## Exempel

Visar hur man skriver ut nodstrukturen för varje strukturerad dokumenttagg i ett dokument.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först-sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av undernoder.
/// Skapar en karta i form av en sträng av alla påträffade StructuredDocumentTag-noder och deras undernoder.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
    }

    /// <summary>
    /// Hämtar klartexten från dokumentet som besökaren samlade in.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en StructuredDocumentTag-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder till en StructuredDocumentTag-nod har besökts.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

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

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
