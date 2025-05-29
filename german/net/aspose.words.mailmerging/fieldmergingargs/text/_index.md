---
title: FieldMergingArgs.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Verwalten Sie die Seriendruckfelder Ihres Dokuments mühelos mit FieldMergingArgs. Legen Sie Text einfach fest oder rufen Sie ihn ab, um eine nahtlose Dokumentintegration zu gewährleisten.
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

Ruft den Text ab oder legt ihn fest, der für das aktuelle Seriendruckfeld in das Dokument eingefügt wird.

```csharp
public string Text { get; set; }
```

## Bemerkungen

Wenn Ihr Eventhandler aufgerufen wird, wird diese Eigenschaft auf`null`.

Wenn Sie Text als`null` , fügt das Serienbriefmodul Folgendes ein[`FieldValue`](../../fieldmergingargsbase/fieldvalue/) anstelle des Seriendruckfelds.

Wenn Sie „Text“ auf eine beliebige Zeichenfolge (auch leer) setzen, wird die Zeichenfolge anstelle des Seriendruckfelds in das Dokument eingefügt.

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

* class [FieldMergingArgs](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
