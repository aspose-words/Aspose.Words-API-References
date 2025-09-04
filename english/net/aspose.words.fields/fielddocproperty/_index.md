---
title: FieldDocProperty Class
linktitle: FieldDocProperty
articleTitle: FieldDocProperty
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldDocProperty class, designed for seamless integration of DOCPROPERTY fields in your documents for enhanced functionality.
type: docs
weight: 2210
url: /net/aspose.words.fields/fielddocproperty/
---
## FieldDocProperty class

Implements the DOCPROPERTY field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldDocProperty : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldDocProperty](fielddocproperty/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| virtual [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Retrieves the indicated document information.

## Examples

Shows how to use DOCPROPERTY fields to display document properties and variables.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways of using DOCPROPERTY fields.
// 1 -  Display a built-in property:
// Set a custom value for the "Category" built-in property, then insert a DOCPROPERTY field that references it.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.That(fieldDocProperty.GetFieldCode(), Is.EqualTo(" DOCPROPERTY Category "));
Assert.That(fieldDocProperty.Result, Is.EqualTo("My category"));

builder.InsertParagraph();

// 2 -  Display a custom document variable:
// Define a custom variable, then reference that variable with a DOCPROPERTY field.
Assert.That(doc.Variables.Count, Is.EqualTo(0));
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.That(fieldDocVariable.GetFieldCode(), Is.EqualTo(" DOCVARIABLE  \"My Variable\""));
Assert.That(fieldDocVariable.Result, Is.EqualTo("My variable's value"));

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
