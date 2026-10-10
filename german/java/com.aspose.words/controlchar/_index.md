---
title: "ControlChar"
linktitle: "ControlChar"
second_title: "Aspose.Words für Java"
description: "Steuerzeichen, die in Dokumenten in Java häufig vorkommen."
type: docs
weight: 130
url: /de/java/com.aspose.words/controlchar/
---

**Inheritance:**
java.lang.Object
```
public class ControlChar
```

Steuerzeichen, die häufig in Dokumenten vorkommen.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working With Control Characters ][Working With Control Characters].

 **Remarks:** 

Bietet sowohl char- als auch string-Versionen derselben Konstanten. Zum Beispiel: string [LINE\_BREAK](../../com.aspose.words/controlchar/\#LINE-BREAK) und char [LINE\_BREAK\_CHAR](../../com.aspose.words/controlchar/\#LINE-BREAK-CHAR) haben denselben Wert.

 **Examples:** 

Zeigt, wie man Steuerzeichen verwendet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CELL](#CELL) | Ende eines Tabellenzellen- oder Tabellenzeilenzeichens: "\\x0007" oder "\\a". |
| [CELL_CHAR](#CELL-CHAR) | Ende eines Tabellenzellen- oder Tabellenzeilenzeichens: (char)7 oder "\\a". |
| [COLUMN_BREAK](#COLUMN-BREAK) | Ende des Spaltenzeichens: "\\x000e". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | Ende des Spaltenzeichens: (char)14. |
| [CR](#CR) | Carriage-Return-Zeichen: "\x000d" oder "\r". |
| [CR_LF](#CR-LF) | Carriage-Return gefolgt von Zeilenumbruchzeichen: "\x000d\x000a" oder "\r\n". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | Dies ist das Zeichen "o", das als Standardwert in Texteingabefeldern verwendet wird. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | Ende-des-MS-Word-Feldzeichens: (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | Das Feldtrennzeichen trennt den Feldcode vom Feldwert. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | Start-des-MS-Word-Feldzeichens: (char)19. |
| [LF](#LF) | Zeilenumbruchzeichen: "\x000a" oder "\n". |
| [LINE_BREAK](#LINE-BREAK) | Zeilenumbruchzeichen: "\x000b" oder "\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | Zeilenumbruchzeichen: (char)11 oder "\v". |
| [LINE_FEED](#LINE-FEED) | Zeilenumbruchzeichen: "\x000a" oder "\n". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | Zeilenumbruchzeichen: (char)10 oder "\n". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Das geschützte Bindestrichzeichen in Microsoft Word ist (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | Geschütztes Leerzeichen: "\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | Geschütztes Leerzeichen: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Optionaler Bindestrich in Microsoft Word ist (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | Seitenumbruchzeichen: "\x000c" oder "\f". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | Seitenumbruchzeichen: (char)12 oder "\f". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | Absatzendezeichen: "\x000d" oder "\r". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | Absatzendezeichen: (char)13 oder "\r". |
| [SECTION_BREAK](#SECTION-BREAK) | Abschnittsendezeichen: "\x000c" oder "\f". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | Abschnittsendezeichen: (char)12 oder "\f". |
| [SPACE_CHAR](#SPACE-CHAR) | Leerzeichen: (char)32. |
| [TAB](#TAB) | Tabulatorzeichen: "\x0009" oder "\t". |
| [TAB_CHAR](#TAB-CHAR) | Tabulatorzeichen: (char)9 oder "\t". |
### CELL {#CELL}
```
public static String CELL
```


Ende eines Tabellenzellen- oder Tabellenzeilenzeichens: "\\x0007" oder "\\a".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Ende eines Tabellenzellen- oder Tabellenzeilenzeichens: (char)7 oder "\\a".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Ende des Spaltenzeichens: "\\x000e".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Ende des Spaltenzeichens: (char)14.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Carriage-Return-Zeichen: "\x000d" oder "\r". Gleich wie [PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK).

 **Examples:** 

Zeigt, wie man Steuerzeichen verwendet.

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


Carriage-Return gefolgt von Zeilenumbruchzeichen: "\\x000d\\x000a" oder "\\r\\n". Wird in Microsoft‑Word‑Dokumenten nicht in dieser Form verwendet, ist aber in Textdateien für Absatzumbrüche üblich.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Dies ist das Zeichen "o", das als Standardwert in Texteingabefeldern verwendet wird.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Ende-des-MS-Word-Feldzeichens: (char)21.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Das Feldtrennzeichen trennt den Feldcode vom Feldwert. In einigen Feldern optional. Wert: (char)20.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Start-des-MS-Word-Feldzeichens: (char)19.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Zeilenumbruchzeichen: "\\x000a" oder "\\n". Gleich wie [LINE_FEED](../../com.aspose.words/controlchar/#LINE-FEED).

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Zeilenumbruchzeichen: "\x000b" oder "\v".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Zeilenumbruchzeichen: (char)11 oder "\v".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Zeilenumbruchzeichen: "\\x000a" oder "\\n". Gleich wie [LF](../../com.aspose.words/controlchar/#LF).

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Zeilenumbruchzeichen: (char)10 oder "\n".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Das geschützte Bindestrichzeichen in Microsoft Word ist (char)30.

 **Remarks:** 

Der geschützte Bindestrich in Microsoft Word entspricht nicht dem Unicode‑Zeichen U+2011 geschützter Bindestrich, sondern stellt interne Informationen dar, die Microsoft Word anweisen, einen Bindestrich anzuzeigen und die Zeile nicht zu umbrechen.

Nützliche Informationen: http://www.cs.tut.fi/~jkorpela/dashes.html#linebreaks.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Geschütztes Leerzeichen: "\x00a0".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Geschütztes Leerzeichen: (char)160.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Optionaler Bindestrich in Microsoft Word ist (char)31.

 **Remarks:** 

Der optionale Bindestrich in Microsoft Word entspricht nicht dem Unicode‑Zeichen U+00AD weicher Bindestrich. Stattdessen fügt er interne Informationen ein, die Word über einen möglichen Trennungs­punkt informieren.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Seitenumbruchzeichen: "\\x000c" oder "\\f". Hinweis: Es hat denselben Wert wie [SECTION_BREAK](../../com.aspose.words/controlchar/#SECTION-BREAK).

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Seitenumbruchzeichen: (char)12 oder "\f".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Absatzendezeichen: "\\x000d" oder "\\r". Gleich wie [CR](../../com.aspose.words/controlchar/#CR)

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Absatzendezeichen: (char)13 oder "\r".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Abschnittsendezeichen: "\\x000c" oder "\\f". Hinweis: Es hat denselben Wert wie [PAGE_BREAK](../../com.aspose.words/controlchar/#PAGE-BREAK).

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Abschnittsendezeichen: (char)12 oder "\f".

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Leerzeichen: (char)32.

 **Examples:** 

Zeigt, wie man verschiedene Steuerzeichen zu einem Dokument hinzufügt.

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


Tabulatorzeichen: "\x0009" oder "\t".

 **Examples:** 

Zeigt, wie man ein benutzerdefiniertes Intervall für Tabulatorpositionen festlegt.

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


Tabulatorzeichen: (char)9 oder "\t".

 **Examples:** 

Zeigt, wie man ein benutzerdefiniertes Intervall für Tabulatorpositionen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

