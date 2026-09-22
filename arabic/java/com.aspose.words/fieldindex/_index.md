---
title: "FieldIndex"
linktitle: "FieldIndex"
second_title: "Aspose.Words لـ Java"
description: "يُنفّذ حقل INDEX في Java."
type: docs
weight: 249
url: /ar/java/com.aspose.words/fieldindex/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldIndex extends Field
```

ينفّذ حقل INDEX.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fields ][Working with Fields].

 **Remarks:** 

يبني فهرسًا باستخدام مدخلات الفهرس المحددة بواسطة حقول XE، ويُدرج ذلك الفهرس في هذا الموضع في المستند.

 **Examples:** 

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | يحصل على اسم الإشارة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الفهرس. |
| [getCrossReferenceSeparator()](#getCrossReferenceSeparator) | يحصل على تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة وغيرها من المدخلات. |
| [getDisplayResult()](#getDisplayResult) | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [getEnd()](#getEnd) | يحصل على العقدة التي تمثل نهاية الحقل. |
| [getEntryType()](#getEntryType) | يحصل على نوع مدخل الفهرس المستخدم لبناء الفهرس. |
| [getFieldCode()](#getFieldCode) | يرجع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | يرجع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [getFormat()](#getFormat) | يحصل على كائن [FieldFormat](../../com.aspose.words/fieldformat/) الذي يوفر وصولًا مكتوبًا إلى تنسيق الحقل. |
| [getHeading()](#getHeading) | يحصل على عنوان يظهر في بداية كل مجموعة من الإدخالات لأي حرف معين. |
| [getLanguageId()](#getLanguageId) | يحصل على معرف اللغة المستخدم لإنشاء الفهرس. |
| [getLetterRange()](#getLetterRange) | يحصل على نطاق الحروف التي يحدّ الفهرس إليها. |
| [getLocaleId()](#getLocaleId) | يحصل على معرف اللغة (LCID) للحقل. |
| [getNumberOfColumns()](#getNumberOfColumns) | يحصل على عدد الأعمدة لكل صفحة المستخدمة عند بناء الفهرس. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator) | يحصل على تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات. |
| [getPageNumberSeparator()](#getPageNumberSeparator) | يحصل على تسلسل الأحرف المستخدم لفصل إدخال الفهرس ورقم صفحته. |
| [getPageRangeSeparator()](#getPageRangeSeparator) | يحصل على تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات. |
| [getResult()](#getResult) | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [getRunSubentriesOnSameLine()](#getRunSubentriesOnSameLine) | يحصل على ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي. |
| [getSeparator()](#getSeparator) | يحصل على العقدة التي تمثل فاصل الحقل. |
| [getSequenceName()](#getSequenceName) | يحصل على اسم تسلسل يُدرج رقمه مع رقم الصفحة. |
| [getSequenceSeparator()](#getSequenceSeparator) | يحصل على تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [getStart()](#getStart) | يحصل على العقدة التي تمثل بداية الحقل. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | يحصل على نوع حقل Microsoft Word. |
| [getUseYomi()](#getUseYomi) | يحصل على ما إذا كان يجب تمكين استخدام نص الـ yomi لإدخالات الفهرس. |
| [hasPageNumberSeparator()](#hasPageNumberSeparator) | يحصل على قيمة تشير إلى ما إذا كان فاصل رقم الصفحة قد تم تجاوزه عبر شفرة الحقل. |
| [hasSequenceName()](#hasSequenceName) | يحصل على قيمة تشير إلى ما إذا كان يجب استخدام تسلسل أثناء بناء نتيجة الحقل. |
| [isDirty()](#isDirty) | يحصل على ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أجريت على المستند. |
| [isDirty(boolean value)](#isDirty-boolean) | يضبط ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أجريت على المستند. |
| [isLocked()](#isLocked) | يحصل على ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته). |
| [isLocked(boolean value)](#isLocked-boolean) | يضبط ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته). |
| [remove()](#remove) | يزيل الحقل من المستند. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | يضبط اسم الإشارة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الفهرس. |
| [setCrossReferenceSeparator(String value)](#setCrossReferenceSeparator-java.lang.String) | يضبط تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة والإدخالات الأخرى. |
| [setEntryType(String value)](#setEntryType-java.lang.String) | يضبط نوع إدخال الفهرس المستخدم لبناء الفهرس. |
| [setHeading(String value)](#setHeading-java.lang.String) | يضبط عنوانًا يظهر في بداية كل مجموعة من الإدخالات لأي حرف معين. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String) | يضبط معرف اللغة المستخدم لإنشاء الفهرس. |
| [setLetterRange(String value)](#setLetterRange-java.lang.String) | يضبط نطاق الحروف التي يحدّ الفهرس إليها. |
| [setLocaleId(int value)](#setLocaleId-int) | يضبط LCID الخاص بالحقل. |
| [setNumberOfColumns(String value)](#setNumberOfColumns-java.lang.String) | يضبط عدد الأعمدة لكل صفحة المستخدمة عند بناء الفهرس. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String) | يضبط تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات. |
| [setPageNumberSeparator(String value)](#setPageNumberSeparator-java.lang.String) | يضبط تسلسل الأحرف المستخدم لفصل إدخال الفهرس ورقم صفحته. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String) | يضبط تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات. |
| [setResult(String value)](#setResult-java.lang.String) | يضبط النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [setRunSubentriesOnSameLine(boolean value)](#setRunSubentriesOnSameLine-boolean) | يضبط ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String) | يضبط اسم تسلسل يُدرج رقمه مع رقم الصفحة. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | يضبط تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [setUseYomi(boolean value)](#setUseYomi-boolean) | يضبط ما إذا كان يجب تمكين استخدام نص الـ yomi لإدخالات الفهرس. |
| [unlink()](#unlink) | ينفذ إلغاء ربط الحقل. |
| [update()](#update) | ينفذ تحديث الحقل. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | ينفذ تحديثًا للحقل. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


يحصل على اسم الإشارة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الفهرس.

 **Examples:** 

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Returns:**
java.lang.String - اسم الإشارة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الفهرس.
### getCrossReferenceSeparator() {#getCrossReferenceSeparator}
```
public String getCrossReferenceSeparator()
```


يحصل على تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة وغيرها من المدخلات.

 **Examples:** 

يوضح كيفية تعريف المراجع المتقاطعة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // We can configure an XE field to get its INDEX entry to display a string instead of a page number.
 // First, for entries that substitute a page number with a string,
 // specify a custom separator between the XE field's Text property value and the string.
 index.setCrossReferenceSeparator(", see: ");

 Assert.assertEquals(" INDEX  \\k \", see: \"", index.getFieldCode());

 // Insert an XE field, which creates a regular INDEX entry which displays this field's page number,
 // and does not invoke the CrossReferenceSeparator value.
 // The entry for this XE field will display "Apple, 2".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");

 Assert.assertEquals(" XE  Apple", indexEntry.getFieldCode());

 // Insert another XE field on page 3 and set a value for the PageNumberReplacement property.
 // This value will show up instead of the number of the page that this field is on,
 // and the INDEX field's CrossReferenceSeparator value will appear in front of it.
 // The entry for this XE field will display "Banana, see: Tropical fruit".
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");
 indexEntry.setPageNumberReplacement("Tropical fruit");

 Assert.assertEquals(" XE  Banana \\t \"Tropical fruit\"", indexEntry.getFieldCode());

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.CrossReferenceSeparator.docx");
 
```

