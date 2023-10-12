---
title: Enum FieldIfComparisonResult
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldIfComparisonResult 枚举. 指定 IF 字段条件评估的结果
type: docs
weight: 2010
url: /zh/net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

指定 IF 字段条件评估的结果。

```csharp
public enum FieldIfComparisonResult
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Error | `0` | 条件有错误。 |
| True | `1` | 条件是`真的`. |
| False | `2` | 条件是`错误的`. |

### 例子

演示如何插入 IF 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// IF 字段将显示来自其“TrueText”属性的字符串，
// 或其“FalseText”属性，具体取决于我们构建的语句的真实性。
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// 在这种情况下，“0 = 1”不正确，因此显示的结果将为“False”。
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

// 这次语句是正确的，所以显示的结果将是“True”。
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


