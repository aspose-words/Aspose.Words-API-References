---
title: Enum MailMergeDestination
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.MailMergeDestination Sıralama. Bir belge üzerinde adresmektup birleştirme gerçekleştirildiğinde oluşturulabilecek olası sonuçları belirtir.
type: docs
weight: 5830
url: /tr/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Bir belge üzerinde adres-mektup birleştirme gerçekleştirildiğinde oluşturulabilecek olası sonuçları belirtir.

```csharp
public enum MailMergeDestination
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| NewDocument | `0` | Uyumlu barındırma uygulamalarının, belirli bir belgedeki alanlarını belirtilen harici veri kaynağından alınan verilerle doldurarak yeni belgeler oluşturacağını belirtir. |
| Printer | `1` | Uyumlu barındırma uygulamalarının, belirli bir belge içindeki alanlarının belirtilen harici veri kaynağından gelen harici verilerle doldurulması sonucunda elde edilen belgeleri yazdıracağını belirtir. |
| Email | `2` | Uyumlu barındırma uygulamalarının, belirli bir belge içindeki alanları belirtilen harici veri kaynağından alınan verilerle doldurma sonucu ortaya çıkan belgeleri kullanarak e-postalar oluşturacağını belirtir. |
| Fax | `4` | Uyumlu barındırma uygulamalarının, belirli bir belge içindeki alanları belirtilen harici veri kaynağından alınan verilerle doldurma sonucu ortaya çıkan belgeleri kullanarak faks oluşturacağını belirtir. |
| Default | `0` | Şuna eşittir:NewDocument değer. |

### Örnekler

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

* property [Destination](../mailmergesettings/destination/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


