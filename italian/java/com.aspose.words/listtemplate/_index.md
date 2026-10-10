---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words per Java"
description: "Specifica uno dei formati di elenco predefiniti disponibili in Microsoft Word in Java."
type: docs
weight: 432
url: /it/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Specifica uno dei formati di elenco predefiniti disponibili in Microsoft Word.

 **Remarks:** 

Un valore di modello di elenco viene utilizzato come parametro nel metodo **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)**.

I modelli di elenco di Aspose.Words corrispondono ai 21 modelli di elenco disponibili nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word 2003.

 **Examples:** 

Mostra come lavorare con i livelli di elenco.

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

Mostra come riavviare la numerazione in un elenco copiando un elenco.

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

Mostra come creare un documento che contiene tutti i modelli di elenco delle intestazioni di struttura.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | Il punto elenco del primo livello è un carattere Wingding a forma di freccia. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | Il punto elenco del primo livello è un cerchio. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Elenco puntato predefinito con 9 livelli. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | Il punto elenco del primo livello è un carattere Wingding a 4 diamanti. |
| [BULLET_DISK](#BULLET-DISK) | Stesso di [BULLET\\_DEFAULT](../../com.aspose.words/listtemplate/\\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | Il punto elenco del primo livello è un quadrato. |
| [BULLET_TICK](#BULLET-TICK) | Il punto elenco del primo livello è un carattere Wingding a spunta. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | Stesso di [NUMBER\\_DEFAULT](../../com.aspose.words/listtemplate/\\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | Il numero del primo livello è "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Elenco numerato predefinito con 9 livelli. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | Il numero del primo livello è "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | Il numero del primo livello è "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | Il numero del primo livello è "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | Il numero del primo livello è "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | Il numero del primo livello è "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Uno schema elenca vari punti per diversi livelli. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Un elenco outline con livelli collegati agli stili di intestazione. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Un elenco outline con livelli collegati agli stili di intestazione. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Un elenco outline con livelli collegati agli stili di intestazione. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Un elenco outline con livelli collegati agli stili di intestazione. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Un elenco outline con livelli numerati "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Un elenco outline con livelli numerati "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


Il punto del primo livello è un carattere Wingding a forma di freccia. I livelli rimanenti sono gli stessi di [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corrisponde al 6° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


Il punto del primo livello è un cerchio. I livelli rimanenti sono gli stessi di [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corrisponde al 2° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Elenco puntato predefinito con 9 livelli. Il punto del primo livello è un disco, il punto del secondo livello è un cerchio, il punto del terzo livello è un quadrato. Poi la formattazione si ripete per i livelli rimanenti.

Ogni livello è rientrato a destra di 0.25" rispetto al livello precedente.

Corrisponde al 1° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


Il punto del primo livello è un carattere Wingding a forma di diamante a 4 punte. I livelli rimanenti sono gli stessi di [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corrisponde al 5° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


Stesso di [BULLET\\_DEFAULT](../../com.aspose.words/listtemplate/\\#BULLET-DEFAULT).

Corrisponde al 1° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


Il punto del primo livello è un quadrato. I livelli rimanenti sono gli stessi di [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corrisponde al 3° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


Il punto del primo livello è un carattere Wingding a forma di spunta. I livelli rimanenti sono gli stessi di [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corrisponde al 7° modello di elenco puntato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


Stesso di [NUMBER\\_DEFAULT](../../com.aspose.words/listtemplate/\\#NUMBER-DEFAULT).

Corrisponde al 1° modello di elenco numerato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


Il numero del primo livello è "1)". I livelli rimanenti sono gli stessi di [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corrisponde al 2° modello di elenco numerato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Elenco numerato predefinito con 9 livelli. Numerazione araba (1., 2., 3., ...) per il primo livello, numerazione con lettere minuscole (a., b., c., ...) per il secondo livello, numerazione romana minuscola (i., ii., iii., ...) per il terzo livello. Poi la formattazione si ripete per i livelli rimanenti.

Ogni livello è rientrato a destra di 0.25" rispetto al livello precedente.

Corrisponde al 1° modello di elenco numerato nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


Il numero del primo livello è "a.". I livelli rimanenti sono gli stessi di [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corrisponde al modello di elenco numerato 6° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


Il numero del primo livello è "a)". I livelli rimanenti sono gli stessi di [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corrisponde al modello di elenco numerato 5° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


Il numero del primo livello è "i.". I livelli rimanenti sono gli stessi di [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corrisponde al modello di elenco numerato 7° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


Il numero del primo livello è "A.". I livelli rimanenti sono gli stessi di [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corrisponde al modello di elenco numerato 4° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


Il numero del primo livello è "I.". I livelli rimanenti sono gli stessi di [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corrisponde al modello di elenco numerato 3° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Uno schema elenca vari punti per diversi livelli.

Corrisponde al modello di elenco outline 3° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Un elenco outline con livelli collegati agli stili di intestazione.

Corrisponde al modello di elenco outline 4° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Un elenco outline con livelli collegati agli stili di intestazione.

Corrisponde al modello di elenco outline 7° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Un elenco outline con livelli collegati agli stili di intestazione.

Corrisponde al modello di elenco outline 5° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Un elenco outline con livelli collegati agli stili di intestazione.

Corrisponde al modello di elenco outline 6° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Un elenco outline con livelli numerati "1., 1.1., 1.1.1, ...".

Corrisponde al modello di elenco outline 2° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Un elenco outline con livelli numerati "1), a), i), (1), (a), (i), 1., a., i.".

Corrisponde al modello di elenco outline 1° nella finestra di dialogo Elenchi puntati e numerazione di Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
