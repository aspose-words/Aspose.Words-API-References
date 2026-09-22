---
title: "ControlChar"
linktitle: "ControlChar"
second_title: "Aspose.Words لـ Java"
description: "أحرف التحكم التي تُصادف غالبًا في المستندات في Java."
type: docs
weight: 130
url: /ar/java/com.aspose.words/controlchar/
---

**Inheritance:**
java.lang.Object
```
public class ControlChar
```

أحرف التحكم التي تُصادف غالبًا في المستندات.

لمزيد من المعلومات، زر مقالة الوثائق [ Working With Control Characters ][Working With Control Characters].

 **Remarks:** 

يوفر إصدارات كل من char و string لنفس الثوابت. على سبيل المثال: string [LINE\\_BREAK](../../com.aspose.words/controlchar/\\#LINE-BREAK) و char [LINE\\_BREAK\\_CHAR](../../com.aspose.words/controlchar/\\#LINE-BREAK-CHAR) لهما نفس القيمة.

 **Examples:** 

يوضح كيفية استخدام أحرف التحكم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert paragraphs with text with DocumentBuilder.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Converting the document to text form reveals that control characters
 // represent some of the document's structural elements, such as page breaks.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         MessageFormat.format("Hello again!{0}", ControlChar.CR) +
         ControlChar.PAGE_BREAK, doc.getText());

 // When converting a document to string form,
 // we can omit some of the control characters with the Trim method.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         "Hello again!", doc.getText().trim());
 
```


[Working With Control Characters]: https://docs.aspose.com/words/java/working-with-control-characters/
## الحقول

| حقل | الوصف |
| --- | --- |
| [CELL](#CELL) | حرف نهاية خلية جدول أو نهاية صف جدول: \"\\\\x0007\" أو \"\\\\a\". |
| [CELL_CHAR](#CELL-CHAR) | حرف نهاية خلية جدول أو نهاية صف جدول: (char)7 أو \"\\\\a\". |
| [COLUMN_BREAK](#COLUMN-BREAK) | حرف نهاية العمود: \"\\\\x000e\". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | حرف نهاية العمود: (char)14. |
| [CR](#CR) | حرف عودة السطر: \"\\\\x000d\" أو \"\\\\r\". |
| [CR_LF](#CR-LF) | عودة السطر متبوعة بحرف تغذية السطر: \"\\\\x000d\\\\x000a\" أو \"\\\\r\\\\n\". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | هذا هو الحرف \"o\" المستخدم كقيمة افتراضية في حقول نماذج إدخال النص. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | حرف نهاية حقل MS Word: (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | حرف فاصل الحقل يفصل بين رمز الحقل وقيمة الحقل. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | حرف بداية حقل MS Word: (char)19. |
| [LF](#LF) | حرف سطر جديد: "\\x000a" أو "\\n". |
| [LINE_BREAK](#LINE-BREAK) | حرف فاصل سطر: "\\x000b" أو "\\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | حرف فاصل سطر: (char)11 أو "\\v". |
| [LINE_FEED](#LINE-FEED) | حرف سطر جديد: "\\x000a" أو "\\n". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | حرف سطر جديد: (char)10 أو "\\n". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | الواصلة غير القابلة للكسر في Microsoft Word هي (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | حرف مساحة غير قابلة للكسر: "\\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | حرف مساحة غير قابلة للكسر: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | الواصلة الاختيارية في Microsoft Word هي (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | حرف فاصل صفحة: "\\x000c" أو "\\f". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | حرف فاصل صفحة: (char)12 أو "\\f". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | حرف نهاية الفقرة: "\\x000d" أو "\\r". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | حرف نهاية الفقرة: (char)13 أو "\\r". |
| [SECTION_BREAK](#SECTION-BREAK) | حرف نهاية القسم: "\\x000c" أو "\\f". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | حرف نهاية القسم: (char)12 أو "\\f". |
| [SPACE_CHAR](#SPACE-CHAR) | حرف مسافة: (char)32. |
| [TAB](#TAB) | حرف تبويب: "\\x0009" أو "\\t". |
| [TAB_CHAR](#TAB-CHAR) | حرف تبويب: (char)9 أو "\\t". |
### CELL {#CELL}
```
public static String CELL
```


حرف نهاية خلية جدول أو نهاية صف جدول: \"\\\\x0007\" أو \"\\\\a\".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### CELL_CHAR {#CELL-CHAR}
```
public static char CELL_CHAR
```


حرف نهاية خلية جدول أو نهاية صف جدول: (char)7 أو \"\\\\a\".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### COLUMN_BREAK {#COLUMN-BREAK}
```
public static String COLUMN_BREAK
```


حرف نهاية العمود: \"\\\\x000e\".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### COLUMN_BREAK_CHAR {#COLUMN-BREAK-CHAR}
```
public static char COLUMN_BREAK_CHAR
```


حرف نهاية العمود: (char)14.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### CR {#CR}
```
public static String CR
```


حرف عودة السطر: "\\x000d" أو "\\r". نفس ما هو [PARAGRAPH\\_BREAK](../../com.aspose.words/controlchar/#PARAGRAPH-BREAK).

 **Examples:** 

يوضح كيفية استخدام أحرف التحكم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert paragraphs with text with DocumentBuilder.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Converting the document to text form reveals that control characters
 // represent some of the document's structural elements, such as page breaks.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         MessageFormat.format("Hello again!{0}", ControlChar.CR) +
         ControlChar.PAGE_BREAK, doc.getText());

 // When converting a document to string form,
 // we can omit some of the control characters with the Trim method.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         "Hello again!", doc.getText().trim());
 
```

