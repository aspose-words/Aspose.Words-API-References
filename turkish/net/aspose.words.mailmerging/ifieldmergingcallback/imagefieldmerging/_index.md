---
title: IFieldMergingCallback.ImageFieldMerging
second_title: Aspose.Words for .NET API Referansı
description: IFieldMergingCallback yöntem. Aspose.Words adresmektup birleştirme motoru birleştirme alanına bir resim eklemek üzereyken çağrılır.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

Aspose.Words adres-mektup birleştirme motoru birleştirme alanına bir resim eklemek üzereyken çağrılır.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
```

### Örnekler

Veritabanı BLOB alanında saklanan görüntülerin bir rapora nasıl ekleneceğini gösterir.

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

        // Tüm kayıtları aynı anda okuyacak modda olması gereken veri okuyucuyu açın.
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
        // Hiçbir şey yapma.
    }

    /// <summary>
    /// Adres-mektup birleştirme, belgede adında "Image:" etiketi bulunan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Ayrıca bakınız

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* ad alanı [Aspose.Words.MailMerging](../../ifieldmergingcallback/)
* toplantı [Aspose.Words](../../../)


