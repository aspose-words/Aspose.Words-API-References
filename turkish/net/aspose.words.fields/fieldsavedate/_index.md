---
title: FieldSaveDate Class
linktitle: FieldSaveDate
articleTitle: FieldSaveDate
second_title: .NET için Aspose.Words
description: Belge yönetimini kolaylaştırmak için SAVEDATE alanını zahmetsizce uygulamak üzere tasarlanmış Aspose.Words.Fields.FieldSaveDate sınıfını keşfedin.
type: docs
weight: 2760
url: /tr/net/aspose.words.fields/fieldsavedate/
---
## FieldSaveDate class

SAVEDATE alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldSaveDate : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSaveDate](fieldsavedate/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseLunarCalendar](../../aspose.words.fields/fieldsavedate/uselunarcalendar/) { get; set; } | Hicri Ay takviminin mi yoksa İbrani Ay takviminin mi kullanılacağını alır veya ayarlar. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldsavedate/usesakaeracalendar/) { get; set; } | Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldsavedate/useumalquracalendar/) { get; set; } | Um-al-Qura takviminin kullanılıp kullanılmayacağını alır veya ayarlar. |

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

Belgenin en son kaydedildiği tarih ve saati alır. Varsayılan olarak, Gregoryen takvimi kullanılır.

## Örnekler

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini görüntülemek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Belgedeki son kaydetme işleminin tarih ve saatini görüntülemek için SAVEDATE alanını kullanabiliriz.
// Bu alanların atıfta bulunduğu kaydetme işlemi, Microsoft Word gibi bir uygulamada manuel kaydetmedir.
// belgenin Kaydetme yöntemi değil.
// Aşağıda SAVEDATE alanının tarih/saati görüntüleyebileceği üç farklı takvim türü bulunmaktadır.
// 1 - Hicri Takvim:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Ümmü'l-Kurâ takvimi:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Hindistan Ulusal Takvimi:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE alanları tarih/saat değerlerini LastSavedTime yerleşik özelliğinden alır.
// Belgenin Kaydetme metodu bu değeri güncellemeyecektir, ancak yine de manuel olarak güncelleyebiliriz.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