**Returns:**
java.lang.String - تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة والإدخالات الأخرى.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


يحصل على النص الذي يمثل نتيجة الحقل المعروضة.

 **Remarks:** 

يجب استدعاء طريقة [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) للحصول على القيمة الصحيحة للحقول [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) و [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

يوضح كيفية الحصول على النص الحقيقي الذي يعرضه الحقل في المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("This document was written by ");
 FieldAuthor fieldAuthor = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 fieldAuthor.setAuthorName("John Doe");

 // We can use the DisplayResult property to verify what exact text
 // a field would display in its place in the document.
 Assert.assertEquals("", fieldAuthor.getDisplayResult());

 // Fields do not maintain accurate result values in real-time.
 // To make sure our fields display accurate results at any given time,
 // such as right before a save operation, we need to update them manually.
 fieldAuthor.update();

 Assert.assertEquals("John Doe", fieldAuthor.getDisplayResult());

 doc.save(getArtifactsDir() + "Field.DisplayResult.docx");
 
```

**Returns:**
java.lang.String - النص الذي يمثل نتيجة الحقل المعروضة.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


يحصل على العقدة التي تمثل نهاية الحقل.

 **Examples:** 

يوضح كيفية العمل مع مجموعة من الحقول.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getEntryType() {#getEntryType}
```
public String getEntryType()
```


يحصل على نوع مدخل الفهرس المستخدم لبناء الفهرس.

 **Examples:** 

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Returns:**
java.lang.String - نوع إدخال الفهرس المستخدم لبناء الفهرس.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية.

 **Examples:** 

يوضح كيفية إدراج حقل في مستند باستخدام شفرة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

يوضح كيفية الحصول على شفرة الحقل.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


يرجع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل).

 **Examples:** 

يوضح كيفية الحصول على شفرة الحقل.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| includeChildFieldCodes | boolean | صحيح إذا كان يجب تضمين شفرة الحقول الفرعية. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


يحصل على كائن [FieldFormat](../../com.aspose.words/fieldformat/) الذي يوفر وصولًا مكتوبًا إلى تنسيق الحقل.

 **Examples:** 

يوضح كيفية تنسيق نتائج الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getHeading() {#getHeading}
```
public String getHeading()
```


يحصل على عنوان يظهر في بداية كل مجموعة من الإدخالات لأي حرف معين.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - عنوان يظهر في بداية كل مجموعة من الإدخالات لأي حرف معين.
### getLanguageId() {#getLanguageId}
```
public String getLanguageId()
```


يحصل على معرف اللغة المستخدم لإنشاء الفهرس.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - معرف اللغة المستخدم لإنشاء الفهرس.
### getLetterRange() {#getLetterRange}
```
public String getLetterRange()
```


يحصل على نطاق الحروف التي يحدّ الفهرس إليها.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - نطاق الحروف التي يحدّ الفهرس إليها.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


يحصل على معرف اللغة (LCID) للحقل.

 **Examples:** 

يوضح كيفية إدراج حقل والعمل مع إعداداته المحلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Returns:**
int - معرف اللغة المحلي (LCID) للحقول.
### getNumberOfColumns() {#getNumberOfColumns}
```
public String getNumberOfColumns()
```


يحصل على عدد الأعمدة لكل صفحة المستخدمة عند بناء الفهرس.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - عدد الأعمدة في كل صفحة المستخدمة عند بناء الفهرس.
### getPageNumberListSeparator() {#getPageNumberListSeparator}
```
public String getPageNumberListSeparator()
```


يحصل على تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات.

 **Examples:** 

يوضح كيفية تعديل فاصل رقم الصفحة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Returns:**
java.lang.String - تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات.
### getPageNumberSeparator() {#getPageNumberSeparator}
```
public String getPageNumberSeparator()
```


يحصل على تسلسل الأحرف المستخدم لفصل إدخال الفهرس ورقم صفحته.

 **Examples:** 

يوضح كيفية تعديل فاصل رقم الصفحة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Returns:**
java.lang.String - تسلسل الأحرف المستخدم لفصل إدخال الفهرس ورقم صفحته.
### getPageRangeSeparator() {#getPageRangeSeparator}
```
public String getPageRangeSeparator()
```


يحصل على تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات.

 **Examples:** 

يوضح كيفية تحديد الصفحات التي يغطيها الإشارة المرجعية كنطاق صفحات لإدخال حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // For INDEX entries that display page ranges, we can specify a separator string
 // which will appear between the number of the first page, and the number of the last.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageRangeSeparator(" to ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("My entry");

 // If an XE field names a bookmark using the PageRangeBookmarkName property,
 // its INDEX entry will show the range of pages that the bookmark spans
 // instead of the number of the page that contains the XE field.
 indexEntry.setPageRangeBookmarkName("MyBookmark");

 Assert.assertEquals(" XE  \"My entry\" \\r MyBookmark", indexEntry.getFieldCode());
 Assert.assertEquals(indexEntry.getPageRangeBookmarkName(), "MyBookmark");

 // Insert a bookmark that starts on page 3 and ends on page 5.
 // The INDEX entry for the XE field that references this bookmark will display this page range.
 // In our table, the INDEX entry will display "My entry, on page(s) 3 to 5".
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MyBookmark");
 builder.write("Start of MyBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("End of MyBookmark");
 builder.endBookmark("MyBookmark");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageRangeBookmark.docx");
 
```

**Returns:**
java.lang.String - تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات.
### getResult() {#getResult}
```
public String getResult()
```


يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل.

 **Examples:** 

يوضح كيفية إدراج حقل في مستند باستخدام شفرة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - النص الموجود بين فاصل الحقل ونهاية الحقل.
### getRunSubentriesOnSameLine() {#getRunSubentriesOnSameLine}
```
public boolean getRunSubentriesOnSameLine()
```


يحصل على ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي.

 **Examples:** 

يوضح كيفية العمل مع الإدخالات الفرعية في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setPageNumberSeparator(", see page ");
 index.setHeading("A");

 // XE fields that have a Text property whose value becomes the heading of the INDEX entry.
 // If this value contains two string segments split by a colon (the INDEX entry will treat :) delimiter,
 // the first segment is heading, and the second segment will become the subheading.
 // The INDEX field first groups entries alphabetically, then, if there are multiple XE fields with the same
 // headings, the INDEX field will further subgroup them by the values of these headings.
 // There can be multiple subgrouping layers, depending on how many times
 // the Text properties of XE fields get segmented like this.
 // By default, an INDEX field entry group will create a new line for every subheading within this group.
 // We can set the RunSubentriesOnSameLine flag to true to keep the heading,
 // and every subheading for the group on one line instead, which will make the INDEX field more compact.
 index.setRunSubentriesOnSameLine(runSubentriesOnTheSameLine);

 if (runSubentriesOnTheSameLine)
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A \\r", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A", index.getFieldCode());

 // Insert two XE fields, each on a new page, and with the same heading named "Heading 1",
 // which the INDEX field will use to group them.
 // If RunSubentriesOnSameLine is false, then the INDEX table will create three lines:
 // one line for the grouping heading "Heading 1", and one more line for each subheading.
 // If RunSubentriesOnSameLine is true, then the INDEX table will create a one-line
 // entry that encompasses the heading and every subheading.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 1");

 Assert.assertEquals(" XE  \"Heading 1:Subheading 1\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 2");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Subheading.docx");
 
