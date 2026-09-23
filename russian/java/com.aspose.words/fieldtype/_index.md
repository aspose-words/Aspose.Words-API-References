---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words для Java"
description: "Определяет типы полей Microsoft Word в Java."
type: docs
weight: 299
url: /ru/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

Указывает типы полей Microsoft Word.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Показывает, как работать с узлом FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | Определяет поле ADDIN. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | Определяет поле ADDRESSBLOCK. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | Определяет поле ADVANCE. |
| [FIELD_ASK](#FIELD-ASK) | Определяет поле ASK. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | Определяет поле AUTHOR. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | Определяет поле AUTONUM. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | Указывает поле AUTONUMLGL. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | Указывает поле AUTONUMOUT. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | Указывает поле AUTOTEXT. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | Указывает поле AUTOTEXTLIST. |
| [FIELD_BARCODE](#FIELD-BARCODE) | Указывает поле BARCODE. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | Указывает поле BIBLIOGRAPHY. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | Указывает поле BIDIOUTLINE. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | Указывает, что поле не удалось разобрать. |
| [FIELD_CITATION](#FIELD-CITATION) | Указывает поле CITATION. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | Указывает поле COMMENTS. |
| [FIELD_COMPARE](#FIELD-COMPARE) | Указывает поле COMPARE. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | Указывает поле CREATEDATE. |
| [FIELD_DATA](#FIELD-DATA) | Указывает поле DATA. |
| [FIELD_DATABASE](#FIELD-DATABASE) | Указывает поле DATABASE. |
| [FIELD_DATE](#FIELD-DATE) | Указывает поле DATE. |
| [FIELD_DDE](#FIELD-DDE) | Указывает поле DDE. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | Указывает поле DDEAUTO. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | Указывает поле DISPLAYBARCODE. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | Указывает поле DOCPROPERTY. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | Указывает поле DOCVARIABLE. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | Указывает поле EDITTIME. |
| [FIELD_EMBED](#FIELD-EMBED) | Указывает поле EMBED. |
| [FIELD_EQUATION](#FIELD-EQUATION) | Указывает поле EQ. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | Указывает поле FILENAME. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | Указывает поле FILESIZE. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | Указывает поле FILLIN. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | Указывает поле FOOTNOTEREF. |
| [FIELD_FORMULA](#FIELD-FORMULA) | Указывает поле = (формула). |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | Указывает поле FORMCHECKBOX. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | Указывает поле FORMDROPDOWN. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | Указывает поле FORMTEXT. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | Указывает поле GLOSSARY. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | Указывает поле GOTOBUTTON. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | Указывает поле GREETINGLINE. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | Указывает поле, представляющее HTML‑элемент. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | Указывает поле HYPERLINK. |
| [FIELD_IF](#FIELD-IF) | Указывает поле IF. |
| [FIELD_IMPORT](#FIELD-IMPORT) | Указывает поле IMPORT. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | Указывает поле INCLUDE. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | Указывает поле INCLUDEPICTURE. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | Указывает поле INCLUDETEXT. |
| [FIELD_INDEX](#FIELD-INDEX) | Указывает поле INDEX. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | Указывает поле XE. |
| [FIELD_INFO](#FIELD-INFO) | Указывает поле INFO. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | Указывает поле KEYWORDS. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | Указывает поле LASTSAVEDBY. |
| [FIELD_LINK](#FIELD-LINK) | Указывает поле LINK. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | Указывает поле LISTNUM. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | Указывает поле MACROBUTTON. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | Указывает поле MERGEBARCODE. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | Указывает поле MERGEFIELD. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | Указывает поле MERGEREC. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | Указывает поле MERGESEQ. |
| [FIELD_NEXT](#FIELD-NEXT) | Указывает поле NEXT. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | Указывает поле NEXTIF. |
| [FIELD_NONE](#FIELD-NONE) | Тип поля не указан или неизвестен. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | Указывает поле NOTEREF. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | Указывает поле NUMCHARS. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | Указывает поле NUMPAGES. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | Указывает поле NUMWORDS. |
| [FIELD_OCX](#FIELD-OCX) | Указывает поле OCX. |
| [FIELD_PAGE](#FIELD-PAGE) | Указывает поле PAGE. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | Указывает поле PAGEREF. |
| [FIELD_PRINT](#FIELD-PRINT) | Указывает поле PRINT. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | Указывает поле PRINTDATE. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | Указывает поле PRIVATE. |
| [FIELD_QUOTE](#FIELD-QUOTE) | Указывает поле QUOTE. |
| [FIELD_REF](#FIELD-REF) | Указывает поле REF. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | Указывает поле RD. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | Указывает, что поле представляет собой поле REF, где ключевое слово было опущено. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | Указывает поле REVNUM. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | Указывает поле SAVEDATE. |
| [FIELD_SECTION](#FIELD-SECTION) | Указывает поле SECTION. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | Указывает поле SECTIONPAGES. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | Указывает поле SEQ. |
| [FIELD_SET](#FIELD-SET) | Указывает поле SET. |
| [FIELD_SHAPE](#FIELD-SHAPE) | Указывает поле SHAPE. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | Указывает поле SKIPIF. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | Указывает поле STYLEREF. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | Указывает поле SUBJECT. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | Указывает поле SYMBOL. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | Указывает поле TEMPLATE. |
| [FIELD_TIME](#FIELD-TIME) | Указывает поле TIME. |
| [FIELD_TITLE](#FIELD-TITLE) | Указывает поле TITLE. |
| [FIELD_TOA](#FIELD-TOA) | Указывает поле TOA. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | Указывает поле TA. |
| [FIELD_TOC](#FIELD-TOC) | Указывает поле TOC. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | Указывает поле TC. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | Указывает поле USERADDRESS. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | Указывает поле USERINITIALS. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | Указывает поле USERNAME. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


Определяет поле ADDIN.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


Определяет поле ADDRESSBLOCK.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


Определяет поле ADVANCE.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


Определяет поле ASK.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


Определяет поле AUTHOR.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


Определяет поле AUTONUM.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


Указывает поле AUTONUMLGL.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


Указывает поле AUTONUMOUT.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


Указывает поле AUTOTEXT.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


Указывает поле AUTOTEXTLIST.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


Указывает поле BARCODE.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


Указывает поле BIBLIOGRAPHY.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


Указывает поле BIDIOUTLINE.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


Указывает, что поле не удалось разобрать.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


Указывает поле CITATION.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


Указывает поле COMMENTS.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


Указывает поле COMPARE.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


Указывает поле CREATEDATE.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


Указывает поле DATA.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


Указывает поле DATABASE.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


Указывает поле DATE.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


Указывает поле DDE.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


Указывает поле DDEAUTO.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


Указывает поле DISPLAYBARCODE.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


Указывает поле DOCPROPERTY.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


Указывает поле DOCVARIABLE.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


Указывает поле EDITTIME.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


Указывает поле EMBED.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


Указывает поле EQ.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


Указывает поле FILENAME.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


Указывает поле FILESIZE.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


Указывает поле FILLIN.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


Указывает поле FOOTNOTEREF.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


Указывает поле = (формула).

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


Указывает поле FORMCHECKBOX.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


Указывает поле FORMDROPDOWN.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


Указывает поле FORMTEXT.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


Указывает поле GLOSSARY.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


Указывает поле GOTOBUTTON.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


Указывает поле GREETINGLINE.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


Указывает поле, представляющее HTML‑элемент.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


Указывает поле HYPERLINK.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


Указывает поле IF.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


Указывает поле IMPORT.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


Указывает поле INCLUDE.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


Указывает поле INCLUDEPICTURE.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


Указывает поле INCLUDETEXT.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


Указывает поле INDEX.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


Указывает поле XE.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


Указывает поле INFO.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


Указывает поле KEYWORDS.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


Указывает поле LASTSAVEDBY.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


Указывает поле LINK.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


Указывает поле LISTNUM.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


Указывает поле MACROBUTTON.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


Указывает поле MERGEBARCODE.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


Указывает поле MERGEFIELD.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


Указывает поле MERGEREC.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


Указывает поле MERGESEQ.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


Указывает поле NEXT.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


Указывает поле NEXTIF.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


Тип поля не указан или неизвестен.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


Указывает поле NOTEREF.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


Указывает поле NUMCHARS.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


Указывает поле NUMPAGES.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


Указывает поле NUMWORDS.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


Указывает поле OCX.

Обычно Aspose.Words будет представлять элемент управления ActiveX как объект [Shape](../../com.aspose.words/shape/), но для некоторых документов, где элемент управления не имеет данных и/или кажется недействительным, он будет представлен как поле.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


Указывает поле PAGE.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


Указывает поле PAGEREF.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


Указывает поле PRINT.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


Указывает поле PRINTDATE.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


Указывает поле PRIVATE.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


Указывает поле QUOTE.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


Указывает поле REF.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


Указывает поле RD.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


Указывает, что поле представляет собой поле REF, где ключевое слово было опущено.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


Указывает поле REVNUM.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


Указывает поле SAVEDATE.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


Указывает поле SECTION.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


Указывает поле SECTIONPAGES.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


Указывает поле SEQ.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


Указывает поле SET.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


Указывает поле SHAPE.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


Указывает поле SKIPIF.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


Указывает поле STYLEREF.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


Указывает поле SUBJECT.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


Указывает поле SYMBOL.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


Указывает поле TEMPLATE.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


Указывает поле TIME.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


Указывает поле TITLE.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


Указывает поле TOA.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


Указывает поле TA.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


Указывает поле TOC.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


Указывает поле TC.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


Указывает поле USERADDRESS.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


Указывает поле USERINITIALS.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


Указывает поле USERNAME.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fieldType) {#toString-int}
```
public static String toString(int fieldType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
