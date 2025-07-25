---
title: FieldComments Class
linktitle: FieldComments
articleTitle: FieldComments
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldComments class to efficiently implement and manage COMMENTS fields in your documents. Enhance your document processing today!
type: docs
weight: 2100
url: /net/aspose.words.fields/fieldcomments/
---
## FieldComments class

Implements the COMMENTS field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldComments : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldComments](fieldcomments/)() | The default constructor. |

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
| [Text](../../aspose.words.fields/fieldcomments/text/) { get; set; } | Gets or sets the text of the comments. |
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

Retrieves, and optionally sets, the comments relating to the current document, as recorded in the [`Comments`](../../aspose.words.properties/builtindocumentproperties/comments/) property of the built-in document properties.

## Examples

Shows how to use the COMMENTS field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set a value for the document's "Comments" built-in property.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Create a COMMENTS field to display the value of that built-in property.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" COMMENTS "));
Assert.That(field.Result, Is.EqualTo("My comment."));

// If we give the COMMENTS field's Text property value and update it, the field will
// overwrite the current value of the "Comments" built-in property with the value of its Text property,
// and then display the new value.
field.Text = "My overriding comment.";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" COMMENTS  \"My overriding comment.\""));
Assert.That(field.Result, Is.EqualTo("My overriding comment."));

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
