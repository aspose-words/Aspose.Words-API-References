---
title: MailMergeSettings.DataSource
linktitle: DataSource
articleTitle: DataSource
second_title: Aspose.Words for .NET
description: MailMergeSettings DataSource mülk. Adresmektup birleştirme veri kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.settings/mailmergesettings/datasource/
---
## MailMergeSettings.DataSource property

Adres-mektup birleştirme veri kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir.

```csharp
public string DataSource { get; set; }
```

## Örnekler

Üst bilgi kaynağından ve veri kaynağından adres-mektup birleştirme için veri kaynağının nasıl oluşturulacağını gösterir.

```csharp
// Tek satırlı bir tablodan oluşacak bir posta etiketi birleştirme başlık dosyası oluşturun.
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

// MERGEFIELDS ile şu adlara sahip bir birleştirme hedefi belgesi oluşturun:
// birleştirme başlığı dosyası tablosundaki sütun adlarını eşleştirin.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Adres-mektup birleştirmemiz için iki belge dosya adı belirterek bir veri kaynağı oluşturun.
// Başlık kaynağı, veri kaynağı tablosunun sütunlarını adlandıracaktır.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// Veri kaynağı, başlık belgesi tablosundaki tüm sütunlar için veri satırları sağlayacaktır.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Microsoft Word'ün yürüteceği posta etiketi türü adres-mektup birleştirmeyi yapılandırın
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
