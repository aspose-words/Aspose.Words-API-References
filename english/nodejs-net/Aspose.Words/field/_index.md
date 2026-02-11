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
To learn more, visit the  documentation article.




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
|[ asFieldAddIn()](./asFieldAddIn/#default) | Cast field to [FieldAddIn](../../aspose.words.fields/fieldaddin/). |
|[ asFieldAddressBlock()](./asFieldAddressBlock/#default) | Cast field to [FieldAddressBlock](../../aspose.words.fields/fieldaddressblock/). |
|[ asFieldAdvance()](./asFieldAdvance/#default) | Cast field to [FieldAdvance](../../aspose.words.fields/fieldadvance/). |
|[ asFieldAsk()](./asFieldAsk/#default) | Cast field to [FieldAsk](../../aspose.words.fields/fieldask/). |
|[ asFieldAuthor()](./asFieldAuthor/#default) | Cast field to [FieldAuthor](../../aspose.words.fields/fieldauthor/). |
|[ asFieldAutoNum()](./asFieldAutoNum/#default) | Cast field to [FieldAutoNum](../../aspose.words.fields/fieldautonum/). |
|[ asFieldAutoNumLgl()](./asFieldAutoNumLgl/#default) | Cast field to [FieldAutoNumLgl](../../aspose.words.fields/fieldautonumlgl/). |
|[ asFieldAutoNumOut()](./asFieldAutoNumOut/#default) | Cast field to [FieldAutoNumOut](../../aspose.words.fields/fieldautonumout/). |
|[ asFieldAutoText()](./asFieldAutoText/#default) | Cast field to [FieldAutoText](../../aspose.words.fields/fieldautotext/). |
|[ asFieldAutoTextList()](./asFieldAutoTextList/#default) | Cast field to [FieldAutoTextList](../../aspose.words.fields/fieldautotextlist/). |
|[ asFieldBarcode()](./asFieldBarcode/#default) | Cast field to [FieldBarcode](../../aspose.words.fields/fieldbarcode/). |
|[ asFieldBibliography()](./asFieldBibliography/#default) | Cast field to [FieldBibliography](../../aspose.words.fields/fieldbibliography/). |
|[ asFieldBidiOutline()](./asFieldBidiOutline/#default) | Cast field to [FieldBidiOutline](../../aspose.words.fields/fieldbidioutline/). |
|[ asFieldCitation()](./asFieldCitation/#default) | Cast field to [FieldCitation](../../aspose.words.fields/fieldcitation/). |
|[ asFieldComments()](./asFieldComments/#default) | Cast field to [FieldComments](../../aspose.words.fields/fieldcomments/). |
|[ asFieldCompare()](./asFieldCompare/#default) | Cast field to [FieldCompare](../../aspose.words.fields/fieldcompare/). |
|[ asFieldCreateDate()](./asFieldCreateDate/#default) | Cast field to [FieldCreateDate](../../aspose.words.fields/fieldcreatedate/). |
|[ asFieldData()](./asFieldData/#default) | Cast field to [FieldData](../../aspose.words.fields/fielddata/). |
|[ asFieldDatabase()](./asFieldDatabase/#default) | Cast field to [FieldDatabase](../../aspose.words.fields/fielddatabase/). |
|[ asFieldDate()](./asFieldDate/#default) | Cast field to [FieldDate](../../aspose.words.fields/fielddate/). |
|[ asFieldDde()](./asFieldDde/#default) | Cast field to [FieldDde](../../aspose.words.fields/fielddde/). |
|[ asFieldDdeAuto()](./asFieldDdeAuto/#default) | Cast field to [FieldDdeAuto](../../aspose.words.fields/fieldddeauto/). |
|[ asFieldDisplayBarcode()](./asFieldDisplayBarcode/#default) | Cast field to [FieldDisplayBarcode](../../aspose.words.fields/fielddisplaybarcode/). |
|[ asFieldDocProperty()](./asFieldDocProperty/#default) | Cast field to [FieldDocProperty](../../aspose.words.fields/fielddocproperty/). |
|[ asFieldDocVariable()](./asFieldDocVariable/#default) | Cast field to [FieldDocVariable](../../aspose.words.fields/fielddocvariable/). |
|[ asFieldEQ()](./asFieldEQ/#default) | Cast field to [FieldEQ](../../aspose.words.fields/fieldeq/). |
|[ asFieldEditTime()](./asFieldEditTime/#default) | Cast field to [FieldEditTime](../../aspose.words.fields/fieldedittime/). |
|[ asFieldEmbed()](./asFieldEmbed/#default) | Cast field to [FieldEmbed](../../aspose.words.fields/fieldembed/). |
|[ asFieldFileName()](./asFieldFileName/#default) | Cast field to [FieldFileName](../../aspose.words.fields/fieldfilename/). |
|[ asFieldFileSize()](./asFieldFileSize/#default) | Cast field to [FieldFileSize](../../aspose.words.fields/fieldfilesize/). |
|[ asFieldFillIn()](./asFieldFillIn/#default) | Cast field to [FieldFillIn](../../aspose.words.fields/fieldfillin/). |
|[ asFieldFootnoteRef()](./asFieldFootnoteRef/#default) | Cast field to [FieldFootnoteRef](../../aspose.words.fields/fieldfootnoteref/). |
|[ asFieldFormCheckBox()](./asFieldFormCheckBox/#default) | Cast field to [FieldFormCheckBox](../../aspose.words.fields/fieldformcheckbox/). |
|[ asFieldFormDropDown()](./asFieldFormDropDown/#default) | Cast field to [FieldFormDropDown](../../aspose.words.fields/fieldformdropdown/). |
|[ asFieldFormText()](./asFieldFormText/#default) | Cast field to [FieldFormText](../../aspose.words.fields/fieldformtext/). |
|[ asFieldFormula()](./asFieldFormula/#default) | Cast field to [FieldFormula](../../aspose.words.fields/fieldformula/). |
|[ asFieldGlossary()](./asFieldGlossary/#default) | Cast field to [FieldGlossary](../../aspose.words.fields/fieldglossary/). |
|[ asFieldGoToButton()](./asFieldGoToButton/#default) | Cast field to [FieldGoToButton](../../aspose.words.fields/fieldgotobutton/). |
|[ asFieldGreetingLine()](./asFieldGreetingLine/#default) | Cast field to [FieldGreetingLine](../../aspose.words.fields/fieldgreetingline/). |
|[ asFieldHyperlink()](./asFieldHyperlink/#default) | Cast field to [FieldHyperlink](../../aspose.words.fields/fieldhyperlink/). |
|[ asFieldIf()](./asFieldIf/#default) | Cast field to [FieldIf](../../aspose.words.fields/fieldif/). |
|[ asFieldImport()](./asFieldImport/#default) | Cast field to [FieldImport](../../aspose.words.fields/fieldimport/). |
|[ asFieldInclude()](./asFieldInclude/#default) | Cast field to [FieldInclude](../../aspose.words.fields/fieldinclude/). |
|[ asFieldIncludePicture()](./asFieldIncludePicture/#default) | Cast field to [FieldIncludePicture](../../aspose.words.fields/fieldincludepicture/). |
|[ asFieldIncludeText()](./asFieldIncludeText/#default) | Cast field to [FieldIncludeText](../../aspose.words.fields/fieldincludetext/). |
|[ asFieldIndex()](./asFieldIndex/#default) | Cast field to [FieldIndex](../../aspose.words.fields/fieldindex/). |
|[ asFieldInfo()](./asFieldInfo/#default) | Cast field to [FieldInfo](../../aspose.words.fields/fieldinfo/). |
|[ asFieldKeywords()](./asFieldKeywords/#default) | Cast field to [FieldKeywords](../../aspose.words.fields/fieldkeywords/). |
|[ asFieldLastSavedBy()](./asFieldLastSavedBy/#default) | Cast field to [FieldLastSavedBy](../../aspose.words.fields/fieldlastsavedby/). |
|[ asFieldLink()](./asFieldLink/#default) | Cast field to [FieldLink](../../aspose.words.fields/fieldlink/). |
|[ asFieldListNum()](./asFieldListNum/#default) | Cast field to [FieldListNum](../../aspose.words.fields/fieldlistnum/). |
|[ asFieldMacroButton()](./asFieldMacroButton/#default) | Cast field to [FieldMacroButton](../../aspose.words.fields/fieldmacrobutton/). |
|[ asFieldMergeBarcode()](./asFieldMergeBarcode/#default) | Cast field to [FieldMergeBarcode](../../aspose.words.fields/fieldmergebarcode/). |
|[ asFieldMergeField()](./asFieldMergeField/#default) | Cast field to [FieldMergeField](../../aspose.words.fields/fieldmergefield/). |
|[ asFieldMergeRec()](./asFieldMergeRec/#default) | Cast field to [FieldMergeRec](../../aspose.words.fields/fieldmergerec/). |
|[ asFieldMergeSeq()](./asFieldMergeSeq/#default) | Cast field to [FieldMergeSeq](../../aspose.words.fields/fieldmergeseq/). |
|[ asFieldNext()](./asFieldNext/#default) | Cast field to [FieldNext](../../aspose.words.fields/fieldnext/). |
|[ asFieldNextIf()](./asFieldNextIf/#default) | Cast field to [FieldNextIf](../../aspose.words.fields/fieldnextif/). |
|[ asFieldNoteRef()](./asFieldNoteRef/#default) | Cast field to [FieldNoteRef](../../aspose.words.fields/fieldnoteref/). |
|[ asFieldNumChars()](./asFieldNumChars/#default) | Cast field to [FieldNumChars](../../aspose.words.fields/fieldnumchars/). |
|[ asFieldNumPages()](./asFieldNumPages/#default) | Cast field to [FieldNumPages](../../aspose.words.fields/fieldnumpages/). |
|[ asFieldNumWords()](./asFieldNumWords/#default) | Cast field to [FieldNumWords](../../aspose.words.fields/fieldnumwords/). |
|[ asFieldOcx()](./asFieldOcx/#default) | Cast field to [FieldOcx](../../aspose.words.fields/fieldocx/). |
|[ asFieldPage()](./asFieldPage/#default) | Cast field to [FieldPage](../../aspose.words.fields/fieldpage/). |
|[ asFieldPageRef()](./asFieldPageRef/#default) | Cast field to [FieldPageRef](../../aspose.words.fields/fieldpageref/). |
|[ asFieldPrint()](./asFieldPrint/#default) | Cast field to [FieldPrint](../../aspose.words.fields/fieldprint/). |
|[ asFieldPrintDate()](./asFieldPrintDate/#default) | Cast field to [FieldPrintDate](../../aspose.words.fields/fieldprintdate/). |
|[ asFieldPrivate()](./asFieldPrivate/#default) | Cast field to [FieldPrivate](../../aspose.words.fields/fieldprivate/). |
|[ asFieldQuote()](./asFieldQuote/#default) | Cast field to [FieldQuote](../../aspose.words.fields/fieldquote/). |
|[ asFieldRD()](./asFieldRD/#default) | Cast field to [FieldRD](../../aspose.words.fields/fieldrd/). |
|[ asFieldRef()](./asFieldRef/#default) | Cast field to [FieldRef](../../aspose.words.fields/fieldref/). |
|[ asFieldRevNum()](./asFieldRevNum/#default) | Cast field to [FieldRevNum](../../aspose.words.fields/fieldrevnum/). |
|[ asFieldSaveDate()](./asFieldSaveDate/#default) | Cast field to [FieldSaveDate](../../aspose.words.fields/fieldsavedate/). |
|[ asFieldSection()](./asFieldSection/#default) | Cast field to [FieldSection](../../aspose.words.fields/fieldsection/). |
|[ asFieldSectionPages()](./asFieldSectionPages/#default) | Cast field to [FieldSectionPages](../../aspose.words.fields/fieldsectionpages/). |
|[ asFieldSeq()](./asFieldSeq/#default) | Cast field to [FieldSeq](../../aspose.words.fields/fieldseq/). |
|[ asFieldSet()](./asFieldSet/#default) | Cast field to [FieldSet](../../aspose.words.fields/fieldset/). |
|[ asFieldShape()](./asFieldShape/#default) | Cast field to [FieldShape](../../aspose.words.fields/fieldshape/). |
|[ asFieldSkipIf()](./asFieldSkipIf/#default) | Cast field to [FieldSkipIf](../../aspose.words.fields/fieldskipif/). |
|[ asFieldStyleRef()](./asFieldStyleRef/#default) | Cast field to [FieldStyleRef](../../aspose.words.fields/fieldstyleref/). |
|[ asFieldSubject()](./asFieldSubject/#default) | Cast field to [FieldSubject](../../aspose.words.fields/fieldsubject/). |
|[ asFieldSymbol()](./asFieldSymbol/#default) | Cast field to [FieldSymbol](../../aspose.words.fields/fieldsymbol/). |
|[ asFieldTA()](./asFieldTA/#default) | Cast field to [FieldTA](../../aspose.words.fields/fieldta/). |
|[ asFieldTC()](./asFieldTC/#default) | Cast field to [FieldTC](../../aspose.words.fields/fieldtc/). |
|[ asFieldTemplate()](./asFieldTemplate/#default) | Cast field to [FieldTemplate](../../aspose.words.fields/fieldtemplate/). |
|[ asFieldTime()](./asFieldTime/#default) | Cast field to [FieldTime](../../aspose.words.fields/fieldtime/). |
|[ asFieldTitle()](./asFieldTitle/#default) | Cast field to [FieldTitle](../../aspose.words.fields/fieldtitle/). |
|[ asFieldToa()](./asFieldToa/#default) | Cast field to [FieldToa](../../aspose.words.fields/fieldtoa/). |
|[ asFieldToc()](./asFieldToc/#default) | Cast field to [FieldToc](../../aspose.words.fields/fieldtoc/). |
|[ asFieldUnknown()](./asFieldUnknown/#default) | Cast field to [FieldUnknown](../../aspose.words.fields/fieldunknown/). |
|[ asFieldUserAddress()](./asFieldUserAddress/#default) | Cast field to [FieldUserAddress](../../aspose.words.fields/fielduseraddress/). |
|[ asFieldUserInitials()](./asFieldUserInitials/#default) | Cast field to [FieldUserInitials](../../aspose.words.fields/fielduserinitials/). |
|[ asFieldUserName()](./asFieldUserName/#default) | Cast field to [FieldUserName](../../aspose.words.fields/fieldusername/). |
|[ asFieldXE()](./asFieldXE/#default) | Cast field to [FieldXE](../../aspose.words.fields/fieldxe/). |
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

