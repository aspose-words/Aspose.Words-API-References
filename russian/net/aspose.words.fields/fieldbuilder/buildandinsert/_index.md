---
title: FieldBuilder.BuildAndInsert
linktitle: BuildAndInsert
articleTitle: BuildAndInsert
second_title: Aspose.Words для .NET
description: FieldBuilder BuildAndInsert метод. Создает и вставляет поле в документ перед указанным встроенным узлом на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldbuilder/buildandinsert/
---
## BuildAndInsert(*[Inline](../../../aspose.words/inline/)*) {#buildandinsert}

Создает и вставляет поле в документ перед указанным встроенным узлом.

```csharp
public Field BuildAndInsert(Inline refNode)
```

### Возвращаемое значение

А[`Field`](../../field/) объект, представляющий вставленное поле.

## Примеры

Показывает, как создать и вставить поле с помощью построителя полей.

```csharp
Document doc = new Document();

// Удобный способ добавления текстового содержимого в документ — использование конструктора документов.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// У полей есть свой конструктор, который мы можем использовать для построения кода поля по частям.
// В этом случае мы создадим поле BARCODE, представляющее почтовый индекс США,
// и затем вставляем его перед Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Смотрите также

* class [Field](../../field/)
* class [Inline](../../../aspose.words/inline/)
* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)

---

## BuildAndInsert(*[Paragraph](../../../aspose.words/paragraph/)*) {#buildandinsert_1}

Создает и вставляет поле в документ до конца указанного абзаца.

```csharp
public Field BuildAndInsert(Paragraph refNode)
```

### Возвращаемое значение

А[`Field`](../../field/) объект, представляющий вставленное поле.

## Примеры

Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.

```csharp
Document doc = new Document();

// Ниже приведены три примера построения полей, выполненные с помощью построителя полей.
// 1 - Одно поле:
// Используйте конструктор полей, чтобы добавить поле СИМВОЛ, в котором отображается символ ƒ (флорин).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Вложенное поле:
// Используйте построитель полей для создания поля формулы, используемого в качестве внутреннего поля другим построителем полей.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Создаем еще один построитель для другого поля СИМВОЛ и вставляем поле формулы
 // который мы создали выше, в поле СИМВОЛ в качестве аргумента.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Внешнее поле СИМВОЛ будет использовать результат поля формулы, 174, в качестве аргумента,
// что приведет к тому, что в поле будет отображаться символ ® (зарегистрированный знак), поскольку его номер символа равен 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 — Несколько вложенных полей и аргументов:
// Теперь мы воспользуемся конструктором для создания поля IF, которое отображает одно из двух пользовательских строковых значений:
// в зависимости от истинного/ложного значения его выражения. Чтобы получить истинное/ложное значение
// который определяет, какую строку отображает поле IF, поле IF будет проверять два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые мы вложим в поле ЕСЛИ.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Далее мы создадим два аргумента поля, которые будут служить строками вывода true/false для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Наконец, мы создадим еще один построитель полей для поля ЕСЛИ и объединим все выражения.
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

### Смотрите также

* class [Field](../../field/)
* class [Paragraph](../../../aspose.words/paragraph/)
* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
