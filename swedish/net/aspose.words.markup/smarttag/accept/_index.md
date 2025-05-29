---
title: SmartTag.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words för .NET
description: Förbättra användarengagemang med SmartTags Accept-metod, utformad för att smidigt välkomna besökare och öka din webbplats interaktion.
type: docs
weight: 60
url: /sv/net/aspose.words.markup/smarttag/accept/
---
## SmartTag.Accept method

Tar emot en besökare.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Besökaren som kommer att besöka noderna. |

### Returvärde

Sant om alla noder besöktes; falskt om[`DocumentVisitor`](../../../aspose.words/documentvisitor/) stoppade operationen innan alla noder besöktes.

## Anmärkningar

Räknar upp denna nod och alla dess underordnade noder. Varje nod anropar en motsvarande metod.[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

För mer information, se designmönstret för besökare.

Samtal[`VisitSmartTagStart`](../../../aspose.words/documentvisitor/visitsmarttagstart/) , ringer sedan[`Accept`](../../../aspose.words/node/accept/) för alla underordnade noder till smarttaggen och anrop[`VisitSmartTagEnd`](../../../aspose.words/documentvisitor/visitsmarttagend/) i slutet.

## Exempel

Visar hur man skapar smarta taggar.

```csharp
public void Create()
{
    Document doc = new Document();

    // En smart tagg visas i ett dokument där Microsoft Word känner igen en del av texten som någon form av data,
    // såsom ett namn, datum eller adress, och konverterar den till en hyperlänk som visar en lila prickad understrykning.
    SmartTag smartTag = new SmartTag(doc);

    // Smarta taggar är sammansatta noder som innehåller sin tolkade text i sin helhet.
    // Lägg till innehåll i den här smarta taggen manuellt.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word kan identifiera ovanstående innehåll som ett datum.
    // Smarta taggar använder egenskapen "Element" för att återspegla vilken typ av data de innehåller.
    smartTag.Element = "date";

    // Vissa smarta taggtyper bearbetar sitt innehåll vidare till anpassade XML-egenskaper.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Ställ in smarttaggens URI till standardvärdet.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Skapa ytterligare en smart tagg för en aktieticker.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Skriv ut alla smarta taggar i vårt dokument med hjälp av en dokumentbesökare.
    doc.Accept(new SmartTagPrinter());

    // Äldre versioner av Microsoft Word har stöd för smarta taggar.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Använd metoden "RemoveSmartTags" för att ta bort alla smarta taggar från ett dokument.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Skriver ut besökta smarta taggar och deras innehåll.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Anropas när en SmartTag-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när besöket av en SmartTag-nod är avslutat.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Se även

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [SmartTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
