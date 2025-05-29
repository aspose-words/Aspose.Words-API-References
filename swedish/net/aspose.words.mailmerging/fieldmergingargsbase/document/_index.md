---
title: FieldMergingArgsBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldMergingArgsBase Document, som tillhandahåller Document-objektet för sömlösa dokumentkopplingsåtgärder. Förbättra ditt arbetsflöde idag!
type: docs
weight: 10
url: /sv/net/aspose.words.mailmerging/fieldmergingargsbase/document/
---
## FieldMergingArgsBase.Document property

Returnerar`Document`objekt för vilket dokumentkopplingen utförs.

```csharp
public Document Document { get; }
```

## Exempel

Visar hur man utför en dokumentkoppling med ett anpassat återanrop som hanterar kopplingsdata i form av HTML-dokument.

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
/// Om dokumentkopplingen stöter på ett MERGEFIELD vars namn börjar med prefixet "html_",
/// denna återanropsfunktion tolkar dess sammanslagningsdata som HTML-innehåll och lägger till resultatet till dokumentets plats för MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en dokumentkoppling sammanfogar data till ett MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Lägg till parsad HTML-data i dokumentets brödtext.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Eftersom vi redan har infogat det sammanfogade innehållet manuellt,
            // vi behöver inte svara på den här händelsen genom att returnera innehåll via egenskapen "Text".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Gör ingenting.
    }
}
```

### Se även

* class [Document](../../../aspose.words/document/)
* class [FieldMergingArgsBase](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