```

**Returns:**
boolean - ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون null .

 **Examples:** 

يوضح كيفية العمل مع مجموعة من الحقول.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getSequenceName() {#getSequenceName}
```
public String getSequenceName()
```


يحصل على اسم تسلسل يُدرج رقمه مع رقم الصفحة.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء عن طريق دمج حقول INDEX و SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Returns:**
java.lang.String - اسم التسلسل الذي يُدرج رقمه مع رقم الصفحة.
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


يحصل على تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء عن طريق دمج حقول INDEX و SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Returns:**
java.lang.String - تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات.
### getStart() {#getStart}
```
public FieldStart getStart()
```


يحصل على العقدة التي تمثل بداية الحقل.

 **Examples:** 

يوضح كيفية العمل مع مجموعة من الحقول.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


يحصل على نوع حقل Microsoft Word.

 **Examples:** 

يوضح كيفية إدراج حقل في مستند باستخدام شفرة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - نوع حقل Microsoft Word. القيمة المرجعة هي واحدة من الثوابت في [FieldType](../../com.aspose.words/fieldtype/).
### getUseYomi() {#getUseYomi}
```
public boolean getUseYomi()
```


يحصل على ما إذا كان يجب تمكين استخدام نص الـ yomi لإدخالات الفهرس.

 **Examples:** 

يعرض كيفية فرز إدخالات حقل INDEX صوتيًا.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // The INDEX table automatically sorts its entries by the values of their Text properties in alphabetic order.
 // Set the INDEX table to sort entries phonetically using Hiragana instead.
 index.setUseYomi(sortEntriesUsingYomi);

 if (sortEntriesUsingYomi)
     Assert.assertEquals(" INDEX  \\y", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX ", index.getFieldCode());

 // Insert 4 XE fields, which would show up as entries in the INDEX field's table of contents.
 // The "Text" property may contain a word's spelling in Kanji, whose pronunciation may be ambiguous,
 // while the "Yomi" version of the word will spell exactly how it is pronounced using Hiragana.
 // If we set our INDEX field to use Yomi, it will sort these entries
 // by the value of their Yomi properties, instead of their Text values.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u5b50");
 indexEntry.setYomi("\u3042");

 Assert.assertEquals(" XE  \u611b\u5b50 \\y \u3042", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u660e\u7f8e");
 indexEntry.setYomi("\u3042");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u6075\u7f8e");
 indexEntry.setYomi("\u3048");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u7f8e");
 indexEntry.setYomi("\u3048");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Yomi.docx");
 
```

