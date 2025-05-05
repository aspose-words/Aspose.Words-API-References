---
title: FieldAddIn Class
linktitle: FieldAddIn
articleTitle: FieldAddIn
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldAddIn class to enhance document automation with powerful ADDIN field capabilities. Boost your productivity today!
type: docs
weight: 1930
url: /net/aspose.words.fields/fieldaddin/
---
## FieldAddIn class

Implements the ADDIN field.

```csharp
public class FieldAddIn : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldAddIn](fieldaddin/)() | The default constructor. |

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

Contains data created by an add-in.

## Examples

Shows how to process an ADDIN field.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDIN.docx");

// Aspose.Words does not support inserting ADDIN fields, but we can still load and read them.
FieldAddIn field = (FieldAddIn)doc.Range.Fields[0];

Assert.AreEqual(" ADDIN \"My value\" ", field.GetFieldCode());
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
