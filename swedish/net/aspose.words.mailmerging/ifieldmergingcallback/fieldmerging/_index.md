---
title: IFieldMergingCallback.FieldMerging
linktitle: FieldMerging
articleTitle: FieldMerging
second_title: Aspose.Words för .NET
description: Optimera dina dokumentarbetsflöden med iFieldMergingCallback-metoden. Integrera data sömlöst i dina Aspose.Words-kopplingsfält för ökad effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words.mailmerging/ifieldmergingcallback/fieldmerging/
---
## IFieldMergingCallback.FieldMerging method

Anropas när Aspose.Words-kopplingsmotorn ska infoga data i ett kopplingsfält i dokumentet.

```csharp
public void FieldMerging(FieldMergingArgs args)
```

## Exempel

Visar hur man infogar bilder som lagras i ett BLOB-fält i en rapport.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Öppna dataläsaren, som måste vara i ett läge som läser alla poster samtidigt.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Gör ingenting.
    }

    /// <summary>
    /// Detta anropas när en dokumentkoppling stöter på ett MERGEFIELD i dokumentet med en "Image:"-tagg i namnet.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgs](../../fieldmergingargs/)
* interface [IFieldMergingCallback](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
