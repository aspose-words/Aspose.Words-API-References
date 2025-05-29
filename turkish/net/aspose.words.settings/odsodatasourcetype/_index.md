---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: .NET için Aspose.Words
description: Harici veri kaynaklarına kolayca bağlanmak ve belge işleme yeteneklerinizi geliştirmek için Aspose.Words OdsoDataSourceType enum'ını keşfedin.
type: docs
weight: 6720
url: /tr/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

ODSO bağlantı bilgilerinin bir parçası olarak bağlanılacak harici veri kaynağının türünü belirtir.

```csharp
public enum OdsoDataSourceType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Text | `0` | Belirli bir belgenin bir metin dosyasına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOther. |
| Database | `1` | Belirli bir belgenin bir veritabanına bağlandığını belirtir. Muhtemelen wdMergeSubTypeAccess. |
| AddressBook | `2` | Belirli bir belgenin bir kişi adres defterine bağlandığını belirtir. Muhtemelen wdMergeSubTypeOAL. |
| Document1 | `3` | Belirli bir belgenin, üreten uygulama tarafından desteklenen başka bir belge biçimine bağlandığını belirtir. Muhtemelen wdMergeSubTypeOLEDBWord. |
| Document2 | `4` | Belirli bir belgenin, üreten uygulama tarafından desteklenen başka bir belge biçimine bağlandığını belirtir. Muhtemelen wdMergeSubTypeWorks. |
| Native | `5` | Belirli bir belgenin, üreten uygulamaya özgü başka bir belge biçimine bağlandığını belirtir. Muhtemelen wdMergeSubTypeOLEDBText |
| Email | `6` | Belirli bir belgenin bir e-posta uygulamasına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOutlook. |
| None | `7` | Harici veri kaynağının türü belirtilmemiş. Muhtemelen wdMergeSubTypeWord. |
| Legacy | `8` | Belirli bir belgenin, üreten uygulama tarafından desteklenen eski bir belge biçimine bağlandığını belirtir. Muhtemelen wdMergeSubTypeWord2000. |
| Master | `9` | Belirli bir belgenin diğer veri kaynaklarını toplayan bir veri kaynağına bağlandığını belirtir. |
| Default | `7` | eşittirNone . |

## Notlar

OOXML belirtimi bu enum için çok belirsiz. Sanırım WdMergeSubType enumeration'ına karşılık gelebilir http://msdn.microsoft.com/en-us/library/bb237801.aspx.

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
