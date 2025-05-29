---
title: SmartTag.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words för .NET
description: Upptäck hur SmartTag AcceptEnd-metoden förbättrar besökarnas engagemang genom att sömlöst hantera besöksupplevelser. Öka din webbplats interaktion idag!
type: docs
weight: 70
url: /sv/net/aspose.words.markup/smarttag/acceptend/
---
## SmartTag.AcceptEnd method

Accepterar en besökare för att besöka slutet av SmartTag.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Dokumentbesökaren. |

### Returvärde

Den åtgärd som besökaren ska vidta.

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

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [SmartTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
