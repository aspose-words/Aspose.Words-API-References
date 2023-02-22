---
title: FieldAutoNum Class
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Fields.FieldAutoNum class. Implements the AUTONUM field in C#.
type: docs
weight: 1430
url: /net/aspose.words.fields/fieldautonum/
---
## FieldAutoNum class

Implements the AUTONUM field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldAutoNum : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldAutoNum](fieldautonum/)() | The default constructor. |

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
| [SeparatorCharacter](../../aspose.words.fields/fieldautonum/separatorcharacter/) { get; set; } | Gets or sets the separator character to be used. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Inserts an automatic number.

## Examples

Shows how to number paragraphs using autonum fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Each AUTONUM field displays the current value of a running count of AUTONUM fields,
// allowing us to automatically number items like a numbered list.
// This field will display a number "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// The separator character, which appears in the field result immediately after the number,is a full stop by default.
// If we leave this property null, our second AUTONUM field will display "2." in the document.
Assert.IsNull(field.SeparatorCharacter);

// We can set this property to apply the first character of its string as the new separator character.
// In this case, our AUTONUM field will now display "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
