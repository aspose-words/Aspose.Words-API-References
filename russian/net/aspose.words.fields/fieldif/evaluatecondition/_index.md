---
title: FieldIf.EvaluateCondition
second_title: Справочник по API Aspose.Words для .NET
description: FieldIf метод. Оценивает условие.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf.EvaluateCondition method

Оценивает условие.

```csharp
public FieldIfComparisonResult EvaluateCondition()
```

### Возвращаемое значение

А[`FieldIfComparisonResult`](../../fieldifcomparisonresult/) значение, представляющее результат оценки условия.

### Примеры

Показывает, как вставить поле ЕСЛИ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Поле ЕСЛИ будет отображать строку либо из его свойства "TrueText",
// или его свойство "FalseText", в зависимости от истинности построенного нами утверждения.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// В этом случае "0 = 1" неверно, поэтому отображаемый результат будет "False".
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

// На этот раз утверждение верно, поэтому отображаемый результат будет «Истина».
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Смотрите также

* enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* class [FieldIf](../)
* пространство имен [Aspose.Words.Fields](../../fieldif/)
* сборка [Aspose.Words](../../../)


