---
title: FieldDatabase.Connection
second_title: Aspose.Words for .NET API Referansı
description: FieldDatabase mülk. Verilere bağlantı alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielddatabase/connection/
---
## FieldDatabase.Connection property

Verilere bağlantı alır veya ayarlar.

```csharp
public string Connection { get; set; }
```

### Örnekler

Veritabanından verinin nasıl çıkarılacağını ve bunun bir alan olarak belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu DATABASE alanı bir veritabanı üzerinde bir sorgu çalıştıracak ve sonucu bir tabloda görüntüleyecektir.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Tüm ürünleri brüt satışlara göre azalan sırada sıralayan daha karmaşık bir sorgu içeren başka bir DATABASE alanı ekleyin.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Bu özellikler LIMIT ve TOP cümleleriyle aynı işleve sahiptir.
// Bunları, alanın tablosunda sorgu sonucunun yalnızca 1'den 10'a kadar olan satırlarını görüntüleyecek şekilde yapılandırın.
field.FirstRecord = "1";
field.LastRecord = "10";

// Bu özellik tablomuz için kullanmak istediğimiz formatın indeksidir. Tablo formatlarının listesi "Tablo Otomatik Formatı..." menüsündedir
// Microsoft Word'de bir DATABASE alanı oluşturduğumuzda bu ortaya çıkıyor. Dizin #10 "Renkli 3" formatına karşılık gelir.
field.TableFormat = "10";

// FormatAttribute özelliği, birden çok bayrağı saklayan bir tam sayının dize temsilidir.
// Bu özellikte farklı flaglar ayarlayarak TableFormat özelliğinin işaret ettiği formatı patrially uygulayabiliriz.
// Kullandığımız sayı, tablo stilinin farklı yönlerine karşılık gelen değerlerin birleşiminin toplamıdır.
// 63, 1 (kenarlıklar) + 2 (gölgelendirme) + 4 (yazı tipi) + 8 (renk) + 16 (otomatik sığdırma) + 32 (başlık satırları) anlamına gelir.
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Ayrıca bakınız

* class [FieldDatabase](../)
* ad alanı [Aspose.Words.Fields](../../fielddatabase/)
* toplantı [Aspose.Words](../../../)


