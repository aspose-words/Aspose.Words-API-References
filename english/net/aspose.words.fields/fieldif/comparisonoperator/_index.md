---
title: FieldIf.ComparisonOperator
linktitle: ComparisonOperator
second_title: Aspose.Words for .NET API Reference
description: FieldIf ComparisonOperator property. Gets or sets the comparison operator in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldif/comparisonoperator/
---
## ComparisonOperator property

Gets or sets the comparison operator.

```csharp
public string ComparisonOperator { get; set; }
```

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

// This time the statement is correct, so the displayed result will be "True".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### See Also

* class [FieldIf](../)
* namespace [Aspose.Words.Fields](../../fieldif/)
* assembly [Aspose.Words](../../../)