**Returns:**
boolean - ما إذا كان يجب تمكين استخدام نص yomi لإدخالات الفهرس.
### hasPageNumberSeparator() {#hasPageNumberSeparator}
```
public boolean hasPageNumberSeparator()
```


يحصل على قيمة تشير إلى ما إذا كان فاصل رقم الصفحة قد تم تجاوزه عبر شفرة الحقل.

 **Examples:** 

يوضح كيفية تعديل فاصل رقم الصفحة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Returns:**
boolean - قيمة تشير إلى ما إذا كان فاصل رقم الصفحة تم تجاوزه عبر كود الحقل.
### hasSequenceName() {#hasSequenceName}
```
public boolean hasSequenceName()
```


يحصل على قيمة تشير إلى ما إذا كان يجب استخدام تسلسل أثناء بناء نتيجة الحقل.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء عن طريق دمج حقول INDEX و SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Returns:**
boolean - قيمة تشير إلى ما إذا كان يجب استخدام تسلسل أثناء بناء نتيجة الحقل.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


يحصل على ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أجريت على المستند.

 **Examples:** 

يوضح كيفية استخدام الخاصية الخاصة لتحديث نتيجة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


يضبط ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أجريت على المستند.

 **Examples:** 

يوضح كيفية استخدام الخاصية الخاصة لتحديث نتيجة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


