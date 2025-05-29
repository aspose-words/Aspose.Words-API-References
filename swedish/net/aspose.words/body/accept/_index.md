---
title: Body.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words för .NET
description: Upptäck Body Accept-metoden för sömlöst besökarengagemang. Förbättra användarupplevelsen och öka konverteringar med vår unika metod!
type: docs
weight: 40
url: /sv/net/aspose.words/body/accept/
---
## Body.Accept method

Tar emot en besökare.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Besökaren som kommer att besöka noderna. |

### Returvärde

Sant om alla noder besöktes; falskt om[`DocumentVisitor`](../../documentvisitor/) stoppade operationen innan alla noder besöktes.

## Anmärkningar

Räknar upp denna nod och alla dess underordnade noder. Varje nod anropar en motsvarande metod.[`DocumentVisitor`](../../documentvisitor/).

För mer information, se designmönstret för besökare.

Samtal[`VisitBodyStart`](../../documentvisitor/visitbodystart/) , ringer sedan[`Accept`](../../node/accept/) för alla underordnade noder till section och anrop[`VisitBodyEnd`](../../documentvisitor/visitbodyend/) i slutet.

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

* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
