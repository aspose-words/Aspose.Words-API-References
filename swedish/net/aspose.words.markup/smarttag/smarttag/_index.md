---
title: SmartTag.SmartTag
second_title: Aspose.Words för .NET API Referens
description: SmartTag byggare. Initierar en ny instans avSmartTag class.
type: docs
weight: 10
url: /sv/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Initierar en ny instans av[`SmartTag`](../) class.

```csharp
public SmartTag(DocumentBase doc)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |

### Anmärkningar

När du skapar en ny nod måste du ange ett dokument som noden tillhör. En nod kan inte existera utan ett dokument eftersom det beror på dokumentomfattande strukturer såsom listor och stilar. Även om en nod alltid tillhör ett dokument, kanske en nod inte är en del av dokumentträdet.

När en nod skapas tillhör den ett dokument, men är ännu inte en del av dokumentträdet och[`ParentNode`](../../../aspose.words/node/parentnode/) är`null` . För att infoga en nod i dokumentet, använd Node) ellerNode) methods på den överordnade noden.

### Exempel

Visar hur man skapar smarta taggar.

```csharp
public void Create()
{
    Document doc = new Document();

    // En smart tagg visas i ett dokument med Microsoft Word känner igen en del av sin text som någon form av data,
    // som ett namn, datum eller adress, och konverterar det till en hyperlänk som visar en lila prickad underlinje.
    SmartTag smartTag = new SmartTag(doc);

    // Smarta taggar är sammansatta noder som innehåller sin igenkända text i sin helhet.
    // Lägg till innehåll till denna smarta tag manuellt.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word kan känna igen ovanstående innehåll som ett datum.
    // Smarta taggar använder egenskapen "Element" för att återspegla typen av data de innehåller.
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

    // Äldre versioner av Microsoft Word stöder smarta taggar.
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
    /// Anropas när besöket av en SmartTag-nod avslutas.
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* namnutrymme [Aspose.Words.Markup](../../smarttag/)
* hopsättning [Aspose.Words](../../../)


