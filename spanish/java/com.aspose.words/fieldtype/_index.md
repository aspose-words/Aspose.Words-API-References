---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words para Java"
description: "Especifica los tipos de campos de Microsoft Word en Java."
type: docs
weight: 299
url: /es/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

Especifica los tipos de campos de Microsoft Word.

 **Examples:** 

Muestra cómo insertar un campo en un documento usando un código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Muestra cómo trabajar con un nodo FieldStart.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | Especifica el campo ADDIN. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | Especifica el campo ADDRESSBLOCK. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | Especifica el campo ADVANCE. |
| [FIELD_ASK](#FIELD-ASK) | Especifica el campo ASK. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | Especifica el campo AUTHOR. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | Especifica el campo AUTONUM. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | Especifica el campo AUTONUMLGL. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | Especifica el campo AUTONUMOUT. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | Especifica el campo AUTOTEXT. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | Especifica el campo AUTOTEXTLIST. |
| [FIELD_BARCODE](#FIELD-BARCODE) | Especifica el campo BARCODE. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | Especifica el campo BIBLIOGRAPHY. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | Especifica el campo BIDIOUTLINE. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | Especifica que el campo no pudo ser analizado. |
| [FIELD_CITATION](#FIELD-CITATION) | Especifica el campo CITATION. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | Especifica el campo COMMENTS. |
| [FIELD_COMPARE](#FIELD-COMPARE) | Especifica el campo COMPARE. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | Especifica el campo CREATEDATE. |
| [FIELD_DATA](#FIELD-DATA) | Especifica el campo DATA. |
| [FIELD_DATABASE](#FIELD-DATABASE) | Especifica el campo DATABASE. |
| [FIELD_DATE](#FIELD-DATE) | Especifica el campo DATE. |
| [FIELD_DDE](#FIELD-DDE) | Especifica el campo DDE. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | Especifica el campo DDEAUTO. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | Especifica el campo DISPLAYBARCODE. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | Especifica el campo DOCPROPERTY. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | Especifica el campo DOCVARIABLE. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | Especifica el campo EDITTIME. |
| [FIELD_EMBED](#FIELD-EMBED) | Especifica el campo EMBED. |
| [FIELD_EQUATION](#FIELD-EQUATION) | Especifica el campo EQ. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | Especifica el campo FILENAME. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | Especifica el campo FILESIZE. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | Especifica el campo FILLIN. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | Especifica el campo FOOTNOTEREF. |
| [FIELD_FORMULA](#FIELD-FORMULA) | Especifica el campo = (formula). |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | Especifica el campo FORMCHECKBOX. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | Especifica el campo FORMDROPDOWN. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | Especifica el campo FORMTEXT. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | Especifica el campo GLOSSARY. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | Especifica el campo GOTOBUTTON. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | Especifica el campo GREETINGLINE. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | Especifica el campo que representa un control HTML. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | Especifica el campo HYPERLINK. |
| [FIELD_IF](#FIELD-IF) | Especifica el campo IF. |
| [FIELD_IMPORT](#FIELD-IMPORT) | Especifica el campo IMPORT. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | Especifica el campo INCLUDE. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | Especifica el campo INCLUDEPICTURE. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | Especifica el campo INCLUDETEXT. |
| [FIELD_INDEX](#FIELD-INDEX) | Especifica el campo INDEX. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | Especifica el campo XE. |
| [FIELD_INFO](#FIELD-INFO) | Especifica el campo INFO. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | Especifica el campo KEYWORDS. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | Especifica el campo LASTSAVEDBY. |
| [FIELD_LINK](#FIELD-LINK) | Especifica el campo LINK. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | Especifica el campo LISTNUM. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | Especifica el campo MACROBUTTON. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | Especifica el campo MERGEBARCODE. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | Especifica el campo MERGEFIELD. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | Especifica el campo MERGEREC. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | Especifica el campo MERGESEQ. |
| [FIELD_NEXT](#FIELD-NEXT) | Especifica el campo NEXT. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | Especifica el campo NEXTIF. |
| [FIELD_NONE](#FIELD-NONE) | El tipo de campo no está especificado o es desconocido. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | Especifica el campo NOTEREF. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | Especifica el campo NUMCHARS. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | Especifica el campo NUMPAGES. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | Especifica el campo NUMWORDS. |
| [FIELD_OCX](#FIELD-OCX) | Especifica el campo OCX. |
| [FIELD_PAGE](#FIELD-PAGE) | Especifica el campo PAGE. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | Especifica el campo PAGEREF. |
| [FIELD_PRINT](#FIELD-PRINT) | Especifica el campo PRINT. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | Especifica el campo PRINTDATE. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | Especifica el campo PRIVATE. |
| [FIELD_QUOTE](#FIELD-QUOTE) | Especifica el campo QUOTE. |
| [FIELD_REF](#FIELD-REF) | Especifica el campo REF. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | Especifica el campo RD. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | Especifica que el campo representa un campo REF donde se ha omitido la palabra clave. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | Especifica el campo REVNUM. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | Especifica el campo SAVEDATE. |
| [FIELD_SECTION](#FIELD-SECTION) | Especifica el campo SECTION. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | Especifica el campo SECTIONPAGES. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | Especifica el campo SEQ. |
| [FIELD_SET](#FIELD-SET) | Especifica el campo SET. |
| [FIELD_SHAPE](#FIELD-SHAPE) | Especifica el campo SHAPE. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | Especifica el campo SKIPIF. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | Especifica el campo STYLEREF. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | Especifica el campo SUBJECT. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | Especifica el campo SYMBOL. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | Especifica el campo TEMPLATE. |
| [FIELD_TIME](#FIELD-TIME) | Especifica el campo TIME. |
| [FIELD_TITLE](#FIELD-TITLE) | Especifica el campo TITLE. |
| [FIELD_TOA](#FIELD-TOA) | Especifica el campo TOA. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | Especifica el campo TA. |
| [FIELD_TOC](#FIELD-TOC) | Especifica el campo TOC. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | Especifica el campo TC. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | Especifica el campo USERADDRESS. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | Especifica el campo USERINITIALS. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | Especifica el campo USERNAME. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


Especifica el campo ADDIN.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


Especifica el campo ADDRESSBLOCK.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


Especifica el campo ADVANCE.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


Especifica el campo ASK.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


Especifica el campo AUTHOR.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


Especifica el campo AUTONUM.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


Especifica el campo AUTONUMLGL.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


Especifica el campo AUTONUMOUT.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


Especifica el campo AUTOTEXT.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


Especifica el campo AUTOTEXTLIST.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


Especifica el campo BARCODE.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


Especifica el campo BIBLIOGRAPHY.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


Especifica el campo BIDIOUTLINE.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


Especifica que el campo no pudo ser analizado.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


Especifica el campo CITATION.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


Especifica el campo COMMENTS.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


Especifica el campo COMPARE.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


Especifica el campo CREATEDATE.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


Especifica el campo DATA.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


Especifica el campo DATABASE.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


Especifica el campo DATE.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


Especifica el campo DDE.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


Especifica el campo DDEAUTO.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


Especifica el campo DISPLAYBARCODE.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


Especifica el campo DOCPROPERTY.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


Especifica el campo DOCVARIABLE.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


Especifica el campo EDITTIME.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


Especifica el campo EMBED.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


Especifica el campo EQ.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


Especifica el campo FILENAME.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


Especifica el campo FILESIZE.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


Especifica el campo FILLIN.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


Especifica el campo FOOTNOTEREF.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


Especifica el campo = (formula).

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


Especifica el campo FORMCHECKBOX.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


Especifica el campo FORMDROPDOWN.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


Especifica el campo FORMTEXT.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


Especifica el campo GLOSSARY.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


Especifica el campo GOTOBUTTON.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


Especifica el campo GREETINGLINE.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


Especifica el campo que representa un control HTML.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


Especifica el campo HYPERLINK.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


Especifica el campo IF.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


Especifica el campo IMPORT.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


Especifica el campo INCLUDE.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


Especifica el campo INCLUDEPICTURE.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


Especifica el campo INCLUDETEXT.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


Especifica el campo INDEX.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


Especifica el campo XE.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


Especifica el campo INFO.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


Especifica el campo KEYWORDS.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


Especifica el campo LASTSAVEDBY.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


Especifica el campo LINK.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


Especifica el campo LISTNUM.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


Especifica el campo MACROBUTTON.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


Especifica el campo MERGEBARCODE.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


Especifica el campo MERGEFIELD.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


Especifica el campo MERGEREC.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


Especifica el campo MERGESEQ.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


Especifica el campo NEXT.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


Especifica el campo NEXTIF.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


El tipo de campo no está especificado o es desconocido.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


Especifica el campo NOTEREF.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


Especifica el campo NUMCHARS.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


Especifica el campo NUMPAGES.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


Especifica el campo NUMWORDS.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


Especifica el campo OCX.

Normalmente, Aspose.Words representará un control ActiveX como un objeto [Shape](../../com.aspose.words/shape/) , pero para algunos documentos, donde un control no tiene datos y/o parece ser inválido, se representará como un campo.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


Especifica el campo PAGE.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


Especifica el campo PAGEREF.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


Especifica el campo PRINT.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


Especifica el campo PRINTDATE.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


Especifica el campo PRIVATE.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


Especifica el campo QUOTE.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


Especifica el campo REF.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


Especifica el campo RD.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


Especifica que el campo representa un campo REF donde se ha omitido la palabra clave.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


Especifica el campo REVNUM.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


Especifica el campo SAVEDATE.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


Especifica el campo SECTION.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


Especifica el campo SECTIONPAGES.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


Especifica el campo SEQ.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


Especifica el campo SET.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


Especifica el campo SHAPE.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


Especifica el campo SKIPIF.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


Especifica el campo STYLEREF.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


Especifica el campo SUBJECT.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


Especifica el campo SYMBOL.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


Especifica el campo TEMPLATE.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


Especifica el campo TIME.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


Especifica el campo TITLE.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


Especifica el campo TOA.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


Especifica el campo TA.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


Especifica el campo TOC.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


Especifica el campo TC.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


Especifica el campo USERADDRESS.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


Especifica el campo USERINITIALS.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


Especifica el campo USERNAME.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
