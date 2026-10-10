---
title: "ControlChar"
linktitle: "ControlChar"
second_title: "Aspose.Words per Java"
description: "Caratteri di controllo spesso incontrati nei documenti in Java."
type: docs
weight: 130
url: /it/java/com.aspose.words/controlchar/
---

**Inheritance:**
java.lang.Object
```
public class ControlChar
```

Caratteri di controllo spesso incontrati nei documenti.

Per saperne di più, visita l'articolo di documentazione [ Working With Control Characters ][Working With Control Characters].

 **Remarks:** 

Fornisce sia versioni char che stringa delle stesse costanti. Ad esempio: string [LINE\_BREAK](../../com.aspose.words/controlchar/\#LINE-BREAK) e char [LINE\_BREAK\_CHAR](../../com.aspose.words/controlchar/\#LINE-BREAK-CHAR) hanno lo stesso valore.

 **Examples:** 

Mostra come utilizzare i caratteri di controllo.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CELL](#CELL) | Carattere di fine cella di tabella o fine riga di tabella: "\\x0007" o "\\a". |
| [CELL_CHAR](#CELL-CHAR) | Carattere di fine cella di tabella o fine riga di tabella: (char)7 o "\\a". |
| [COLUMN_BREAK](#COLUMN-BREAK) | Carattere di fine colonna: "\\x000e". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | Carattere di fine colonna: (char)14. |
| [CR](#CR) | Carattere di ritorno a capo: "\\x000d" o "\\r". |
| [CR_LF](#CR-LF) | Carattere di ritorno a capo seguito da avanzamento riga: "\\x000d\\x000a" o "\\r\\n". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | Questo è il carattere "o" usato come valore predefinito nei campi di input di testo del modulo. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | Carattere di fine campo MS Word: (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | Il carattere separatore di campo separa il codice del campo dal valore del campo. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | Carattere di inizio campo MS Word: (char)19. |
| [LF](#LF) | Carattere di avanzamento riga: "\x000a" o "\n". |
| [LINE_BREAK](#LINE-BREAK) | Carattere di interruzione di riga: "\x000b" o "\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | Carattere di interruzione di riga: (char)11 o "\v". |
| [LINE_FEED](#LINE-FEED) | Carattere di avanzamento riga: "\x000a" o "\n". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | Carattere di avanzamento riga: (char)10 o "\n". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Il trattino non interrotto in Microsoft Word è (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | Carattere di spazio non interrotto: "\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | Carattere di spazio non interrotto: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Il trattino opzionale in Microsoft Word è (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | Carattere di interruzione di pagina: "\x000c" o "\f". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | Carattere di interruzione di pagina: (char)12 o "\f". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | Carattere di fine paragrafo: "\x000d" o "\r". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | Carattere di fine paragrafo: (char)13 o "\r". |
| [SECTION_BREAK](#SECTION-BREAK) | Carattere di fine sezione: "\x000c" o "\f". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | Carattere di fine sezione: (char)12 o "\f". |
| [SPACE_CHAR](#SPACE-CHAR) | Carattere di spazio: (char)32. |
| [TAB](#TAB) | Carattere di tabulazione: "\x0009" o "\t". |
| [TAB_CHAR](#TAB-CHAR) | Carattere di tabulazione: (char)9 o "\t". |
### CELL {#CELL}
```
public static String CELL
```


Carattere di fine cella di tabella o fine riga di tabella: "\\x0007" o "\\a".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine cella di tabella o fine riga di tabella: (char)7 o "\\a".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine colonna: "\\x000e".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine colonna: (char)14.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di ritorno a capo: "\x000d" o "\r". Stesso di [PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK).

 **Examples:** 

Mostra come utilizzare i caratteri di controllo.

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


Carattere di ritorno a capo seguito da avanzamento riga: "\x000d\x000a" o "\r\n". Non utilizzato così nei documenti Microsoft Word, ma comunemente usato nei file di testo per le interruzioni di paragrafo.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Questo è il carattere "o" usato come valore predefinito nei campi di input di testo del modulo.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine campo MS Word: (char)21.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Il carattere separatore di campo separa il codice del campo dal valore del campo. Opzionale in alcuni campi. Valore: (char)20.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di inizio campo MS Word: (char)19.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di avanzamento riga: "\x000a" o "\n". Stesso di [LINE\_FEED](../../com.aspose.words/controlchar/\#LINE-FEED).

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di interruzione di riga: "\x000b" o "\v".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di interruzione di riga: (char)11 o "\v".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di avanzamento riga: "\x000a" o "\n". Stesso di [LF](../../com.aspose.words/controlchar/\#LF).

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di avanzamento riga: (char)10 o "\n".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Il trattino non interrotto in Microsoft Word è (char)30.

 **Remarks:** 

Il trattino non interrotto in Microsoft Word non corrisponde al carattere Unicode U+2011 trattino non interrotto ma rappresenta invece informazioni interne che indicano a Microsoft Word di visualizzare un trattino e di non interrompere la linea.

Informazioni utili: http://www.cs.tut.fi/~jkorpela/dashes.html\#linebreaks.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di spazio non interrotto: "\x00a0".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di spazio non interrotto: (char)160.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Il trattino opzionale in Microsoft Word è (char)31.

 **Remarks:** 

Il trattino opzionale in Microsoft Word non corrisponde al carattere Unicode U+00AD soft hyphen. Invece, inserisce informazioni interne che indicano a Word un possibile punto di sillabazione.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di interruzione di pagina: "\\x000c" o "\\f". Nota che ha lo stesso valore di [SECTION\\_BREAK](../../com.aspose.words/controlchar/\\#SECTION-BREAK).

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di interruzione di pagina: (char)12 o "\f".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine paragrafo: "\\x000d" o "\\r". Uguale a [CR](../../com.aspose.words/controlchar/\\#CR).

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine paragrafo: (char)13 o "\r".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine sezione: "\\x000c" o "\\f". Nota che ha lo stesso valore di [PAGE\\_BREAK](../../com.aspose.words/controlchar/\\#PAGE-BREAK).

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di fine sezione: (char)12 o "\f".

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di spazio: (char)32.

 **Examples:** 

Mostra come aggiungere vari caratteri di controllo a un documento.

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


Carattere di tabulazione: "\x0009" o "\t".

 **Examples:** 

Mostra come impostare un intervallo personalizzato per le posizioni dei tabulatori.

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


Carattere di tabulazione: (char)9 o "\t".

 **Examples:** 

Mostra come impostare un intervallo personalizzato per le posizioni dei tabulatori.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

