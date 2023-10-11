---
title: FieldArgumentBuilder.AddField
second_title: Aspose.Words for .NET API Referansı
description: FieldArgumentBuilder yöntem. Bir ile temsil edilen bir alan eklerFieldBuilder argümana.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldargumentbuilder/addfield/
---
## FieldArgumentBuilder.AddField method

Bir ile temsil edilen bir alan ekler[`FieldBuilder`](../../fieldbuilder/) argümana.

```csharp
public FieldArgumentBuilder AddField(FieldBuilder fieldBuilder)
```

### Örnekler

Alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından bunların belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Aşağıda bir saha oluşturucu kullanılarak yapılan üç saha inşaatı örneği verilmiştir.
// 1 - Tek alan:
// ƒ (Florin) sembolünü görüntüleyen bir SEMBOL alanı eklemek için bir alan oluşturucu kullanın.
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - İç içe alan:
// Başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturmak için alan oluşturucuyu kullanın.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Başka bir SEMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
 // yukarıda oluşturduğumuz SYMBOL alanına argümanı olarak ekledik.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Dış SEMBOL alanı argüman olarak formül alanı sonucunu (174) kullanacaktır,
// karakter numarası 174 olduğundan alanın ® (Kayıtlı İşaret) sembolünü göstermesini sağlayacaktır.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Birden fazla iç içe geçmiş alan ve argüman:
// Şimdi, iki özel dize değerinden birini görüntüleyen bir IF alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış değerini elde etmek için
// IF alanının hangi dizeyi görüntüleyeceğini belirleyen IF alanı, iki sayısal ifadenin eşitliğini test edecektir.
// IF alanının içine yerleştireceğimiz iki ifadeyi formül alanları şeklinde sağlayacağız.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Daha sonra, IF alanı için doğru/yanlış çıktı dizeleri olarak hizmet edecek iki alan argümanı oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Son olarak IF alanı için bir alan oluşturucu daha oluşturacağız ve tüm ifadeleri birleştireceğiz.
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

* class [FieldBuilder](../../fieldbuilder/)
* class [FieldArgumentBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldargumentbuilder/)
* toplantı [Aspose.Words](../../../)


