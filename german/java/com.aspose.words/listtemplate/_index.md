---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words für Java"
description: "Gibt eines der vordefinierten Listenformate an, die in Microsoft Word für Java verfügbar sind."
type: docs
weight: 432
url: /de/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Gibt eines der vordefinierten Listformate an, die in Microsoft Word verfügbar sind.

 **Remarks:** 

Ein Listenvorlagenwert wird als Parameter in die **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)** Methode verwendet.

Aspose.Words Listenvorlagen entsprechen den 21 Listenvorlagen, die im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word 2003 verfügbar sind.

 **Examples:** 

Zeigt, wie man mit Listenebenen arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertFalse(builder.getListFormat().isListItem());

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create using a document builder.
 // 1 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.NUMBER_DEFAULT));

 Assert.assertTrue(builder.getListFormat().isListItem());

 // By setting the "ListLevelNumber" property, we can increase the list level
 // to begin a self-contained sub-list at the current list item.
 // The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
 // Deeper list levels use letters and lowercase Roman numerals.
 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // 2 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 // Deeper levels of this list will use different symbols, such as "\u25a0" and "\u25cb".
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));

 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
 builder.getListFormat().setList(null);

 Assert.assertFalse(builder.getListFormat().isListItem());

 doc.save(getArtifactsDir() + "Lists.SpecifyListLevel.docx");
 
```

Zeigt, wie man die Nummerierung in einer Liste durch Kopieren einer Liste neu startet.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize its first list level.
 List list1 = doc.getLists().add(ListTemplate.NUMBER_ARABIC_PARENTHESIS);
 list1.getListLevels().get(0).getFont().setColor(Color.RED);
 list1.getListLevels().get(0).setAlignment(ListLevelAlignment.RIGHT);

 // Apply our list to some paragraphs.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("List 1 starts below:");
 builder.getListFormat().setList(list1);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 // We can add a copy of an existing list to the document's list collection
 // to create a similar list without making changes to the original.
 List list2 = doc.getLists().addCopy(list1);
 list2.getListLevels().get(0).getFont().setColor(Color.BLUE);
 list2.getListLevels().get(0).setStartAt(10);

 // Apply the second list to new paragraphs.
 builder.writeln("List 2 starts below:");
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.RestartNumberingUsingListCopy.docx");
 
```

Zeigt, wie man ein Dokument erstellt, das alle Gliederungsüberschriften-Listenvorlagen enthält.

