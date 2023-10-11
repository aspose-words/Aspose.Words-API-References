---
title: FieldBuilder.AddSwitch
second_title: Справочник по API Aspose.Words для .NET
description: FieldBuilder метод. Добавляет переключатель поля.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldbuilder/addswitch/
---
## AddSwitch(string) {#addswitch}

Добавляет переключатель поля.

```csharp
public FieldBuilder AddSwitch(string switchName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | String | Имя переключателя. |

### Примечания

Эта перегрузка добавляет флаг (переключатель без аргумента).

### Примеры

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

* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../fieldbuilder/)
* сборка [Aspose.Words](../../../)

---

## AddSwitch(string, string) {#addswitch_3}

Добавляет переключатель поля.

```csharp
public FieldBuilder AddSwitch(string switchName, string switchArgument)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | String | Имя переключателя. |
| switchArgument | String | Значение переключателя. |

### Примеры

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

* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../fieldbuilder/)
* сборка [Aspose.Words](../../../)

---

## AddSwitch(string, int) {#addswitch_2}

Добавляет переключатель поля.

```csharp
public FieldBuilder AddSwitch(string switchName, int switchArgument)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | String | Имя переключателя. |
| switchArgument | Int32 | Значение переключателя. |

### Примеры

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

* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../fieldbuilder/)
* сборка [Aspose.Words](../../../)

---

## AddSwitch(string, double) {#addswitch_1}

Добавляет переключатель поля.

```csharp
public FieldBuilder AddSwitch(string switchName, double switchArgument)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | String | Имя переключателя. |
| switchArgument | Double | Значение переключателя. |

### Примеры

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

* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../fieldbuilder/)
* сборка [Aspose.Words](../../../)


