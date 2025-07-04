---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words for .NET
description: Enhance your documents with DocumentBuilder's InsertField method. Effortlessly add and update Word fields for dynamic content and improved functionality.
type: docs
weight: 330
url: /net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Inserts a Word field into a document and optionally updates the field result.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | FieldType | The type of the field to append. |
| updateField | Boolean | Specifies whether to update the field immediately. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the inserted field.

## Remarks

This method inserts a field into a document. Aspose.Words can update fields of most types, but not all. For more details see the `InsertField` overload.

## Examples

Shows how to insert a field into a document using FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
// In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.That(doc.Range.Fields[0].GetFieldCode(), Is.EqualTo(" AUTHOR "));
Assert.That(doc.Range.Fields[1].GetFieldCode(), Is.EqualTo(" PAGE "));

if (updateInsertedFieldsImmediately)
{
    Assert.That(doc.Range.Fields[0].Result, Is.EqualTo("John Doe"));
    Assert.That(doc.Range.Fields[1].Result, Is.EqualTo("1"));
}
else
{
    Assert.That(doc.Range.Fields[0].Result, Is.EqualTo(string.Empty));
    Assert.That(doc.Range.Fields[1].Result, Is.EqualTo(string.Empty));

    // We will need to update these fields using the update methods manually.
    doc.Range.Fields[0].Update();

    Assert.That(doc.Range.Fields[0].Result, Is.EqualTo("John Doe"));

    doc.UpdateFields();

    Assert.That(doc.Range.Fields[1].Result, Is.EqualTo("1"));
}
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Inserts a Word field into a document and updates the field result.

```csharp
public Field InsertField(string fieldCode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | String | The field code to insert (without curly braces). |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the inserted field.

## Remarks

This method inserts a field into a document and updates the field result immediately. Aspose.Words can update fields of most types, but not all. For more details see the `InsertField` overload.

## Examples

Shows how to insert a field into a document using a field code.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.That(field.Type, Is.EqualTo(FieldType.FieldDate));
Assert.That(field.GetFieldCode(), Is.EqualTo("DATE \\@ \"dddd, MMMM dd, yyyy\""));

// This overload of the InsertField method automatically updates inserted fields.
Assert.That((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1, Is.True);
```

Shows how to insert fields, and move the document builder's cursor to them.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Move the cursor to the first MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
Assert.That(builder.CurrentNode, Is.EqualTo(doc.Range.Fields[1].Start));
Assert.That(builder.CurrentNode.PreviousSibling, Is.EqualTo(doc.Range.Fields[0].End));

// If we wish to edit the field's field code or contents using the builder,
// its cursor would need to be inside a field.
// To place it inside a field, we would need to call the document builder's MoveTo method
// and pass the field's start or separator node as an argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Inserts a Word field into a document without updating the field result.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | String | The field code to insert (without curly braces). |
| fieldValue | String | The field value to insert. Pass `null` for fields that do not have a value. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the inserted field.

## Remarks

Fields in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

You can switch between displaying field codes and results in your document in Microsoft Word using the keyboard shortcut Alt+F9. Field codes appear between curly braces ( { } ).

To create a field, you need to specify a field type, field code and a "placeholder" field value. If you are not sure about a particular field code syntax, create the field in Microsoft Word first and switch to see its field code.

Aspose.Words can calculate field results for most of the field types, but this method does not update the field result automatically. Because the field result is not calculated automatically, you are expected to pass some string value (or even an empty string) that will be inserted into the field result. This value will remain in the field result as a placeholder until the field is updated. To update the field result you can call [`Update`](../../../aspose.words.fields/field/update/) on the field object returned to you or [`UpdateFields`](../../document/updatefields/) to update fields in the whole document.

## Examples

Shows how to set up page numbering in a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Move the document builder to the first section's primary header,
// which every page in that section will display.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Insert a PAGE field, which will display the number of the current page.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configure the section to have the page count that PAGE fields display start from 5.
// Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Create another primary header for the second section, with another PAGE field.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configure the section to have the page count that PAGE fields display start from 10.
// Also, configure all PAGE fields to display their page numbers using Arabic numbers.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
