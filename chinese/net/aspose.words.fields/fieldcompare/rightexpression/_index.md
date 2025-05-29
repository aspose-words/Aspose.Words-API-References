---
title: FieldCompare.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words for .NET
description: 探索 FieldCompare 的 RightExpression 属性，轻松管理和自定义比较表达式的右侧，以获得最佳性能。
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldcompare/rightexpression/
---
## FieldCompare.RightExpression property

获取或设置比较表达式的正确部分。

```csharp
public string RightExpression { get; set; }
```

## 例子

展示如何使用 COMPARE 字段比较表达式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// COMPARE 字段显示“0”或“1”，取决于其语句的真实性。
// 该语句的结果为假，因此该字段将显示“0”。
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// 由于该语句为真，因此该字段显示“1”。
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### 也可以看看

* class [FieldCompare](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
