---
title: FieldMergingArgs Class
linktitle: FieldMergingArgs
articleTitle: FieldMergingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.MailMerging.FieldMergingArgs för sömlös datahantering i MergeField-händelser, vilket förbättrar din dokumentbehandlingsupplevelse.
type: docs
weight: 4460
url: /sv/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

Tillhandahåller data för**SammanfogaFält** händelse.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Returnerar[`Document`](../fieldmergingargsbase/document/)objekt för vilket dokumentkopplingen utförs. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Hämtar namnet på kopplingsfältet som anges i dokumentet. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Hämtar objektet som representerar det aktuella kopplingsfältet. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Hämtar namnet på kopplingsfältet i datakällan. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Hämtar eller anger värdet för fältet från datakällan. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Hämtar det nollbaserade indexet för posten som sammanfogas. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Hämtar namnet på datatabellen för den aktuella sammanfogningsoperationen eller en tom sträng om namnet inte är tillgängligt. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | Hämtar eller anger texten som ska infogas i dokumentet för det aktuella kopplingsfältet. |

## Anmärkningar

De**SammanfogaFält** Händelsen inträffar under dokumentkoppling när ett enkelt fält för dokumentkoppling påträffas i dokumentet. Du kan svara på den här händelsen för att returnera -text som dokumentkopplingsmotorn ska infoga i dokumentet.

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)
