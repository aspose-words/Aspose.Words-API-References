---
title: IFieldMergingCallback
second_title: Aspose.Words for .NET API Referansı
description: Adres mektup birleştirme işlemi sırasında verilerin birleştirme alanlarına nasıl ekleneceğini denetlemek istiyorsanız bu arabirimi uygulayın.
type: docs
weight: 3570
url: /tr/net/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface

Adres mektup birleştirme işlemi sırasında verilerin birleştirme alanlarına nasıl ekleneceğini denetlemek istiyorsanız bu arabirimi uygulayın.

```csharp
public interface IFieldMergingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [FieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/fieldmerging/)(FieldMergingArgs) | Aspose.Words adres mektup birleştirme motoru belgedeki bir birleştirme alanına veri eklemek üzereyken çağrılır. |
| [ImageFieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/)(ImageFieldMergingArgs) | Aspose.Words adres mektup birleştirme motoru bir birleştirme alanına bir resim eklemek üzereyken çağrılır. |

### Örnekler

Veritabanı BLOB alanında saklanan görüntülerin bir rapora nasıl ekleneceğini gösterir.

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

        // Tüm kayıtları bir kerede okuyan bir modda olması gereken veri okuyucuyu açın.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hiçbir şey yapma.
    }

    /// <summary>
    /// Adres mektup birleştirme, belgede adında "Image:" etiketi olan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Birleştirme verilerini HTML belgeleri biçiminde işleyen özel bir geri aramayla adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

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
/// Adres mektup birleştirme, adı "html_" öneki ile başlayan bir MERGEFIELD ile karşılaşırsa,
/// bu geri arama, birleştirme verilerini HTML içeriği olarak ayrıştırır ve sonucu MERGEFIELD'in belge konumuna ekler.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Adres mektup birleştirme verileri bir MERGEFIELD ile birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Ayrıştırılmış HTML verilerini belgenin gövdesine ekleyin.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Birleştirilmiş içeriği zaten manuel olarak eklediğimiz için,
             // "Metin" özelliği aracılığıyla içerik döndürerek bu olaya yanıt vermemiz gerekmeyecek.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hiçbir şey yapma.
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
