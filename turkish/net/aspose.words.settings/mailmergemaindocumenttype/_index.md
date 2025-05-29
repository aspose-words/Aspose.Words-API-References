---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: .NET için Aspose.Words
description: Kusursuz belge otomasyonu için çeşitli posta birleştirme kaynak belge türlerini tanımlayan Aspose.Words.MailMergeMainDocumentType enum'unu keşfedin.
type: docs
weight: 6670
url: /tr/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

Bir posta birleştirme kaynak belgesi için olası türleri belirtir.

```csharp
public enum MailMergeMainDocumentType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| NotAMergeDocument | `0` | Bu belge bir posta birleştirme belgesi değildir. |
| FormLetters | `1` | Posta birleştirme kaynak belgesinin form mektup türünde olduğunu belirtir. |
| MailingLabels | `2` | Posta birleştirme kaynak belgesinin posta etiketi türünde olduğunu belirtir. |
| Envelopes | `4` | Posta birleştirme kaynak belgesinin zarf türünde olduğunu belirtir. |
| Catalog | `8` | Posta birleştirme kaynak belgesinin katalog türünde olduğunu belirtir. |
| Email | `16` | Posta birleştirme kaynak belgesinin e-posta iletisi türünde olduğunu belirtir. |
| Fax | `32` | Posta birleştirme kaynak belgesinin faks türünde olduğunu belirtir. |
| Default | `0` | eşittirNotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
