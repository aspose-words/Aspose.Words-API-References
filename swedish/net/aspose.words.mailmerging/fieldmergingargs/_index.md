---
title: Class FieldMergingArgs
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.MailMerging.FieldMergingArgs klass. Tillhandahåller data för MergeField händelse.
type: docs
weight: 3550
url: /sv/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

Tillhandahåller data för **MergeField** händelse.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Returnerar[`Document`](../fieldmergingargsbase/document/) objekt för vilket sammanslagningen utförs. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Hämtar namnet på sammanslagningsfältet som specificerats i dokumentet. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Hämtar objektet som representerar det aktuella sammanslagningsfältet. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Hämtar namnet på sammanslagningsfältet i datakällan. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Hämtar eller ställer in fältets värde från datakällan. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Hämtar det nollbaserade indexet för posten som slås samman. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Hämtar namnet på datatabellen för den aktuella sammanslagningsoperationen eller tom sträng om namnet inte är tillgängligt. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | Hämtar eller ställer in texten som ska infogas i dokumentet för det aktuella sammanslagningsfältet. |

### Anmärkningar

De **MergeField** händelse inträffar under sammankoppling när ett enkelt sammanslagningsfält påträffas i dokumentet. Du kan svara på den här händelsen på return text för kopplingsmotorn att infoga i dokumentet.

### Exempel

Visar hur man utför en sammankoppling med en anpassad återuppringning som hanterar sammanslagningsdata i form av HTML-dokument.

```csharp
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
/// Om kopplingen stöter på ett MERGEFIELD vars namn börjar med prefixet "html_",
/// denna återuppringning analyserar dess sammanslagningsdata som HTML-innehåll och lägger till resultatet till dokumentplatsen för MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en e-postsammanfogning slår samman data till ett MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Lägg till analyserad HTML-data till dokumentets brödtext.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Eftersom vi redan har infogat det sammanslagna innehållet manuellt,
              // vi behöver inte svara på denna händelse genom att returnera innehåll via "Text"-egenskapen.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Göra ingenting.
    }
}
```

### Se även

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)


