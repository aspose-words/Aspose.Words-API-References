---
title: BuildAndInsert
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen satır içi düğümden önce belgeye bir alan oluşturur ve ekler.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldbuilder/buildandinsert/
---
## BuildAndInsert(Inline) {#buildandinsert}

Belirtilen satır içi düğümden önce belgeye bir alan oluşturur ve ekler.

```csharp
public Field BuildAndInsert(Inline refNode)
```

### Geri dönüş değeri

A[`Field`](../../field/) eklenen alanı temsil eden nesne.

### Örnekler

Alan oluşturucu kullanarak bir alanın nasıl oluşturulacağını ve ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Bir belgeye metin içeriği eklemenin uygun bir yolu belge oluşturucudur.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Alanların, parça parça alan kodu oluşturmak için kullanabileceğimiz oluşturucuları vardır.
// Bu durumda, ABD posta kodunu temsil eden bir BARKOD alanı oluşturacağız,
// ve ardından bir Run'ın önüne ekleyin.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Ayrıca bakınız

* class [Field](../../field/)
* class [Inline](../../../aspose.words/inline/)
* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

---

## BuildAndInsert(Paragraph) {#buildandinsert_1}

Belirtilen paragrafın sonuna kadar belgeye bir alan oluşturur ve ekler.

```csharp
public Field BuildAndInsert(Paragraph refNode)
```

### Geri dönüş değeri

A[`Field`](../../field/) eklenen alanı temsil eden nesne.

### Örnekler

Alan oluşturucu kullanarak alanların nasıl oluşturulacağını ve ardından bunların belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// Aşağıda, bir alan oluşturucu kullanılarak yapılan üç alan oluşturma örneği verilmiştir.
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
// Başka bir alan oluşturucu tarafından iç alan olarak kullanılan bir formül alanı oluşturmak için bir alan oluşturucu kullanın.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Başka bir SEMBOL alanı için başka bir oluşturucu oluşturun ve formül alanını ekleyin
 // SYMBOL alanına argümanı olarak yukarıda oluşturduğumuz.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Dış SEMBOL alanı, argümanı olarak formül alanı sonucu 174'ü kullanır,
// karakter numarası 174 olduğundan alanın ® (Kayıtlı İşaret) sembolünü göstermesini sağlar.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Birden çok iç içe alan ve bağımsız değişken:
// Şimdi, iki özel dize değerinden birini görüntüleyen bir EĞER alanı oluşturmak için bir oluşturucu kullanacağız,
// ifadesinin doğru/yanlış değerine bağlı olarak. Doğru/yanlış bir değer elde etmek için
// EĞER alanının hangi dizeyi görüntülediğini belirleyen EĞER alanı, eşitlik için iki sayısal ifadeyi test edecektir.
// EĞER alanının içine yerleştireceğimiz iki ifadeyi formül alanları şeklinde sağlayacağız.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Sonra, EĞER alanı için doğru/yanlış çıktı dizeleri olarak hizmet edecek iki alan bağımsız değişkeni oluşturacağız.
// Bu argümanlar sayısal ifadelerimizin çıktı değerlerini yeniden kullanacak.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Son olarak, IF alanı için bir tane daha alan oluşturucu oluşturacağız ve tüm ifadeleri birleştireceğiz.
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

* class [Field](../../field/)
* class [Paragraph](../../../aspose.words/paragraph/)
* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
