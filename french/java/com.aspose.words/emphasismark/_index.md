---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words pour Java"
description: "Spécifie les types possibles de marques d'emphase en Java."
type: docs
weight: 187
url: /fr/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Spécifie les types possibles de marque d'emphase.

 **Examples:** 

Montre comment ajouter un caractère supplémentaire rendu au-dessus/au-dessous du glyphe.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [NONE](#NONE) | Aucune marque d'emphase. |
| [OVER_COMMA](#OVER-COMMA) | Le signe d'emphase est un caractère virgule affiché au-dessus du texte. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | Le signe d'emphase est un cercle noir plein affiché au-dessus du texte. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | Le signe d'emphase est un cercle blanc vide affiché au-dessus du texte. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | Le signe d'emphase est un cercle noir plein affiché en dessous du texte. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Aucune marque d'emphase.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


Le signe d'emphase est un caractère virgule affiché au-dessus du texte.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


Le signe d'emphase est un cercle noir plein affiché au-dessus du texte.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


Le signe d'emphase est un cercle blanc vide affiché au-dessus du texte.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


Le signe d'emphase est un cercle noir plein affiché en dessous du texte.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
