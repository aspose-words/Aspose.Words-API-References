---
title: FieldIf.TrueText
linktitle: TrueText
articleTitle: TrueText
second_title: Aspose.Words for .NET
description: 发现 FieldIf TrueText 属性，轻松管理真实比较表达式的显示文本，增强用户体验和数据清晰度。
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldif/truetext/
---
## FieldIf.TrueText property

获取或设置比较表达式为真时显示的文本。

```csharp
public string TrueText { get; set; }
```

## 例子

显示如何插入 IF 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// IF 字段将显示来自其“TrueText”属性的字符串，
// 或其“FalseText”属性，取决于我们构建的语句的真实性。
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// 在这种情况下，“0 = 1”是不正确的，因此显示的结果将为“False”。
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

* class [FieldIf](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
