---
title: MailMergeSettings.CheckErrors
linktitle: CheckErrors
articleTitle: CheckErrors
second_title: .NET için Aspose.Words
description: Posta birleştirmeleri sırasında etkili hata raporlaması için Microsoft Word'deki MailMergeSettings CheckErrors özelliğini keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.settings/mailmergesettings/checkerrors/
---
## MailMergeSettings.CheckErrors property

Microsoft Word tarafından posta birleştirme işlemi gerçekleştirilirken gerçekleştirilecek hata raporlama türünü belirtir. Varsayılan değerDefault .

```csharp
public MailMergeCheckErrors CheckErrors { get; set; }
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

* enum [MailMergeCheckErrors](../../mailmergecheckerrors/)
* class [MailMergeSettings](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
