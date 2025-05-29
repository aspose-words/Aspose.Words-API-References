---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldCompare LeftExpression, легко получайте доступ или изменяйте левую часть выражений сравнения для расширенного анализа данных.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

Возвращает или задает левую часть выражения сравнения.

```csharp
public string LeftExpression { get; set; }
```

## Примеры

Показывает, как сравнивать выражения с помощью поля COMPARE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// Поле COMPARE отображает «0» или «1» в зависимости от истинности утверждения.
// Результат этого оператора — false, поэтому в этом поле будет отображаться «0».
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// В этом поле отображается «1», поскольку утверждение истинно.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Смотрите также

* class [FieldCompare](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
