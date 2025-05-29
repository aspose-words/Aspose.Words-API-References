---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: .NET için Aspose.Words
description: Sorunsuz belge posta birleştirmeleri için sonuçları tanımlayan Aspose.Words.MailMergeDestination enum'unu keşfedin. Belge işlemenizi bugün optimize edin!
type: docs
weight: 6660
url: /tr/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Bir belge üzerinde posta birleştirme işlemi gerçekleştirildiğinde oluşabilecek olası sonuçları belirtir.

```csharp
public enum MailMergeDestination
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| NewDocument | `0` | Uyumlu barındırma uygulamalarının, belirtilen harici veri kaynağından alınan verilerle belirli bir belgedeki alanlarını doldurarak yeni belgeler oluşturması gerektiğini belirtir. |
| Printer | `1` | Uyumlu barındırma uygulamalarının, belirtilen harici veri kaynağından gelen harici verilerle belirli bir belgedeki alanlarının doldurulmasıyla oluşan belgeleri yazdırması gerektiğini belirtir. |
| Email | `2` | Uyumlu barındırma uygulamalarının, belirtilen harici veri kaynağından alınan verilerle belirli bir belgedeki alanları doldurarak elde edilen belgeleri kullanarak e-postalar oluşturması gerektiğini belirtir. |
| Fax | `4` | Uyumlu barındırma uygulamalarının, belirtilen harici veri kaynağından alınan verilerle belirli bir belgedeki alanları doldurarak elde edilen belgeleri kullanarak fakslar üretmesi gerektiğini belirtir. |
| Default | `0` | eşittirNewDocument değer. |

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

* property [Destination](../mailmergesettings/destination/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
