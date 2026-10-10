---
title: "ListTemplate"
linktitle: "ListTemplate"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'un des formats de liste prédéfinis disponibles dans Microsoft Word en Java."
type: docs
weight: 432
url: /fr/java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Spécifie l'un des formats de liste prédéfinis disponibles dans Microsoft Word.

 **Remarks:** 

Une valeur de modèle de liste est utilisée comme paramètre dans la méthode **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)**.

Les modèles de liste Aspose.Words correspondent aux 21 modèles de liste disponibles dans la boîte de dialogue Puces et numérotation de Microsoft Word 2003.

 **Examples:** 

Montre comment travailler avec les niveaux de liste.

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

Montre comment redémarrer la numérotation dans une liste en copiant une liste.

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

Montre comment créer un document qui contient tous les modèles de liste des titres de plan.

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
## Champs

| Champ | Description |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | La puce du premier niveau est un caractère Wingding en forme de flèche. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | La puce du premier niveau est un cercle. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Liste à puces par défaut avec 9 niveaux. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | La puce du premier niveau est un caractère Wingding en forme de 4 diamants. |
| [BULLET_DISK](#BULLET-DISK) | Identique à [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | La puce du premier niveau est un carré. |
| [BULLET_TICK](#BULLET-TICK) | La puce du premier niveau est un caractère Wingding en forme de coche. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | Identique à [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | Le numéro du premier niveau est "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Liste numérotée par défaut avec 9 niveaux. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | Le numéro du premier niveau est "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | Le numéro du premier niveau est "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | Le numéro du premier niveau est "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | Le numéro du premier niveau est "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | Le numéro du premier niveau est "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | Une liste de plan comporte diverses puces pour différents niveaux. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | Une liste de plan avec des niveaux liés aux styles de titre. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | Une liste de plan avec des niveaux liés aux styles de titre. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | Une liste de plan avec des niveaux liés aux styles de titre. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | Une liste de plan avec des niveaux liés aux styles de titre. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | Une liste de plan dont les niveaux sont numérotés "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | Une liste de plan avec des niveaux numérotés "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


Le symbole de puce du premier niveau est un caractère Wingding en forme de flèche. Les niveaux restants sont les mêmes que dans [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Correspond à la 6e modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


Le symbole de puce du premier niveau est un cercle. Les niveaux restants sont les mêmes que dans [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Correspond à la 2e modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Liste à puces par défaut avec 9 niveaux. Le symbole de puce du premier niveau est un disque, celui du deuxième niveau est un cercle, celui du troisième niveau est un carré. Ensuite, le formatage se répète pour les niveaux restants.

Chaque niveau est indenté vers la droite de 0,25" par rapport au niveau précédent.

Correspond à la 1re modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


Le symbole de puce du premier niveau est un caractère Wingding à 4 diamants. Les niveaux restants sont les mêmes que dans [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Correspond à la 5e modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


Identique à [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Correspond à la 1re modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


Le symbole de puce du premier niveau est un carré. Les niveaux restants sont les mêmes que dans [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Correspond à la 3e modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


Le symbole de puce du premier niveau est un caractère Wingding en forme de coche. Les niveaux restants sont les mêmes que dans [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Correspond à la 7e modèle de liste à puces dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


Identique à [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 1re modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


Le numéro du premier niveau est "1)". Les niveaux restants sont les mêmes que dans [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 2e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Liste numérotée par défaut avec 9 niveaux. Numérotation arabe (1., 2., 3., ...) pour le premier niveau, numérotation en lettres minuscules (a., b., c., ...) pour le deuxième niveau, numérotation romaine en minuscules (i., ii., iii., ...) pour le troisième niveau. Ensuite, le formatage se répète pour les niveaux restants.

Chaque niveau est indenté vers la droite de 0,25" par rapport au niveau précédent.

Correspond à la 1re modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


Le numéro du premier niveau est "a.". Les niveaux restants sont les mêmes que dans [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 6e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


Le numéro du premier niveau est "a)". Les niveaux restants sont les mêmes que dans [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 5e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


Le numéro du premier niveau est "i.". Les niveaux restants sont les mêmes que dans [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 7e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


Le numéro du premier niveau est "A.". Les niveaux restants sont les mêmes que dans [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 4e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


Le numéro du premier niveau est "I.". Les niveaux restants sont les mêmes que dans [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Correspond à la 3e modèle de liste numérotée dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


Une liste de plan comporte diverses puces pour différents niveaux.

Correspond à la 3e modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


Une liste de plan avec des niveaux liés aux styles de titre.

Correspond à la 4e modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


Une liste de plan avec des niveaux liés aux styles de titre.

Correspond à la 7e modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


Une liste de plan avec des niveaux liés aux styles de titre.

Correspond à la 5e modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


Une liste de plan avec des niveaux liés aux styles de titre.

Correspond à la 6e modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


Une liste de plan dont les niveaux sont numérotés "1., 1.1., 1.1.1, ...".

Correspond à la 2e modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


Une liste de plan avec des niveaux numérotés "1), a), i), (1), (a), (i), 1., a., i.".

Correspond à la 1re modèle de liste hiérarchique dans la boîte de dialogue Puces et numérotation de Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
