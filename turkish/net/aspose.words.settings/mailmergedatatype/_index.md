---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: .NET için Aspose.Words
description: Belge otomasyon projelerinize harici veri kaynaklarının sorunsuz entegrasyonu için Aspose.Words.MailMergeDataType enum'unu keşfedin.
type: docs
weight: 6650
url: /tr/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Harici bir posta birleştirme veri kaynağının türünü belirtir.

```csharp
public enum MailMergeDataType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Hiçbir posta birleştirme veri kaynağı belirtilmedi. |
| TextFile | `0` | Belirli bir belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir metin dosyasına bağlandığını belirtir. |
| Database | `1` | Belirli bir belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Access veritabanına bağlandığını belirtir. |
| Spreadsheet | `2` | Belirli bir belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Excel elektronik tablosuna bağlandığını belirtir. |
| Query | `3` | Belirli bir belgenin harici bir sorgu aracı kullanılarak harici bir veri kaynağına bağlandığını belirtir. |
| Odbc | `4` | Belirli bir belgenin Açık Veritabanı Bağlantısı arayüzü aracılığıyla harici bir veri kaynağına bağlandığını belirtir. |
| Native | `5` | Belirli bir belgenin Office Veri Kaynağı Nesnesi (ODSO) arayüzü aracılığıyla harici bir veri kaynağına bağlandığını belirtir. |
| Default | `-1` | eşittirNone . |

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

* property [DataType](../mailmergesettings/datatype/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
