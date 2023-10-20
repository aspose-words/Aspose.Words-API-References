---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.MailMerging.MailMergeCleanupOptions Sıralama. Adresmektup birleştirme sırasında hangi öğelerin kaldırılacağını belirleyen seçenekleri belirtir C#'da.
type: docs
weight: 3850
url: /tr/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Adres-mektup birleştirme sırasında hangi öğelerin kaldırılacağını belirleyen seçenekleri belirtir.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan bir değeri belirtir. |
| RemoveEmptyParagraphs | `1` | Veri içermeyen adres-mektup birleştirme alanları içeren paragrafların belgeden kaldırılıp kaldırılmayacağını belirtir. Bu seçenek ayarlandığında, aksi durumda boş olan bölge başlangıç ve bitiş birleştirme alanlarını içeren paragraflar da kaldırılır. |
| RemoveUnusedRegions | `2` | Kullanılmayan adres-mektup birleştirme bölgelerinin belgeden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveUnusedFields | `4` | Kullanılmayan birleştirme alanlarının belgeden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveContainingFields | `8` | İç içe geçmiş birleştirme alanları kaldırılırsa, birleştirme alanları içeren alanların (örneğin IF'ler) document 'den kaldırılıp kaldırılmayacağını belirtir. |
| RemoveStaticFields | `10` | Statik alanların belgeden kaldırılıp kaldırılmayacağını belirtir. Statik alanlar, herhangi bir belge değişikliğinde sonuçlarının aynı kaldığı alanlardır. Sonuçlarını bir document dosyasında saklamayan ve anında hesaplanan alanlar (örneğinFieldListNum , FieldSymbol , vb.) statik olarak kabul edilmez. |
| RemoveEmptyTableRows | `20` | Adres-mektup birleştirme bölgelerini içeren boş satırların belgeden kaldırılıp kaldırılmayacağını belirtir. |

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
