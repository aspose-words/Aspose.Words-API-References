---
title: FieldKeywords Class
linktitle: FieldKeywords
articleTitle: FieldKeywords
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldKeywords class to efficiently implement the KEYWORDS field, enhancing your document's metadata and searchability.
type: docs
weight: 2490
url: /net/aspose.words.fields/fieldkeywords/
---
## FieldKeywords class

Implements the KEYWORDS field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldKeywords : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldKeywords](fieldkeywords/)() | The default constructor. |

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
| [Text](../../aspose.words.fields/fieldkeywords/text/) { get; set; } | Gets or sets the text of the keywords. |
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

Retrieves, and optionally sets, the document's keywords, as recorded in the **Keywords** property of the built-in document properties.

## Examples

Shows to insert a KEYWORDS field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add some keywords, also referred to as "tags" in File Explorer.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// The KEYWORDS field displays the value of this property.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" KEYWORDS "));
Assert.That(field.Result, Is.EqualTo("Keyword1, Keyword2"));

// Setting a value for the field's Text property,
// and then updating the field will also overwrite the corresponding built-in property with the new value.
field.Text = "OverridingKeyword";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" KEYWORDS  OverridingKeyword"));
Assert.That(field.Result, Is.EqualTo("OverridingKeyword"));
Assert.That(doc.BuiltInDocumentProperties.Keywords, Is.EqualTo("OverridingKeyword"));

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
