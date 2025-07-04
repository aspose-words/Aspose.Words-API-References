---
title: FieldIfComparisonResult Enum
linktitle: FieldIfComparisonResult
articleTitle: FieldIfComparisonResult
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldIfComparisonResult enum, which defines outcomes of IF field evaluations, enhancing your document automation capabilities.
type: docs
weight: 2410
url: /net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

Specifies the result of the IF field condition evaluation.

```csharp
public enum FieldIfComparisonResult
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Error | `0` | There is an error in the condition. |
| True | `1` | The condition is `true`. |
| False | `2` | The condition is `false`. |

## Examples

Shows how to insert an IF field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// The IF field will display a string from either its "TrueText" property,
// or its "FalseText" property, depending on the truth of the statement that we have constructed.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// In this case, "0 = 1" is incorrect, so the displayed result will be "False".
Assert.That(field.GetFieldCode(), Is.EqualTo(" IF  0 = 1 True False"));
Assert.That(field.EvaluateCondition(), Is.EqualTo(FieldIfComparisonResult.False));
Assert.That(field.Result, Is.EqualTo("False"));

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// This time the statement is correct, so the displayed result will be "True".
Assert.That(field.GetFieldCode(), Is.EqualTo(" IF  5 = \"2 + 3\" True False"));
Assert.That(field.EvaluateCondition(), Is.EqualTo(FieldIfComparisonResult.True));
Assert.That(field.Result, Is.EqualTo("True"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
