---
title: FieldDatabase.Connection
linktitle: Connection
articleTitle: Connection
second_title: .NET için Aspose.Words
description: FieldDatabase Bağlantı özelliğiyle verilerinizi zahmetsizce yönetin. Sorunsuz veri entegrasyonu için bağlantıları kolayca alın veya ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielddatabase/connection/
---
## FieldDatabase.Connection property

Verilere bir bağlantı alır veya ayarlar.

```csharp
public string Connection { get; set; }
```

## Örnekler

Bir veritabanından verinin nasıl çıkarılacağını ve bir belgeye alan olarak nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu DATABASE alanı bir veritabanında sorgu çalıştıracak ve sonucu bir tabloda gösterecektir.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Tüm ürünleri brüt satışlara göre azalan düzende sıralayan daha karmaşık bir sorgu içeren başka bir VERİ TABANI alanı ekleyin.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Bu özellikler LIMIT ve TOP ifadeleriyle aynı işleve sahiptir.
// Sorgu sonucunun yalnızca 1 ila 10. satırlarını alanın tablosunda görüntüleyecek şekilde yapılandırın.
field.FirstRecord = "1";
field.LastRecord = "10";

// Bu özellik tablomuz için kullanmak istediğimiz biçimin dizinidir. Tablo biçimlerinin listesi "Tablo Otomatik Biçimlendirme..." menüsündedir
// Microsoft Word'de bir DATABASE alanı oluşturduğumuzda ortaya çıkar. İndeks #10 "Renkli 3" formatına karşılık gelir.
field.TableFormat = "10";

// FormatAttribute özelliği, birden fazla bayrağı depolayan bir tamsayının dize gösterimidir.
// TableFormat özelliğinin işaret ettiği formatı, bu özelliğe farklı bayraklar ekleyerek patriyal olarak uygulayabiliriz.
// Kullandığımız sayı, tablo stilinin farklı yönlerine karşılık gelen değerlerin birleşiminden oluşan bir sayıdır.
// 63, 1 (kenarlıklar) + 2 (gölgelendirme) + 4 (yazı tipi) + 8 (renk) + 16 (otomatik sığdırma) + 32 (başlık satırları) değerini temsil eder.
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Ayrıca bakınız

* class [FieldDatabase](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
