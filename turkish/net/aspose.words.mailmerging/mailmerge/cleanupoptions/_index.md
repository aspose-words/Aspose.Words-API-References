---
title: MailMerge.CleanupOptions
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: .NET için Aspose.Words
description: CleanupOptions özelliğiyle posta birleştirmenizi optimize edin; sorunsuz ve verimli bir süreç için hangi öğelerin kaldırılacağını kolayca yönetin.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirten bir dizi bayrak alır veya ayarlar.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

## Örnekler

Birleştirme çıktı belgesinden, birleştirme işleminin oluşturabileceği boş paragrafların nasıl kaldırılacağını gösterir.

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

Posta birleştirme sırasında kullanılmayan MERGEFIELD'lerin otomatik olarak nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir posta birleştirme veri kaynağı tablosunun üç sütunu için MERGEFIELD'leri içeren bir belge oluşturun,
// ve ardından MERGEFIELD'larımızla eşleşen yalnızca iki sütundan oluşan bir tablo oluşturalım.
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

// Üçüncü MERGEFIELD'ımız veri kaynağımızda bulunmayan bir "Şehir" sütununa atıfta bulunuyor.
// Posta birleştirme işlemi, bu gibi alanların birleştirme öncesi durumlarını olduğu gibi bırakacaktır.
// "CleanupOptions" özelliğini "RemoveUnusedFields" olarak ayarlamak tüm MERGEFIELD'leri kaldıracaktır
// birleştirme sırasında kullanılmayan birleştirme belgelerini temizlemek için.
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
