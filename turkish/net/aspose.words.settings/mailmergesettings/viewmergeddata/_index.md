---
title: MailMergeSettings.ViewMergedData
linktitle: ViewMergedData
articleTitle: ViewMergedData
second_title: .NET için Aspose.Words
description: Microsoft Word'deki MailMergeSettings'in ViewMergedData özelliğinin, birleştirilmiş verileri harici kaynaklardan önizleyerek belge oluşturma sürecinizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 170
url: /tr/net/aspose.words.settings/mailmergesettings/viewmergeddata/
---
## MailMergeSettings.ViewMergedData property

Microsoft Word'ün birleştirme alanlarının eklendiği belirtilen harici veri kaynağından gelen verileri görüntülemesini belirtir (örneğin birleştirilmiş verileri önizleme). Varsayılan değer:`YANLIŞ` .

```csharp
public bool ViewMergedData { get; set; }
```

## Örnekler

Office Veri Kaynağı Nesnesi'ndeki verilerle bir posta birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// "|" karakterini kullanarak ASCII dosyası biçiminde bir veri kaynağı oluşturun
// sütunları ayıran ayırıcı olarak işlev görür. İlk satır üç sütunun adlarını içerir,
// ve her bir sonraki satır, kendi değerlerine sahip bir satırdır.
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

 // Bu belgeyi Microsoft Word'de açmak, içerikleri görüntülemeden önce posta birleştirme işlemini gerçekleştirecektir.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ayrıca bakınız

* class [MailMergeSettings](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
