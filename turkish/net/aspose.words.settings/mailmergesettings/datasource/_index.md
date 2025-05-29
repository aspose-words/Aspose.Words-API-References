---
title: MailMergeSettings.DataSource
linktitle: DataSource
articleTitle: DataSource
second_title: .NET için Aspose.Words
description: Sorunsuz posta birleştirme entegrasyonu için MailMergeSettings DataSource özelliğinin nasıl ayarlanacağını keşfedin. En iyi sonuçlar için veri kaynağı yolunuzu kolayca belirtin!
type: docs
weight: 60
url: /tr/net/aspose.words.settings/mailmergesettings/datasource/
---
## MailMergeSettings.DataSource property

Posta birleştirme veri kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir.

```csharp
public string DataSource { get; set; }
```

## Örnekler

Bir başlık kaynağı ve bir veri kaynağından bir posta birleştirme için bir veri kaynağının nasıl oluşturulacağını gösterir.

```csharp
// Tek satırdan oluşan bir tablodan oluşan bir posta etiketi birleştirme başlık dosyası oluşturun.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Tek satırlı bir tablodan oluşan bir posta etiketi birleştirme veri dosyası oluşturun
 // ve başlık belgesinin tablosuyla aynı sayıda sütun.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// MERGEFIELDS ile bir birleştirme hedefi belgesi oluşturun ve adlarını şu şekilde girin:
// birleştirme başlık dosyası tablosundaki sütun adlarıyla eşleşir.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// İki belge dosya adı belirterek posta birleştirmemiz için bir veri kaynağı oluşturun.
// Başlık kaynağı, veri kaynağı tablosunun sütunlarını adlandıracaktır.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Veri kaynağı, başlık belge tablosundaki tüm sütunlar için veri satırları sağlayacaktır.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Microsoft Word'ün yürüteceği bir posta etiketi türü posta birleştirmeyi yapılandırın
// çıktı belgesini yüklemek için kullandığımız anda.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Ayrıca bakınız

* class [MailMergeSettings](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
