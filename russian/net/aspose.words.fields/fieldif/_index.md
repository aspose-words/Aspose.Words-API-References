---
title: FieldIf Class
linktitle: FieldIf
articleTitle: FieldIf
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldIf — эффективно реализуйте поля IF для улучшения автоматизации документов и оптимизации рабочего процесса.
type: docs
weight: 2410
url: /ru/net/aspose.words.fields/fieldif/
---
## FieldIf class

Реализует поле IF.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldIf : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldIf](fieldif/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | Получает или задает оператор сравнения. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | Возвращает или задает текст, отображаемый, если выражение сравнения равно`ЛОЖЬ` . |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | Возвращает или задает левую часть выражения сравнения. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | Возвращает или задает правую часть выражения сравнения. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | Возвращает или задает текст, отображаемый, если выражение сравнения истинно. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | Оценивает условие. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Сравнивает значения, обозначенные выражениями[`LeftExpression`](./leftexpression/) и[`RightExpression`](./rightexpression/) в сравнении с использованием оператора, обозначенного[`ComparisonOperator`](./comparisonoperator/).

В качестве источника слияния почты будет использоваться поле в следующем формате: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Примеры

Показывает, как вставить поле IF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Поле IF отобразит строку либо из своего свойства "TrueText",
// или его свойство "FalseText", в зависимости от истинности построенного нами утверждения.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// В этом случае «0 = 1» неверно, поэтому отображаемый результат будет «Ложь».
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

// На этот раз утверждение верно, поэтому отображаемый результат будет «True».
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
