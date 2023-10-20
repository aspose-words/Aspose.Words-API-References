---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words for .NET
description: Document MailMergeSettings mülk. Bir belgeye ilişkin tüm adresmektup birleştirme bilgilerini içeren nesneyi alır veya ayarlar C#'da.
type: docs
weight: 270
url: /tr/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Bir belgeye ilişkin tüm adres-mektup birleştirme bilgilerini içeren nesneyi alır veya ayarlar.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## Notlar

Bu nesneyi bir belge için adres-mektup birleştirme veri kaynağı belirtmek için kullanabilirsiniz ve kullanıcı bu belgeyi açtığında bu information (mevcut veri alanlarıyla birlikte) Microsoft Word'de görünecektir. Veya bu nesneyi adres-mektup birleştirme ayarlarını sorgulamak için kullanabilirsiniz kullanıcının bu belge için Microsoft Word 'de belirttiği.

Bu nesne asla`hükümsüz`.

## Örnekler

Bir Office Veri Kaynağı Nesnesinden alınan verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// ASCII dosyası biçiminde "|" işaretli bir veri kaynağı oluşturun karakter
// sütunları ayıran sınırlayıcı görevi görüyor. İlk satır üç sütunun adını içerir,
// ve sonraki her satır, ilgili değerlerin bulunduğu bir satırdır.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // Bu belgeyi Microsoft Word'de açmak, içerikleri görüntülemeden önce adres-mektup birleştirme işlemini gerçekleştirecektir.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ayrıca bakınız

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
