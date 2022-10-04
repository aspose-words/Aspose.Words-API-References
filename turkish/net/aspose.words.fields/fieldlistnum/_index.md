---
title: FieldListNum
second_title: Aspose.Words for .NET API Referansı
description: LISTNUM alanını uygular.
type: docs
weight: 1970
url: /tr/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

LISTNUM alanını uygular.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Soyut numaralandırma tanımının adının alan kodu tarafından sağlanıp sağlanmadığını gösteren bir değer döndürür. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Alanın varsayılan davranışını geçersiz kılarak listedeki düzeyi alır veya ayarlar. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Bu alan için başlangıç değerini alır veya ayarlar. |
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

### Örnekler

LISTNUM alanlarıyla paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca, onları numaralı listeleri taklit etmek için kullanmamıza izin veren çeşitli seçeneklere sahiptir.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
// Bu alan "0)" gösterecektir.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM alanları, her liste düzeyi için ayrı sayıları korur.
// LISTNUM alanını başka bir LISTNUM alanıyla aynı paragrafa ekleme
// sayı yerine liste düzeyini artırır.
// Bir sonraki alan yukarıda başlattığımız sayıma devam edecek ve liste düzeyinde 1 değerini gösterecek.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde bir sayıma başlar. "1" değerini görüntüler.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde bir sayıma başlar. "1" değerini görüntüler.
// Farklı liste düzeylerinin farklı biçimlendirmeleri vardır,
// böylece bu alanlar birleştirilmiş "1)a)i)" değerini gösterecek.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Ekleyeceğimiz sonraki LISTNUM alanı, saymaya liste düzeyinde devam edecek
// önceki LISTNUM alanının açık olduğunu.
// Farklı bir liste düzeyine atlamak için "ListLevel" özelliğini kullanabiliriz.
// Bu LISTNUM alanı 3. liste seviyesinde kalsaydı, "ii)" gösterirdi,
// ancak 2. listeye taşıdığımız için saymaya o seviyede devam ediyor ve "b)" gösteriyor.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Alanın farklı bir AUTONUM alan türüne öykünmesini sağlamak için ListName özelliğini ayarlayabiliriz.
// "NumberDefault", AUTONUM'a öykünür, "OutlineDefault", AUTONUMOUT'a öykünür,
// ve "LegalDefault", AUTONUMLGL alanlarını öykünür.
// Başlangıç numarası 1 olan "OutlineDefault" liste adı, "I" öğesinin görüntülenmesine neden olur.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName önceki alandan taşınmaz, bu yüzden her yeni alan için onu ayarlamamız gerekecek.
// Bu alan saymaya farklı liste adı ile devam eder ve "II." gösterir.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
