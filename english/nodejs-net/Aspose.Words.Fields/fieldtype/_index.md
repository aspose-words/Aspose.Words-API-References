---
title: FieldType enumeration
linktitle: FieldType enumeration
articleTitle: FieldType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fields.FieldType enumeration. Specifies Microsoft Word field types."
type: docs
weight: 1070
url: /nodejs-net/aspose.words.fields/fieldtype/
---

## FieldType enumeration

Specifies Microsoft Word field types.


### Members

| Name | Description |
| --- | --- |
| FieldNone | Field type is not specified or unknown. |
| FieldCannotParse | Specifies that the field was unable to be parsed. |
| FieldAddin | Specifies the ADDIN field. |
| FieldAddressBlock | Specifies the ADDRESSBLOCK field. |
| FieldAdvance | Specifies the ADVANCE field. |
| FieldAsk | Specifies the ASK field. |
| FieldAuthor | Specifies the AUTHOR field. |
| FieldAutoNum | Specifies the AUTONUM field. |
| FieldAutoNumLegal | Specifies the AUTONUMLGL field. |
| FieldAutoNumOutline | Specifies the AUTONUMOUT field. |
| FieldAutoText | Specifies the AUTOTEXT field. |
| FieldAutoTextList | Specifies the AUTOTEXTLIST field. |
| FieldBarcode | Specifies the BARCODE field. |
| FieldBibliography | Specifies the BIBLIOGRAPHY field. |
| FieldBidiOutline | Specifies the BIDIOUTLINE field. |
| FieldCitation | Specifies the CITATION field. |
| FieldComments | Specifies the COMMENTS field. |
| FieldCompare | Specifies the COMPARE field. |
| FieldCreateDate | Specifies the CREATEDATE field. |
| FieldData | Specifies the DATA field. |
| FieldDatabase | Specifies the DATABASE field. |
| FieldDate | Specifies the DATE field. |
| FieldDDE | Specifies the DDE field. |
| FieldDisplayBarcode | Specifies the DISPLAYBARCODE field. |
| FieldMergeBarcode | Specifies the MERGEBARCODE field. |
| FieldDDEAuto | Specifies the DDEAUTO field. |
| FieldDocProperty | Specifies the DOCPROPERTY field. |
| FieldDocVariable | Specifies the DOCVARIABLE field. |
| FieldEditTime | Specifies the EDITTIME field. |
| FieldEmbed | Specifies the EMBED field. |
| FieldEquation | Specifies the EQ field. |
| FieldFileName | Specifies the FILENAME field. |
| FieldFileSize | Specifies the FILESIZE field. |
| FieldFillIn | Specifies the FILLIN field. |
| FieldFootnoteRef | Specifies the FOOTNOTEREF field. |
| FieldFormCheckBox | Specifies the FORMCHECKBOX field. |
| FieldFormDropDown | Specifies the FORMDROPDOWN field. |
| FieldFormTextInput | Specifies the FORMTEXT field. |
| FieldFormula | Specifies the = (formula) field. |
| FieldGreetingLine | Specifies the GREETINGLINE field. |
| FieldGlossary | Specifies the GLOSSARY field. |
| FieldGoToButton | Specifies the GOTOBUTTON field. |
| FieldHtmlActiveX | Specifies the field that represents an HTML control. |
| FieldHyperlink | Specifies the HYPERLINK field. |
| FieldIf | Specifies the IF field. |
| FieldInclude | Specifies the INCLUDE field. |
| FieldIncludePicture | Specifies the INCLUDEPICTURE field. |
| FieldIncludeText | Specifies the INCLUDETEXT field. |
| FieldIndex | Specifies the INDEX field. |
| FieldIndexEntry | Specifies the XE field. |
| FieldInfo | Specifies the INFO field. |
| FieldImport | Specifies the IMPORT field. |
| FieldKeyword | Specifies the KEYWORDS field. |
| FieldLastSavedBy | Specifies the LASTSAVEDBY field. |
| FieldLink | Specifies the LINK field. |
| FieldListNum | Specifies the LISTNUM field. |
| FieldMacroButton | Specifies the MACROBUTTON field. |
| FieldMergeField | Specifies the MERGEFIELD field. |
| FieldMergeRec | Specifies the MERGEREC field. |
| FieldMergeSeq | Specifies the MERGESEQ field. |
| FieldNext | Specifies the NEXT field. |
| FieldNextIf | Specifies the NEXTIF field. |
| FieldNoteRef | Specifies the NOTEREF field. |
| FieldNumChars | Specifies the NUMCHARS field. |
| FieldNumPages | Specifies the NUMPAGES field. |
| FieldNumWords | Specifies the NUMWORDS field. |
| FieldOcx | Specifies the OCX field. |
| FieldPage | Specifies the PAGE field. |
| FieldPageRef | Specifies the PAGEREF field. |
| FieldPrint | Specifies the PRINT field. |
| FieldPrintDate | Specifies the PRINTDATE field. |
| FieldPrivate | Specifies the PRIVATE field. |
| FieldQuote | Specifies the QUOTE field. |
| FieldRef | Specifies the REF field. |
| FieldRefNoKeyword | Specifies that the field represents a REF field where the keyword has been omitted. |
| FieldRefDoc | Specifies the RD field. |
| FieldRevisionNum | Specifies the REVNUM field. |
| FieldSaveDate | Specifies the SAVEDATE field. |
| FieldSection | Specifies the SECTION field. |
| FieldSectionPages | Specifies the SECTIONPAGES field. |
| FieldSequence | Specifies the SEQ field. |
| FieldSet | Specifies the SET field. |
| FieldShape | Specifies the SHAPE field. |
| FieldSkipIf | Specifies the SKIPIF field. |
| FieldStyleRef | Specifies the STYLEREF field. |
| FieldSubject | Specifies the SUBJECT field. |
| FieldSymbol | Specifies the SYMBOL field. |
| FieldTemplate | Specifies the TEMPLATE field. |
| FieldTime | Specifies the TIME field. |
| FieldTitle | Specifies the TITLE field. |
| FieldTOA | Specifies the TOA field. |
| FieldTOAEntry | Specifies the TA field. |
| FieldTOC | Specifies the TOC field. |
| FieldTOCEntry | Specifies the TC field. |
| FieldUserAddress | Specifies the USERADDRESS field. |
| FieldUserInitials | Specifies the USERINITIALS field. |
| FieldUserName | Specifies the USERNAME field. |

### Examples

Shows how to work with a FieldStart node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let field = builder.insertField(aw.Fields.FieldType.FieldDate, true).asFieldDate();
field.format.dateTimeFormat = "dddd, MMMM dd, yyyy";
field.update();

let fieldStart = field.start;

expect(fieldStart.fieldType).toEqual(aw.Fields.FieldType.FieldDate);
expect(fieldStart.isDirty).toEqual(false);
expect(fieldStart.isLocked).toEqual(false);

// Retrieve the facade object which represents the field in the document.
field = fieldStart.getField().asFieldDate();

expect(field.isLocked).toEqual(false);
expect(field.getFieldCode()).toEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"");

// Update the field to show the current date.
field.update();
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

### See Also

* module [Aspose.Words.Fields](../)

