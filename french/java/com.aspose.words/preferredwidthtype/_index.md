---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'unité de mesure de la largeur préférée d'un tableau ou d'une cellule en Java."
type: docs
weight: 551
url: /fr/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Spécifie l'unité de mesure de la largeur préférée d'un tableau ou d'une cellule.

 **Examples:** 

Montre comment vérifier le type et la valeur de la largeur préférée d’une cellule de tableau.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | La largeur préférée n’est pas spécifiée. |
| [PERCENT](#PERCENT) | Mesurez la largeur actuelle de l’élément en utilisant un pourcentage spécifié. |
| [POINTS](#POINTS) | Mesurez la largeur actuelle de l’élément en utilisant un nombre de points spécifié (1/72 pouce). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


La largeur préférée n’est pas spécifiée. La largeur réelle du tableau ou de la cellule est soit spécifiée à l’aide de la largeur explicite, soit déterminée automatiquement par l’algorithme de mise en page du tableau lors de l’affichage du tableau, selon le paramètre d’ajustement automatique du tableau.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Mesurez la largeur actuelle de l’élément en utilisant un pourcentage spécifié.

### POINTS {#POINTS}
```
public static int POINTS
```


Mesurez la largeur actuelle de l’élément en utilisant un nombre de points spécifié (1/72 pouce).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
