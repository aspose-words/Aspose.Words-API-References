---
title: Document.MailMergeSettings
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: .NET için Aspose.Words
description: Tüm belgelerinizin posta birleştirme verilerini etkin bir şekilde yönetmek ve iş akışınızı geliştirmek için MailMergeSettings özelliğini nasıl kullanacağınızı keşfedin.
type: docs
weight: 280
url: /tr/net/aspose.words/document/mailmergesettings/
---
## Document.MailMergeSettings property

Bir belgenin tüm posta birleştirme bilgilerini içeren nesneyi alır veya ayarlar.

```csharp
public MailMergeSettings MailMergeSettings { get; set; }
```

## Notlar

Bu nesneyi bir belge için bir posta birleştirme veri kaynağı belirtmek için kullanabilirsiniz ve bu bilgi (mevcut veri alanlarıyla birlikte) kullanıcı bu belgeyi açtığında Microsoft Word'de görünür. Veya bu nesneyi, kullanıcının bu belge için Microsoft Word 'de belirttiği posta birleştirme ayarlarını sorgulamak için kullanabilirsiniz.

Bu nesne asla`hükümsüz`.

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

* class [MailMergeSettings](../../../aspose.words.settings/mailmergesettings/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
