---
title: FieldCompare Class
linktitle: FieldCompare
articleTitle: FieldCompare
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldCompare class for effortless document comparison. Enhance your workflow with powerful, accurate field functionalities.
type: docs
weight: 2110
url: /net/aspose.words.fields/fieldcompare/
---
## FieldCompare class

Implements the COMPARE field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldCompare : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldCompare](fieldcompare/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldcompare/comparisonoperator/) { get; set; } | Gets or sets the comparison operator. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LeftExpression](../../aspose.words.fields/fieldcompare/leftexpression/) { get; set; } | Gets or sets the left part of the comparison expression. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [RightExpression](../../aspose.words.fields/fieldcompare/rightexpression/) { get; set; } | Gets or sets the right part of the comparison expression. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Compares the values designated by the expressions [`LeftExpression`](./leftexpression/) and [`RightExpression`](./rightexpression/) in comparison using the operator designated by [`ComparisonOperator`](./comparisonoperator/).

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

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
