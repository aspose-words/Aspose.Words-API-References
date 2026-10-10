---
title: "FieldType"
linktitle: "FieldType"
second_title: "Aspose.Words لـ Java"
description: "يحدد أنواع حقول Microsoft Word في Java."
type: docs
weight: 299
url: /ar/java/com.aspose.words/fieldtype/
---

**Inheritance:**
java.lang.Object
```
public class FieldType
```

يحدد أنواع حقول Microsoft Word.

 **Examples:** 

يوضح كيفية إدراج حقل في مستند باستخدام شفرة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

يوضح كيفية العمل مع عقدة FieldStart.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [FIELD_ADDIN](#FIELD-ADDIN) | يحدد حقل ADDIN. |
| [FIELD_ADDRESS_BLOCK](#FIELD-ADDRESS-BLOCK) | يحدد حقل ADDRESSBLOCK. |
| [FIELD_ADVANCE](#FIELD-ADVANCE) | يحدد حقل ADVANCE. |
| [FIELD_ASK](#FIELD-ASK) | يحدد حقل ASK. |
| [FIELD_AUTHOR](#FIELD-AUTHOR) | يحدد حقل AUTHOR. |
| [FIELD_AUTO_NUM](#FIELD-AUTO-NUM) | يحدد حقل AUTONUM. |
| [FIELD_AUTO_NUM_LEGAL](#FIELD-AUTO-NUM-LEGAL) | يحدد حقل AUTONUMLGL. |
| [FIELD_AUTO_NUM_OUTLINE](#FIELD-AUTO-NUM-OUTLINE) | يحدد حقل AUTONUMOUT. |
| [FIELD_AUTO_TEXT](#FIELD-AUTO-TEXT) | يحدد حقل AUTOTEXT. |
| [FIELD_AUTO_TEXT_LIST](#FIELD-AUTO-TEXT-LIST) | يحدد حقل AUTOTEXTLIST. |
| [FIELD_BARCODE](#FIELD-BARCODE) | يحدد حقل BARCODE. |
| [FIELD_BIBLIOGRAPHY](#FIELD-BIBLIOGRAPHY) | يحدد حقل BIBLIOGRAPHY. |
| [FIELD_BIDI_OUTLINE](#FIELD-BIDI-OUTLINE) | يحدد حقل BIDIOUTLINE. |
| [FIELD_CANNOT_PARSE](#FIELD-CANNOT-PARSE) | يحدد أن الحقل لم يتمكن من التحليل. |
| [FIELD_CITATION](#FIELD-CITATION) | يحدد حقل CITATION. |
| [FIELD_COMMENTS](#FIELD-COMMENTS) | يحدد حقل COMMENTS. |
| [FIELD_COMPARE](#FIELD-COMPARE) | يحدد حقل COMPARE. |
| [FIELD_CREATE_DATE](#FIELD-CREATE-DATE) | يحدد حقل CREATEDATE. |
| [FIELD_DATA](#FIELD-DATA) | يحدد حقل DATA. |
| [FIELD_DATABASE](#FIELD-DATABASE) | يحدد حقل DATABASE. |
| [FIELD_DATE](#FIELD-DATE) | يحدد حقل DATE. |
| [FIELD_DDE](#FIELD-DDE) | يحدد حقل DDE. |
| [FIELD_DDE_AUTO](#FIELD-DDE-AUTO) | يحدد حقل DDEAUTO. |
| [FIELD_DISPLAY_BARCODE](#FIELD-DISPLAY-BARCODE) | يحدد حقل DISPLAYBARCODE. |
| [FIELD_DOC_PROPERTY](#FIELD-DOC-PROPERTY) | يحدد حقل DOCPROPERTY. |
| [FIELD_DOC_VARIABLE](#FIELD-DOC-VARIABLE) | يحدد حقل DOCVARIABLE. |
| [FIELD_EDIT_TIME](#FIELD-EDIT-TIME) | يحدد حقل EDITTIME. |
| [FIELD_EMBED](#FIELD-EMBED) | يحدد حقل EMBED. |
| [FIELD_EQUATION](#FIELD-EQUATION) | يحدد حقل EQ. |
| [FIELD_FILE_NAME](#FIELD-FILE-NAME) | يحدد حقل FILENAME. |
| [FIELD_FILE_SIZE](#FIELD-FILE-SIZE) | يحدد حقل FILESIZE. |
| [FIELD_FILL_IN](#FIELD-FILL-IN) | يحدد حقل FILLIN. |
| [FIELD_FOOTNOTE_REF](#FIELD-FOOTNOTE-REF) | يحدد حقل FOOTNOTEREF. |
| [FIELD_FORMULA](#FIELD-FORMULA) | يحدد حقل = (formula). |
| [FIELD_FORM_CHECK_BOX](#FIELD-FORM-CHECK-BOX) | يحدد حقل FORMCHECKBOX. |
| [FIELD_FORM_DROP_DOWN](#FIELD-FORM-DROP-DOWN) | يحدد حقل FORMDROPDOWN. |
| [FIELD_FORM_TEXT_INPUT](#FIELD-FORM-TEXT-INPUT) | يحدد حقل FORMTEXT. |
| [FIELD_GLOSSARY](#FIELD-GLOSSARY) | يحدد حقل GLOSSARY. |
| [FIELD_GO_TO_BUTTON](#FIELD-GO-TO-BUTTON) | يحدد حقل GOTOBUTTON. |
| [FIELD_GREETING_LINE](#FIELD-GREETING-LINE) | يحدد حقل GREETINGLINE. |
| [FIELD_HTML_ACTIVE_X](#FIELD-HTML-ACTIVE-X) | يحدد الحقل الذي يمثل عنصر تحكم HTML. |
| [FIELD_HYPERLINK](#FIELD-HYPERLINK) | يحدد حقل HYPERLINK. |
| [FIELD_IF](#FIELD-IF) | يحدد حقل IF. |
| [FIELD_IMPORT](#FIELD-IMPORT) | يحدد حقل IMPORT. |
| [FIELD_INCLUDE](#FIELD-INCLUDE) | يحدد حقل INCLUDE. |
| [FIELD_INCLUDE_PICTURE](#FIELD-INCLUDE-PICTURE) | يحدد حقل INCLUDEPICTURE. |
| [FIELD_INCLUDE_TEXT](#FIELD-INCLUDE-TEXT) | يحدد حقل INCLUDETEXT. |
| [FIELD_INDEX](#FIELD-INDEX) | يحدد حقل INDEX. |
| [FIELD_INDEX_ENTRY](#FIELD-INDEX-ENTRY) | يحدد حقل XE. |
| [FIELD_INFO](#FIELD-INFO) | يحدد حقل INFO. |
| [FIELD_KEYWORD](#FIELD-KEYWORD) | يحدد حقل KEYWORDS. |
| [FIELD_LAST_SAVED_BY](#FIELD-LAST-SAVED-BY) | يحدد حقل LASTSAVEDBY. |
| [FIELD_LINK](#FIELD-LINK) | يحدد حقل LINK. |
| [FIELD_LIST_NUM](#FIELD-LIST-NUM) | يحدد حقل LISTNUM. |
| [FIELD_MACRO_BUTTON](#FIELD-MACRO-BUTTON) | يحدد حقل MACROBUTTON. |
| [FIELD_MERGE_BARCODE](#FIELD-MERGE-BARCODE) | يحدد حقل MERGEBARCODE. |
| [FIELD_MERGE_FIELD](#FIELD-MERGE-FIELD) | يحدد حقل MERGEFIELD. |
| [FIELD_MERGE_REC](#FIELD-MERGE-REC) | يحدد حقل MERGEREC. |
| [FIELD_MERGE_SEQ](#FIELD-MERGE-SEQ) | يحدد حقل MERGESEQ. |
| [FIELD_NEXT](#FIELD-NEXT) | يحدد حقل NEXT. |
| [FIELD_NEXT_IF](#FIELD-NEXT-IF) | يحدد حقل NEXTIF. |
| [FIELD_NONE](#FIELD-NONE) | نوع الحقل غير محدد أو غير معروف. |
| [FIELD_NOTE_REF](#FIELD-NOTE-REF) | يحدد حقل NOTEREF. |
| [FIELD_NUM_CHARS](#FIELD-NUM-CHARS) | يحدد حقل NUMCHARS. |
| [FIELD_NUM_PAGES](#FIELD-NUM-PAGES) | يحدد حقل NUMPAGES. |
| [FIELD_NUM_WORDS](#FIELD-NUM-WORDS) | يحدد حقل NUMWORDS. |
| [FIELD_OCX](#FIELD-OCX) | يحدد حقل OCX. |
| [FIELD_PAGE](#FIELD-PAGE) | يحدد حقل PAGE. |
| [FIELD_PAGE_REF](#FIELD-PAGE-REF) | يحدد حقل PAGEREF. |
| [FIELD_PRINT](#FIELD-PRINT) | يحدد حقل PRINT. |
| [FIELD_PRINT_DATE](#FIELD-PRINT-DATE) | يحدد حقل PRINTDATE. |
| [FIELD_PRIVATE](#FIELD-PRIVATE) | يحدد حقل PRIVATE. |
| [FIELD_QUOTE](#FIELD-QUOTE) | يحدد حقل QUOTE. |
| [FIELD_REF](#FIELD-REF) | يحدد حقل REF. |
| [FIELD_REF_DOC](#FIELD-REF-DOC) | يحدد حقل RD. |
| [FIELD_REF_NO_KEYWORD](#FIELD-REF-NO-KEYWORD) | يحدد أن الحقل يمثل حقل REF حيث تم حذف الكلمة المفتاحية. |
| [FIELD_REVISION_NUM](#FIELD-REVISION-NUM) | يحدد حقل REVNUM. |
| [FIELD_SAVE_DATE](#FIELD-SAVE-DATE) | يحدد حقل SAVEDATE. |
| [FIELD_SECTION](#FIELD-SECTION) | يحدد حقل SECTION. |
| [FIELD_SECTION_PAGES](#FIELD-SECTION-PAGES) | يحدد حقل SECTIONPAGES. |
| [FIELD_SEQUENCE](#FIELD-SEQUENCE) | يحدد حقل SEQ. |
| [FIELD_SET](#FIELD-SET) | يحدد حقل SET. |
| [FIELD_SHAPE](#FIELD-SHAPE) | يحدد حقل SHAPE. |
| [FIELD_SKIP_IF](#FIELD-SKIP-IF) | يحدد حقل SKIPIF. |
| [FIELD_STYLE_REF](#FIELD-STYLE-REF) | يحدد حقل STYLEREF. |
| [FIELD_SUBJECT](#FIELD-SUBJECT) | يحدد حقل SUBJECT. |
| [FIELD_SYMBOL](#FIELD-SYMBOL) | يحدد حقل SYMBOL. |
| [FIELD_TEMPLATE](#FIELD-TEMPLATE) | يحدد حقل TEMPLATE. |
| [FIELD_TIME](#FIELD-TIME) | يحدد حقل TIME. |
| [FIELD_TITLE](#FIELD-TITLE) | يحدد حقل TITLE. |
| [FIELD_TOA](#FIELD-TOA) | يحدد حقل TOA. |
| [FIELD_TOA_ENTRY](#FIELD-TOA-ENTRY) | يحدد حقل TA. |
| [FIELD_TOC](#FIELD-TOC) | يحدد حقل TOC. |
| [FIELD_TOC_ENTRY](#FIELD-TOC-ENTRY) | يحدد حقل TC. |
| [FIELD_USER_ADDRESS](#FIELD-USER-ADDRESS) | يحدد حقل USERADDRESS. |
| [FIELD_USER_INITIALS](#FIELD-USER-INITIALS) | يحدد حقل USERINITIALS. |
| [FIELD_USER_NAME](#FIELD-USER-NAME) | يحدد حقل USERNAME. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String fieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int fieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldType)](#toString-int) |  |
### FIELD_ADDIN {#FIELD-ADDIN}
```
public static int FIELD_ADDIN
```


يحدد حقل ADDIN.

### FIELD_ADDRESS_BLOCK {#FIELD-ADDRESS-BLOCK}
```
public static int FIELD_ADDRESS_BLOCK
```


يحدد حقل ADDRESSBLOCK.

### FIELD_ADVANCE {#FIELD-ADVANCE}
```
public static int FIELD_ADVANCE
```


يحدد حقل ADVANCE.

### FIELD_ASK {#FIELD-ASK}
```
public static int FIELD_ASK
```


يحدد حقل ASK.

### FIELD_AUTHOR {#FIELD-AUTHOR}
```
public static int FIELD_AUTHOR
```


يحدد حقل AUTHOR.

### FIELD_AUTO_NUM {#FIELD-AUTO-NUM}
```
public static int FIELD_AUTO_NUM
```


يحدد حقل AUTONUM.

### FIELD_AUTO_NUM_LEGAL {#FIELD-AUTO-NUM-LEGAL}
```
public static int FIELD_AUTO_NUM_LEGAL
```


يحدد حقل AUTONUMLGL.

### FIELD_AUTO_NUM_OUTLINE {#FIELD-AUTO-NUM-OUTLINE}
```
public static int FIELD_AUTO_NUM_OUTLINE
```


يحدد حقل AUTONUMOUT.

### FIELD_AUTO_TEXT {#FIELD-AUTO-TEXT}
```
public static int FIELD_AUTO_TEXT
```


يحدد حقل AUTOTEXT.

### FIELD_AUTO_TEXT_LIST {#FIELD-AUTO-TEXT-LIST}
```
public static int FIELD_AUTO_TEXT_LIST
```


يحدد حقل AUTOTEXTLIST.

### FIELD_BARCODE {#FIELD-BARCODE}
```
public static int FIELD_BARCODE
```


يحدد حقل BARCODE.

### FIELD_BIBLIOGRAPHY {#FIELD-BIBLIOGRAPHY}
```
public static int FIELD_BIBLIOGRAPHY
```


يحدد حقل BIBLIOGRAPHY.

### FIELD_BIDI_OUTLINE {#FIELD-BIDI-OUTLINE}
```
public static int FIELD_BIDI_OUTLINE
```


يحدد حقل BIDIOUTLINE.

### FIELD_CANNOT_PARSE {#FIELD-CANNOT-PARSE}
```
public static int FIELD_CANNOT_PARSE
```


يحدد أن الحقل لم يتمكن من التحليل.

### FIELD_CITATION {#FIELD-CITATION}
```
public static int FIELD_CITATION
```


يحدد حقل CITATION.

### FIELD_COMMENTS {#FIELD-COMMENTS}
```
public static int FIELD_COMMENTS
```


يحدد حقل COMMENTS.

### FIELD_COMPARE {#FIELD-COMPARE}
```
public static int FIELD_COMPARE
```


يحدد حقل COMPARE.

### FIELD_CREATE_DATE {#FIELD-CREATE-DATE}
```
public static int FIELD_CREATE_DATE
```


يحدد حقل CREATEDATE.

### FIELD_DATA {#FIELD-DATA}
```
public static int FIELD_DATA
```


يحدد حقل DATA.

### FIELD_DATABASE {#FIELD-DATABASE}
```
public static int FIELD_DATABASE
```


يحدد حقل DATABASE.

### FIELD_DATE {#FIELD-DATE}
```
public static int FIELD_DATE
```


يحدد حقل DATE.

### FIELD_DDE {#FIELD-DDE}
```
public static int FIELD_DDE
```


يحدد حقل DDE.

### FIELD_DDE_AUTO {#FIELD-DDE-AUTO}
```
public static int FIELD_DDE_AUTO
```


يحدد حقل DDEAUTO.

### FIELD_DISPLAY_BARCODE {#FIELD-DISPLAY-BARCODE}
```
public static int FIELD_DISPLAY_BARCODE
```


يحدد حقل DISPLAYBARCODE.

### FIELD_DOC_PROPERTY {#FIELD-DOC-PROPERTY}
```
public static int FIELD_DOC_PROPERTY
```


يحدد حقل DOCPROPERTY.

### FIELD_DOC_VARIABLE {#FIELD-DOC-VARIABLE}
```
public static int FIELD_DOC_VARIABLE
```


يحدد حقل DOCVARIABLE.

### FIELD_EDIT_TIME {#FIELD-EDIT-TIME}
```
public static int FIELD_EDIT_TIME
```


يحدد حقل EDITTIME.

### FIELD_EMBED {#FIELD-EMBED}
```
public static int FIELD_EMBED
```


يحدد حقل EMBED.

### FIELD_EQUATION {#FIELD-EQUATION}
```
public static int FIELD_EQUATION
```


يحدد حقل EQ.

### FIELD_FILE_NAME {#FIELD-FILE-NAME}
```
public static int FIELD_FILE_NAME
```


يحدد حقل FILENAME.

### FIELD_FILE_SIZE {#FIELD-FILE-SIZE}
```
public static int FIELD_FILE_SIZE
```


يحدد حقل FILESIZE.

### FIELD_FILL_IN {#FIELD-FILL-IN}
```
public static int FIELD_FILL_IN
```


يحدد حقل FILLIN.

### FIELD_FOOTNOTE_REF {#FIELD-FOOTNOTE-REF}
```
public static int FIELD_FOOTNOTE_REF
```


يحدد حقل FOOTNOTEREF.

### FIELD_FORMULA {#FIELD-FORMULA}
```
public static int FIELD_FORMULA
```


يحدد حقل = (formula).

### FIELD_FORM_CHECK_BOX {#FIELD-FORM-CHECK-BOX}
```
public static int FIELD_FORM_CHECK_BOX
```


يحدد حقل FORMCHECKBOX.

### FIELD_FORM_DROP_DOWN {#FIELD-FORM-DROP-DOWN}
```
public static int FIELD_FORM_DROP_DOWN
```


يحدد حقل FORMDROPDOWN.

### FIELD_FORM_TEXT_INPUT {#FIELD-FORM-TEXT-INPUT}
```
public static int FIELD_FORM_TEXT_INPUT
```


يحدد حقل FORMTEXT.

### FIELD_GLOSSARY {#FIELD-GLOSSARY}
```
public static int FIELD_GLOSSARY
```


يحدد حقل GLOSSARY.

### FIELD_GO_TO_BUTTON {#FIELD-GO-TO-BUTTON}
```
public static int FIELD_GO_TO_BUTTON
```


يحدد حقل GOTOBUTTON.

### FIELD_GREETING_LINE {#FIELD-GREETING-LINE}
```
public static int FIELD_GREETING_LINE
```


يحدد حقل GREETINGLINE.

### FIELD_HTML_ACTIVE_X {#FIELD-HTML-ACTIVE-X}
```
public static int FIELD_HTML_ACTIVE_X
```


يحدد الحقل الذي يمثل عنصر تحكم HTML.

### FIELD_HYPERLINK {#FIELD-HYPERLINK}
```
public static int FIELD_HYPERLINK
```


يحدد حقل HYPERLINK.

### FIELD_IF {#FIELD-IF}
```
public static int FIELD_IF
```


يحدد حقل IF.

### FIELD_IMPORT {#FIELD-IMPORT}
```
public static int FIELD_IMPORT
```


يحدد حقل IMPORT.

### FIELD_INCLUDE {#FIELD-INCLUDE}
```
public static int FIELD_INCLUDE
```


يحدد حقل INCLUDE.

### FIELD_INCLUDE_PICTURE {#FIELD-INCLUDE-PICTURE}
```
public static int FIELD_INCLUDE_PICTURE
```


يحدد حقل INCLUDEPICTURE.

### FIELD_INCLUDE_TEXT {#FIELD-INCLUDE-TEXT}
```
public static int FIELD_INCLUDE_TEXT
```


يحدد حقل INCLUDETEXT.

### FIELD_INDEX {#FIELD-INDEX}
```
public static int FIELD_INDEX
```


يحدد حقل INDEX.

### FIELD_INDEX_ENTRY {#FIELD-INDEX-ENTRY}
```
public static int FIELD_INDEX_ENTRY
```


يحدد حقل XE.

### FIELD_INFO {#FIELD-INFO}
```
public static int FIELD_INFO
```


يحدد حقل INFO.

### FIELD_KEYWORD {#FIELD-KEYWORD}
```
public static int FIELD_KEYWORD
```


يحدد حقل KEYWORDS.

### FIELD_LAST_SAVED_BY {#FIELD-LAST-SAVED-BY}
```
public static int FIELD_LAST_SAVED_BY
```


يحدد حقل LASTSAVEDBY.

### FIELD_LINK {#FIELD-LINK}
```
public static int FIELD_LINK
```


يحدد حقل LINK.

### FIELD_LIST_NUM {#FIELD-LIST-NUM}
```
public static int FIELD_LIST_NUM
```


يحدد حقل LISTNUM.

### FIELD_MACRO_BUTTON {#FIELD-MACRO-BUTTON}
```
public static int FIELD_MACRO_BUTTON
```


يحدد حقل MACROBUTTON.

### FIELD_MERGE_BARCODE {#FIELD-MERGE-BARCODE}
```
public static int FIELD_MERGE_BARCODE
```


يحدد حقل MERGEBARCODE.

### FIELD_MERGE_FIELD {#FIELD-MERGE-FIELD}
```
public static int FIELD_MERGE_FIELD
```


يحدد حقل MERGEFIELD.

### FIELD_MERGE_REC {#FIELD-MERGE-REC}
```
public static int FIELD_MERGE_REC
```


يحدد حقل MERGEREC.

### FIELD_MERGE_SEQ {#FIELD-MERGE-SEQ}
```
public static int FIELD_MERGE_SEQ
```


يحدد حقل MERGESEQ.

### FIELD_NEXT {#FIELD-NEXT}
```
public static int FIELD_NEXT
```


يحدد حقل NEXT.

### FIELD_NEXT_IF {#FIELD-NEXT-IF}
```
public static int FIELD_NEXT_IF
```


يحدد حقل NEXTIF.

### FIELD_NONE {#FIELD-NONE}
```
public static int FIELD_NONE
```


نوع الحقل غير محدد أو غير معروف.

### FIELD_NOTE_REF {#FIELD-NOTE-REF}
```
public static int FIELD_NOTE_REF
```


يحدد حقل NOTEREF.

### FIELD_NUM_CHARS {#FIELD-NUM-CHARS}
```
public static int FIELD_NUM_CHARS
```


يحدد حقل NUMCHARS.

### FIELD_NUM_PAGES {#FIELD-NUM-PAGES}
```
public static int FIELD_NUM_PAGES
```


يحدد حقل NUMPAGES.

### FIELD_NUM_WORDS {#FIELD-NUM-WORDS}
```
public static int FIELD_NUM_WORDS
```


يحدد حقل NUMWORDS.

### FIELD_OCX {#FIELD-OCX}
```
public static int FIELD_OCX
```


يحدد حقل OCX.

عادةً، سيقوم Aspose.Words بتمثيل عنصر تحكم ActiveX ككائن [Shape](../../com.aspose.words/shape/)، ولكن لبعض المستندات، حيث لا يحتوي العنصر على بيانات أو يبدو غير صالح، سيتم تمثيله كحقل.

### FIELD_PAGE {#FIELD-PAGE}
```
public static int FIELD_PAGE
```


يحدد حقل PAGE.

### FIELD_PAGE_REF {#FIELD-PAGE-REF}
```
public static int FIELD_PAGE_REF
```


يحدد حقل PAGEREF.

### FIELD_PRINT {#FIELD-PRINT}
```
public static int FIELD_PRINT
```


يحدد حقل PRINT.

### FIELD_PRINT_DATE {#FIELD-PRINT-DATE}
```
public static int FIELD_PRINT_DATE
```


يحدد حقل PRINTDATE.

### FIELD_PRIVATE {#FIELD-PRIVATE}
```
public static int FIELD_PRIVATE
```


يحدد حقل PRIVATE.

### FIELD_QUOTE {#FIELD-QUOTE}
```
public static int FIELD_QUOTE
```


يحدد حقل QUOTE.

### FIELD_REF {#FIELD-REF}
```
public static int FIELD_REF
```


يحدد حقل REF.

### FIELD_REF_DOC {#FIELD-REF-DOC}
```
public static int FIELD_REF_DOC
```


يحدد حقل RD.

### FIELD_REF_NO_KEYWORD {#FIELD-REF-NO-KEYWORD}
```
public static int FIELD_REF_NO_KEYWORD
```


يحدد أن الحقل يمثل حقل REF حيث تم حذف الكلمة المفتاحية.

### FIELD_REVISION_NUM {#FIELD-REVISION-NUM}
```
public static int FIELD_REVISION_NUM
```


يحدد حقل REVNUM.

### FIELD_SAVE_DATE {#FIELD-SAVE-DATE}
```
public static int FIELD_SAVE_DATE
```


يحدد حقل SAVEDATE.

### FIELD_SECTION {#FIELD-SECTION}
```
public static int FIELD_SECTION
```


يحدد حقل SECTION.

### FIELD_SECTION_PAGES {#FIELD-SECTION-PAGES}
```
public static int FIELD_SECTION_PAGES
```


يحدد حقل SECTIONPAGES.

### FIELD_SEQUENCE {#FIELD-SEQUENCE}
```
public static int FIELD_SEQUENCE
```


يحدد حقل SEQ.

### FIELD_SET {#FIELD-SET}
```
public static int FIELD_SET
```


يحدد حقل SET.

### FIELD_SHAPE {#FIELD-SHAPE}
```
public static int FIELD_SHAPE
```


يحدد حقل SHAPE.

### FIELD_SKIP_IF {#FIELD-SKIP-IF}
```
public static int FIELD_SKIP_IF
```


يحدد حقل SKIPIF.

### FIELD_STYLE_REF {#FIELD-STYLE-REF}
```
public static int FIELD_STYLE_REF
```


يحدد حقل STYLEREF.

### FIELD_SUBJECT {#FIELD-SUBJECT}
```
public static int FIELD_SUBJECT
```


يحدد حقل SUBJECT.

### FIELD_SYMBOL {#FIELD-SYMBOL}
```
public static int FIELD_SYMBOL
```


يحدد حقل SYMBOL.

### FIELD_TEMPLATE {#FIELD-TEMPLATE}
```
public static int FIELD_TEMPLATE
```


يحدد حقل TEMPLATE.

### FIELD_TIME {#FIELD-TIME}
```
public static int FIELD_TIME
```


يحدد حقل TIME.

### FIELD_TITLE {#FIELD-TITLE}
```
public static int FIELD_TITLE
```


يحدد حقل TITLE.

### FIELD_TOA {#FIELD-TOA}
```
public static int FIELD_TOA
```


يحدد حقل TOA.

### FIELD_TOA_ENTRY {#FIELD-TOA-ENTRY}
```
public static int FIELD_TOA_ENTRY
```


يحدد حقل TA.

### FIELD_TOC {#FIELD-TOC}
```
public static int FIELD_TOC
```


يحدد حقل TOC.

### FIELD_TOC_ENTRY {#FIELD-TOC-ENTRY}
```
public static int FIELD_TOC_ENTRY
```


يحدد حقل TC.

### FIELD_USER_ADDRESS {#FIELD-USER-ADDRESS}
```
public static int FIELD_USER_ADDRESS
```


يحدد حقل USERADDRESS.

### FIELD_USER_INITIALS {#FIELD-USER-INITIALS}
```
public static int FIELD_USER_INITIALS
```


يحدد حقل USERINITIALS.

### FIELD_USER_NAME {#FIELD-USER-NAME}
```
public static int FIELD_USER_NAME
```


يحدد حقل USERNAME.

### length {#length}
```
public static int length
```


### fromName(String fieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fieldTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fieldType) {#getName-int}
```
public static String getName(int fieldType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldType | int |  |

**Returns:**
java.lang.String
