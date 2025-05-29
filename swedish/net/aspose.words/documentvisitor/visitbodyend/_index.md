---
title: DocumentVisitor.VisitBodyEnd
linktitle: VisitBodyEnd
articleTitle: VisitBodyEnd
second_title: Aspose.Words för .NET
description: Upptäck DocumentVisitor VisitBodyEnd-metoden – hantera textartikeluppräkning effektivt och förbättra dina dokumentbehandlingsmöjligheter.
type: docs
weight: 20
url: /sv/net/aspose.words/documentvisitor/visitbodyend/
---
## DocumentVisitor.VisitBodyEnd method

Anropas när uppräkningen av huvudtextens berättelse i ett avsnitt är avslutad.

```csharp
public virtual VisitorAction VisitBodyEnd(Body body)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| body | Body | Objektet som besöks. |

### Returvärde

En[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

## Exempel

Visar hur man använder en dokumentbesökare för att skriva ut ett dokuments nodstruktur.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först-sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods träd av undernoder.
/// Skapar en karta över detta träd i form av en sträng.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Anropas när en dokumentnod påträffas.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Tillåt besökaren att fortsätta besöka andra noder.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder till en dokumentnod har besökts.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en sektionsnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Hämta indexet för vårt avsnitt i dokumentet.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder till en sektionsnod har besökts.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Body-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder till en Body-nod har besökts.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en styckenod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder till en styckenod har besökts.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en underdokumentnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en underdokumentnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
    {
        IndentAndAppendLine("[SdtRangeStart]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en underdokumentnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
    {
        IndentAndAppendLine("[SdtRangeEnd]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt inne i dokumentträdet besökaren befinner sig.
    /// </summary>
    /// <param namn="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [Body](../../body/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
