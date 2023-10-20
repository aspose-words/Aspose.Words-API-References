---
title: FieldListNum Class
linktitle: FieldListNum
articleTitle: FieldListNum
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldListNum sınıf. LISTNUM alanını uygular C#'da.
type: docs
weight: 2120
url: /tr/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

LISTNUM alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldListNum : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Soyut numaralandırma tanımının adının alanın kodu tarafından sağlanıp sağlanmadığını belirten bir değer döndürür. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Alanın varsayılan davranışını geçersiz kılarak listedeki düzeyi alır veya ayarlar. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Bu alanın başlangıç değerini alır veya ayarlar. |
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

## Örnekler

LISTNUM alanlarıyla paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı görüntüler.
// Bu alanlar aynı zamanda onları numaralandırılmış listeleri taklit etmek için kullanmamıza izin veren çeşitli seçeneklere de sahiptir.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listeler varsayılan olarak 1'den saymaya başlar ancak bu sayıyı 0 gibi farklı bir değere de ayarlayabiliriz.
// Bu alanda "0)" görüntülenecektir.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM alanları her liste düzeyi için ayrı sayıları korur.
// LISTNUM alanını başka bir LISTNUM alanıyla aynı paragrafa ekleme
// sayı yerine liste düzeyini artırır.
// Bir sonraki alan yukarıda başlattığımız sayıma devam edecek ve liste düzeyi 1'de "1" değerini görüntüleyecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde 2'den bir sayım başlatacaktır. "1" değerini görüntüleyecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde 3'ten bir sayım başlatacaktır. "1" değerini görüntüleyecektir.
// Farklı liste seviyelerinin farklı formatları vardır,
// böylece bu alanlar bir araya getirildiğinde "1)a)i)" değeri görüntülenecektir.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Ekleyeceğimiz bir sonraki LISTNUM alanı liste düzeyinde sayıma devam edecek
// önceki LISTNUM alanının açık olduğu.
// Farklı bir liste düzeyine atlamak için "ListLevel" özelliğini kullanabiliriz.
// Bu LISTNUM alanı liste düzeyi 3'te kalırsa "ii)" görüntülenir,
// ama liste düzeyi 2'ye taşıdığımız için o düzeyde saymaya devam ediyor ve "b)" gösteriyor.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Alanın farklı bir AUTONUM alan tipini taklit etmesini sağlamak için ListName özelliğini ayarlayabiliriz.
// "NumberDefault" AUTONUM'u taklit eder, "OutlineDefault" AUTONUMOUT'u taklit eder,
// ve "LegalDefault", AUTONUMLGL alanlarını taklit eder.
// Başlangıç numarası 1 olan "OutlineDefault" liste adı, "I." görüntülenmesiyle sonuçlanacaktır.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName önceki alandan taşınmaz, dolayısıyla onu her yeni alan için ayarlamamız gerekecek.
// Bu alan farklı liste adı ile sayıma devam eder ve "II." değerini görüntüler.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
