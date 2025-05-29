---
title: IFieldMergingCallback Interface
linktitle: IFieldMergingCallback
articleTitle: IFieldMergingCallback
second_title: .NET için Aspose.Words
description: Aspose.Words ile e-posta birleştirmede ustalaşın! Kusursuz belge oluşturma için birleştirme alanlarına veri eklemeyi özelleştirmek amacıyla IFieldMergingCallback arayüzünü uygulayın.
type: docs
weight: 4480
url: /tr/net/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface

Bir posta birleştirme işlemi sırasında verilerin birleştirme alanlarına nasıl ekleneceğini kontrol etmek istiyorsanız bu arayüzü uygulayın.

```csharp
public interface IFieldMergingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [FieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/fieldmerging/)(*[FieldMergingArgs](../fieldmergingargs/)*) | Aspose.Words posta birleştirme motoru belgedeki birleştirme alanına veri eklemek üzereyken çağrılır. |
| [ImageFieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/)(*[ImageFieldMergingArgs](../imagefieldmergingargs/)*) | Aspose.Words posta birleştirme motoru birleştirme alanına bir resim eklemek üzereyken çağrılır. |

## Örnekler

Bir veritabanı BLOB alanında saklanan görsellerin bir rapora nasıl ekleneceğini gösterir.

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

        // Tüm kayıtları aynı anda okuyan bir modda olması gereken veri okuyucusunu açın.
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
        // Hiçbir şey yapmayın.
    }

    /// <summary>
    /// Bu, bir posta birleştirme işlemi belgede adında "Image:" etiketi bulunan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

HTML belgeleri biçiminde birleştirme verilerini işleyen özel bir geri aramayla bir posta birleştirmenin nasıl yürütüleceğini gösterir.

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
/// Posta birleştirme işlemi, adı "html_" önekiyle başlayan bir MERGEFIELD ile karşılaşırsa,
/// bu geri çağırma birleştirme verilerini HTML içeriği olarak ayrıştırır ve sonucu MERGEFIELD'ın belge konumuna ekler.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Bir posta birleştirme işlemi verileri bir MERGEFIELD'a birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Ayrıştırılmış HTML verilerini belgenin gövdesine ekle.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Birleştirilmiş içeriği zaten manuel olarak eklediğimizden,
            // Bu olaya "Metin" özelliği aracılığıyla içerik döndürerek yanıt vermemize gerek kalmayacak.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hiçbir şey yapmayın.
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