يحصل على ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته).

 **Examples:** 

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

**Returns:**
boolean - ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


يضبط ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته).

 **Examples:** 

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته). |

### remove() {#remove}
```
public Node remove()
```


يزيل الحقل من المستند. يُرجع عقدة تقع مباشرة بعد الحقل. إذا كان نهاية الحقل هي الطفل الأخير لعقدة الوالد، يُرجع الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يُرجع null .

 **Examples:** 

يوضح كيفية إزالة الحقول من مجموعة الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
 builder.insertField(" TIME ");
 builder.insertField(" REVNUM ");
 builder.insertField(" AUTHOR  \"John Doe\" ");
 builder.insertField(" SUBJECT \"My Subject\" ");
 builder.insertField(" QUOTE \"Hello world!\" ");
 doc.updateFields();

 FieldCollection fields = doc.getRange().getFields();

 Assert.assertEquals(6, fields.getCount());

 // Below are four ways of removing fields from a field collection.
 // 1 -  Get a field to remove itself:
 fields.get(0).remove();
 Assert.assertEquals(5, fields.getCount());

 // 2 -  Get the collection to remove a field that we pass to its removal method:
 Field lastField = fields.get(3);
 fields.remove(lastField);
 Assert.assertEquals(4, fields.getCount());

 // 3 -  Remove a field from a collection at an index:
 fields.removeAt(2);
 Assert.assertEquals(3, fields.getCount());

 // 4 -  Remove all the fields from the collection at once:
 fields.clear();
 Assert.assertEquals(0, fields.getCount());
 
