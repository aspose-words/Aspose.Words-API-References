---
title: FieldIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldIf ComparisonOperator, легко управляйте и настраивайте операторы сравнения для улучшенной обработки и анализа данных.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldif/comparisonoperator/
---
## FieldIf.ComparisonOperator property

Получает или задает оператор сравнения.

```csharp
public string ComparisonOperator { get; set; }
```

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

* class [FieldIf](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
