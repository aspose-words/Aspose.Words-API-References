---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words Java için"
description: "Java'da Microsoft Word alan türlerini belirtir."
type: docs
weight: 299
url: /tr/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

Microsoft Word alan türlerini belirtir.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | ADDIN alanını belirtir. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | ADDRESSBLOCK alanını belirtir. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | ADVANCE alanını belirtir. |
| [FIELD_ASK](#FIELD-ASK) | ASK alanını belirtir. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | AUTHOR alanını belirtir. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | AUTONUM alanını belirtir. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | AUTONUMLGL alanını belirtir. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | AUTONUMOUT alanını belirtir. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | AUTOTEXT alanını belirtir. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | AUTOTEXTLIST alanını belirtir. |
| [FIELD_BARCODE](#FIELD-BARCODE) | BARCODE alanını belirtir. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | BIBLIOGRAPHY alanını belirtir. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | BIDIOUTLINE alanını belirtir. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | Alanın ayrıştırılamadığını belirtir. |
| [FIELD_CITATION](#FIELD-CITATION) | CITATION alanını belirtir. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | COMMENTS alanını belirtir. |
| [FIELD_COMPARE](#FIELD-COMPARE) | COMPARE alanını belirtir. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | CREATEDATE alanını belirtir. |
| [FIELD_DATA](#FIELD-DATA) | DATA alanını belirtir. |
| [FIELD_DATABASE](#FIELD-DATABASE) | DATABASE alanını belirtir. |
| [FIELD_DATE](#FIELD-DATE) | DATE alanını belirtir. |
| [FIELD_DDE](#FIELD-DDE) | DDE alanını belirtir. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | DDEAUTO alanını belirtir. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | DISPLAYBARCODE alanını belirtir. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | DOCPROPERTY alanını belirtir. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | DOCVARIABLE alanını belirtir. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | EDITTIME alanını belirtir. |
| [FIELD_EMBED](#FIELD-EMBED) | EMBED alanını belirtir. |
| [FIELD_EQUATION](#FIELD-EQUATION) | EQ alanını belirtir. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | FILENAME alanını belirtir. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | FILESIZE alanını belirtir. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | FILLIN alanını belirtir. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | FOOTNOTEREF alanını belirtir. |
| [FIELD_FORMULA](#FIELD-FORMULA) | = (formül) alanını belirtir. |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | FORMCHECKBOX alanını belirtir. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | FORMDROPDOWN alanını belirtir. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | FORMTEXT alanını belirtir. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | GLOSSARY alanını belirtir. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | GOTOBUTTON alanını belirtir. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | GREETINGLINE alanını belirtir. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | HTML denetimini temsil eden alanı belirtir. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | HYPERLINK alanını belirtir. |
| [FIELD_IF](#FIELD-IF) | IF alanını belirtir. |
| [FIELD_IMPORT](#FIELD-IMPORT) | IMPORT alanını belirtir. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | INCLUDE alanını belirtir. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | INCLUDEPICTURE alanını belirtir. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | INCLUDETEXT alanını belirtir. |
| [FIELD_INDEX](#FIELD-INDEX) | INDEX alanını belirtir. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | XE alanını belirtir. |
| [FIELD_INFO](#FIELD-INFO) | INFO alanını belirtir. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | KEYWORDS alanını belirtir. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | LASTSAVEDBY alanını belirtir. |
| [FIELD_LINK](#FIELD-LINK) | LINK alanını belirtir. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | LISTNUM alanını belirtir. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | MACROBUTTON alanını belirtir. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | MERGEBARCODE alanını belirtir. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | MERGEFIELD alanını belirtir. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | MERGEREC alanını belirtir. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | MERGESEQ alanını belirtir. |
| [FIELD_NEXT](#FIELD-NEXT) | NEXT alanını belirtir. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | NEXTIF alanını belirtir. |
| [FIELD_NONE](#FIELD-NONE) | Alan türü belirtilmemiş veya bilinmiyor. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | NOTEREF alanını belirtir. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | NUMCHARS alanını belirtir. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | NUMPAGES alanını belirtir. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | NUMWORDS alanını belirtir. |
| [FIELD_OCX](#FIELD-OCX) | OCX alanını belirtir. |
| [FIELD_PAGE](#FIELD-PAGE) | PAGE alanını belirtir. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | PAGEREF alanını belirtir. |
| [FIELD_PRINT](#FIELD-PRINT) | PRINT alanını belirtir. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | PRINTDATE alanını belirtir. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | PRIVATE alanını belirtir. |
| [FIELD_QUOTE](#FIELD-QUOTE) | QUOTE alanını belirtir. |
| [FIELD_REF](#FIELD-REF) | REF alanını belirtir. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | RD alanını belirtir. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | Bu alanın, anahtar kelimenin atlandığı bir REF alanını temsil ettiğini belirtir. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | REVNUM alanını belirtir. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | SAVEDATE alanını belirtir. |
| [FIELD_SECTION](#FIELD-SECTION) | SECTION alanını belirtir. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | SECTIONPAGES alanını belirtir. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | SEQ alanını belirtir. |
| [FIELD_SET](#FIELD-SET) | SET alanını belirtir. |
| [FIELD_SHAPE](#FIELD-SHAPE) | SHAPE alanını belirtir. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | SKIPIF alanını belirtir. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | STYLEREF alanını belirtir. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | SUBJECT alanını belirtir. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | SYMBOL alanını belirtir. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | TEMPLATE alanını belirtir. |
| [FIELD_TIME](#FIELD-TIME) | TIME alanını belirtir. |
| [FIELD_TITLE](#FIELD-TITLE) | TITLE alanını belirtir. |
| [FIELD_TOA](#FIELD-TOA) | TOA alanını belirtir. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | TA alanını belirtir. |
| [FIELD_TOC](#FIELD-TOC) | TOC alanını belirtir. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | TC alanını belirtir. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | USERADDRESS alanını belirtir. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | USERINITIALS alanını belirtir. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | USERNAME alanını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


ADDIN alanını belirtir.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


ADDRESSBLOCK alanını belirtir.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


ADVANCE alanını belirtir.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


ASK alanını belirtir.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


AUTHOR alanını belirtir.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


AUTONUM alanını belirtir.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


AUTONUMLGL alanını belirtir.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


AUTONUMOUT alanını belirtir.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


AUTOTEXT alanını belirtir.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


AUTOTEXTLIST alanını belirtir.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


BARCODE alanını belirtir.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


BIBLIOGRAPHY alanını belirtir.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


BIDIOUTLINE alanını belirtir.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


Alanın ayrıştırılamadığını belirtir.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


CITATION alanını belirtir.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


COMMENTS alanını belirtir.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


COMPARE alanını belirtir.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


CREATEDATE alanını belirtir.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


DATA alanını belirtir.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


DATABASE alanını belirtir.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


DATE alanını belirtir.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


DDE alanını belirtir.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


DDEAUTO alanını belirtir.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


DISPLAYBARCODE alanını belirtir.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


DOCPROPERTY alanını belirtir.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


DOCVARIABLE alanını belirtir.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


EDITTIME alanını belirtir.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


EMBED alanını belirtir.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


EQ alanını belirtir.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


FILENAME alanını belirtir.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


FILESIZE alanını belirtir.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


FILLIN alanını belirtir.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


FOOTNOTEREF alanını belirtir.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


= (formül) alanını belirtir.

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


FORMCHECKBOX alanını belirtir.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


FORMDROPDOWN alanını belirtir.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


FORMTEXT alanını belirtir.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


GLOSSARY alanını belirtir.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


GOTOBUTTON alanını belirtir.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


GREETINGLINE alanını belirtir.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


HTML denetimini temsil eden alanı belirtir.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


HYPERLINK alanını belirtir.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


IF alanını belirtir.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


IMPORT alanını belirtir.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


INCLUDE alanını belirtir.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


INCLUDEPICTURE alanını belirtir.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


INCLUDETEXT alanını belirtir.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


INDEX alanını belirtir.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


XE alanını belirtir.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


INFO alanını belirtir.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


KEYWORDS alanını belirtir.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


LASTSAVEDBY alanını belirtir.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


LINK alanını belirtir.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


LISTNUM alanını belirtir.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


MACROBUTTON alanını belirtir.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


MERGEBARCODE alanını belirtir.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


MERGEFIELD alanını belirtir.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


MERGEREC alanını belirtir.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


MERGESEQ alanını belirtir.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


NEXT alanını belirtir.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


NEXTIF alanını belirtir.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


Alan türü belirtilmemiş veya bilinmiyor.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


NOTEREF alanını belirtir.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


NUMCHARS alanını belirtir.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


NUMPAGES alanını belirtir.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


NUMWORDS alanını belirtir.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


OCX alanını belirtir.

Normalde, Aspose.Words bir ActiveX denetimini bir [Shape](../../com.aspose.words/shape/) nesnesi olarak temsil eder, ancak bazı belgelerde, bir denetimin verisi yoksa ve/veya geçersiz görünüyorsa, bu bir alan olarak temsil edilir.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


PAGE alanını belirtir.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


PAGEREF alanını belirtir.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


PRINT alanını belirtir.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


PRINTDATE alanını belirtir.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


PRIVATE alanını belirtir.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


QUOTE alanını belirtir.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


REF alanını belirtir.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


RD alanını belirtir.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


Bu alanın, anahtar kelimenin atlandığı bir REF alanını temsil ettiğini belirtir.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


REVNUM alanını belirtir.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


SAVEDATE alanını belirtir.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


SECTION alanını belirtir.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


SECTIONPAGES alanını belirtir.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


SEQ alanını belirtir.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


SET alanını belirtir.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


SHAPE alanını belirtir.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


SKIPIF alanını belirtir.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


STYLEREF alanını belirtir.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


SUBJECT alanını belirtir.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


SYMBOL alanını belirtir.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


TEMPLATE alanını belirtir.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


TIME alanını belirtir.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


TITLE alanını belirtir.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


TOA alanını belirtir.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


TA alanını belirtir.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


TOC alanını belirtir.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


TC alanını belirtir.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


USERADDRESS alanını belirtir.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


USERINITIALS alanını belirtir.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


USERNAME alanını belirtir.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
