---
title: FieldEmbed Class
linktitle: FieldEmbed
articleTitle: FieldEmbed
second_title: .NET için Aspose.Words
description: Sorunsuz EMBED alanı uygulaması, belge işlevselliğini ve çok yönlülüğünü artırmak için Aspose.Words.Fields.FieldEmbed sınıfını keşfedin.
type: docs
weight: 2260
url: /tr/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

EMBED alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldEmbed : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldEmbed](fieldembed/)() | Default_Constructor |

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

## Örnekler

SHAPE ve EMBED gibi bazı eski Microsoft Word alanlarının yükleme sırasında nasıl işlendiğini gösterir.

```csharp
// Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Word belgesini açıp Alt+F9'a basarsak SHAPE ve EMBED alanını göreceğiz.
// SHAPE alanı, "Metinle aynı hizada" sarma stili etkinleştirilmiş bir AutoShape nesnesi için bağlantı/tuvaldir.
// Bir EMBED alanı aynı işleve sahiptir, ancak gömülü bir nesne için,
// harici bir Excel belgesinden alınan bir elektronik tablo gibi.
// Ancak bu alanlar belgenin Alanlar koleksiyonunda görünmeyecektir.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Bu alanlar yalnızca Microsoft Word'ün eski sürümlerinde desteklenmektedir.
// Belge yükleme işlemi bu alanları Şekil nesnelerine dönüştürecektir.
// belgenin node koleksiyonunda erişebileceğimiz.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// İlk Şekil düğümü, giriş belgesindeki ŞEKİL alanına karşılık gelir,
// AutoShape için satır içi tuvaldir.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// İkinci Şekil düğümü AutoShape'in kendisidir.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Üçüncü Şekil, harici elektronik tabloyu içeren EMBED alanının ne olduğudur.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
