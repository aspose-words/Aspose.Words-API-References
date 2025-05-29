---
title: SmartTag
linktitle: SmartTag
articleTitle: SmartTag
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos dynamische SmartTags mit unserem Konstruktor. Optimieren Sie Ihre Projekte mit anpassbaren Funktionen und nahtloser Integration für optimale Leistung.
type: docs
weight: 10
url: /de/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Initialisiert eine neue Instanz des[`SmartTag`](../) Klasse.

```csharp
public SmartTag(DocumentBase doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |

## Bemerkungen

Beim Erstellen eines neuen Knotens müssen Sie das Dokument angeben, zu dem der Knoten gehört. Ein Knoten kann nicht ohne Dokument existieren, da er von dokumentweiten Strukturen wie Listen und Stilen abhängt. Obwohl ein Knoten immer zu einem Dokument gehört, kann er Teil des Dokumentbaums sein oder nicht.

Wenn ein Knoten erstellt wird, gehört er zu einem Dokument, ist aber noch nicht Teil des Dokumentbaums und[`ParentNode`](../../../aspose.words/node/parentnode/) ist null. Um einen Knoten in das Dokument einzufügen, verwenden Sie the [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) oder[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) -Methoden auf dem übergeordneten Knoten.

## Beispiele

Zeigt, wie Smarttags erstellt werden.

```csharp
public void Create()
{
    Document doc = new Document();

    // Ein Smarttag erscheint in einem Dokument, in dem Microsoft Word einen Teil des Textes als eine Art Daten erkennt.
    // wie etwa einen Namen, ein Datum oder eine Adresse, und wandelt es in einen Hyperlink um, der eine violette gepunktete Unterstreichung anzeigt.
    SmartTag smartTag = new SmartTag(doc);

    // Smarttags sind zusammengesetzte Knoten, die den erkannten Text vollständig enthalten.
    // Fügen Sie diesem Smarttag manuell Inhalte hinzu.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word erkennt den obigen Inhalt möglicherweise als Datum.
    // Smarttags verwenden die Eigenschaft „Element“, um den Typ der enthaltenen Daten widerzuspiegeln.
    smartTag.Element = "date";

    // Einige Smarttag-Typen verarbeiten ihren Inhalt weiter in benutzerdefinierte XML-Eigenschaften.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Setzen Sie die URI des Smarttags auf den Standardwert.
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

    // Ältere Versionen von Microsoft Word unterstützen Smarttags.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Verwenden Sie die Methode „RemoveSmartTags“, um alle Smarttags aus einem Dokument zu entfernen.
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
    /// Wird aufgerufen, wenn der Besuch eines SmartTag-Knotens beendet ist.
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
