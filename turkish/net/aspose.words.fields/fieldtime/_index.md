---
title: FieldTime Class
linktitle: FieldTime
articleTitle: FieldTime
second_title: .NET için Aspose.Words
description: Kusursuz TIME alanı uygulaması için Aspose.Words.Fields.FieldTime sınıfını keşfedin. Güçlü özellikler ile belge otomasyonunuzu geliştirin!
type: docs
weight: 2910
url: /tr/net/aspose.words.fields/fieldtime/
---
## FieldTime class

TIME alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldTime : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldTime](fieldtime/)() | Default_Constructor |

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

Geçerli tarih ve saati ekler.

## Örnekler

TIME alanını kullanarak geçerli saatin nasıl görüntüleneceğini gösterir.

```csharp
public void FieldTime()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Varsayılan olarak, saat "s:dd am/pm" biçiminde görüntülenir.
    FieldTime field = InsertFieldTime(builder, "");

    Assert.AreEqual(" TIME ", field.GetFieldCode());

    // Gösterilen zamanın formatını değiştirmek için \@ işaretini kullanabiliriz.
    field = InsertFieldTime(builder, "\\@ HHmm");

    Assert.AreEqual(" TIME \\@ HHmm", field.GetFieldCode());

    // TIME alanının biçimini ayarlayarak tarihin de Miladi takvime göre gösterilmesini sağlayabiliriz.
    field = InsertFieldTime(builder, "\\@ \"M/d/yyyy h mm:ss am/pm\"");

    Assert.AreEqual(" TIME \\@ \"M/d/yyyy h mm:ss am/pm\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.TIME.docx");
}

/// <summary>
/// Bir TIME alanı eklemek, yeni bir paragraf eklemek ve alanı döndürmek için bir belge oluşturucu kullanın.
/// </summary>
private static FieldTime InsertFieldTime(DocumentBuilder builder, string format)
{
    FieldTime field = (FieldTime)builder.InsertField(FieldType.FieldTime, true);
    builder.MoveTo(field.Separator);
    builder.Write(format);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