### CR_LF {#CR-LF}
```
public static String CR_LF
```


عودة السطر متبوعة بحرف سطر جديد: "\\x000d\\x000a" أو "\\r\\n". لا تُستخدم بهذه الطريقة في مستندات Microsoft Word، ولكنها تُستخدم عادةً في ملفات النص لفواصل الفقرات.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### DEFAULT_TEXT_INPUT_CHAR {#DEFAULT-TEXT-INPUT-CHAR}
```
public static char DEFAULT_TEXT_INPUT_CHAR
```


هذا هو الحرف \"o\" المستخدم كقيمة افتراضية في حقول نماذج إدخال النص.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### FIELD_END_CHAR {#FIELD-END-CHAR}
```
public static char FIELD_END_CHAR
```


حرف نهاية حقل MS Word: (char)21.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### FIELD_SEPARATOR_CHAR {#FIELD-SEPARATOR-CHAR}
```
public static char FIELD_SEPARATOR_CHAR
```


حرف فاصل الحقول يفصل رمز الحقل عن قيمة الحقل. اختياري في بعض الحقول. القيمة: (char)20.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### FIELD_START_CHAR {#FIELD-START-CHAR}
```
public static char FIELD_START_CHAR
```


حرف بداية حقل MS Word: (char)19.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### LF {#LF}
```
public static String LF
```


