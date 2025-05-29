---
title: DocumentVisitor.VisitAbsolutePositionTab
linktitle: VisitAbsolutePositionTab
articleTitle: VisitAbsolutePositionTab
second_title: Aspose.Words för .NET
description: Upptäck DocumentVisitor VisitAbsolutePositionTab-metoden, utformad för att förbättra dokumentbehandling genom att effektivt hantera AbsolutePositionTab-noder.
type: docs
weight: 10
url: /sv/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

Anropades när en[`AbsolutePositionTab`](../../absolutepositiontab/) nod påträffas i dokumentet.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tab | AbsolutePositionTab | Objektet som besöks. |

### Returvärde

En[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

## Exempel

Visar hur man bearbetar tabbtecken för absolut position med en dokumentbesökare.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extrahera textinnehållet i vårt dokument genom att acceptera denna anpassade dokumentbesökare.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Besök endast början av dokumentets brödtext.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Besök endast slutet av dokumentets brödtext.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // Den absoluta positionstabben, som inte har någon motsvarighet i strängform, har explicit konverterats till ett tabbtecken.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // En AbsolutePositionTab kan också acceptera en DocumentVisitor i sig själv.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Samlar in textinnehållet från alla körningar i det besökta dokumentet. Ersätter alla absoluta tabbtecken med vanliga tabbtecken.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en AbsolutePositionTab-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägger till text i den aktuella utdatan. Respekterar flaggan för aktiverad/inaktiverad utdata.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Klartext för dokumentet som besökaren samlade in.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [AbsolutePositionTab](../../absolutepositiontab/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
