---
title: FieldArgumentBuilder
linktitle: FieldArgumentBuilder
articleTitle: FieldArgumentBuilder
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор FieldArgumentBuilder для эффективного создания и настройки экземпляров FieldArgumentBuilder для нужд вашей разработки.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/fieldargumentbuilder/fieldargumentbuilder/
---
## FieldArgumentBuilder constructor

Инициализирует экземпляр[`FieldArgumentBuilder`](../) класс.

```csharp
public FieldArgumentBuilder()
```

## Примеры

Показывает, как создавать поля с помощью конструктора полей, а затем вставлять их в документ.

```csharp
Document doc = new Document();

// Ниже приведены три примера построения поля, выполненного с помощью конструктора полей.
// 1 - Одно поле:
// Используйте конструктор полей, чтобы добавить поле SYMBOL, отображающее символ ƒ (флорин).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - Вложенное поле:
// Используйте конструктор полей для создания поля формулы, используемого в качестве внутреннего поля другим конструктором полей.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// Создаем еще один конструктор для другого поля SYMBOL и вставляем поле формулы
 // который мы создали выше, в поле SYMBOL в качестве аргумента.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
// что заставит поле отображать символ ® (зарегистрированный знак), поскольку его номер символа равен 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Несколько вложенных полей и аргументов:
// Теперь мы воспользуемся конструктором для создания поля IF, которое отображает одно из двух пользовательских строковых значений,
// в зависимости от истинного/ложного значения его выражения. Чтобы получить истинное/ложное значение
// который определяет, какую строку отображает поле IF, поле IF будет проверять два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формул, которые мы вложим в поле IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// Далее мы создадим два аргумента поля, которые будут служить выходными строками true/false для поля IF.
// Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // Наконец, мы создадим еще один конструктор полей для поля IF и объединим все выражения.
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

* class [FieldArgumentBuilder](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