حرف سطر جديد: "\\x000a" أو "\\n". نفس ما هو [LINE\\_FEED](../../com.aspose.words/controlchar/#LINE-FEED).

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### LINE_BREAK {#LINE-BREAK}
```
public static String LINE_BREAK
```


حرف فاصل سطر: "\\x000b" أو "\\v".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### LINE_BREAK_CHAR {#LINE-BREAK-CHAR}
```
public static char LINE_BREAK_CHAR
```


حرف فاصل سطر: (char)11 أو "\\v".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### LINE_FEED {#LINE-FEED}
```
public static String LINE_FEED
```


حرف سطر جديد: "\\x000a" أو "\\n". نفس ما هو [LF](../../com.aspose.words/controlchar/#LF).

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### LINE_FEED_CHAR {#LINE-FEED-CHAR}
```
public static char LINE_FEED_CHAR
```


حرف سطر جديد: (char)10 أو "\\n".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### NON_BREAKING_HYPHEN_CHAR {#NON-BREAKING-HYPHEN-CHAR}
```
public static char NON_BREAKING_HYPHEN_CHAR
```


الواصلة غير القابلة للكسر في Microsoft Word هي (char)30.

 **Remarks:** 

الواصلة غير القابلة للكسر في Microsoft Word لا تتطابق مع حرف Unicode U+2011 الواصلة غير القابلة للكسر، بل تمثل معلومات داخلية تخبر Microsoft Word بعرض واصلة وعدم كسر السطر.

معلومات مفيدة: http://www.cs.tut.fi/~jkorpela/dashes.html\\#linebreaks.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### NON_BREAKING_SPACE {#NON-BREAKING-SPACE}
```
public static String NON_BREAKING_SPACE
```


حرف مساحة غير قابلة للكسر: "\\x00a0".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### NON_BREAKING_SPACE_CHAR {#NON-BREAKING-SPACE-CHAR}
```
public static char NON_BREAKING_SPACE_CHAR
```


حرف مساحة غير قابلة للكسر: (char)160.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### OPTIONAL_HYPHEN_CHAR {#OPTIONAL-HYPHEN-CHAR}
```
public static char OPTIONAL_HYPHEN_CHAR
```


الواصلة الاختيارية في Microsoft Word هي (char)31.

 **Remarks:** 

الواصلة الاختيارية في Microsoft Word لا تتطابق مع حرف Unicode U+00AD وهو الواصلة الناعمة. بدلاً من ذلك، تُدرج معلومات داخلية تخبر Word بنقطة احتمالية للفصل الواصل.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### PAGE_BREAK {#PAGE-BREAK}
```
public static String PAGE_BREAK
```


حرف فاصل الصفحة: "\\x000c" أو "\\f". لاحظ أن له نفس القيمة مثل [SECTION\_BREAK](../../com.aspose.words/controlchar/\#SECTION-BREAK).

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### PAGE_BREAK_CHAR {#PAGE-BREAK-CHAR}
```
public static char PAGE_BREAK_CHAR
```


حرف فاصل صفحة: (char)12 أو "\\f".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### PARAGRAPH_BREAK {#PARAGRAPH-BREAK}
```
public static String PARAGRAPH_BREAK
```


حرف نهاية الفقرة: "\\x000d" أو "\\r". نفس القيمة مثل [CR](../../com.aspose.words/controlchar/\#CR)

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### PARAGRAPH_BREAK_CHAR {#PARAGRAPH-BREAK-CHAR}
```
public static char PARAGRAPH_BREAK_CHAR
```


حرف نهاية الفقرة: (char)13 أو "\\r".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### SECTION_BREAK {#SECTION-BREAK}
```
public static String SECTION_BREAK
```


حرف نهاية القسم: "\\x000c" أو "\\f". لاحظ أن له نفس القيمة مثل [PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK).

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### SECTION_BREAK_CHAR {#SECTION-BREAK-CHAR}
```
public static char SECTION_BREAK_CHAR
```


حرف نهاية القسم: (char)12 أو "\\f".

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### SPACE_CHAR {#SPACE-CHAR}
```
public static char SPACE_CHAR
```


حرف مسافة: (char)32.

 **Examples:** 

يظهر كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a regular space.
 builder.write("Before space." + ControlChar.SPACE_CHAR + "After space.");

 // Add an NBSP, which is a non-breaking space.
 // Unlike the regular space, this space cannot have an automatic line break at its position.
 builder.write("Before space." + ControlChar.NON_BREAKING_SPACE + "After space.");

 // Add a tab character.
 builder.write("Before tab." + ControlChar.TAB + "After tab.");

 // Add a line break.
 builder.write("Before line break." + ControlChar.LINE_BREAK + "After line break.");

 // Add a new line and starts a new paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());
 builder.write("Before line feed." + ControlChar.LINE_FEED + "After line feed.");
 Assert.assertEquals(2, doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount());

 // The line feed character has two versions.
 Assert.assertEquals(ControlChar.LINE_FEED, ControlChar.LF);

 // Carriage returns and line feeds can be represented together by one character.
 Assert.assertEquals(ControlChar.CR_LF, ControlChar.CR + ControlChar.LF);

 // Add a paragraph break, which will start a new paragraph.
 builder.write("Before paragraph break." + ControlChar.PARAGRAPH_BREAK + "After paragraph break.");
 Assert.assertEquals(doc.getFirstSection().getBody().getChildNodes(NodeType.PARAGRAPH, true).getCount(), 3);

 // Add a section break. This does not make a new section or paragraph.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 builder.write("Before section break." + ControlChar.SECTION_BREAK + "After section break.");
 Assert.assertEquals(doc.getSections().getCount(), 1);

 // Add a page break.
 builder.write("Before page break." + ControlChar.PAGE_BREAK + "After page break.");

 // A page break is the same value as a section break.
 Assert.assertEquals(ControlChar.PAGE_BREAK, ControlChar.SECTION_BREAK);

 // Insert a new section, and then set its column count to two.
 doc.appendChild(new Section(doc));
 builder.moveToSection(1);
 builder.getCurrentSection().getPageSetup().getTextColumns().setCount(2);

 // We can use a control character to mark the point where text moves to the next column.
 builder.write("Text at end of column 1." + ControlChar.COLUMN_BREAK + "Text at beginning of column 2.");

 doc.save(getArtifactsDir() + "ControlChar.InsertControlChars.docx");

 // There are char and string counterparts for most characters.
 Assert.assertEquals(ControlChar.CELL.toCharArray()[0], ControlChar.CELL_CHAR);
 Assert.assertEquals(ControlChar.NON_BREAKING_SPACE.toCharArray()[0], ControlChar.NON_BREAKING_SPACE_CHAR);
 Assert.assertEquals(ControlChar.TAB.toCharArray()[0], ControlChar.TAB_CHAR);
 Assert.assertEquals(ControlChar.LINE_BREAK.toCharArray()[0], ControlChar.LINE_BREAK_CHAR);
 Assert.assertEquals(ControlChar.LINE_FEED.toCharArray()[0], ControlChar.LINE_FEED_CHAR);
 Assert.assertEquals(ControlChar.PARAGRAPH_BREAK.toCharArray()[0], ControlChar.PARAGRAPH_BREAK_CHAR);
 Assert.assertEquals(ControlChar.SECTION_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.PAGE_BREAK.toCharArray()[0], ControlChar.SECTION_BREAK_CHAR);
 Assert.assertEquals(ControlChar.COLUMN_BREAK.toCharArray()[0], ControlChar.COLUMN_BREAK_CHAR);
 
```

### TAB {#TAB}
```
public static String TAB
```


حرف تبويب: "\\x0009" أو "\\t".

 **Examples:** 

يوضح كيفية تعيين فاصل مخصص لمواقع إيقاف التبويب.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

### TAB_CHAR {#TAB-CHAR}
```
public static char TAB_CHAR
```


حرف تبويب: (char)9 أو "\\t".

 **Examples:** 

يوضح كيفية تعيين فاصل مخصص لمواقع إيقاف التبويب.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

