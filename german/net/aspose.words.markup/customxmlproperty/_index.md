---
title: CustomXmlProperty Class
linktitle: CustomXmlProperty
articleTitle: CustomXmlProperty
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.CustomXmlProperty, die die Verwaltung benutzerdefinierter XML-Attribute und Smarttag-Eigenschaften für eine verbesserte Dokumentkontrolle vereinfacht.
type: docs
weight: 4630
url: /de/net/aspose.words.markup/customxmlproperty/
---
## CustomXmlProperty class

Stellt ein einzelnes benutzerdefiniertes XML-Attribut oder eine Smarttag-Eigenschaft dar.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class CustomXmlProperty
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CustomXmlProperty](customxmlproperty/)(*string, string, string*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Name](../../aspose.words.markup/customxmlproperty/name/) { get; } | Gibt den Namen des benutzerdefinierten XML-Attributs oder der Smarttag-Eigenschaft an. |
| [Uri](../../aspose.words.markup/customxmlproperty/uri/) { get; set; } | Ruft den Namespace-URI des benutzerdefinierten XML-Attributs oder der Smarttag-Eigenschaft ab oder legt ihn fest. |
| [Value](../../aspose.words.markup/customxmlproperty/value/) { get; set; } | Ruft den Wert des benutzerdefinierten XML-Attributs oder der Smarttag-Eigenschaft ab oder legt ihn fest. |

## Bemerkungen

Wird als Artikel eines[`CustomXmlPropertyCollection`](../customxmlpropertycollection/) Sammlung.

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
