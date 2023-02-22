---
title: DocumentVisitor.VisitFieldSeparator
second_title: Aspose.Words för .NET API Referens
description: DocumentVisitor metod. Anropas när en fältavgränsare påträffas i dokumentet.
type: docs
weight: 190
url: /sv/net/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor.VisitFieldSeparator method

Anropas när en fältavgränsare påträffas i dokumentet.

```csharp
public virtual VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldSeparator | FieldSeparator | Objektet som besöks. |

### Returvärde

A[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

### Anmärkningar

Fältavgränsaren separerar fältkoden från fältvärdet i dokumentet. Observera att vissa -fält endast har fältkod och inte har fältavgränsare och fältvärde.

För mer info se[`VisitFieldStart`](../visitfieldstart/)

### Exempel

Visar hur man skriver ut nodstrukturen för varje fält i ett dokument.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods icke-binära träd av underordnade noder.
/// Skapar en karta i form av en sträng av alla påträffade fältnoder och deras barn.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en körnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldStart-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldEnd-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldSeparator-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djup besökaren är
    /// in i fältets träd av underordnade noder.
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

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../documentvisitor/)
* hopsättning [Aspose.Words](../../../)


