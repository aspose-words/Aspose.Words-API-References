---
title: FieldMergingArgsBase.DocumentFieldName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldMergingArgsBase eigendom. Ruft den Namen des Briefvorlagenfelds ab wie im Dokument angegeben.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/
---
## FieldMergingArgsBase.DocumentFieldName property

Ruft den Namen des Briefvorlagenfelds ab, wie im Dokument angegeben.

```csharp
public string DocumentFieldName { get; }
```

### Bemerkungen

Wenn Sie eine Zuordnung von einem Dokumentfeldnamen zu einem anderen Datenquellenfeldnamen haben, , dann ist dies der ursprüngliche Feldname, wie er im Dokument angegeben ist.

Wenn Sie im Dokument ein Feldnamenpräfix angegeben haben, zum Beispiel „Image:MyFieldName“, dann`DocumentFieldName` gibt den Feldnamen ohne Präfix zurück, also „MyFieldName“.

### Beispiele

Zeigt, wie ein Serienbrief mit einem benutzerdefinierten Rückruf ausgeführt wird, der Seriendaten in Form von HTML-Dokumenten verarbeitet.

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
/// Wenn der Seriendruck auf ein MERGEFIELD trifft, dessen Name mit dem Präfix „html_“ beginnt,
/// Dieser Rückruf analysiert seine Zusammenführungsdaten als HTML-Inhalt und fügt das Ergebnis dem Dokumentspeicherort des MERGEFIELD hinzu.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in einem MERGEFIELD zusammenführt.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Geparste HTML-Daten zum Hauptteil des Dokuments hinzufügen.
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

* class [FieldMergingArgsBase](../)
* namensraum [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* Montage [Aspose.Words](../../../)


