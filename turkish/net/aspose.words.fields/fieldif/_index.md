---
title: FieldIf Class
linktitle: FieldIf
articleTitle: FieldIf
second_title: .NET için Aspose.Words
description: Aspose.Words.Fields.FieldIf sınıfını keşfedin; belge otomasyonunu geliştirmek ve iş akışınızı kolaylaştırmak için IF alanlarını verimli bir şekilde uygulayın.
type: docs
weight: 2410
url: /tr/net/aspose.words.fields/fieldif/
---
## FieldIf class

IF alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldIf : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldIf](fieldif/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | Karşılaştırma operatörünü alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | Karşılaştırma ifadesinin görüntülenmesi durumunda görüntülenecek metni alır veya ayarlar`YANLIŞ` . |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | Karşılaştırma ifadesinin sol kısmını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | Karşılaştırma ifadesinin doğru kısmını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | Karşılaştırma ifadesi doğruysa görüntülenen metni alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | Durumu değerlendirir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

İfadelerle belirtilen değerleri karşılaştırır[`LeftExpression`](./leftexpression/) Ve[`RightExpression`](./rightexpression/) ile belirtilen operatör kullanılarak karşılaştırma[`ComparisonOperator`](./comparisonoperator/).

Aşağıdaki biçimdeki bir alan, posta birleştirme kaynağı olarak kullanılacaktır: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Örnekler

Bir IF alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// IF alanı, "TrueText" özelliğinden bir dize görüntüler,
// veya oluşturduğumuz ifadenin doğruluğuna bağlı olarak onun "FalseText" özelliği.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Bu durumda "0 = 1" yanlıştır, dolayısıyla görüntülenen sonuç "False" olacaktır.
Assert.AreEqual(" IF  0 = 1 True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.False, field.EvaluateCondition());
Assert.AreEqual("False", field.Result);

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Bu sefer ifade doğru olduğundan görüntülenen sonuç "True" olacaktır.
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