```

يوضح كيفية معالجة الحقول PRIVATE.

```

 public void fieldPrivate() throws Exception {
     // Open a Corel WordPerfect document which we have converted to .docx format.
     Document doc = new Document(getMyDir() + "Field sample - PRIVATE.docx");

     // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
     // Microsoft Word preserves PRIVATE fields during load/save operations,
     // but provides no functionality for them.
     FieldPrivate field = (FieldPrivate) doc.getRange().getFields().get(0);

     Assert.assertEquals(" PRIVATE \"My value\" ", field.getFieldCode());
     Assert.assertEquals(FieldType.FIELD_PRIVATE, field.getType());

     // We can also insert PRIVATE fields using a document builder.
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(FieldType.FIELD_PRIVATE, true);

     // These fields are not a viable way of protecting sensitive information.
     // Unless backward compatibility with older versions of WordPerfect is essential,
     // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
     Assert.assertEquals(2, doc.getRange().getFields().getCount());

     FieldPrivateRemover remover = new FieldPrivateRemover();
     doc.accept(remover);

     Assert.assertEquals(remover.getFieldsRemovedCount(), 2);
     Assert.assertEquals(doc.getRange().getFields().getCount(), 0);
 }

 /// 
 /// Removes all encountered PRIVATE fields.
 /// 
 public static class FieldPrivateRemover extends DocumentVisitor {
     public FieldPrivateRemover() {
         mFieldsRemovedCount = 0;
     }

     public int getFieldsRemovedCount() {
         return mFieldsRemovedCount;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// If the node belongs to a PRIVATE field, the entire field is removed.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) throws Exception {
         if (fieldEnd.getFieldType() == FieldType.FIELD_PRIVATE) {
             fieldEnd.getField().remove();
             mFieldsRemovedCount++;
         }

         return VisitorAction.CONTINUE;
     }

     private int mFieldsRemovedCount;
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String}
```
public void setBookmarkName(String value)
```


يضبط اسم الإشارة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الفهرس.

 **Examples:** 

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم العلامة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الفهرس. |

### setCrossReferenceSeparator(String value) {#setCrossReferenceSeparator-java.lang.String}
```
public void setCrossReferenceSeparator(String value)
```


يضبط تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة والإدخالات الأخرى.

 **Examples:** 

يوضح كيفية تعريف المراجع المتقاطعة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // We can configure an XE field to get its INDEX entry to display a string instead of a page number.
 // First, for entries that substitute a page number with a string,
 // specify a custom separator between the XE field's Text property value and the string.
 index.setCrossReferenceSeparator(", see: ");

 Assert.assertEquals(" INDEX  \\k \", see: \"", index.getFieldCode());

 // Insert an XE field, which creates a regular INDEX entry which displays this field's page number,
 // and does not invoke the CrossReferenceSeparator value.
 // The entry for this XE field will display "Apple, 2".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");

 Assert.assertEquals(" XE  Apple", indexEntry.getFieldCode());

 // Insert another XE field on page 3 and set a value for the PageNumberReplacement property.
 // This value will show up instead of the number of the page that this field is on,
 // and the INDEX field's CrossReferenceSeparator value will appear in front of it.
 // The entry for this XE field will display "Banana, see: Tropical fruit".
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");
 indexEntry.setPageNumberReplacement("Tropical fruit");

 Assert.assertEquals(" XE  Banana \\t \"Tropical fruit\"", indexEntry.getFieldCode());

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.CrossReferenceSeparator.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة وغيرها من الإدخالات. |

### setEntryType(String value) {#setEntryType-java.lang.String}
```
public void setEntryType(String value)
```


يضبط نوع إدخال الفهرس المستخدم لبناء الفهرس.

 **Examples:** 

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | نوع إدخال الفهرس المستخدم لبناء الفهرس. |

### setHeading(String value) {#setHeading-java.lang.String}
```
public void setHeading(String value)
```


يضبط عنوانًا يظهر في بداية كل مجموعة من الإدخالات لأي حرف معين.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عنوان يظهر في بداية كل مجموعة من الإدخالات لأي حرف معين. |

### setLanguageId(String value) {#setLanguageId-java.lang.String}
```
public void setLanguageId(String value)
```


يضبط معرف اللغة المستخدم لإنشاء الفهرس.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | معرف اللغة المستخدم لإنشاء الفهرس. |

### setLetterRange(String value) {#setLetterRange-java.lang.String}
```
public void setLetterRange(String value)
```


يضبط نطاق الحروف التي يحدّ الفهرس إليها.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | نطاق الحروف التي يقتصر عليها الفهرس. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


