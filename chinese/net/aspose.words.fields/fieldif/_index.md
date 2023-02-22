---
title: Class FieldIf
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldIf 班级. 实现 IF 字段
type: docs
weight: 1850
url: /zh/net/aspose.words.fields/fieldif/
---
## FieldIf class

实现 IF 字段。

```csharp
public class FieldIf : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldIf](fieldif/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | 获取或设置比较运算符。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段end的节点。 |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | 获取或设置比较表达式为假时显示的文本。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 得到一个[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | 获取或设置比较表达式的左边部分。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | 获取或设置比较表达式的右边部分。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | 获取或设置比较表达式为真时显示的文本。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | 评估条件。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回 **无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update/)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

比较表达式指定的值[`LeftExpression`](./leftexpression/)和[`RightExpression`](./rightexpression/) 使用指定的运算符进行比较[`ComparisonOperator`](./comparisonoperator/).

以下格式的字段将用作邮件合并源： { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

### 例子

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
// 或它的“FalseText”属性，取决于我们构造的语句的真实性。
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// 在这种情况下，“0 = 1”是不正确的，所以显示的结果将是“False”。
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

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


