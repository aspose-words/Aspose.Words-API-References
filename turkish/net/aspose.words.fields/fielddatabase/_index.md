---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldDatabase sınıf. DATABASE alanını uygular C#'da.
type: docs
weight: 1740
url: /tr/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

DATABASE alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldDatabase : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Verilere bağlantı alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Database 'nin tam yolunu ve dosya adını alır veya ayarlar |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Eklenecek ilk veri kaydının integral kayıt numarasını alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Formatın hangi niteliklerinin tabloya uygulanacağını alır veya ayarlar. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Veritabanındaki alan adlarının sonuç tablosundaki sütun başlıkları olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Birleştirmenin başlangıcına veri eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Eklenecek son veri kaydının integral kayıt numarasını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Veritabanını sorgulayan bir dizi SQL talimatını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Veritabanı sorgusunun sonucuna uygulanacak formatı alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

Bir veritabanı sorgusunun sonuçlarını bir WordprocessingML tablosuna ekler.

## Örnekler

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
