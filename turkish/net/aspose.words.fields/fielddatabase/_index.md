---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: .NET için Aspose.Words
description: Belgelerinizde DATABASE alanlarını verimli bir şekilde uygulamak için Aspose.Words.Fields.FieldDatabase sınıfını keşfedin. Belge otomasyonunuzu bugün geliştirin!
type: docs
weight: 2150
url: /tr/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

DATABASE alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

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
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Eklenecek ilk veri kaydının tamsayı kayıt numarasını alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Tabloya hangi format niteliklerinin uygulanacağını alır veya ayarlar. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Alan adlarının veritabanından sütun başlıkları olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Bir birleştirmenin başına veri eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Eklenecek son veri kaydının tamsayı kayıt numarasını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Veritabanını sorgulayan bir dizi SQL talimatını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Veritabanı sorgusunun sonucuna uygulanacak formatı alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Bir veritabanı sorgusunun sonuçlarını bir WordprocessingML tablosuna ekler.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
