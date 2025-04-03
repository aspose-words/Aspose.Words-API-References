---
title: DocumentBuilder.insertField method
linktitle: insertField method
articleTitle: insertField method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertField method"
type: docs
weight: 330
url: /nodejs-net/aspose.words/documentbuilder/insertField/
---

## insertField(fieldType, updateField) {#fieldtype_boolean}

Inserts a Word field into a document and optionally updates the field result.


```js
insertField(fieldType: Aspose.Words.Fields.FieldType, updateField: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | [FieldType](../../../aspose.words.fields/fieldtype/) | The type of the field to append. |
| updateField | boolean | Specifies whether to update the field immediately. |

### Remarks

This method inserts a field into a document.
Aspose.Words can update fields of most types, but not all. For more details see the
[DocumentBuilder.insertField()](./#string_string) overload.




### Returns

A [Field](../../field/) object that represents the inserted field.


## insertField(fieldCode) {#string}

Inserts a Word field into a document and updates the field result.


```js
insertField(fieldCode: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to insert (without curly braces). |

### Remarks

This method inserts a field into a document and updates the field result immediately.
Aspose.Words can update fields of most types, but not all. For more details see the
[DocumentBuilder.insertField()](./#string_string) overload.




### Returns

A [Field](../../field/) object that represents the inserted field.


## insertField(fieldCode, fieldValue) {#string_string}

Inserts a Word field into a document without updating the field result.


```js
insertField(fieldCode: string, fieldValue: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to insert (without curly braces). |
| fieldValue | string | The field value to insert. Pass ``null`` for fields that do not have a value. |

### Remarks

Fields in Microsoft Word documents consist of a field code and a field result.
The field code is like a formula and the field result is like the value that
the formula produces. The field code may also contain field switches
that are like additional instructions to perform a specific action.

You can switch between displaying field codes and results in your document in
Microsoft Word using the keyboard shortcut Alt+F9. Field codes appear between curly braces ( { } ).

To create a field, you need to specify a field type, field code and a "placeholder" field value.
If you are not sure about a particular field code syntax, create the field in Microsoft Word first
and switch to see its field code.

Aspose.Words can calculate field results for most of the field types, but this method
does not update the field result automatically. Because the field result is not calculated automatically,
you are expected to pass some string value (or even an empty string) that will be inserted into the field result.
This value will remain in the field result as a placeholder until the field is updated.
To update the field result you can call [Field.update()](../../field/update/#default) on the field object returned
to you or [Document.updateFields()](../../document/updateFields/#default) to update fields in the whole document.




### Returns

A [Field](../../field/) object that represents the inserted field.


## Examples

Shows how to insert a field into a document using FieldType.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
// In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
doc.builtInDocumentProperties.author = "John Doe";
builder.write("This document was written by ");
builder.insertField(aw.Fields.FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.insertParagraph();
builder.write("\nThis is page ");
builder.insertField(aw.Fields.FieldType.FieldPage, updateInsertedFieldsImmediately);

expect(doc.range.fields.at(0).getFieldCode()).toEqual(" AUTHOR ");
expect(doc.range.fields.at(1).getFieldCode()).toEqual(" PAGE ");

if (updateInsertedFieldsImmediately)
{
  expect(doc.range.fields.at(0).result).toEqual("John Doe");
  expect(doc.range.fields.at(1).result).toEqual("1");
}
else
{
  expect(doc.range.fields.at(0).result).toEqual('');
  expect(doc.range.fields.at(1).result).toEqual('');

  // We will need to update these fields using the update methods manually.
  doc.range.fields.at(0).update();

  expect(doc.range.fields.at(0).result).toEqual("John Doe");

  doc.updateFields();

  expect(doc.range.fields.at(1).result).toEqual("1");
}
```

Shows how to insert fields, and move the document builder's cursor to them.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertField("MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.insertField("MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Move the cursor to the first MERGEFIELD.
builder.moveToMergeField("MyMergeField1", true, false);

// Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
expect(builder.currentNode).toEqual(doc.range.fields.at(1).start);
expect(builder.currentNode.previousSibling).toEqual(doc.range.fields.at(0).end);

// If we wish to edit the field's field code or contents using the builder,
// its cursor would need to be inside a field.
// To place it inside a field, we would need to call the document builder's MoveTo method
// and pass the field's start or separator node as an argument.
builder.write(" Text between our merge fields. ");

doc.save(base.artifactsDir + "DocumentBuilder.MergeFields.docx");
```

Shows how to insert a field into a document using a field code.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let field = builder.insertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

expect(field.type).toEqual(aw.Fields.FieldType.FieldDate);
expect(field.getFieldCode()).toEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"");

// This overload of the InsertField method automatically updates inserted fields.
expect((Date.now() - Date.parse(field.result)) / 86400000).toBeLessThanOrEqual(1);
```

Shows how to set up page numbering in a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Section 1, page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 1, page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 1, page 3.");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.writeln("Section 2, page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 2, page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 2, page 3.");

// Move the document builder to the first section's primary header,
// which every page in that section will display.
builder.moveToSection(0);
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);

// Insert a PAGE field, which will display the number of the current page.
builder.write("Page ");
builder.insertField("PAGE", "");

// Configure the section to have the page count that PAGE fields display start from 5.
// Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.restartPageNumbering = true;
pageSetup.pageStartingNumber = 5;
pageSetup.pageNumberStyle = aw.NumberStyle.UppercaseRoman;

// Create another primary header for the second section, with another PAGE field.
builder.moveToSection(1);
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
builder.write(" - ");
builder.insertField("PAGE", "");
builder.write(" - ");

// Configure the section to have the page count that PAGE fields display start from 10.
// Also, configure all PAGE fields to display their page numbers using Arabic numbers.
pageSetup = doc.sections.at(1).pageSetup;
pageSetup.pageStartingNumber = 10;
pageSetup.restartPageNumbering = true;
pageSetup.pageNumberStyle = aw.NumberStyle.Arabic;

doc.save(base.artifactsDir + "PageSetup.PageNumbering.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)
* class [Field](../../field/)

