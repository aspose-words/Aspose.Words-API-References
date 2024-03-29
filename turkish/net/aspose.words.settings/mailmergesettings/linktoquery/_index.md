---
title: MailMergeSettings.LinkToQuery
linktitle: LinkToQuery
articleTitle: LinkToQuery
second_title: Aspose.Words for .NET
description: MailMergeSettings LinkToQuery mülk. Bundan emin değilim. Microsoft Word Otomasyon Referansı bunun belgesi Microsoft Wordde her açıldığında sorgunun yürütüldüğünü belirttiğini öne sürüyor. Ancak OOXML spesifikasyonu bunun sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini öne sürer. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.settings/mailmergesettings/linktoquery/
---
## MailMergeSettings.LinkToQuery property

Bundan emin değilim. Microsoft Word Otomasyon Referansı, bunun, belgesi Microsoft Word'de her açıldığında sorgunun yürütüldüğünü belirttiğini öne sürüyor. Ancak OOXML spesifikasyonu, bunun, sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini öne sürer. Varsayılan değer:`YANLIŞ` .

```csharp
public bool LinkToQuery { get; set; }
```

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

* class [MailMergeSettings](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
