---
title: "ControlChar"
linktitle: "ControlChar"
second_title: "Aspose.Words для Java"
description: "Управляющие символы, часто встречающиеся в документах Java."
type: docs
weight: 130
url: /ru/java/com.aspose.words/controlchar/
---

**Inheritance:**
java.lang.Object
```
public class ControlChar
```

Управляющие символы, часто встречающиеся в документах.

Чтобы узнать больше, посетите статью документации [ Working With Control Characters ][Working With Control Characters].

 **Remarks:** 

Предоставляет как версии char, так и string одних и тех же констант. Например: string [LINE\_BREAK](../../com.aspose.words/controlchar/\#LINE-BREAK) и char [LINE\_BREAK\_CHAR](../../com.aspose.words/controlchar/\#LINE-BREAK-CHAR) имеют одинаковое значение.

 **Examples:** 

Показывает, как использовать управляющие символы.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CELL](#CELL) | Символ конца ячейки таблицы или конца строки таблицы: "\\x0007" или "\\a". |
| [CELL_CHAR](#CELL-CHAR) | Символ конца ячейки таблицы или конца строки таблицы: (char)7 или "\\a". |
| [COLUMN_BREAK](#COLUMN-BREAK) | Символ конца столбца: "\\x000e". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | Символ конца столбца: (char)14. |
| [CR](#CR) | Символ возврата каретки: "\\x000d" или "\\r". |
| [CR_LF](#CR-LF) | Символ возврата каретки, за которым следует перевод строки: "\\x000d\\x000a" или "\\r\\n". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | Это символ "o", используемый в качестве значения по умолчанию в текстовых полях форм. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | Символ конца поля MS Word: (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | Символ-разделитель поля отделяет код поля от его значения. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | Символ начала поля MS Word: (char)19. |
| [LF](#LF) | Символ перевода строки: "\x000a" или "\n". |
| [LINE_BREAK](#LINE-BREAK) | Символ разрыва строки: "\x000b" или "\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | Символ разрыва строки: (char)11 или "\v". |
| [LINE_FEED](#LINE-FEED) | Символ перевода строки: "\x000a" или "\n". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | Символ перевода строки: (char)10 или "\n". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Неразрывный дефис в Microsoft Word имеет значение (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | Символ неразрывного пробела: "\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | Символ неразрывного пробела: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Опциональный дефис в Microsoft Word имеет значение (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | Символ разрыва страницы: "\x000c" или "\f". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | Символ разрыва страницы: (char)12 или "\f". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | Символ конца абзаца: "\x000d" или "\r". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | Символ конца абзаца: (char)13 или "\r". |
| [SECTION_BREAK](#SECTION-BREAK) | Символ конца раздела: "\x000c" или "\f". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | Символ конца раздела: (char)12 или "\f". |
| [SPACE_CHAR](#SPACE-CHAR) | Символ пробела: (char)32. |
| [TAB](#TAB) | Символ табуляции: "\x0009" или "\t". |
| [TAB_CHAR](#TAB-CHAR) | Символ табуляции: (char)9 или "\t". |
### CELL {#CELL}
```
public static String CELL
```


Символ конца ячейки таблицы или конца строки таблицы: "\\x0007" или "\\a".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца ячейки таблицы или конца строки таблицы: (char)7 или "\\a".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца столбца: "\\x000e".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца столбца: (char)14.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ возврата каретки: "\x000d" или "\r". То же, что и [PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK).

 **Examples:** 

Показывает, как использовать управляющие символы.

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


Возврат каретки, за которым следует символ перевода строки: "\x000d\x000a" или "\r\n". Не используется так в документах Microsoft Word, но часто применяется в текстовых файлах для разрывов абзацев.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Это символ "o", используемый в качестве значения по умолчанию в текстовых полях форм.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца поля MS Word: (char)21.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ разделителя полей отделяет код поля от его значения. Необязателен в некоторых полях. Значение: (char)20.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ начала поля MS Word: (char)19.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ перевода строки: "\x000a" или "\n". То же, что и [LINE\_FEED](../../com.aspose.words/controlchar/\#LINE-FEED).

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ разрыва строки: "\x000b" или "\v".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ разрыва строки: (char)11 или "\v".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ перевода строки: "\x000a" или "\n". То же, что и [LF](../../com.aspose.words/controlchar/\#LF).

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ перевода строки: (char)10 или "\n".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Неразрывный дефис в Microsoft Word имеет значение (char)30.

 **Remarks:** 

Неразрывный дефис в Microsoft Word не соответствует символу Unicode U+2011 неразрывного дефиса, а представляет собой внутреннюю информацию, указывающую Microsoft Word отображать дефис и не разрывать строку.

Полезная информация: http://www.cs.tut.fi/~jkorpela/dashes.html\#linebreaks.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ неразрывного пробела: "\x00a0".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ неразрывного пробела: (char)160.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Опциональный дефис в Microsoft Word имеет значение (char)31.

 **Remarks:** 

Необязательный дефис в Microsoft Word не соответствует символу Unicode U+00AD (мягкий дефис). Вместо этого он вставляет внутреннюю информацию, которая сообщает Word о возможной точке переноса.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ разрыва страницы: "\\x000c" или "\\f". Обратите внимание, что он имеет то же значение, что и [SECTION\_BREAK](../../com.aspose.words/controlchar/\#SECTION-BREAK).

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ разрыва страницы: (char)12 или "\f".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца абзаца: "\\x000d" или "\\r". То же, что и [CR](../../com.aspose.words/controlchar/\#CR).

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца абзаца: (char)13 или "\r".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца раздела: "\\x000c" или "\\f". Обратите внимание, что он имеет то же значение, что и [PAGE\_BREAK](../../com.aspose.words/controlchar/\#PAGE-BREAK).

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ конца раздела: (char)12 или "\f".

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ пробела: (char)32.

 **Examples:** 

Показывает, как добавить различные управляющие символы в документ.

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


Символ табуляции: "\x0009" или "\t".

 **Examples:** 

Показывает, как задать пользовательский интервал для позиций табуляции.

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


Символ табуляции: (char)9 или "\t".

 **Examples:** 

Показывает, как задать пользовательский интервал для позиций табуляции.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

