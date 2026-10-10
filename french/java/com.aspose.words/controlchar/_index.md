---
title: "ControlChar"
linktitle: "ControlChar"
second_title: "Aspose.Words pour Java"
description: "Caractères de contrôle souvent rencontrés dans les documents en Java."
type: docs
weight: 130
url: /fr/java/com.aspose.words/controlchar/
---

**Inheritance:**
java.lang.Object
```
public class ControlChar
```

Caractères de contrôle souvent rencontrés dans les documents.

Pour en savoir plus, consultez l'article de documentation [ Working With Control Characters ][Working With Control Characters].

 **Remarks:** 

Fournit à la fois les versions char et string des mêmes constantes. Par exemple : string [LINE\_BREAK](../../com.aspose.words/controlchar/\#LINE-BREAK) et char [LINE\_BREAK\_CHAR](../../com.aspose.words/controlchar/\#LINE-BREAK-CHAR) ont la même valeur.

 **Examples:** 

Montre comment utiliser les caractères de contrôle.

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
## Champs

| Champ | Description |
| --- | --- |
| [CELL](#CELL) | Caractère de fin de cellule de tableau ou de fin de ligne de tableau : "\\x0007" ou "\\a". |
| [CELL_CHAR](#CELL-CHAR) | Caractère de fin de cellule de tableau ou de fin de ligne de tableau : (char)7 ou "\\a". |
| [COLUMN_BREAK](#COLUMN-BREAK) | Caractère de fin de colonne : "\\x000e". |
| [COLUMN_BREAK_CHAR](#COLUMN-BREAK-CHAR) | Caractère de fin de colonne : (char)14. |
| [CR](#CR) | Caractère de retour chariot : "\\x000d" ou "\\r". |
| [CR_LF](#CR-LF) | Retour chariot suivi du caractère saut de ligne : "\\x000d\\x000a" ou "\\r\\n". |
| [DEFAULT_TEXT_INPUT_CHAR](#DEFAULT-TEXT-INPUT-CHAR) | Ceci est le caractère "o" utilisé comme valeur par défaut dans les champs de formulaire de saisie de texte. |
| [FIELD_END_CHAR](#FIELD-END-CHAR) | Caractère de fin de champ MS Word : (char)21. |
| [FIELD_SEPARATOR_CHAR](#FIELD-SEPARATOR-CHAR) | Le caractère séparateur de champ sépare le code du champ de la valeur du champ. |
| [FIELD_START_CHAR](#FIELD-START-CHAR) | Caractère de début de champ MS Word : (char)19. |
| [LF](#LF) | Caractère de saut de ligne : "\x000a" ou "\n". |
| [LINE_BREAK](#LINE-BREAK) | Caractère de saut de ligne : "\x000b" ou "\v". |
| [LINE_BREAK_CHAR](#LINE-BREAK-CHAR) | Caractère de saut de ligne : (char)11 ou "\v". |
| [LINE_FEED](#LINE-FEED) | Caractère de saut de ligne : "\x000a" ou "\n". |
| [LINE_FEED_CHAR](#LINE-FEED-CHAR) | Caractère de saut de ligne : (char)10 ou "\n". |
| [NON_BREAKING_HYPHEN_CHAR](#NON-BREAKING-HYPHEN-CHAR) | Le trait d'union insécable dans Microsoft Word est (char)30. |
| [NON_BREAKING_SPACE](#NON-BREAKING-SPACE) | Caractère d'espace insécable : "\x00a0". |
| [NON_BREAKING_SPACE_CHAR](#NON-BREAKING-SPACE-CHAR) | Caractère d'espace insécable : (char)160. |
| [OPTIONAL_HYPHEN_CHAR](#OPTIONAL-HYPHEN-CHAR) | Le trait d'union optionnel dans Microsoft Word est (char)31. |
| [PAGE_BREAK](#PAGE-BREAK) | Caractère de saut de page : "\x000c" ou "\f". |
| [PAGE_BREAK_CHAR](#PAGE-BREAK-CHAR) | Caractère de saut de page : (char)12 ou "\f". |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | Caractère de fin de paragraphe : "\x000d" ou "\r". |
| [PARAGRAPH_BREAK_CHAR](#PARAGRAPH-BREAK-CHAR) | Caractère de fin de paragraphe : (char)13 ou "\r". |
| [SECTION_BREAK](#SECTION-BREAK) | Caractère de fin de section : "\x000c" ou "\f". |
| [SECTION_BREAK_CHAR](#SECTION-BREAK-CHAR) | Caractère de fin de section : (char)12 ou "\f". |
| [SPACE_CHAR](#SPACE-CHAR) | Caractère d'espace : (char)32. |
| [TAB](#TAB) | Caractère de tabulation : "\x0009" ou "\t". |
| [TAB_CHAR](#TAB-CHAR) | Caractère de tabulation : (char)9 ou "\t". |
### CELL {#CELL}
```
public static String CELL
```


Caractère de fin de cellule de tableau ou de fin de ligne de tableau : "\\x0007" ou "\\a".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de cellule de tableau ou de fin de ligne de tableau : (char)7 ou "\\a".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de colonne : "\\x000e".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de colonne : (char)14.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de retour chariot : "\x000d" ou "\r". Identique à [PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK).

 **Examples:** 

Montre comment utiliser les caractères de contrôle.

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


Retour chariot suivi du caractère de saut de ligne : "\x000d\x000a" ou "\r\n". Non utilisé ainsi dans les documents Microsoft Word, mais couramment utilisé dans les fichiers texte pour les sauts de paragraphe.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Ceci est le caractère "o" utilisé comme valeur par défaut dans les champs de formulaire de saisie de texte.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de champ MS Word : (char)21.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Le caractère séparateur de champ sépare le code du champ de la valeur du champ. Facultatif dans certains champs. Valeur : (char)20.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de début de champ MS Word : (char)19.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de ligne : "\x000a" ou "\n". Identique à [LINE\_FEED](../../com.aspose.words/controlchar/\#LINE-FEED).

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de ligne : "\x000b" ou "\v".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de ligne : (char)11 ou "\v".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de ligne : "\x000a" ou "\n". Identique à [LF](../../com.aspose.words/controlchar/\#LF).

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de ligne : (char)10 ou "\n".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Le trait d'union insécable dans Microsoft Word est (char)30.

 **Remarks:** 

Le trait d'union insécable dans Microsoft Word ne correspond pas au caractère Unicode U+2011 trait d'union insécable, mais représente plutôt une information interne indiquant à Microsoft Word d'afficher un trait d'union et de ne pas couper la ligne.

Informations utiles : http://www.cs.tut.fi/~jkorpela/dashes.html\#linebreaks.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère d'espace insécable : "\x00a0".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère d'espace insécable : (char)160.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Le trait d'union optionnel dans Microsoft Word est (char)31.

 **Remarks:** 

Le tiret optionnel dans Microsoft Word ne correspond pas au caractère Unicode U+00AD tiret doux. Au lieu de cela, il insère des informations internes qui indiquent à Word un point de césure possible.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de page : "\x000c" ou "\f". Notez qu’il a la même valeur que [SECTION_BREAK](../../com.aspose.words/controlchar/#SECTION-BREAK).

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de saut de page : (char)12 ou "\f".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de paragraphe : "\x000d" ou "\r". Identique à [CR](../../com.aspose.words/controlchar/#CR)

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de paragraphe : (char)13 ou "\r".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de section : "\x000c" ou "\f". Notez qu’il a la même valeur que [PAGE_BREAK](../../com.aspose.words/controlchar/#PAGE-BREAK).

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de fin de section : (char)12 ou "\f".

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère d'espace : (char)32.

 **Examples:** 

Montre comment ajouter divers caractères de contrôle à un document.

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


Caractère de tabulation : "\x0009" ou "\t".

 **Examples:** 

Montre comment définir un intervalle personnalisé pour les positions des tabulations.

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


Caractère de tabulation : (char)9 ou "\t".

 **Examples:** 

Montre comment définir un intervalle personnalisé pour les positions des tabulations.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

