---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words para Java"
description: "Especifica uno de los formatos de lista predefinidos disponibles en Microsoft Word en Java."
type: docs
weight: 432
url: /es/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Especifica uno de los formatos de lista predefinidos disponibles en Microsoft Word.

 **Remarks:** 

Se utiliza un valor de plantilla de lista como parámetro en el método **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)**.

Las plantillas de lista de Aspose.Words corresponden a las 21 plantillas de lista disponibles en el cuadro de diálogo Viñetas y Numeración de Microsoft Word 2003.

 **Examples:** 

Muestra cómo trabajar con niveles de lista.

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

Muestra cómo reiniciar la numeración en una lista copiando una lista.

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

Muestra cómo crear un documento que contiene todas las plantillas de lista de encabezados de esquema.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | La viñeta del primer nivel es un carácter Wingding de punta de flecha. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | La viñeta del primer nivel es un círculo. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Lista con viñetas predeterminada con 9 niveles. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | La viñeta del primer nivel es un carácter Wingding de cuatro diamantes. |
| [BULLET_DISK](#BULLET-DISK) | Igual que [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | La viñeta del primer nivel es un cuadrado. |
| [BULLET_TICK](#BULLET-TICK) | La viñeta del primer nivel es un carácter Wingding de marca de verificación. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | Igual que [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | El número del primer nivel es "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Lista numerada predeterminada con 9 niveles. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | El número del primer nivel es "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | El número del primer nivel es "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | El número del primer nivel es "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | El número del primer nivel es "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | El número del primer nivel es "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Una lista de esquema contiene varias viñetas para diferentes niveles. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Una lista de esquema con niveles vinculados a los estilos de título. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Una lista de esquema con niveles vinculados a los estilos de título. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Una lista de esquema con niveles vinculados a los estilos de título. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Una lista de esquema con niveles vinculados a los estilos de título. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Una lista de esquema con niveles numerados "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Una lista de esquema con niveles numerados "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


La viñeta del primer nivel es un carácter Wingding de cabeza de flecha. Los niveles restantes son los mismos que en [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponde a la sexta plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


La viñeta del primer nivel es un círculo. Los niveles restantes son los mismos que en [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponde a la segunda plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Lista con viñetas predeterminada con 9 niveles. La viñeta del primer nivel es un disco, la del segundo nivel es un círculo, la del tercer nivel es un cuadrado. Luego el formato se repite para los niveles restantes.

Cada nivel está sangrado a la derecha 0.25" respecto al nivel anterior.

Corresponde a la primera plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


La viñeta del primer nivel es un carácter Wingding de 4 diamantes. Los niveles restantes son los mismos que en [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponde a la quinta plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


Igual que [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponde a la primera plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


La viñeta del primer nivel es un cuadrado. Los niveles restantes son los mismos que en [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponde a la tercera plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


La viñeta del primer nivel es un carácter Wingding de marca de verificación. Los niveles restantes son los mismos que en [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponde a la séptima plantilla de lista con viñetas en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


Igual que [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la primera plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


El número del primer nivel es "1)". Los niveles restantes son los mismos que en [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la segunda plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Lista numerada predeterminada con 9 niveles. Numeración arábiga (1., 2., 3., ...) para el primer nivel, numeración con letras minúsculas (a., b., c., ...) para el segundo nivel, numeración romana minúscula (i., ii., iii., ...) para el tercer nivel. Luego el formato se repite para los niveles restantes.

Cada nivel está sangrado a la derecha 0.25" respecto al nivel anterior.

Corresponde a la primera plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


El número del primer nivel es "a.". Los niveles restantes son los mismos que en [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la sexta plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


El número del primer nivel es "a)". Los niveles restantes son los mismos que en [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la quinta plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


El número del primer nivel es "i.". Los niveles restantes son los mismos que en [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la séptima plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


El número del primer nivel es "A.". Los niveles restantes son los mismos que en [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la cuarta plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


El número del primer nivel es "I.". Los niveles restantes son los mismos que en [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponde a la tercera plantilla de lista numerada en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Una lista de esquema contiene varias viñetas para diferentes niveles.

Corresponde a la tercera plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Una lista de esquema con niveles vinculados a los estilos de título.

Corresponde a la cuarta plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Una lista de esquema con niveles vinculados a los estilos de título.

Corresponde a la séptima plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Una lista de esquema con niveles vinculados a los estilos de título.

Corresponde a la quinta plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Una lista de esquema con niveles vinculados a los estilos de título.

Corresponde a la sexta plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Una lista de esquema con niveles numerados "1., 1.1., 1.1.1, ...".

Corresponde a la segunda plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Una lista de esquema con niveles numerados "1), a), i), (1), (a), (i), 1., a., i.".

Corresponde a la primera plantilla de lista de esquema en el cuadro de diálogo Viñetas y numeración de Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
