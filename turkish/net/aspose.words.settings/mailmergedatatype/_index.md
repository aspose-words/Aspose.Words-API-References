---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.MailMergeDataType Sıralama. Harici adresmektup birleştirme veri kaynağının türünü belirtir C#'da.
type: docs
weight: 5820
url: /tr/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Harici adres-mektup birleştirme veri kaynağının türünü belirtir.

```csharp
public enum MailMergeDataType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Adres-mektup birleştirme veri kaynağı belirtilmedi. |
| TextFile | `0` | Belirli bir belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir metin dosyasına bağlandığını belirtir. |
| Database | `1` | Belirli bir belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla Access veritabanına bağlandığını belirtir. |
| Spreadsheet | `2` | Belirli bir belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Excel elektronik tablosuna bağlandığını belirtir. |
| Query | `3` | Belirli bir belgenin harici bir sorgu aracı kullanılarak harici bir veri kaynağına bağlandığını belirtir. |
| Odbc | `4` | Belirli bir belgenin Açık Veritabanı Bağlantısı arayüzü aracılığıyla harici bir veri kaynağına bağlandığını belirtir. |
| Native | `5` | Belirli bir belgenin, Office Veri Kaynağı Nesnesi (ODSO) arabirimi aracılığıyla harici bir veri kaynağına bağlandığını belirtir. |
| Default | `-1` | Şuna eşittir:None . |

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

* property [DataType](../mailmergesettings/datatype/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
