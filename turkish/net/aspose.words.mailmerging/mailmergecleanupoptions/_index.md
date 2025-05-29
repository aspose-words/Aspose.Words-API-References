---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: .NET için Aspose.Words
description: Posta birleştirme temizliğini etkili bir şekilde yönetmek için Aspose.Words.MailMergeCleanupOptions enum'unu keşfedin. Öğe kaldırmayı sorunsuz bir şekilde kontrol ederek belgelerinizi optimize edin.
type: docs
weight: 4540
url: /tr/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirleyen seçenekleri belirtir.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan bir değer belirtir. |
| RemoveEmptyParagraphs | `1` | Veri içermeyen birleştirme alanlarını içeren paragrafların belgeden kaldırılıp kaldırılmayacağını belirtir. Bu seçenek ayarlandığında, aksi takdirde boş olan bölge başlangıç ve bitiş birleştirme alanlarını içeren paragraflar da kaldırılır. |
| RemoveUnusedRegions | `2` | Kullanılmayan posta birleştirme bölgelerinin belgeden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveUnusedFields | `4` | Kullanılmayan birleştirme alanlarının belgeden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveContainingFields | `8` | Birleştirme alanları içeren alanların (örneğin, IF'ler) belgeden kaldırılıp kaldırılmayacağını belirtir. İç içe geçmiş birleştirme alanları kaldırılırsa. |
| RemoveStaticFields | `10` | Statik alanların belgeden kaldırılıp kaldırılmayacağını belirtir. Statik alanlar, herhangi bir belge değişikliğinde sonuçları aynı kalan alanlardır. Sonuçlarını bir belgede saklamayan ve anında hesaplanan alanlar (örneğinFieldListNum , FieldSymbol , vb.) statik olarak kabul edilmez. |
| RemoveEmptyTableRows | `20` | Posta birleştirme bölgeleri içeren boş satırların belgeden kaldırılıp kaldırılmayacağını belirtir. |
| RemoveEmptyTables | `40` | kullanılarak kaldırılan posta birleştirme bölgelerini içeren belge tablolarından kaldırılıp kaldırılmayacağını belirtir.RemoveUnusedRegions veyaRemoveEmptyTableRows seçenek. |

## Örnekler

Posta birleştirme sırasında tüm boş tablonun nasıl kaldırılacağını gösterir.

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
