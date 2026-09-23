---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words per Java"
description: "Specifica i tipi di campo di Microsoft Word in Java."
type: docs
weight: 299
url: /it/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

Specifica i tipi di campo di Microsoft Word.

 **Examples:** 

Mostra come inserire un campo in un documento usando un codice di campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Mostra come lavorare con un nodo FieldStart.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | Specifica il campo ADDIN. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | Specifica il campo ADDRESSBLOCK. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | Specifica il campo ADVANCE. |
| [FIELD_ASK](#FIELD-ASK) | Specifica il campo ASK. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | Specifica il campo AUTHOR. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | Specifica il campo AUTONUM. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | Specifica il campo AUTONUMLGL. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | Specifica il campo AUTONUMOUT. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | Specifica il campo AUTOTEXT. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | Specifica il campo AUTOTEXTLIST. |
| [FIELD_BARCODE](#FIELD-BARCODE) | Specifica il campo BARCODE. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | Specifica il campo BIBLIOGRAPHY. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | Specifica il campo BIDIOUTLINE. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | Specifica che il campo non è stato analizzato. |
| [FIELD_CITATION](#FIELD-CITATION) | Specifica il campo CITATION. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | Specifica il campo COMMENTS. |
| [FIELD_COMPARE](#FIELD-COMPARE) | Specifica il campo COMPARE. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | Specifica il campo CREATEDATE. |
| [FIELD_DATA](#FIELD-DATA) | Specifica il campo DATA. |
| [FIELD_DATABASE](#FIELD-DATABASE) | Specifica il campo DATABASE. |
| [FIELD_DATE](#FIELD-DATE) | Specifica il campo DATE. |
| [FIELD_DDE](#FIELD-DDE) | Specifica il campo DDE. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | Specifica il campo DDEAUTO. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | Specifica il campo DISPLAYBARCODE. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | Specifica il campo DOCPROPERTY. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | Specifica il campo DOCVARIABLE. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | Specifica il campo EDITTIME. |
| [FIELD_EMBED](#FIELD-EMBED) | Specifica il campo EMBED. |
| [FIELD_EQUATION](#FIELD-EQUATION) | Specifica il campo EQ. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | Specifica il campo FILENAME. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | Specifica il campo FILESIZE. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | Specifica il campo FILLIN. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | Specifica il campo FOOTNOTEREF. |
| [FIELD_FORMULA](#FIELD-FORMULA) | Specifica il campo = (formula). |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | Specifica il campo FORMCHECKBOX. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | Specifica il campo FORMDROPDOWN. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | Specifica il campo FORMTEXT. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | Specifica il campo GLOSSARY. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | Specifica il campo GOTOBUTTON. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | Specifica il campo GREETINGLINE. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | Specifica il campo che rappresenta un controllo HTML. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | Specifica il campo HYPERLINK. |
| [FIELD_IF](#FIELD-IF) | Specifica il campo IF. |
| [FIELD_IMPORT](#FIELD-IMPORT) | Specifica il campo IMPORT. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | Specifica il campo INCLUDE. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | Specifica il campo INCLUDEPICTURE. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | Specifica il campo INCLUDETEXT. |
| [FIELD_INDEX](#FIELD-INDEX) | Specifica il campo INDEX. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | Specifica il campo XE. |
| [FIELD_INFO](#FIELD-INFO) | Specifica il campo INFO. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | Specifica il campo KEYWORDS. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | Specifica il campo LASTSAVEDBY. |
| [FIELD_LINK](#FIELD-LINK) | Specifica il campo LINK. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | Specifica il campo LISTNUM. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | Specifica il campo MACROBUTTON. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | Specifica il campo MERGEBARCODE. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | Specifica il campo MERGEFIELD. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | Specifica il campo MERGEREC. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | Specifica il campo MERGESEQ. |
| [FIELD_NEXT](#FIELD-NEXT) | Specifica il campo NEXT. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | Specifica il campo NEXTIF. |
| [FIELD_NONE](#FIELD-NONE) | Il tipo di campo non è specificato o è sconosciuto. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | Specifica il campo NOTEREF. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | Specifica il campo NUMCHARS. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | Specifica il campo NUMPAGES. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | Specifica il campo NUMWORDS. |
| [FIELD_OCX](#FIELD-OCX) | Specifica il campo OCX. |
| [FIELD_PAGE](#FIELD-PAGE) | Specifica il campo PAGE. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | Specifica il campo PAGEREF. |
| [FIELD_PRINT](#FIELD-PRINT) | Specifica il campo PRINT. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | Specifica il campo PRINTDATE. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | Specifica il campo PRIVATE. |
| [FIELD_QUOTE](#FIELD-QUOTE) | Specifica il campo QUOTE. |
| [FIELD_REF](#FIELD-REF) | Specifica il campo REF. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | Specifica il campo RD. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | Specifica che il campo rappresenta un campo REF dove la parola chiave è stata omessa. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | Specifica il campo REVNUM. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | Specifica il campo SAVEDATE. |
| [FIELD_SECTION](#FIELD-SECTION) | Specifica il campo SECTION. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | Specifica il campo SECTIONPAGES. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | Specifica il campo SEQ. |
| [FIELD_SET](#FIELD-SET) | Specifica il campo SET. |
| [FIELD_SHAPE](#FIELD-SHAPE) | Specifica il campo SHAPE. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | Specifica il campo SKIPIF. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | Specifica il campo STYLEREF. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | Specifica il campo SUBJECT. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | Specifica il campo SYMBOL. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | Specifica il campo TEMPLATE. |
| [FIELD_TIME](#FIELD-TIME) | Specifica il campo TIME. |
| [FIELD_TITLE](#FIELD-TITLE) | Specifica il campo TITLE. |
| [FIELD_TOA](#FIELD-TOA) | Specifica il campo TOA. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | Specifica il campo TA. |
| [FIELD_TOC](#FIELD-TOC) | Specifica il campo TOC. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | Specifica il campo TC. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | Specifica il campo USERADDRESS. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | Specifica il campo USERINITIALS. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | Specifica il campo USERNAME. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


Specifica il campo ADDIN.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


Specifica il campo ADDRESSBLOCK.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


Specifica il campo ADVANCE.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


Specifica il campo ASK.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


Specifica il campo AUTHOR.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


Specifica il campo AUTONUM.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


Specifica il campo AUTONUMLGL.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


Specifica il campo AUTONUMOUT.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


Specifica il campo AUTOTEXT.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


Specifica il campo AUTOTEXTLIST.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


Specifica il campo BARCODE.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


Specifica il campo BIBLIOGRAPHY.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


Specifica il campo BIDIOUTLINE.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


Specifica che il campo non è stato analizzato.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


Specifica il campo CITATION.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


Specifica il campo COMMENTS.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


Specifica il campo COMPARE.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


Specifica il campo CREATEDATE.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


Specifica il campo DATA.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


Specifica il campo DATABASE.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


Specifica il campo DATE.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


Specifica il campo DDE.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


Specifica il campo DDEAUTO.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


Specifica il campo DISPLAYBARCODE.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


Specifica il campo DOCPROPERTY.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


Specifica il campo DOCVARIABLE.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


Specifica il campo EDITTIME.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


Specifica il campo EMBED.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


Specifica il campo EQ.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


Specifica il campo FILENAME.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


Specifica il campo FILESIZE.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


Specifica il campo FILLIN.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


Specifica il campo FOOTNOTEREF.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


Specifica il campo = (formula).

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


Specifica il campo FORMCHECKBOX.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


Specifica il campo FORMDROPDOWN.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


Specifica il campo FORMTEXT.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


Specifica il campo GLOSSARY.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


Specifica il campo GOTOBUTTON.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


Specifica il campo GREETINGLINE.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


Specifica il campo che rappresenta un controllo HTML.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


Specifica il campo HYPERLINK.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


Specifica il campo IF.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


Specifica il campo IMPORT.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


Specifica il campo INCLUDE.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


Specifica il campo INCLUDEPICTURE.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


Specifica il campo INCLUDETEXT.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


Specifica il campo INDEX.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


Specifica il campo XE.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


Specifica il campo INFO.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


Specifica il campo KEYWORDS.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


Specifica il campo LASTSAVEDBY.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


Specifica il campo LINK.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


Specifica il campo LISTNUM.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


Specifica il campo MACROBUTTON.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


Specifica il campo MERGEBARCODE.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


Specifica il campo MERGEFIELD.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


Specifica il campo MERGEREC.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


Specifica il campo MERGESEQ.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


Specifica il campo NEXT.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


Specifica il campo NEXTIF.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


Il tipo di campo non è specificato o è sconosciuto.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


Specifica il campo NOTEREF.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


Specifica il campo NUMCHARS.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


Specifica il campo NUMPAGES.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


Specifica il campo NUMWORDS.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


Specifica il campo OCX.

Normalmente, Aspose.Words rappresenterà un controllo ActiveX come un oggetto [Shape](../../com.aspose.words/shape/), ma per alcuni documenti, dove un controllo non ha dati e/o sembra non valido, verrà rappresentato come un campo.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


Specifica il campo PAGE.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


Specifica il campo PAGEREF.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


Specifica il campo PRINT.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


Specifica il campo PRINTDATE.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


Specifica il campo PRIVATE.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


Specifica il campo QUOTE.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


Specifica il campo REF.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


Specifica il campo RD.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


Specifica che il campo rappresenta un campo REF dove la parola chiave è stata omessa.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


Specifica il campo REVNUM.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


Specifica il campo SAVEDATE.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


Specifica il campo SECTION.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


Specifica il campo SECTIONPAGES.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


Specifica il campo SEQ.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


Specifica il campo SET.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


Specifica il campo SHAPE.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


Specifica il campo SKIPIF.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


Specifica il campo STYLEREF.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


Specifica il campo SUBJECT.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


Specifica il campo SYMBOL.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


Specifica il campo TEMPLATE.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


Specifica il campo TIME.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


Specifica il campo TITLE.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


Specifica il campo TOA.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


Specifica il campo TA.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


Specifica il campo TOC.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


Specifica il campo TC.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


Specifica il campo USERADDRESS.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


Specifica il campo USERINITIALS.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


Specifica il campo USERNAME.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
