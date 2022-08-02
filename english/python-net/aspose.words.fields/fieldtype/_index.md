---
title: FieldType enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies Microsoft Word field types."
type: docs
weight: 1080
url: /python-net/aspose.words.fields/fieldtype/
---

## FieldType enumeration

Specifies Microsoft Word field types.


### Members

| Name | Description |
| --- | --- |
| FIELD_NONE | Field type is not specified or unknown. |
| FIELD_CANNOT_PARSE | Specifies that the field was unable to be parsed. |
| FIELD_ADDIN | Specifies the ADDIN field. |
| FIELD_ADDRESS_BLOCK | Specifies the ADDRESSBLOCK field. |
| FIELD_ADVANCE | Specifies the ADVANCE field. |
| FIELD_ASK | Specifies the ASK field. |
| FIELD_AUTHOR | Specifies the AUTHOR field. |
| FIELD_AUTO_NUM | Specifies the AUTONUM field. |
| FIELD_AUTO_NUM_LEGAL | Specifies the AUTONUMLGL field. |
| FIELD_AUTO_NUM_OUTLINE | Specifies the AUTONUMOUT field. |
| FIELD_AUTO_TEXT | Specifies the AUTOTEXT field. |
| FIELD_AUTO_TEXT_LIST | Specifies the AUTOTEXTLIST field. |
| FIELD_BARCODE | Specifies the BARCODE field. |
| FIELD_BIBLIOGRAPHY | Specifies the BIBLIOGRAPHY field. |
| FIELD_BIDI_OUTLINE | Specifies the BIDIOUTLINE field. |
| FIELD_CITATION | Specifies the CITATION field. |
| FIELD_COMMENTS | Specifies the COMMENTS field. |
| FIELD_COMPARE | Specifies the COMPARE field. |
| FIELD_CREATE_DATE | Specifies the CREATEDATE field. |
| FIELD_DATA | Specifies the DATA field. |
| FIELD_DATABASE | Specifies the DATABASE field. |
| FIELD_DATE | Specifies the DATE field. |
| FIELD_DDE | Specifies the DDE field. |
| FIELD_DISPLAY_BARCODE | Specifies the DISPLAYBARCODE field. |
| FIELD_MERGE_BARCODE | Specifies the MERGEBARCODE field. |
| FIELD_DDE_AUTO | Specifies the DDEAUTO field. |
| FIELD_DOC_PROPERTY | Specifies the DOCPROPERTY field. |
| FIELD_DOC_VARIABLE | Specifies the DOCVARIABLE field. |
| FIELD_EDIT_TIME | Specifies the EDITTIME field. |
| FIELD_EMBED | Specifies the EMBED field. |
| FIELD_EQUATION | Specifies the EQ field. |
| FIELD_FILE_NAME | Specifies the FILENAME field. |
| FIELD_FILE_SIZE | Specifies the FILESIZE field. |
| FIELD_FILL_IN | Specifies the FILLIN field. |
| FIELD_FOOTNOTE_REF | Specifies the FOOTNOTEREF field. |
| FIELD_FORM_CHECK_BOX | Specifies the FORMCHECKBOX field. |
| FIELD_FORM_DROP_DOWN | Specifies the FORMDROPDOWN field. |
| FIELD_FORM_TEXT_INPUT | Specifies the FORMTEXT field. |
| FIELD_FORMULA | Specifies the = (formula) field. |
| FIELD_GREETING_LINE | Specifies the GREETINGLINE field. |
| FIELD_GLOSSARY | Specifies the GLOSSARY field. |
| FIELD_GO_TO_BUTTON | Specifies the GOTOBUTTON field. |
| FIELD_HTML_ACTIVE_X | Specifies the field that represents an HTML control. |
| FIELD_HYPERLINK | Specifies the HYPERLINK field. |
| FIELD_IF | Specifies the IF field. |
| FIELD_INCLUDE | Specifies the INCLUDE field. |
| FIELD_INCLUDE_PICTURE | Specifies the INCLUDEPICTURE field. |
| FIELD_INCLUDE_TEXT | Specifies the INCLUDETEXT field. |
| FIELD_INDEX | Specifies the INDEX field. |
| FIELD_INDEX_ENTRY | Specifies the XE field. |
| FIELD_INFO | Specifies the INFO field. |
| FIELD_IMPORT | Specifies the IMPORT field. |
| FIELD_KEYWORD | Specifies the KEYWORDS field. |
| FIELD_LAST_SAVED_BY | Specifies the LASTSAVEDBY field. |
| FIELD_LINK | Specifies the LINK field. |
| FIELD_LIST_NUM | Specifies the LISTNUM field. |
| FIELD_MACRO_BUTTON | Specifies the MACROBUTTON field. |
| FIELD_MERGE_FIELD | Specifies the MERGEFIELD field. |
| FIELD_MERGE_REC | Specifies the MERGEREC field. |
| FIELD_MERGE_SEQ | Specifies the MERGESEQ field. |
| FIELD_NEXT | Specifies the NEXT field. |
| FIELD_NEXT_IF | Specifies the NEXTIF field. |
| FIELD_NOTE_REF | Specifies the NOTEREF field. |
| FIELD_NUM_CHARS | Specifies the NUMCHARS field. |
| FIELD_NUM_PAGES | Specifies the NUMPAGES field. |
| FIELD_NUM_WORDS | Specifies the NUMWORDS field. |
| FIELD_OCX | Specifies the OCX field. |
| FIELD_PAGE | Specifies the PAGE field. |
| FIELD_PAGE_REF | Specifies the PAGEREF field. |
| FIELD_PRINT | Specifies the PRINT field. |
| FIELD_PRINT_DATE | Specifies the PRINTDATE field. |
| FIELD_PRIVATE | Specifies the PRIVATE field. |
| FIELD_QUOTE | Specifies the QUOTE field. |
| FIELD_REF | Specifies the REF field. |
| FIELD_REF_NO_KEYWORD | Specifies that the field represents a REF field where the keyword has been omitted. |
| FIELD_REF_DOC | Specifies the RD field. |
| FIELD_REVISION_NUM | Specifies the REVNUM field. |
| FIELD_SAVE_DATE | Specifies the SAVEDATE field. |
| FIELD_SECTION | Specifies the SECTION field. |
| FIELD_SECTION_PAGES | Specifies the SECTIONPAGES field. |
| FIELD_SEQUENCE | Specifies the SEQ field. |
| FIELD_SET | Specifies the SET field. |
| FIELD_SHAPE | Specifies the SHAPE field. |
| FIELD_SKIP_IF | Specifies the SKIPIF field. |
| FIELD_STYLE_REF | Specifies the STYLEREF field. |
| FIELD_SUBJECT | Specifies the SUBJECT field. |
| FIELD_SYMBOL | Specifies the SYMBOL field. |
| FIELD_TEMPLATE | Specifies the TEMPLATE field. |
| FIELD_TIME | Specifies the TIME field. |
| FIELD_TITLE | Specifies the TITLE field. |
| FIELD_TOA | Specifies the TOA field. |
| FIELD_TOA_ENTRY | Specifies the TA field. |
| FIELD_TOC | Specifies the TOC field. |
| FIELD_TOC_ENTRY | Specifies the TC field. |
| FIELD_USER_ADDRESS | Specifies the USERADDRESS field. |
| FIELD_USER_INITIALS | Specifies the USERINITIALS field. |
| FIELD_USER_NAME | Specifies the USERNAME field. |

### Examples

Shows how to insert a field into a document using a field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field("DATE \\@ \"dddd, MMMM dd, yyyy\"")

self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.get_field_code())

# This overload of the "insert_field" method automatically updates inserted fields.
self.assertAlmostEqual(datetime.strptime(field.result, "%A, %B %d, %Y"), datetime.now(), delta=timedelta(1))
```

Shows how to work with a FieldStart node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.format.date_time_format = "dddd, MMMM dd, yyyy"
field.update()

field_start = field.start

self.assertEqual(aw.fields.FieldType.FIELD_DATE, field_start.field_type)
self.assertFalse(field_start.is_dirty)
self.assertFalse(field_start.is_locked)

# Retrieve the facade object which represents the field in the document.
field = field_start.get_field().as_field_date()

self.assertFalse(field.is_locked)
self.assertEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.get_field_code())

# Update the field to show the current date.
field.update()
```

### See Also

* module [aspose.words.fields](../)

