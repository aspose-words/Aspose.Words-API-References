---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words pour Java"
description: "Spécifie les types de champs Microsoft Word en Java."
type: docs
weight: 299
url: /fr/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

Spécifie les types de champs Microsoft Word.

 **Examples:** 

Montre comment insérer un champ dans un document en utilisant un code de champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Montre comment travailler avec un nœud FieldStart.

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
## Champs

| Champ | Description |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | Spécifie le champ ADDIN. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | Spécifie le champ ADDRESSBLOCK. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | Spécifie le champ ADVANCE. |
| [FIELD_ASK](#FIELD-ASK) | Spécifie le champ ASK. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | Spécifie le champ AUTHOR. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | Spécifie le champ AUTONUM. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | Spécifie le champ AUTONUMLGL. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | Spécifie le champ AUTONUMOUT. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | Spécifie le champ AUTOTEXT. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | Spécifie le champ AUTOTEXTLIST. |
| [FIELD_BARCODE](#FIELD-BARCODE) | Spécifie le champ BARCODE. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | Spécifie le champ BIBLIOGRAPHY. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | Spécifie le champ BIDIOUTLINE. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | Spécifie que le champ n'a pas pu être analysé. |
| [FIELD_CITATION](#FIELD-CITATION) | Spécifie le champ CITATION. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | Spécifie le champ COMMENTS. |
| [FIELD_COMPARE](#FIELD-COMPARE) | Spécifie le champ COMPARE. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | Spécifie le champ CREATEDATE. |
| [FIELD_DATA](#FIELD-DATA) | Spécifie le champ DATA. |
| [FIELD_DATABASE](#FIELD-DATABASE) | Spécifie le champ DATABASE. |
| [FIELD_DATE](#FIELD-DATE) | Spécifie le champ DATE. |
| [FIELD_DDE](#FIELD-DDE) | Spécifie le champ DDE. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | Spécifie le champ DDEAUTO. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | Spécifie le champ DISPLAYBARCODE. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | Spécifie le champ DOCPROPERTY. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | Spécifie le champ DOCVARIABLE. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | Spécifie le champ EDITTIME. |
| [FIELD_EMBED](#FIELD-EMBED) | Spécifie le champ EMBED. |
| [FIELD_EQUATION](#FIELD-EQUATION) | Spécifie le champ EQ. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | Spécifie le champ FILENAME. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | Spécifie le champ FILESIZE. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | Spécifie le champ FILLIN. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | Spécifie le champ FOOTNOTEREF. |
| [FIELD_FORMULA](#FIELD-FORMULA) | Spécifie le champ = (formule). |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | Spécifie le champ FORMCHECKBOX. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | Spécifie le champ FORMDROPDOWN. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | Spécifie le champ FORMTEXT. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | Spécifie le champ GLOSSARY. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | Spécifie le champ GOTOBUTTON. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | Spécifie le champ GREETINGLINE. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | Spécifie le champ qui représente un contrôle HTML. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | Spécifie le champ HYPERLINK. |
| [FIELD_IF](#FIELD-IF) | Spécifie le champ IF. |
| [FIELD_IMPORT](#FIELD-IMPORT) | Spécifie le champ IMPORT. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | Spécifie le champ INCLUDE. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | Spécifie le champ INCLUDEPICTURE. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | Spécifie le champ INCLUDETEXT. |
| [FIELD_INDEX](#FIELD-INDEX) | Spécifie le champ INDEX. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | Spécifie le champ XE. |
| [FIELD_INFO](#FIELD-INFO) | Spécifie le champ INFO. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | Spécifie le champ KEYWORDS. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | Spécifie le champ LASTSAVEDBY. |
| [FIELD_LINK](#FIELD-LINK) | Spécifie le champ LINK. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | Spécifie le champ LISTNUM. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | Spécifie le champ MACROBUTTON. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | Spécifie le champ MERGEBARCODE. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | Spécifie le champ MERGEFIELD. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | Spécifie le champ MERGEREC. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | Spécifie le champ MERGESEQ. |
| [FIELD_NEXT](#FIELD-NEXT) | Spécifie le champ NEXT. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | Spécifie le champ NEXTIF. |
| [FIELD_NONE](#FIELD-NONE) | Le type de champ n'est pas spécifié ou inconnu. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | Spécifie le champ NOTEREF. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | Spécifie le champ NUMCHARS. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | Spécifie le champ NUMPAGES. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | Spécifie le champ NUMWORDS. |
| [FIELD_OCX](#FIELD-OCX) | Spécifie le champ OCX. |
| [FIELD_PAGE](#FIELD-PAGE) | Spécifie le champ PAGE. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | Spécifie le champ PAGEREF. |
| [FIELD_PRINT](#FIELD-PRINT) | Spécifie le champ PRINT. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | Spécifie le champ PRINTDATE. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | Spécifie le champ PRIVATE. |
| [FIELD_QUOTE](#FIELD-QUOTE) | Spécifie le champ QUOTE. |
| [FIELD_REF](#FIELD-REF) | Spécifie le champ REF. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | Spécifie le champ RD. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | Spécifie que le champ représente un champ REF où le mot‑clé a été omis. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | Spécifie le champ REVNUM. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | Spécifie le champ SAVEDATE. |
| [FIELD_SECTION](#FIELD-SECTION) | Spécifie le champ SECTION. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | Spécifie le champ SECTIONPAGES. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | Spécifie le champ SEQ. |
| [FIELD_SET](#FIELD-SET) | Spécifie le champ SET. |
| [FIELD_SHAPE](#FIELD-SHAPE) | Spécifie le champ SHAPE. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | Spécifie le champ SKIPIF. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | Spécifie le champ STYLEREF. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | Spécifie le champ SUBJECT. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | Spécifie le champ SYMBOL. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | Spécifie le champ TEMPLATE. |
| [FIELD_TIME](#FIELD-TIME) | Spécifie le champ TIME. |
| [FIELD_TITLE](#FIELD-TITLE) | Spécifie le champ TITLE. |
| [FIELD_TOA](#FIELD-TOA) | Spécifie le champ TOA. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | Spécifie le champ TA. |
| [FIELD_TOC](#FIELD-TOC) | Spécifie le champ TOC. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | Spécifie le champ TC. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | Spécifie le champ USERADDRESS. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | Spécifie le champ USERINITIALS. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | Spécifie le champ USERNAME. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


Spécifie le champ ADDIN.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


Spécifie le champ ADDRESSBLOCK.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


Spécifie le champ ADVANCE.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


Spécifie le champ ASK.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


Spécifie le champ AUTHOR.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


Spécifie le champ AUTONUM.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


Spécifie le champ AUTONUMLGL.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


Spécifie le champ AUTONUMOUT.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


Spécifie le champ AUTOTEXT.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


Spécifie le champ AUTOTEXTLIST.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


Spécifie le champ BARCODE.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


Spécifie le champ BIBLIOGRAPHY.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


Spécifie le champ BIDIOUTLINE.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


Spécifie que le champ n'a pas pu être analysé.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


Spécifie le champ CITATION.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


Spécifie le champ COMMENTS.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


Spécifie le champ COMPARE.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


Spécifie le champ CREATEDATE.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


Spécifie le champ DATA.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


Spécifie le champ DATABASE.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


Spécifie le champ DATE.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


Spécifie le champ DDE.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


Spécifie le champ DDEAUTO.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


Spécifie le champ DISPLAYBARCODE.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


Spécifie le champ DOCPROPERTY.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


Spécifie le champ DOCVARIABLE.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


Spécifie le champ EDITTIME.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


Spécifie le champ EMBED.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


Spécifie le champ EQ.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


Spécifie le champ FILENAME.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


Spécifie le champ FILESIZE.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


Spécifie le champ FILLIN.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


Spécifie le champ FOOTNOTEREF.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


Spécifie le champ = (formule).

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


Spécifie le champ FORMCHECKBOX.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


Spécifie le champ FORMDROPDOWN.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


Spécifie le champ FORMTEXT.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


Spécifie le champ GLOSSARY.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


Spécifie le champ GOTOBUTTON.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


Spécifie le champ GREETINGLINE.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


Spécifie le champ qui représente un contrôle HTML.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


Spécifie le champ HYPERLINK.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


Spécifie le champ IF.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


Spécifie le champ IMPORT.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


Spécifie le champ INCLUDE.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


Spécifie le champ INCLUDEPICTURE.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


Spécifie le champ INCLUDETEXT.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


Spécifie le champ INDEX.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


Spécifie le champ XE.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


Spécifie le champ INFO.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


Spécifie le champ KEYWORDS.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


Spécifie le champ LASTSAVEDBY.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


Spécifie le champ LINK.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


Spécifie le champ LISTNUM.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


Spécifie le champ MACROBUTTON.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


Spécifie le champ MERGEBARCODE.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


Spécifie le champ MERGEFIELD.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


Spécifie le champ MERGEREC.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


Spécifie le champ MERGESEQ.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


Spécifie le champ NEXT.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


Spécifie le champ NEXTIF.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


Le type de champ n'est pas spécifié ou inconnu.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


Spécifie le champ NOTEREF.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


Spécifie le champ NUMCHARS.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


Spécifie le champ NUMPAGES.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


Spécifie le champ NUMWORDS.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


Spécifie le champ OCX.

Normalement, Aspose.Words représentera un contrôle ActiveX sous forme d'un objet [Shape](../../com.aspose.words/shape/), mais pour certains documents, où un contrôle n'a pas de données et/ou semble être invalide, il sera représenté comme un champ.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


Spécifie le champ PAGE.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


Spécifie le champ PAGEREF.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


Spécifie le champ PRINT.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


Spécifie le champ PRINTDATE.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


Spécifie le champ PRIVATE.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


Spécifie le champ QUOTE.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


Spécifie le champ REF.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


Spécifie le champ RD.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


Spécifie que le champ représente un champ REF où le mot‑clé a été omis.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


Spécifie le champ REVNUM.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


Spécifie le champ SAVEDATE.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


Spécifie le champ SECTION.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


Spécifie le champ SECTIONPAGES.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


Spécifie le champ SEQ.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


Spécifie le champ SET.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


Spécifie le champ SHAPE.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


Spécifie le champ SKIPIF.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


Spécifie le champ STYLEREF.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


Spécifie le champ SUBJECT.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


Spécifie le champ SYMBOL.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


Spécifie le champ TEMPLATE.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


Spécifie le champ TIME.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


Spécifie le champ TITLE.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


Spécifie le champ TOA.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


Spécifie le champ TA.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


Spécifie le champ TOC.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


Spécifie le champ TC.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


Spécifie le champ USERADDRESS.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


Spécifie le champ USERINITIALS.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


Spécifie le champ USERNAME.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
