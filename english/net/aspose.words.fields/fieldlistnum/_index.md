---
title: Class FieldListNum
second_title: Aspose.Words for .NET API Reference
description: Implements the LISTNUM field.
type: docs
weight: 1970
url: /net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Implements the LISTNUM field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldListNum : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Gets or sets the level in the list, overriding the default behavior of the field. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Gets or sets the name of the abstract numbering definition used for the numbering. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Gets or sets the starting value for this field. |
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

## Examples

Shows how to number paragraphs with LISTNUM fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM fields display a number that increments at each LISTNUM field.
// These fields also have a variety of options that allow us to use them to emulate numbered lists.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Lists start counting at 1 by default, but we can set this number to a different value, such as 0.
// This field will display "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// LISTNUM fields maintain separate counts for each list level. 
// Inserting a LISTNUM field in the same paragraph as another LISTNUM field
// increases the list level instead of the count.
// The next field will continue the count we started above and display a value of "1" at list level 1.
builder.InsertField(FieldType.FieldListNum, true);

// This field will start a count at list level 2. It will display a value of "1".
builder.InsertField(FieldType.FieldListNum, true);

// This field will start a count at list level 3. It will display a value of "1".
// Different list levels have different formatting,
// so these fields combined will display a value of "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// The next LISTNUM field that we insert will continue the count at the list level
// that the previous LISTNUM field was on.
// We can use the "ListLevel" property to jump to a different list level.
// If this LISTNUM field stayed on list level 3, it would display "ii)",
// but, since we have moved it to list level 2, it carries on the count at that level and displays "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// We can set the ListName property to get the field to emulate a different AUTONUM field type.
// "NumberDefault" emulates AUTONUM, "OutlineDefault" emulates AUTONUMOUT,
// and "LegalDefault" emulates AUTONUMLGL fields.
// The "OutlineDefault" list name with 1 as the starting number will result in displaying "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// The ListName does not carry over from the previous field, so we will need to set it for each new field.
// This field continues the count with the different list name and displays "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
