---
title: DocumentVisitor.VisitSmartTagEnd
linktitle: VisitSmartTagEnd
articleTitle: VisitSmartTagEnd
second_title: Aspose.Words för .NET
description: DocumentVisitor VisitSmartTagEnd metod. Anropas när uppräkningen av en smart tagg har avslutats i C#.
type: docs
weight: 410
url: /sv/net/aspose.words/documentvisitor/visitsmarttagend/
---
## DocumentVisitor.VisitSmartTagEnd method

Anropas när uppräkningen av en smart tagg har avslutats.

```csharp
public virtual VisitorAction VisitSmartTagEnd(SmartTag smartTag)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| smartTag | SmartTag | Objektet som besöks. |

### Returvärde

A[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

## Exempel

Visar hur man skriver ut nodstrukturen för varje smart tagg i ett dokument.

```csharp
public void SmartTagToText()
{
    Document doc = new Document(MyDir + "Smart tags.doc");
    SmartTagStructurePrinter visitor = new SmartTagStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av underordnade noder.
/// Skapar en karta i form av en sträng av alla påträffade SmartTag-noder och deras barn.
/// </summary>
public class SmartTagStructurePrinter : DocumentVisitor
{
    public SmartTagStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideSmartTag = false;
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
        if (mVisitorIsInsideSmartTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en SmartTag-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        IndentAndAppendLine("[SmartTag start] Name: " + smartTag.Element);
        mDocTraversalDepth++;
        mVisitorIsInsideSmartTag = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla underordnade noder i en SmartTag-nod har besökts.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[SmartTag end]");
        mVisitorIsInsideSmartTag = false;

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

    private bool mVisitorIsInsideSmartTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [SmartTag](../../../aspose.words.markup/smarttag/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
