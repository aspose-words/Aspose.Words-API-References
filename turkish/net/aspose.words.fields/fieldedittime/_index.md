---
title: Class FieldEditTime
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldEditTime sınıf. EDITTIME alanını uygular.
type: docs
weight: 1690
url: /tr/net/aspose.words.fields/fieldedittime/
---
## FieldEditTime class

EDITTIME alanını uygular.

```csharp
public class FieldEditTime : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldEditTime](fieldedittime/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
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

Belge oluşturulduğundan beri toplam düzenleme süresini dakika cinsinden alır.

### Örnekler

EDITTIME alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// EDITTIME alanı dakika cinsinden şunu gösterecektir:
// Microsoft Word penceresinde belge açıkken harcanan süre.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("You've been editing this document for ");
FieldEditTime field = (FieldEditTime)builder.InsertField(FieldType.FieldEditTime, true);
builder.Writeln(" minutes.");

// Bu yerleşik belge özelliği, dakikaları izler. Microsoft Word bu özelliği kullanır
// belge açıkken harcanan süreyi izlemek için. Kendimiz de düzenleyebiliriz.
doc.BuiltInDocumentProperties.TotalEditingTime = 10;
field.Update();

Assert.AreEqual(" EDITTIME ", field.GetFieldCode());
Assert.AreEqual("10", field.Result);

// Alan kendini gerçek zamanlı olarak güncellemez ve ayrıca
// doğru bir değere ihtiyacımız olduğunda Microsoft Word'de manuel olarak güncellenir.
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.EDITTIME.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


