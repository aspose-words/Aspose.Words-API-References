---
title: Field class
linktitle: Field class
articleTitle: Field class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Field class. Represents a Microsoft Word document field"
type: docs
weight: 420
url: /nodejs-net/aspose.words/field/
---

## Field class

Represents a Microsoft Word document field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Remarks

A field in a Word document is a complex structure consisting of multiple nodes that include field start,
field code, field separator, field result and field end. Fields can be nested, contain rich content and span
multiple paragraphs or sections in a document. The [Field](./) class is a "facade" object that provides
properties and methods that allow to work with a field as a single object. 

The [Field.start](./start/), [Field.separator](./separator/) and [Field.end](./end/) properties point to the
field start, separator and end nodes of the field respectively.

The content between the field start and separator is the field code. The content between the
field separator and field end is the field result. The field code typically consists of one or more
[Run](../run/) objects that specify instructions. The processing application is expected to execute
the field code to calculate the field result.

The process of calculating field results is called the field update. Aspose.Words can update field
results of most of the field types in exactly the same way as Microsoft Word does it. Most notably,
Aspose.Words can calculate results of even the most complex formula fields. To calculate the field
result of a single field use the [Field.update()](./update/#default) method. To update fields in the whole document
use [Document.updateFields()](../document/updateFields/#default).

You can get the plain text version of the field code using the [Field.getFieldCode()](./getFieldCode/#boolean) method.
You can get and set the plain text version of the field result using the [Field.result](./result/) property.
Both the field code and field result can contain complex content, such as nested fields, paragraphs, shapes,
tables and in this case you might want to work with the field nodes directly if you need more control.

You do not create instances of the [Field](./) class directly.
To create a new field use the [DocumentBuilder.insertField()](../documentbuilder/insertField/#string) method.




### Properties

| Name | Description |
| --- | --- |
| [displayResult](./displayResult/) | Gets the text that represents the displayed field result. |
| [end](./end/) | Gets the node that represents the field end. |
| [format](./format/) | Gets a [FieldFormat](../../aspose.words.fields/fieldformat/) object that provides typed access to field's formatting. |
| [isDirty](./isDirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked](./isLocked/) | Gets or sets whether the field is locked (should not recalculate its result). |
| [localeId](./localeId/) | Gets or sets the LCID of the field. |
| [result](./result/) | Gets or sets text that is between the field separator and field end. |
| [separator](./separator/) | Gets the node that represents the field separator. Can be ``null``. |
| [start](./start/) | Gets the node that represents the start of the field. |
| [type](./type/) | Gets the Microsoft Word field type. |

### Methods

| Name | Description |
| --- | --- |
|[ asField()](./asField/#default) |  |
|[ asFieldAddIn()](./asFieldAddIn/#default) |  |
|[ asFieldAddressBlock()](./asFieldAddressBlock/#default) |  |
|[ asFieldAdvance()](./asFieldAdvance/#default) |  |
|[ asFieldAsk()](./asFieldAsk/#default) |  |
|[ asFieldAuthor()](./asFieldAuthor/#default) |  |
|[ asFieldAutoNum()](./asFieldAutoNum/#default) |  |
|[ asFieldAutoNumLgl()](./asFieldAutoNumLgl/#default) |  |
|[ asFieldAutoNumOut()](./asFieldAutoNumOut/#default) |  |
|[ asFieldAutoText()](./asFieldAutoText/#default) |  |
|[ asFieldAutoTextList()](./asFieldAutoTextList/#default) |  |
|[ asFieldBarcode()](./asFieldBarcode/#default) |  |
|[ asFieldBibliography()](./asFieldBibliography/#default) |  |
|[ asFieldBidiOutline()](./asFieldBidiOutline/#default) |  |
|[ asFieldCitation()](./asFieldCitation/#default) |  |
|[ asFieldComments()](./asFieldComments/#default) |  |
|[ asFieldCompare()](./asFieldCompare/#default) |  |
|[ asFieldCreateDate()](./asFieldCreateDate/#default) |  |
|[ asFieldData()](./asFieldData/#default) |  |
|[ asFieldDatabase()](./asFieldDatabase/#default) |  |
|[ asFieldDate()](./asFieldDate/#default) |  |
|[ asFieldDde()](./asFieldDde/#default) |  |
|[ asFieldDdeAuto()](./asFieldDdeAuto/#default) |  |
|[ asFieldDisplayBarcode()](./asFieldDisplayBarcode/#default) |  |
|[ asFieldDocProperty()](./asFieldDocProperty/#default) |  |
|[ asFieldDocVariable()](./asFieldDocVariable/#default) |  |
|[ asFieldEQ()](./asFieldEQ/#default) |  |
|[ asFieldEditTime()](./asFieldEditTime/#default) |  |
|[ asFieldEmbed()](./asFieldEmbed/#default) |  |
|[ asFieldFileName()](./asFieldFileName/#default) |  |
|[ asFieldFileSize()](./asFieldFileSize/#default) |  |
|[ asFieldFillIn()](./asFieldFillIn/#default) |  |
|[ asFieldFootnoteRef()](./asFieldFootnoteRef/#default) |  |
|[ asFieldFormCheckBox()](./asFieldFormCheckBox/#default) |  |
|[ asFieldFormDropDown()](./asFieldFormDropDown/#default) |  |
|[ asFieldFormText()](./asFieldFormText/#default) |  |
|[ asFieldFormula()](./asFieldFormula/#default) |  |
|[ asFieldGlossary()](./asFieldGlossary/#default) |  |
|[ asFieldGoToButton()](./asFieldGoToButton/#default) |  |
|[ asFieldGreetingLine()](./asFieldGreetingLine/#default) |  |
|[ asFieldHyperlink()](./asFieldHyperlink/#default) |  |
|[ asFieldIf()](./asFieldIf/#default) |  |
|[ asFieldImport()](./asFieldImport/#default) |  |
|[ asFieldInclude()](./asFieldInclude/#default) |  |
|[ asFieldIncludePicture()](./asFieldIncludePicture/#default) |  |
|[ asFieldIncludeText()](./asFieldIncludeText/#default) |  |
|[ asFieldIndex()](./asFieldIndex/#default) |  |
|[ asFieldInfo()](./asFieldInfo/#default) |  |
|[ asFieldKeywords()](./asFieldKeywords/#default) |  |
|[ asFieldLastSavedBy()](./asFieldLastSavedBy/#default) |  |
|[ asFieldLink()](./asFieldLink/#default) |  |
|[ asFieldListNum()](./asFieldListNum/#default) |  |
|[ asFieldMacroButton()](./asFieldMacroButton/#default) |  |
|[ asFieldMergeBarcode()](./asFieldMergeBarcode/#default) |  |
|[ asFieldMergeField()](./asFieldMergeField/#default) |  |
|[ asFieldMergeRec()](./asFieldMergeRec/#default) |  |
|[ asFieldMergeSeq()](./asFieldMergeSeq/#default) |  |
|[ asFieldNext()](./asFieldNext/#default) |  |
|[ asFieldNextIf()](./asFieldNextIf/#default) |  |
|[ asFieldNoteRef()](./asFieldNoteRef/#default) |  |
|[ asFieldNumChars()](./asFieldNumChars/#default) |  |
|[ asFieldNumPages()](./asFieldNumPages/#default) |  |
|[ asFieldNumWords()](./asFieldNumWords/#default) |  |
|[ asFieldOcx()](./asFieldOcx/#default) |  |
|[ asFieldPage()](./asFieldPage/#default) |  |
|[ asFieldPageRef()](./asFieldPageRef/#default) |  |
|[ asFieldPrint()](./asFieldPrint/#default) |  |
|[ asFieldPrintDate()](./asFieldPrintDate/#default) |  |
|[ asFieldPrivate()](./asFieldPrivate/#default) |  |
|[ asFieldQuote()](./asFieldQuote/#default) |  |
|[ asFieldRD()](./asFieldRD/#default) |  |
|[ asFieldRef()](./asFieldRef/#default) |  |
|[ asFieldRevNum()](./asFieldRevNum/#default) |  |
|[ asFieldSaveDate()](./asFieldSaveDate/#default) |  |
|[ asFieldSection()](./asFieldSection/#default) |  |
|[ asFieldSectionPages()](./asFieldSectionPages/#default) |  |
|[ asFieldSeq()](./asFieldSeq/#default) |  |
|[ asFieldSet()](./asFieldSet/#default) |  |
|[ asFieldShape()](./asFieldShape/#default) |  |
|[ asFieldSkipIf()](./asFieldSkipIf/#default) |  |
|[ asFieldStyleRef()](./asFieldStyleRef/#default) |  |
|[ asFieldSubject()](./asFieldSubject/#default) |  |
|[ asFieldSymbol()](./asFieldSymbol/#default) |  |
|[ asFieldTA()](./asFieldTA/#default) |  |
|[ asFieldTC()](./asFieldTC/#default) |  |
|[ asFieldTemplate()](./asFieldTemplate/#default) |  |
|[ asFieldTime()](./asFieldTime/#default) |  |
|[ asFieldTitle()](./asFieldTitle/#default) |  |
|[ asFieldToa()](./asFieldToa/#default) |  |
|[ asFieldToc()](./asFieldToc/#default) |  |
|[ asFieldUnknown()](./asFieldUnknown/#default) |  |
|[ asFieldUserAddress()](./asFieldUserAddress/#default) |  |
|[ asFieldUserInitials()](./asFieldUserInitials/#default) |  |
|[ asFieldUserName()](./asFieldUserName/#default) |  |
|[ asFieldXE()](./asFieldXE/#default) |  |
|[ getFieldCode()](./getFieldCode/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
|[ getFieldCode(includeChildFieldCodes)](./getFieldCode/#boolean) | Returns text between field start and field separator (or field end if there is no separator). |
|[ remove()](./remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``null``. |
|[ unlink()](./unlink/#default) | Performs the field unlink. |
|[ update()](./update/#default) | Performs the field update. Throws if the field is being updated already. |
|[ update(ignoreMergeFormat)](./update/#boolean) | Performs a field update. Throws if the field is being updated already. |

### Examples

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

### See Also

* module [Aspose.Words](../)

