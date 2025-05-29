---
title: FieldBuilder Class
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: .NET için Aspose.Words
description: Kod belirteçleri ve anahtarları kullanarak alanları zahmetsizce oluşturmak için Aspose.Words.Fields.FieldBuilder sınıfını keşfedin. Belge otomasyonunuzu bugün geliştirin!
type: docs
weight: 2070
url: /tr/net/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class

Alan kodu belirteçlerinden (bağımsız değişkenler ve anahtarlar) bir alan oluşturur.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldBuilder
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldBuilder](fieldbuilder/)(*[FieldType](../fieldtype/)*) | Bir örneğini başlatır`FieldBuilder` sınıf. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_2)(*double*) | Bir alanın argümanını ekler. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument)(*[FieldArgumentBuilder](../fieldargumentbuilder/)*) | ile temsil edilen bir alanın argümanını ekler[`FieldArgumentBuilder`](../fieldargumentbuilder/) alanın koduna. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_1)(*FieldBuilder*) | Başka bir alan tarafından temsil edilen bir alt alan ekler`FieldBuilder` alanın koduna. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_3)(*int*) | Bir alanın argümanını ekler. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_4)(*string*) | Bir alanın argümanını ekler. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch)(*string*) | Bir alanın anahtarını ekler. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_1)(*string, double*) | Bir alanın anahtarını ekler. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_2)(*string, int*) | Bir alanın anahtarını ekler. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_3)(*string, string*) | Bir alanın anahtarını ekler. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert)(*[Inline](../../aspose.words/inline/)*) | Belirtilen satır içi düğümden önce belgeye bir alan oluşturur ve ekler. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert_1)(*[Paragraph](../../aspose.words/paragraph/)*) | Belirtilen paragrafın sonuna kadar belgeye bir alan oluşturur ve ekler. |

## Örnekler

Alan oluşturucuyu kullanarak alanların nasıl oluşturulacağını ve daha sonra bunların belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Aşağıda bir alan oluşturucu kullanılarak yapılmış üç alan inşası örneği bulunmaktadır.
// 1 - Tek alan:
// ƒ (Florin) sembolünü görüntüleyen bir SEMBOL alanı eklemek için bir alan oluşturucu kullanın.
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - İç içe geçmiş alan:
// Başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturmak için bir alan oluşturucu kullanın.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Başka bir SEMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
 // yukarıda oluşturduğumuz SYMBOL alanına argüman olarak ekliyoruz.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Dış SYMBOL alanı, argümanı olarak formül alanı sonucu olan 174'ü kullanacaktır.
// karakter sayısı 174 olduğundan alanın ® (Kayıtlı İşaret) sembolünü göstermesini sağlayacaktır.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Çoklu iç içe geçmiş alanlar ve argümanlar:
// Şimdi, iki özel dize değerinden birini görüntüleyen bir IF alanı oluşturmak için bir oluşturucu kullanacağız.
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış değeri elde etmek için
// IF alanının hangi dizeyi görüntüleyeceğini belirleyen, IF alanı iki sayısal ifadenin eşitliğini test edecektir.
// İki ifadeyi, IF alanının içine yerleştireceğimiz formül alanları biçiminde sağlayacağız.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Sonra, IF alanı için doğru/yanlış çıkış dizeleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacaktır.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Son olarak, IF alanı için bir alan oluşturucu daha oluşturacağız ve tüm ifadeleri birleştireceğiz.
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.AreEqual(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
