---
title: MailMerge.CleanupOptions
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words for .NET
description: MailMerge CleanupOptions mülk. Adresmektup birleştirme sırasında hangi öğelerin kaldırılması gerektiğini belirten bir dizi işaret alır veya ayarlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Adres-mektup birleştirme sırasında hangi öğelerin kaldırılması gerektiğini belirten bir dizi işaret alır veya ayarlar.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

## Örnekler

Adres-mektup birleştirmenin birleştirme çıktı belgesinden oluşturabileceği boş paragrafların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

Adres-mektup birleştirme sırasında kullanılmayan MERGEFIELD'lerin otomatik olarak nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme veri kaynağı tablosunun üç sütunu için MERGEFIELD'leri içeren bir belge oluşturun,
// ve ardından adları MERGEFIELD'lerimizle eşleşen yalnızca iki sütunlu bir tablo oluşturun.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// Üçüncü MERGEFIELD'ımız, veri kaynağımızda bulunmayan bir "Şehir" sütununa başvuruyor.
// Adres-mektup birleştirme, bunun gibi alanları birleştirme öncesi durumlarında olduğu gibi bırakacaktır.
// "CleanupOptions" özelliğinin "RemoveUnusedFields" olarak ayarlanması tüm MERGEFIELD'leri kaldıracaktır
// adres-mektup birleştirme sırasında birleştirme belgelerini temizlemek için kullanılmayanlar.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Ayrıca bakınız

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
