---
title: ImageFieldMergingArgs.ImageStream
second_title: Aspose.Words för .NET API Referens
description: ImageFieldMergingArgs fast egendom. Anger strömmen för kopplingsmotorn att läsa en bild från.
type: docs
weight: 40
url: /sv/net/aspose.words.mailmerging/imagefieldmergingargs/imagestream/
---
## ImageFieldMergingArgs.ImageStream property

Anger strömmen för kopplingsmotorn att läsa en bild från.

```csharp
public Stream ImageStream { get; set; }
```

### Anmärkningar

Aspose.Words stänger den här strömmen efter att den sammanfogar bilden i dokumentet.

### Exempel

Visar hur man infogar bilder lagrade i ett databas BLOB-fält i en rapport.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
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

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Göra ingenting.
    }

    /// <summary>
    /// Detta kallas när en sammanslagning stöter på ett MERGEFIELD i dokumentet med en "Image:"-tagg i sitt namn.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Se även

* class [ImageFieldMergingArgs](../)
* namnutrymme [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* hopsättning [Aspose.Words](../../../)


