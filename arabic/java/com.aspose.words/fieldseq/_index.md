---
title: "FieldSeq"
linktitle: "FieldSeq"
second_title: "Aspose.Words لـ Java"
description: "يطبق حقل SEQ في Java."
type: docs
weight: 284
url: /ar/java/com.aspose.words/fieldseq/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldSeq extends Field
```

ينفّذ حقل SEQ.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fields ][Working with Fields].

 **Remarks:** 

يرقم الفصول والجداول والرسوم وغيرها من القوائم المعرفة من قبل المستخدم في المستند بشكل تسلسلي.

 **Examples:** 

يظهر كيفية تعبئة حقل الفهرس (TOC) بالمدخلات باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

يظهر كيفية دمج جدول المحتويات وحقول التسلسل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that contains the SEQ field,
 // and the number of the page that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
 // named "TOCBookmark".
 fieldToc.setBookmarkName("TOCBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);

 Assert.assertEquals(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that has a sequence identifier that matches the TOC's
 // TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
 // the bookmark's bounds designated by "BookmarkName".
 builder.write("MySequence #");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will not show up in the TOC because it is outside of the bookmark.");

 builder.startBookmark("TOCBookmark");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
 // The paragraph that contains this field will show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will show up in the TOC next to the entry for the above caption.");

 // This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
 // and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("OtherSequence");
 builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
 // This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
 // The SEQ field itself will not display the contents of that bookmark.
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setBookmarkName("SEQBookmark");
 Assert.assertEquals(" SEQ  MySequence SEQBookmark", fieldSeq.getFieldCode());

 // Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("SEQBookmark");
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", text from inside SEQBookmark.");
 builder.endBookmark("SEQBookmark");

 builder.endBookmark("TOCBookmark");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.Bookmark.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | يحصل على اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |
| [getDisplayResult()](#getDisplayResult) | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [getEnd()](#getEnd) | يحصل على العقدة التي تمثل نهاية الحقل. |
| [getFieldCode()](#getFieldCode) | يرجع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | يرجع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [getFormat()](#getFormat) | يحصل على كائن [FieldFormat](../../com.aspose.words/fieldformat/) الذي يوفر وصولًا مكتوبًا إلى تنسيق الحقل. |
| [getInsertNextNumber()](#getInsertNextNumber) | يحصل على ما إذا كان يجب إدراج رقم التسلسل التالي للعنصر المحدد. |
| [getLocaleId()](#getLocaleId) | يحصل على معرف اللغة (LCID) للحقل. |
| [getResetHeadingLevel()](#getResetHeadingLevel) | يحصل على عدد صحيح يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. |
| [getResetNumber()](#getResetNumber) | يحصل على عدد صحيح لإعادة تعيين رقم التسلسل إليه. |
| [getResult()](#getResult) | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [getSeparator()](#getSeparator) | يحصل على العقدة التي تمثل فاصل الحقل. |
| [getSequenceIdentifier()](#getSequenceIdentifier) | يحصل على الاسم المعين لسلسلة العناصر التي سيتم ترقيمها. |
| [getStart()](#getStart) | يحصل على العقدة التي تمثل بداية الحقل. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | يحصل على نوع حقل Microsoft Word. |
| [isDirty()](#isDirty) | يحصل على ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أجريت على المستند. |
| [isDirty(boolean value)](#isDirty-boolean) | يضبط ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أجريت على المستند. |
| [isLocked()](#isLocked) | يحصل على ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته). |
| [isLocked(boolean value)](#isLocked-boolean) | يضبط ما إذا كان الحقل مقفلاً (يجب عدم إعادة حساب نتيجته). |
| [remove()](#remove) | يزيل الحقل من المستند. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | يضبط اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |
| [setInsertNextNumber(boolean value)](#setInsertNextNumber-boolean) | يضبط ما إذا كان يجب إدراج رقم التسلسل التالي للعنصر المحدد. |
| [setLocaleId(int value)](#setLocaleId-int) | يضبط LCID الخاص بالحقل. |
| [setResetHeadingLevel(String value)](#setResetHeadingLevel-java.lang.String) | يضبط عددًا صحيحًا يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. |
| [setResetNumber(String value)](#setResetNumber-java.lang.String) | يضبط عددًا صحيحًا لإعادة تعيين رقم التسلسل إليه. |
| [setResult(String value)](#setResult-java.lang.String) | يضبط النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [setSequenceIdentifier(String value)](#setSequenceIdentifier-java.lang.String) | يضبط الاسم المعين لسلسلة العناصر التي سيتم ترقيمها. |
| [unlink()](#unlink) | ينفذ إلغاء ربط الحقل. |
| [update()](#update) | ينفذ تحديث الحقل. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | ينفذ تحديثًا للحقل. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


يحصل على اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.

 **Examples:** 

يظهر كيفية دمج جدول المحتويات وحقول التسلسل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that contains the SEQ field,
 // and the number of the page that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
 // named "TOCBookmark".
 fieldToc.setBookmarkName("TOCBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);

 Assert.assertEquals(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that has a sequence identifier that matches the TOC's
 // TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
 // the bookmark's bounds designated by "BookmarkName".
 builder.write("MySequence #");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will not show up in the TOC because it is outside of the bookmark.");

 builder.startBookmark("TOCBookmark");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
 // The paragraph that contains this field will show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will show up in the TOC next to the entry for the above caption.");

 // This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
 // and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("OtherSequence");
 builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
 // This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
 // The SEQ field itself will not display the contents of that bookmark.
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setBookmarkName("SEQBookmark");
 Assert.assertEquals(" SEQ  MySequence SEQBookmark", fieldSeq.getFieldCode());

 // Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("SEQBookmark");
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", text from inside SEQBookmark.");
 builder.endBookmark("SEQBookmark");

 builder.endBookmark("TOCBookmark");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.Bookmark.docx");
 
```

