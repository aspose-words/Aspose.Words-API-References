---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words pour Java"
description: "Spécifie à quoi la position horizontale d’une forme ou d’un cadre de texte est relative en Java."
type: docs
weight: 561
url: /fr/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Spécifie par rapport à quoi la position horizontale d'une forme ou d'un cadre de texte est relative.

 **Examples:** 

Montre comment insérer une image et l’utiliser comme filigrane.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Montre comment insérer une image flottante au centre d’une page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CHARACTER](#CHARACTER) | L’objet est positionné par rapport au côté gauche du paragraphe. |
| [COLUMN](#COLUMN) | L’objet est positionné par rapport au côté gauche de la colonne. |
| [DEFAULT](#DEFAULT) | La valeur par défaut est [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Spécifie que le positionnement horizontal doit être relatif à la marge intérieure de la page courante (la marge gauche sur les pages impaires, droite sur les pages paires). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Spécifie que le positionnement horizontal doit être relatif à la marge gauche de la page. |
| [MARGIN](#MARGIN) | Spécifie que le positionnement horizontal doit être relatif aux marges de la page. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Spécifie que le positionnement horizontal doit être relatif à la marge extérieure de la page courante (la marge droite sur les pages impaires, gauche sur les pages paires). |
| [PAGE](#PAGE) | L’objet est positionné par rapport au bord gauche de la page. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Spécifie que le positionnement horizontal doit être relatif à la marge droite de la page. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


L’objet est positionné par rapport au côté gauche du paragraphe.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


L’objet est positionné par rapport au côté gauche de la colonne.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


La valeur par défaut est [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Spécifie que le positionnement horizontal doit être relatif à la marge intérieure de la page courante (la marge gauche sur les pages impaires, droite sur les pages paires).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Spécifie que le positionnement horizontal doit être relatif à la marge gauche de la page.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Spécifie que le positionnement horizontal doit être relatif aux marges de la page.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Spécifie que le positionnement horizontal doit être relatif à la marge extérieure de la page courante (la marge droite sur les pages impaires, gauche sur les pages paires).

### PAGE {#PAGE}
```
public static int PAGE
```


L’objet est positionné par rapport au bord gauche de la page.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Spécifie que le positionnement horizontal doit être relatif à la marge droite de la page.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
