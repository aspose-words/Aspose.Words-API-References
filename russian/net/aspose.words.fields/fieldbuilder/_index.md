---
title: FieldBuilder
second_title: Справочник по API Aspose.Words для .NET
description: Создает поле из токенов кода поля аргументы и переключатели.
type: docs
weight: 1510
url: /ru/net/aspose.words.fields/fieldbuilder/
---
## FieldBuilder class

Создает поле из токенов кода поля (аргументы и переключатели).

```csharp
public class FieldBuilder
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldBuilder](fieldbuilder/)(FieldType) | Инициализирует экземпляр[`FieldBuilder`](./fieldbuilder/) класс. |

## Методы

| Имя | Описание |
| --- | --- |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_2)(double) | Добавляет аргумент поля. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument)(FieldArgumentBuilder) | Добавляет аргумент поля, представленный[`FieldArgumentBuilder`](../fieldargumentbuilder/) к коду поля. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_1)(FieldBuilder) | Добавляет дочернее поле, представленное другим[`FieldBuilder`](./fieldbuilder/) к коду поля. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_3)(int) | Добавляет аргумент поля. |
| [AddArgument](../../aspose.words.fields/fieldbuilder/addargument/#addargument_4)(string) | Добавляет аргумент поля. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch)(string) | Добавляет переключатель поля. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_1)(string, double) | Добавляет переключатель поля. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_2)(string, int) | Добавляет переключатель поля. |
| [AddSwitch](../../aspose.words.fields/fieldbuilder/addswitch/#addswitch_3)(string, string) | Добавляет переключатель поля. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert)(Inline) | Создает и вставляет поле в документ перед указанным встроенным узлом. |
| [BuildAndInsert](../../aspose.words.fields/fieldbuilder/buildandinsert/#buildandinsert_1)(Paragraph) | Создает и вставляет поле в документ до конца указанного абзаца. |

### Примеры

Показывает, как создавать поля с помощью построителя полей, а затем вставлять их в документ.

```csharp
Document doc = new Document();

// Ниже приведены три примера построения поля с помощью конструктора полей.
// 1 - Одно поле:
// Используйте конструктор полей, чтобы добавить поле СИМВОЛ, которое отображает символ ƒ (флорин).
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
 // который мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве аргумента,
// что заставит поле отображать символ ® (зарегистрированный знак), так как его число символов равно 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - Несколько вложенных полей и аргументов:
// Теперь мы будем использовать построитель для создания поля ЕСЛИ, которое отображает одно из двух пользовательских строковых значений,
// в зависимости от истинного/ложного значения его выражения. Чтобы получить истинное/ложное значение
// который определяет, какую строку отображает поле ЕСЛИ, поле ЕСЛИ будет проверять два числовых выражения на равенство.
// Мы предоставим два выражения в виде полей формулы, которые мы вложим в поле ЕСЛИ.
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

 // Наконец, мы создадим еще один построитель поля для поля ЕСЛИ и объединим все выражения.
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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