يضبط LCID الخاص بالحقل.

 **Examples:** 

يوضح كيفية إدراج حقل والعمل مع إعداداته المحلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | معرف اللغة المحلي (LCID) للحقول. |

### setNumberOfColumns(String value) {#setNumberOfColumns-java.lang.String}
```
public void setNumberOfColumns(String value)
```


يضبط عدد الأعمدة لكل صفحة المستخدمة عند بناء الفهرس.

 **Examples:** 

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وأيضًا تعديل مظهره.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عدد الأعمدة في كل صفحة المستخدمة عند بناء الفهرس. |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String}
```
public void setPageNumberListSeparator(String value)
```


يضبط تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات.

 **Examples:** 

يوضح كيفية تعديل فاصل رقم الصفحة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات. |

### setPageNumberSeparator(String value) {#setPageNumberSeparator-java.lang.String}
```
public void setPageNumberSeparator(String value)
```


يضبط تسلسل الأحرف المستخدم لفصل إدخال الفهرس ورقم صفحته.

 **Examples:** 

يوضح كيفية تعديل فاصل رقم الصفحة في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | تسلسل الأحرف المستخدم لفصل إدخال الفهرس ورقم صفحته. |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String}
```
public void setPageRangeSeparator(String value)
```


يضبط تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات.

 **Examples:** 

يوضح كيفية تحديد الصفحات التي يغطيها الإشارة المرجعية كنطاق صفحات لإدخال حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // For INDEX entries that display page ranges, we can specify a separator string
 // which will appear between the number of the first page, and the number of the last.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageRangeSeparator(" to ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("My entry");

 // If an XE field names a bookmark using the PageRangeBookmarkName property,
 // its INDEX entry will show the range of pages that the bookmark spans
 // instead of the number of the page that contains the XE field.
 indexEntry.setPageRangeBookmarkName("MyBookmark");

 Assert.assertEquals(" XE  \"My entry\" \\r MyBookmark", indexEntry.getFieldCode());
 Assert.assertEquals(indexEntry.getPageRangeBookmarkName(), "MyBookmark");

 // Insert a bookmark that starts on page 3 and ends on page 5.
 // The INDEX entry for the XE field that references this bookmark will display this page range.
 // In our table, the INDEX entry will display "My entry, on page(s) 3 to 5".
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MyBookmark");
 builder.write("Start of MyBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("End of MyBookmark");
 builder.endBookmark("MyBookmark");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageRangeBookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


يضبط النص الموجود بين فاصل الحقل ونهاية الحقل.

 **Examples:** 

يوضح كيفية إدراج حقل في مستند باستخدام شفرة الحقل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | النص الموجود بين فاصل الحقل ونهاية الحقل. |

### setRunSubentriesOnSameLine(boolean value) {#setRunSubentriesOnSameLine-boolean}
```
public void setRunSubentriesOnSameLine(boolean value)
```


يضبط ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي.

 **Examples:** 

يوضح كيفية العمل مع الإدخالات الفرعية في حقل INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setPageNumberSeparator(", see page ");
 index.setHeading("A");

 // XE fields that have a Text property whose value becomes the heading of the INDEX entry.
 // If this value contains two string segments split by a colon (the INDEX entry will treat :) delimiter,
 // the first segment is heading, and the second segment will become the subheading.
 // The INDEX field first groups entries alphabetically, then, if there are multiple XE fields with the same
 // headings, the INDEX field will further subgroup them by the values of these headings.
 // There can be multiple subgrouping layers, depending on how many times
 // the Text properties of XE fields get segmented like this.
 // By default, an INDEX field entry group will create a new line for every subheading within this group.
 // We can set the RunSubentriesOnSameLine flag to true to keep the heading,
 // and every subheading for the group on one line instead, which will make the INDEX field more compact.
 index.setRunSubentriesOnSameLine(runSubentriesOnTheSameLine);

 if (runSubentriesOnTheSameLine)
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A \\r", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A", index.getFieldCode());

 // Insert two XE fields, each on a new page, and with the same heading named "Heading 1",
 // which the INDEX field will use to group them.
 // If RunSubentriesOnSameLine is false, then the INDEX table will create three lines:
 // one line for the grouping heading "Heading 1", and one more line for each subheading.
 // If RunSubentriesOnSameLine is true, then the INDEX table will create a one-line
 // entry that encompasses the heading and every subheading.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 1");

 Assert.assertEquals(" XE  \"Heading 1:Subheading 1\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 2");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Subheading.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي. |

