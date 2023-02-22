---
title: Class FieldDatabase
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldDatabase sınıf. VERİTABANI alanını uygular.
type: docs
weight: 1590
url: /tr/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

VERİTABANI alanını uygular.

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
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Verilere bir bağlantı alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Veritabanının tam yolunu ve dosya adını alır veya ayarlar |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Eklenecek ilk veri kaydının integral kayıt numarasını alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Biçimin hangi özniteliklerinin tabloya uygulanacağını alır veya ayarlar. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Sonuç tablosunda veritabanından alan adlarının sütun başlıkları olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Bir birleştirmenin başlangıcında veri eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Eklenecek son veri kaydının integral kayıt numarasını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Veritabanını sorgulayan bir dizi SQL talimatı alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Veritabanı sorgusunun sonucuna uygulanacak formatı alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Bir veritabanı sorgusunun sonuçlarını bir WordprocessingML tablosuna ekler.

### Örnekler

Bir veritabanından nasıl veri alınacağını ve bir belgeye alan olarak nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu DATABASE alanı, bir veritabanı üzerinde bir sorgu çalıştıracak ve sonucu bir tabloda gösterecektir.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d \"{DatabaseDir.Replace("\\", "\\\\") + "Northwind.mdb"}\" \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", 
    field.GetFieldCode());

// Tüm ürünleri brüt satışlara göre azalan düzende sıralayan daha karmaşık bir sorguya sahip başka bir DATABASE alanı ekleyin.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = MyDir + @"Database\Northwind.mdb";
field.Connection = "DSN=MS Access Databases";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Bu özellikler, LIMIT ve TOP yan tümceleri ile aynı işleve sahiptir.
// Alan tablosunda sorgu sonucunun yalnızca 1'den 10'a kadar olan satırlarını görüntüleyecek şekilde yapılandırın.
field.FirstRecord = "1";
field.LastRecord = "10";

// Bu özellik, tablomuz için kullanmak istediğimiz formatın indeksidir. Tablo biçimlerinin listesi "Tablo Otomatik Biçimi..." menüsündedir.
// Microsoft Word'de bir DATABASE alanı oluşturduğumuzda ortaya çıkıyor. Dizin #10, "Renkli 3" biçimine karşılık gelir.
field.TableFormat = "10";

// FormatAttribute özelliği, birden çok bayrağı saklayan bir tamsayının dize temsilidir.
// TableFormat özelliğinin gösterdiği formatı bu özellikte farklı flaglar ayarlayarak patrially uygulayabiliriz.
// Kullandığımız sayı, tablo stilinin farklı yönlerine karşılık gelen değerlerin birleşiminin toplamıdır.
// 63, 1 (kenarlıklar) + 2 (gölgeleme) + 4 (yazı tipi) + 8 (renk) + 16 (otomatik sığdırma) + 32'yi (başlık satırları) temsil eder.
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


