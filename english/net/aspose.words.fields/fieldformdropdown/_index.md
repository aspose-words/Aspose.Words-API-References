---
title: FieldFormDropDown Class
linktitle: FieldFormDropDown
articleTitle: FieldFormDropDown
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldFormDropDown class, designed to enhance document interactivity with dynamic dropdown fields for seamless user experiences.
type: docs
weight: 2320
url: /net/aspose.words.fields/fieldformdropdown/
---
## FieldFormDropDown class

Implements the FORMDROPDOWN field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldFormDropDown : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldFormDropDown](fieldformdropdown/)() | The default constructor. |

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
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Inserts a drop-down list style form field.

## Examples

Shows how to process FORMCHECKBOX, FORMDROPDOWN and FORMTEXT fields.

```csharp
// These fields are legacy equivalents of the FormField. We can read, but not create these fields using Aspose.Words.
// In Microsoft Word, we can insert these fields via the Legacy Tools menu in the Developer tab.
Document doc = new Document(MyDir + "Form fields.docx");

FieldFormCheckBox fieldFormCheckBox = (FieldFormCheckBox)doc.Range.Fields[1];
Assert.That(fieldFormCheckBox.GetFieldCode(), Is.EqualTo(" FORMCHECKBOX \u0001"));

FieldFormDropDown fieldFormDropDown = (FieldFormDropDown)doc.Range.Fields[2];
Assert.That(fieldFormDropDown.GetFieldCode(), Is.EqualTo(" FORMDROPDOWN \u0001"));

FieldFormText fieldFormText = (FieldFormText)doc.Range.Fields[0];
Assert.That(fieldFormText.GetFieldCode(), Is.EqualTo(" FORMTEXT \u0001"));
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
