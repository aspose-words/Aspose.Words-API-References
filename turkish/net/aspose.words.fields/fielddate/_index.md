---
title: FieldDate Class
linktitle: FieldDate
articleTitle: FieldDate
second_title: .NET için Aspose.Words
description: Belge otomasyonunuzu ve biçimlendirmenizi geliştirerek DATE alanlarını zahmetsizce uygulamak için tasarlanmış Aspose.Words.Fields.FieldDate sınıfını keşfedin.
type: docs
weight: 2180
url: /tr/net/aspose.words.fields/fielddate/
---
## FieldDate class

DATE alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldDate : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldDate](fielddate/)() | Default_Constructor |

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
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat/) { get; set; } | Yeni bir TARİH alanı eklerken barındırma uygulaması tarafından en son kullanılan biçimin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar/) { get; set; } | Hicri Ay takviminin mi yoksa İbrani Ay takviminin mi kullanılacağını alır veya ayarlar. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar/) { get; set; } | Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar/) { get; set; } | Um-al-Qura takviminin kullanılıp kullanılmayacağını alır veya ayarlar. |

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

Geçerli tarih ve saati ekler. Varsayılan olarak, Gregoryen takvimi kullanılır.

## Örnekler

Farklı takvim türlerine göre tarihleri görüntülemek için DATE alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki metnin her zaman doğru tarihi göstermesini istiyorsak DATE alanını kullanabiliriz.
// Aşağıda, bir DATE alanının bir tarihi görüntülemek için kullanabileceği üç tür kültürel takvim bulunmaktadır.
// 1 - Hicri Takvim:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Ümmü'l-Kurâ takvimi:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Hindistan Ulusal Takvimi:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Bir TARİH alanı ekleyin ve takvim türünü, ana bilgisayar uygulaması tarafından en son kullanılan türe ayarlayın.
// Microsoft Word'de, tür Ekle -> Metin -> Tarih ve Saat iletişim kutusunda en son kullanılan tür olacaktır.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
