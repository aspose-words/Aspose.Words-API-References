---
title: AddArgument
second_title: Aspose.Words for .NET API Referansı
description: Bir alanın argümanını ekler.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldbuilder/addargument/
---
## AddArgument(string) {#addargument_4}

Bir alanın argümanını ekler.

```csharp
public FieldBuilder AddArgument(string argument)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| argument | String | Argüman değeri. |

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

* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

---

## AddArgument(int) {#addargument_3}

Bir alanın argümanını ekler.

```csharp
public FieldBuilder AddArgument(int argument)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| argument | Int32 | Argüman değeri. |

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

* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

---

## AddArgument(double) {#addargument_2}

Bir alanın argümanını ekler.

```csharp
public FieldBuilder AddArgument(double argument)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| argument | Double | Argüman değeri. |

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

* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

---

## AddArgument(FieldBuilder) {#addargument_1}

Bir başkası tarafından temsil edilen bir alt alan ekler[`FieldBuilder`](../) alanın koduna.

```csharp
public FieldBuilder AddArgument(FieldBuilder argument)
```

### Notlar

Bu aşırı yükleme, bağımsız değişken tek bir alt alandan oluştuğunda kullanılır.

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

* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

---

## AddArgument(FieldArgumentBuilder) {#addargument}

ile temsil edilen bir alanın argümanını ekler[`FieldArgumentBuilder`](../../fieldargumentbuilder/) alanın koduna.

```csharp
public FieldBuilder AddArgument(FieldArgumentBuilder argument)
```

### Notlar

Bu aşırı yükleme, bağımsız değişken alt alanlar, düğümler ve düz metin gibi farklı parçaların bir karışımından oluştuğunda kullanılır.

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

* class [FieldArgumentBuilder](../../fieldargumentbuilder/)
* class [FieldBuilder](../)
* ad alanı [Aspose.Words.Fields](../../fieldbuilder/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
