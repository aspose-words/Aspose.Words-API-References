---
title: FieldCompare.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words for .NET
description: Discover FieldCompare's RightExpression property to easily manage and customize the right side of your comparison expressions for optimal performance.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldcompare/rightexpression/
---
## FieldCompare.RightExpression property

Gets or sets the right part of the comparison expression.

```csharp
public string RightExpression { get; set; }
```

## Examples

Shows how to compare expressions using a COMPARE field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// The COMPARE field displays a "0" or a "1", depending on its statement's truth.
// The result of this statement is false so that this field will display a "0".
Assert.That(field.GetFieldCode(), Is.EqualTo(" COMPARE  3 < 2"));
Assert.That(field.Result, Is.EqualTo("0"));

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// This field displays a "1" since the statement is true.
Assert.That(field.GetFieldCode(), Is.EqualTo(" COMPARE  5 = \"2 + 3\""));
Assert.That(field.Result, Is.EqualTo("1"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### See Also

* class [FieldCompare](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