**Returns:**
java.lang.String - اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.
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
### getInsertNextNumber() {#getInsertNextNumber}
```
public boolean getInsertNextNumber()
```


يحصل على ما إذا كان يجب إدراج رقم التسلسل التالي للعنصر المحدد.

 **Examples:** 

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
boolean - ما إذا كان يجب إدراج رقم التسلسل التالي للعنصر المحدد.
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
### getResetHeadingLevel() {#getResetHeadingLevel}
```
public String getResetHeadingLevel()
```


يحصل على عدد صحيح يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. يرجع -1 إذا كان العدد غير موجود.

 **Examples:** 

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
java.lang.String - عدد صحيح يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه.
### getResetNumber() {#getResetNumber}
```
public String getResetNumber()
```


يحصل على عدد صحيح لإعادة تعيين رقم التسلسل إليه. يرجع -1 إذا كان العدد غير موجود.

 **Examples:** 

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
java.lang.String - عدد صحيح لإعادة تعيين رقم التسلسل إليه.
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
### getSequenceIdentifier() {#getSequenceIdentifier}
```
public String getSequenceIdentifier()
```


يحصل على الاسم المعين لسلسلة العناصر التي سيتم ترقيمها.

 **Examples:** 

يظهر كيفية تعبئة حقل الفهرس (TOC) بالمدخلات باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Returns:**
java.lang.String - الاسم المعين لسلسلة العناصر التي سيتم ترقيمها.
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


يضبط اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.

 **Examples:** 

يظهر كيفية دمج جدول المحتويات وحقول التسلسل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that contains the SEQ field,
 // and the number of the page that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // Configure this TOC field to have a SequenceIdentifier property with a value of "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
 // named "TOCBookmark".
 fieldToc.setBookmarkName("TOCBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);

 Assert.assertEquals(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that has a sequence identifier that matches the TOC's
 // TableOfFiguresLabel property. This field will not create an entry in the TOC since it is outside
 // the bookmark's bounds designated by "BookmarkName".
 builder.write("MySequence #");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will not show up in the TOC because it is outside of the bookmark.");

 builder.startBookmark("TOCBookmark");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bookmark's bounds.
 // The paragraph that contains this field will show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", will show up in the TOC next to the entry for the above caption.");

 // This SEQ field's sequence does not match the TOC's "TableOfFiguresLabel" property,
 // and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("OtherSequence");
 builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.");

 // This SEQ field's sequence matches the TOC's "TableOfFiguresLabel" property and is within the bounds of the bookmark.
 // This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
 // The SEQ field itself will not display the contents of that bookmark.
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setBookmarkName("SEQBookmark");
 Assert.assertEquals(" SEQ  MySequence SEQBookmark", fieldSeq.getFieldCode());

 // Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("SEQBookmark");
 builder.write("MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 builder.writeln(", text from inside SEQBookmark.");
 builder.endBookmark("SEQBookmark");

 builder.endBookmark("TOCBookmark");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.Bookmark.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |

### setInsertNextNumber(boolean value) {#setInsertNextNumber-boolean}
```
public void setInsertNextNumber(boolean value)
```


يضبط ما إذا كان يجب إدراج رقم التسلسل التالي للعنصر المحدد.

 **Examples:** 

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | ما إذا كان يجب إدراج رقم التسلسل التالي للعنصر المحدد. |

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

### setResetHeadingLevel(String value) {#setResetHeadingLevel-java.lang.String}
```
public void setResetHeadingLevel(String value)
```


يضبط عددًا صحيحًا يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. يرجع -1 إذا كان العدد غير موجود.

 **Examples:** 

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عدد صحيح يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. |

### setResetNumber(String value) {#setResetNumber-java.lang.String}
```
public void setResetNumber(String value)
```


يضبط عددًا صحيحًا لإعادة تعيين رقم التسلسل إليه. يرجع -1 إذا كان العدد غير موجود.

 **Examples:** 

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عدد صحيح لإعادة تعيين رقم التسلسل إليه. |

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

### setSequenceIdentifier(String value) {#setSequenceIdentifier-java.lang.String}
```
public void setSequenceIdentifier(String value)
```


يضبط الاسم المعين لسلسلة العناصر التي سيتم ترقيمها.

 **Examples:** 

يظهر كيفية تعبئة حقل الفهرس (TOC) بالمدخلات باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field that will display the current count value of "MySequence",
 // after using the "ResetNumber" property to set it to 100.
 builder.write("#");
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetNumber("100");
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\r 100", fieldSeq.getFieldCode());
 Assert.assertEquals("100", fieldSeq.getResult());

 // Display the next number in this sequence with another SEQ field.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.update();

 Assert.assertEquals("101", fieldSeq.getResult());

 // Insert a level 1 heading.
 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("This level 1 heading will reset MySequence to 1");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));

 // Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
 builder.write("\n#");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setResetHeadingLevel("1");
 fieldSeq.update();

 // The above heading is a level 1 heading, so the count for this sequence is reset to 1.
 Assert.assertEquals(" SEQ  MySequence \\s 1", fieldSeq.getFieldCode());
 Assert.assertEquals("1", fieldSeq.getResult());

 // Move to the next number of this sequence.
 builder.write(", #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");
 fieldSeq.setInsertNextNumber(true);
 fieldSeq.update();

 Assert.assertEquals(" SEQ  MySequence \\n", fieldSeq.getFieldCode());
 Assert.assertEquals("2", fieldSeq.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SEQ.ResetNumbering.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | الاسم المعين لسلسلة العناصر التي سيتم ترقيمها. |

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

