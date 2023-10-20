---
title: SmartTag
linktitle: SmartTag
articleTitle: SmartTag
second_title: Aspose.Words für .NET
description: SmartTag constructeur. Initialisiert eine neue Instanz vonSmartTag Klasse in C#.
type: docs
weight: 10
url: /de/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Initialisiert eine neue Instanz von[`SmartTag`](../) Klasse.

```csharp
public SmartTag(DocumentBase doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |

## Bemerkungen

Wenn Sie einen neuen Knoten erstellen, müssen Sie ein Dokument angeben, zu dem der Knoten gehört. Ein Knoten kann ohne ein Dokument nicht existieren, da er von den dokumentweiten Strukturen wie Listen und Stilen abhängt. Obwohl ein Knoten immer zu einem Dokument gehört, kann ein Knoten Teil des Dokumentbaums sein oder auch nicht.

Wenn ein Knoten erstellt wird, gehört er zu einem Dokument, ist aber noch nicht Teil des Dokumentbaums und[`ParentNode`](../../../aspose.words/node/parentnode/) Ist`Null` . Um einen Knoten in das Dokument einzufügen, verwenden Sie the [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) oder[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) methoden auf dem übergeordneten Knoten.

## Beispiele

Zeigt, wie man Smarttags erstellt.

```csharp
public void Create()
{
    Document doc = new Document();

    // Ein Smarttag erscheint in einem Dokument, wobei Microsoft Word einen Teil seines Textes als irgendeine Form von Daten erkennt.
    // beispielsweise einen Namen, ein Datum oder eine Adresse und wandelt ihn in einen Hyperlink um, der eine violette gepunktete Unterstreichung anzeigt.
    SmartTag smartTag = new SmartTag(doc);

    // Smart Tags sind zusammengesetzte Knoten, die ihren erkannten Text vollständig enthalten.
    // Inhalte manuell zu diesem Smarttag hinzufügen.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word erkennt die oben genannten Inhalte möglicherweise als Datum.
    // Smart Tags verwenden die Eigenschaft „Element“, um den Typ der darin enthaltenen Daten widerzuspiegeln.
    smartTag.Element = "date";

    // Einige Smart-Tag-Typen verarbeiten ihren Inhalt weiter in benutzerdefinierte XML-Eigenschaften.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Setze den URI des Smarttags auf den Standardwert.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Erstellen Sie ein weiteres Smarttag für einen Börsenticker.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Drucken Sie alle Smarttags in unserem Dokument mithilfe eines Dokumentbesuchers.
    doc.Accept(new SmartTagPrinter());

    // Ältere Versionen von Microsoft Word unterstützen Smart Tags.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Verwenden Sie die Methode „RemoveSmartTags“, um alle Smart Tags aus einem Dokument zu entfernen.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Druckt besuchte Smarttags und deren Inhalte.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein SmartTag-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines SmartTag-Knotens beendet wird.
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

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
