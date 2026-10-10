---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie le mode de mise en page d'une section permettant de définir le comportement de la grille du document en Java."
type: docs
weight: 607
url: /fr/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Spécifie le mode de mise en page d'une section permettant de définir le comportement de la grille du document.

 **Examples:** 

Montre comment spécifier une valeur pour le nombre de caractères que chaque ligne peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Montre comment spécifier une limite du nombre de lignes que chaque page peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Spécifie qu'aucune grille de document ne doit être appliquée au contenu de la section correspondante dans le document. |
| [GRID](#GRID) | Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et caractère à l'intérieur afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. |
| [LINE_GRID](#LINE-GRID) | Spécifie que la section correspondante doit avoir un pas de ligne supplémentaire ajouté à chaque ligne afin de maintenir le nombre spécifié de lignes par page. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et caractère à l'intérieur afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Spécifie qu'aucune grille de document ne doit être appliquée au contenu de la section correspondante dans le document.

### GRID {#GRID}
```
public static int GRID
```


Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et caractère à l'intérieur afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. Les caractères ne seront pas automatiquement alignés avec les lignes de la grille lors de la saisie.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Spécifie que la section correspondante doit avoir un pas de ligne supplémentaire ajouté à chaque ligne afin de maintenir le nombre spécifié de lignes par page.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et caractère à l'intérieur afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. Les caractères seront automatiquement alignés avec les lignes de la grille lors de la saisie.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
