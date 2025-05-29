---
title: FieldListNum Class
linktitle: FieldListNum
articleTitle: FieldListNum
second_title: .NET için Aspose.Words
description: Kusursuz LISTNUM alan uygulaması için Aspose.Words.Fields.FieldListNum sınıfını keşfedin. Güçlü özellikler ile belge otomasyonunu bugün geliştirin!
type: docs
weight: 2530
url: /tr/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

LISTNUM alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Soyut numaralandırma tanımının adının alanın kodu tarafından sağlanıp sağlanmadığını belirten bir değer döndürür. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Alanın varsayılan davranışını geçersiz kılarak listedeki seviyeyi alır veya ayarlar. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Bu alan için başlangıç değerini alır veya ayarlar. |
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

## Örnekler

LISTNUM alanlarıyla paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca numaralandırılmış listeleri taklit etmemize olanak tanıyan çeşitli seçeneklere sahiptir.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
// Bu alanda "0)" gösterilecektir.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// LISTNUM alanları her liste düzeyi için ayrı sayımları korur.
// Aynı paragrafa başka bir LISTNUM alanıyla birlikte bir LISTNUM alanı ekleme
// sayım yerine liste düzeyini artırır.
// Bir sonraki alan yukarıda başlattığımız sayımı sürdürecek ve liste düzeyi 1'de "1" değerini gösterecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste seviyesi 2'den itibaren sayımı başlatacaktır. "1" değerini gösterecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste seviyesi 3'te bir sayım başlatacaktır. "1" değerini gösterecektir.
// Farklı liste seviyelerinin farklı biçimlendirmeleri vardır,
// bu alanların birleştirilmesiyle "1)a)i)" değeri görüntülenecektir.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Eklediğimiz bir sonraki LISTNUM alanı sayımı liste düzeyinde sürdürecektir
// önceki LISTNUM alanının açık olduğu.
// Farklı bir liste düzeyine geçmek için "ListLevel" özelliğini kullanabiliriz.
// Bu LISTNUM alanı liste düzeyi 3'te kalsaydı, "ii)" görüntülenirdi,
// ancak, bunu liste düzeyi 2'ye taşıdığımız için, sayımı o düzeyde sürdürür ve "b)" görüntüler.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Alanın farklı bir AUTONUM alan türünü taklit etmesini sağlamak için ListName özelliğini ayarlayabiliriz.
// "NumberDefault" AUTONUM'u taklit eder, "OutlineDefault" AUTONUMOUT'u taklit eder,
// ve "LegalDefault" AUTONUMLGL alanlarını taklit eder.
// Başlangıç numarası 1 olan "OutlineDefault" liste adı, "I." görüntülenmesiyle sonuçlanacaktır.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName önceki alandan taşınmaz, bu yüzden her yeni alan için bunu ayarlamamız gerekecektir.
// Bu alan farklı liste adıyla sayımı sürdürür ve "II." görüntüler.
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
