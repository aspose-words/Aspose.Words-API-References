---
title: IFieldMergingCallback.ImageFieldMerging
linktitle: ImageFieldMerging
articleTitle: ImageFieldMerging
second_title: Aspose.Words för .NET
description: Upptäck ImageFieldMerging-metoden i iFieldMergingCallback, utformad för sömlös bildinsättning i Aspose.Words-dokumentkoppling. Förbättra din dokumentautomation!
type: docs
weight: 20
url: /sv/net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

Anropas när Aspose.Words-kopplingsmotorn ska infoga en bild i ett kopplingsfält.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
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

### Se även

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