### setSequenceName(String value) {#setSequenceName-java.lang.String}
```
public void setSequenceName(String value)
```


يضبط اسم تسلسل يُدرج رقمه مع رقم الصفحة.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء عن طريق دمج حقول INDEX و SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم التسلسل الذي يُدرج رقمه مع رقم الصفحة. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


يضبط تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء عن طريق دمج حقول INDEX و SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |

### setUseYomi(boolean value) {#setUseYomi-boolean}
```
public void setUseYomi(boolean value)
```


يضبط ما إذا كان يجب تمكين استخدام نص الـ yomi لإدخالات الفهرس.

 **Examples:** 

يعرض كيفية فرز إدخالات حقل INDEX صوتيًا.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // The INDEX table automatically sorts its entries by the values of their Text properties in alphabetic order.
 // Set the INDEX table to sort entries phonetically using Hiragana instead.
 index.setUseYomi(sortEntriesUsingYomi);

 if (sortEntriesUsingYomi)
     Assert.assertEquals(" INDEX  \\y", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX ", index.getFieldCode());

 // Insert 4 XE fields, which would show up as entries in the INDEX field's table of contents.
 // The "Text" property may contain a word's spelling in Kanji, whose pronunciation may be ambiguous,
 // while the "Yomi" version of the word will spell exactly how it is pronounced using Hiragana.
 // If we set our INDEX field to use Yomi, it will sort these entries
 // by the value of their Yomi properties, instead of their Text values.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u5b50");
 indexEntry.setYomi("\u3042");

 Assert.assertEquals(" XE  \u611b\u5b50 \\y \u3042", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u660e\u7f8e");
 indexEntry.setYomi("\u3042");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u6075\u7f8e");
 indexEntry.setYomi("\u3048");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u7f8e");
 indexEntry.setYomi("\u3048");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Yomi.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان يجب تمكين استخدام نص yomi لإدخالات الفهرس. |

### unlink() {#unlink}
```
public boolean unlink()
```


ينفذ إلغاء ربط الحقل.

 **Remarks:** 

يستبدل الحقل بأحدث نتيجة له.

بعض الحقول، مثل حقول XE (إدخال الفهرس) و SEQ (التسلسل)، لا يمكن إلغاء ربطها.

 **Examples:** 

يوضح كيفية إلغاء ربط حقل.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  إذا تم إلغاء ربط الحقل، وإلا  false .
### update() {#update}
```
public void update()
```


ينفّذ تحديث الحقل. يرمي استثناءً إذا كان الحقل قيد التحديث بالفعل.

 **Examples:** 

يوضح كيفية إدراج حقل في مستند باستخدام FieldType.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
 // In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 builder.write("This document was written by ");
 builder.insertField(FieldType.FIELD_AUTHOR, updateInsertedFieldsImmediately);

 builder.insertParagraph();
 builder.write("\nThis is page ");
 builder.insertField(FieldType.FIELD_PAGE, updateInsertedFieldsImmediately);

 Assert.assertEquals(" AUTHOR ", doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(" PAGE ", doc.getRange().getFields().get(1).getFieldCode());

 if (updateInsertedFieldsImmediately) {
     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 } else {
     Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

     // We will need to update these fields using the update methods manually.
     doc.getRange().getFields().get(0).update();

     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());

     doc.updateFields();

     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 }
 
```

يوضح كيفية تنسيق نتائج الحقول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


ينفّذ تحديثًا للحقل. يرمي استثناءً إذا كان الحقل قيد التحديث بالفعل.

 **Examples:** 

يوضح كيفية الحفاظ على حقول INCLUDEPICTURE أو تجاهلها عند تحميل مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| ignoreMergeFormat | boolean | إذا كان  true  فسيتم إهمال تنسيق نتيجة الحقل المباشر، بغض النظر عن مفتاح MERGEFORMAT، وإلا سيتم إجراء تحديث عادي. |

