---
title: FieldMergingArgsBase Class
linktitle: FieldMergingArgsBase
articleTitle: FieldMergingArgsBase
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.MailMerging.FieldMergingArgsBase, die Grundlage für effizientes Feldzusammenführen und Bildhandling bei der Dokumentenautomatisierung.
type: docs
weight: 4470
url: /de/net/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class

Basisklasse für[`FieldMergingArgs`](../fieldmergingargs/) Und[`ImageFieldMergingArgs`](../imagefieldmergingargs/) .

Um mehr zu erfahren, besuchen Sie die[Serienbriefe und Berichte](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public abstract class FieldMergingArgsBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Gibt die[`Document`](./document/)Objekt, für das der Serienbrief ausgeführt wird. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Ruft den Namen des Seriendruckfelds ab, wie im Dokument angegeben. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Ruft das Objekt ab, das das aktuelle Seriendruckfeld darstellt. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Ruft den Namen des Seriendruckfelds in der Datenquelle ab. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Ruft den Wert des Felds aus der Datenquelle ab oder legt ihn fest. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Ruft den nullbasierten Index des Datensatzes ab, der zusammengeführt wird. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Ruft den Namen der Datentabelle für den aktuellen Zusammenführungsvorgang oder eine leere Zeichenfolge ab, wenn der Name nicht verfügbar ist. |

## Beispiele

Zeigt, wie ein Serienbrief mit einem benutzerdefinierten Rückruf ausgeführt wird, der Serienbriefdaten in Form von HTML-Dokumenten verarbeitet.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Wenn der Serienbrief auf ein MERGEFIELD trifft, dessen Name mit dem Präfix "html_" beginnt,
/// Dieser Rückruf analysiert seine Zusammenführungsdaten als HTML-Inhalt und fügt das Ergebnis zum Dokumentspeicherort des MERGEFIELD hinzu.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in ein MERGEFIELD zusammenführt.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Fügen Sie dem Hauptteil des Dokuments analysierte HTML-Daten hinzu.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Da wir den zusammengeführten Inhalt bereits manuell eingefügt haben,
            // Wir müssen auf dieses Ereignis nicht reagieren, indem wir Inhalte über die Eigenschaft „Text“ zurückgeben.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Nichts tun.
    }
}
```

### Siehe auch

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
