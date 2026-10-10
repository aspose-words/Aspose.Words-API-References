---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words für Java"
description: "Gibt die Microsoft‑Word-Feldtypen in Java an."
type: docs
weight: 299
url: /de/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

Gibt Microsoft Word-Feldtypen an.

 **Examples:** 

Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Zeigt, wie man mit einem FieldStart‑Knoten arbeitet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | Gibt das ADDIN-Feld an. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | Gibt das ADDRESSBLOCK-Feld an. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | Gibt das ADVANCE-Feld an. |
| [FIELD_ASK](#FIELD-ASK) | Gibt das ASK-Feld an. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | Gibt das AUTHOR-Feld an. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | Gibt das AUTONUM-Feld an. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | Gibt das AUTONUMLGL-Feld an. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | Gibt das AUTONUMOUT-Feld an. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | Gibt das AUTOTEXT-Feld an. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | Gibt das AUTOTEXTLIST-Feld an. |
| [FIELD_BARCODE](#FIELD-BARCODE) | Gibt das BARCODE-Feld an. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | Gibt das BIBLIOGRAPHY-Feld an. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | Gibt das BIDIOUTLINE-Feld an. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | Gibt an, dass das Feld nicht geparst werden konnte. |
| [FIELD_CITATION](#FIELD-CITATION) | Gibt das CITATION-Feld an. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | Gibt das COMMENTS-Feld an. |
| [FIELD_COMPARE](#FIELD-COMPARE) | Gibt das COMPARE-Feld an. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | Gibt das CREATEDATE-Feld an. |
| [FIELD_DATA](#FIELD-DATA) | Gibt das DATA-Feld an. |
| [FIELD_DATABASE](#FIELD-DATABASE) | Gibt das DATABASE-Feld an. |
| [FIELD_DATE](#FIELD-DATE) | Gibt das DATE-Feld an. |
| [FIELD_DDE](#FIELD-DDE) | Gibt das DDE-Feld an. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | Gibt das DDEAUTO-Feld an. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | Gibt das DISPLAYBARCODE-Feld an. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | Gibt das DOCPROPERTY-Feld an. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | Gibt das DOCVARIABLE-Feld an. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | Gibt das EDITTIME-Feld an. |
| [FIELD_EMBED](#FIELD-EMBED) | Gibt das EMBED-Feld an. |
| [FIELD_EQUATION](#FIELD-EQUATION) | Gibt das EQ-Feld an. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | Gibt das FILENAME-Feld an. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | Gibt das FILESIZE-Feld an. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | Gibt das FILLIN-Feld an. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | Gibt das FOOTNOTEREF-Feld an. |
| [FIELD_FORMULA](#FIELD-FORMULA) | Gibt das = (Formel)-Feld an. |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | Gibt das FORMCHECKBOX-Feld an. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | Gibt das FORMDROPDOWN-Feld an. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | Gibt das FORMTEXT-Feld an. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | Gibt das GLOSSARY-Feld an. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | Gibt das GOTOBUTTON-Feld an. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | Gibt das GREETINGLINE-Feld an. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | Gibt das Feld an, das ein HTML-Steuerelement darstellt. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | Gibt das HYPERLINK-Feld an. |
| [FIELD_IF](#FIELD-IF) | Gibt das IF-Feld an. |
| [FIELD_IMPORT](#FIELD-IMPORT) | Gibt das IMPORT-Feld an. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | Gibt das INCLUDE-Feld an. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | Gibt das INCLUDEPICTURE-Feld an. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | Gibt das INCLUDETEXT-Feld an. |
| [FIELD_INDEX](#FIELD-INDEX) | Gibt das INDEX-Feld an. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | Gibt das XE-Feld an. |
| [FIELD_INFO](#FIELD-INFO) | Gibt das INFO-Feld an. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | Gibt das Feld KEYWORDS an. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | Gibt das Feld LASTSAVEDBY an. |
| [FIELD_LINK](#FIELD-LINK) | Gibt das Feld LINK an. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | Gibt das Feld LISTNUM an. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | Gibt das Feld MACROBUTTON an. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | Gibt das Feld MERGEBARCODE an. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | Gibt das Feld MERGEFIELD an. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | Gibt das Feld MERGEREC an. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | Gibt das Feld MERGESEQ an. |
| [FIELD_NEXT](#FIELD-NEXT) | Gibt das Feld NEXT an. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | Gibt das Feld NEXTIF an. |
| [FIELD_NONE](#FIELD-NONE) | Feldtyp ist nicht angegeben oder unbekannt. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | Gibt das Feld NOTEREF an. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | Gibt das Feld NUMCHARS an. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | Gibt das Feld NUMPAGES an. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | Gibt das Feld NUMWORDS an. |
| [FIELD_OCX](#FIELD-OCX) | Gibt das Feld OCX an. |
| [FIELD_PAGE](#FIELD-PAGE) | Gibt das Feld PAGE an. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | Gibt das Feld PAGEREF an. |
| [FIELD_PRINT](#FIELD-PRINT) | Gibt das Feld PRINT an. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | Gibt das Feld PRINTDATE an. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | Gibt das Feld PRIVATE an. |
| [FIELD_QUOTE](#FIELD-QUOTE) | Gibt das Feld QUOTE an. |
| [FIELD_REF](#FIELD-REF) | Gibt das Feld REF an. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | Gibt das Feld RD an. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | Gibt an, dass das Feld ein REF-Feld darstellt, bei dem das Schlüsselwort weggelassen wurde. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | Gibt das REVNUM-Feld an. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | Gibt das SAVEDATE-Feld an. |
| [FIELD_SECTION](#FIELD-SECTION) | Gibt das SECTION-Feld an. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | Gibt das SECTIONPAGES-Feld an. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | Gibt das SEQ-Feld an. |
| [FIELD_SET](#FIELD-SET) | Gibt das SET-Feld an. |
| [FIELD_SHAPE](#FIELD-SHAPE) | Gibt das SHAPE-Feld an. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | Gibt das SKIPIF-Feld an. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | Gibt das STYLEREF-Feld an. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | Gibt das SUBJECT-Feld an. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | Gibt das SYMBOL-Feld an. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | Gibt das TEMPLATE-Feld an. |
| [FIELD_TIME](#FIELD-TIME) | Gibt das TIME-Feld an. |
| [FIELD_TITLE](#FIELD-TITLE) | Gibt das TITLE-Feld an. |
| [FIELD_TOA](#FIELD-TOA) | Gibt das TOA-Feld an. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | Gibt das TA-Feld an. |
| [FIELD_TOC](#FIELD-TOC) | Gibt das TOC-Feld an. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | Gibt das TC-Feld an. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | Gibt das USERADDRESS-Feld an. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | Gibt das USERINITIALS-Feld an. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | Gibt das USERNAME-Feld an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


Gibt das ADDIN-Feld an.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


Gibt das ADDRESSBLOCK-Feld an.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


Gibt das ADVANCE-Feld an.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


Gibt das ASK-Feld an.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


Gibt das AUTHOR-Feld an.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


Gibt das AUTONUM-Feld an.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


Gibt das AUTONUMLGL-Feld an.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


Gibt das AUTONUMOUT-Feld an.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


Gibt das AUTOTEXT-Feld an.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


Gibt das AUTOTEXTLIST-Feld an.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


Gibt das BARCODE-Feld an.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


Gibt das BIBLIOGRAPHY-Feld an.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


Gibt das BIDIOUTLINE-Feld an.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


Gibt an, dass das Feld nicht geparst werden konnte.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


Gibt das CITATION-Feld an.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


Gibt das COMMENTS-Feld an.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


Gibt das COMPARE-Feld an.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


Gibt das CREATEDATE-Feld an.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


Gibt das DATA-Feld an.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


Gibt das DATABASE-Feld an.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


Gibt das DATE-Feld an.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


Gibt das DDE-Feld an.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


Gibt das DDEAUTO-Feld an.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


Gibt das DISPLAYBARCODE-Feld an.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


Gibt das DOCPROPERTY-Feld an.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


Gibt das DOCVARIABLE-Feld an.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


Gibt das EDITTIME-Feld an.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


Gibt das EMBED-Feld an.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


Gibt das EQ-Feld an.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


Gibt das FILENAME-Feld an.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


Gibt das FILESIZE-Feld an.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


Gibt das FILLIN-Feld an.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


Gibt das FOOTNOTEREF-Feld an.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


Gibt das = (Formel)-Feld an.

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


Gibt das FORMCHECKBOX-Feld an.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


Gibt das FORMDROPDOWN-Feld an.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


Gibt das FORMTEXT-Feld an.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


Gibt das GLOSSARY-Feld an.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


Gibt das GOTOBUTTON-Feld an.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


Gibt das GREETINGLINE-Feld an.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


Gibt das Feld an, das ein HTML-Steuerelement darstellt.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


Gibt das HYPERLINK-Feld an.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


Gibt das IF-Feld an.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


Gibt das IMPORT-Feld an.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


Gibt das INCLUDE-Feld an.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


Gibt das INCLUDEPICTURE-Feld an.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


Gibt das INCLUDETEXT-Feld an.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


Gibt das INDEX-Feld an.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


Gibt das XE-Feld an.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


Gibt das INFO-Feld an.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


Gibt das Feld KEYWORDS an.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


Gibt das Feld LASTSAVEDBY an.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


Gibt das Feld LINK an.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


Gibt das Feld LISTNUM an.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


Gibt das Feld MACROBUTTON an.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


Gibt das Feld MERGEBARCODE an.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


Gibt das Feld MERGEFIELD an.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


Gibt das Feld MERGEREC an.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


Gibt das Feld MERGESEQ an.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


Gibt das Feld NEXT an.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


Gibt das Feld NEXTIF an.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


Feldtyp ist nicht angegeben oder unbekannt.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


Gibt das Feld NOTEREF an.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


Gibt das Feld NUMCHARS an.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


Gibt das Feld NUMPAGES an.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


Gibt das Feld NUMWORDS an.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


Gibt das Feld OCX an.

Normalerweise stellt Aspose.Words ein ActiveX-Steuerelement als ein [Shape](../../com.aspose.words/shape/)‑Objekt dar, aber bei einigen Dokumenten, bei denen ein Steuerelement keine Daten hat und/oder ungültig zu sein scheint, wird es als Feld dargestellt.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


Gibt das Feld PAGE an.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


Gibt das Feld PAGEREF an.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


Gibt das Feld PRINT an.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


Gibt das Feld PRINTDATE an.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


Gibt das Feld PRIVATE an.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


Gibt das Feld QUOTE an.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


Gibt das Feld REF an.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


Gibt das Feld RD an.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


Gibt an, dass das Feld ein REF-Feld darstellt, bei dem das Schlüsselwort weggelassen wurde.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


Gibt das REVNUM-Feld an.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


Gibt das SAVEDATE-Feld an.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


Gibt das SECTION-Feld an.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


Gibt das SECTIONPAGES-Feld an.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


Gibt das SEQ-Feld an.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


Gibt das SET-Feld an.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


Gibt das SHAPE-Feld an.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


Gibt das SKIPIF-Feld an.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


Gibt das STYLEREF-Feld an.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


Gibt das SUBJECT-Feld an.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


Gibt das SYMBOL-Feld an.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


Gibt das TEMPLATE-Feld an.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


Gibt das TIME-Feld an.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


Gibt das TITLE-Feld an.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


Gibt das TOA-Feld an.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


Gibt das TA-Feld an.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


Gibt das TOC-Feld an.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


Gibt das TC-Feld an.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


Gibt das USERADDRESS-Feld an.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


Gibt das USERINITIALS-Feld an.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


Gibt das USERNAME-Feld an.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