```

 public void outlineHeadingTemplates() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     List docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_ARTICLE_SECTION);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Article Section\"");

     docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_LEGAL);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Legal\"");

     builder.insertBreak(BreakType.PAGE_BREAK);

     docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_NUMBERS);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Numbers\"");

     docList = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_CHAPTER);
     addOutlineHeadingParagraphs(builder, docList, "Aspose.Words Outline - \"Chapters\"");

     doc.save(getArtifactsDir() + "Lists.OutlineHeadingTemplates.docx");
 }

 private static void addOutlineHeadingParagraphs(final DocumentBuilder builder, final List docList, final String title) {
     builder.getParagraphFormat().clearFormatting();
     builder.writeln(title);

     for (int i = 0; i < 9; i++) {
         builder.getListFormat().setList(docList);
         builder.getListFormat().setListLevelNumber(i);

         String styleName = "Heading " + (i + 1);
         builder.getParagraphFormat().setStyleName(styleName);
         builder.writeln(styleName);
     }

     builder.getListFormat().removeNumbers();
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | Das Aufzählungszeichen der ersten Ebene ist ein Pfeilspitzen‑Wingding‑Zeichen. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | Das Aufzählungszeichen der ersten Ebene ist ein Kreis. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Standard‑Aufzählungsliste mit 9 Ebenen. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | Das Aufzählungszeichen der ersten Ebene ist ein 4‑Diamanten‑Wingding‑Zeichen. |
| [BULLET_DISK](#BULLET-DISK) | Entspricht [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | Das Aufzählungszeichen der ersten Ebene ist ein Quadrat. |
| [BULLET_TICK](#BULLET-TICK) | Das Aufzählungszeichen der ersten Ebene ist ein Häkchen‑Wingding‑Zeichen. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | Entspricht [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | Die Nummer der ersten Ebene ist "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Standard nummerierte Liste mit 9 Ebenen. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | Die Nummer der ersten Ebene ist "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | Die Nummer der ersten Ebene ist "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | Die Nummer der ersten Ebene ist "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | Die Nummer der ersten Ebene ist "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | Die Nummer der ersten Ebene ist "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Eine Gliederungsliste mit verschiedenen Aufzählungszeichen für unterschiedliche Ebenen. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Eine Gliederungsliste, bei der die Ebenen nummeriert sind "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Eine Gliederungsliste mit Ebenen, die nummeriert sind "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


Das Aufzählungszeichen der ersten Ebene ist ein Pfeilspitzen‑Wingding‑Zeichen. Die übrigen Ebenen sind dieselben wie in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Entspricht der 6. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


Das Aufzählungszeichen der ersten Ebene ist ein Kreis. Die übrigen Ebenen sind dieselben wie in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Entspricht der 2. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Standard‑Aufzählungsliste mit 9 Ebenen. Das Aufzählungszeichen der ersten Ebene ist eine Scheibe, das der zweiten Ebene ein Kreis, das der dritten Ebene ein Quadrat. Dann wiederholt sich die Formatierung für die übrigen Ebenen.

Jede Ebene ist relativ zur vorherigen Ebene um 0,25" nach rechts eingerückt.

Entspricht der 1. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


Das Aufzählungszeichen der ersten Ebene ist ein 4‑Diamanten‑Wingding‑Zeichen. Die übrigen Ebenen sind dieselben wie in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Entspricht der 5. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


Entspricht [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Entspricht der 1. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


Das Aufzählungszeichen der ersten Ebene ist ein Quadrat. Die übrigen Ebenen sind dieselben wie in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Entspricht der 3. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


Das Aufzählungszeichen der ersten Ebene ist ein Häkchen‑Wingding‑Zeichen. Die übrigen Ebenen sind dieselben wie in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Entspricht der 7. Aufzählungslisten‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


Entspricht [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 1. nummerierten Listen‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


Die Nummer der ersten Ebene ist "1)". Die übrigen Ebenen sind dieselben wie in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 2. nummerierten Listen‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Standard‑nummerierte Liste mit 9 Ebenen. Arabische Nummerierung (1., 2., 3., ...) für die erste Ebene, Kleinbuchstaben‑Nummerierung (a., b., c., ...) für die zweite Ebene, römische Kleinbuchstaben‑Nummerierung (i., ii., iii., ...) für die dritte Ebene. Dann wiederholt sich die Formatierung für die übrigen Ebenen.

Jede Ebene ist relativ zur vorherigen Ebene um 0,25" nach rechts eingerückt.

Entspricht der 1. nummerierten Listen‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


Die Nummer der ersten Ebene ist "a.". Die übrigen Ebenen sind dieselben wie in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 6. nummerierten Listen‑Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


Die Nummer der ersten Ebene ist "a)". Die übrigen Ebenen sind dieselben wie in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 5. nummerierten Listenvorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


Die Nummer der ersten Ebene ist "i.". Die übrigen Ebenen sind dieselben wie in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 7. nummerierten Listenvorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


Die Nummer der ersten Ebene ist "A.". Die übrigen Ebenen sind dieselben wie in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 4. nummerierten Listenvorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


Die Nummer der ersten Ebene ist "I.". Die übrigen Ebenen sind dieselben wie in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Entspricht der 3. nummerierten Listenvorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Eine Gliederungsliste mit verschiedenen Aufzählungszeichen für unterschiedliche Ebenen.

Entspricht der 3. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind.

Entspricht der 4. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind.

Entspricht der 7. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind.

Entspricht der 5. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Eine Gliederungsliste mit Ebenen, die mit Überschriftenformaten verknüpft sind.

Entspricht der 6. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Eine Gliederungsliste, bei der die Ebenen nummeriert sind "1., 1.1., 1.1.1, ...".

Entspricht der 2. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Eine Gliederungsliste mit Ebenen, die nummeriert sind "1), a), i), (1), (a), (i), 1., a., i.".

Entspricht der 1. Gliederungslisten-Vorlage im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int listTemplate) {#toString-int}
```
public static String toString(int listTemplate)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
