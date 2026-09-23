---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words pour Java"
description: "Spécifie à quoi la position verticale d'une forme ou d'un cadre de texte est relative en Java."
type: docs
weight: 563
url: /fr/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Spécifie par rapport à quoi la position verticale d'une forme ou d'un cadre de texte est relative.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Spécifie que le positionnement vertical doit être relatif à la marge inférieure de la page actuelle. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Spécifie que le positionnement vertical doit être relatif à la marge intérieure de la page actuelle. |
| [LINE](#LINE) | Non documenté. |
| [MARGIN](#MARGIN) | Spécifie que le positionnement vertical doit être relatif aux marges de la page. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Spécifie que le positionnement vertical doit être relatif à la marge extérieure de la page actuelle. |
| [PAGE](#PAGE) | L'objet est positionné par rapport au bord supérieur de la page. |
| [PARAGRAPH](#PARAGRAPH) | L'objet est positionné par rapport au haut du paragraphe qui contient l'ancre. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | La valeur par défaut est [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | La valeur par défaut est [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Spécifie que le positionnement vertical doit être relatif à la marge supérieure de la page actuelle. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Spécifie que le positionnement vertical doit être relatif à la marge inférieure de la page actuelle.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Spécifie que le positionnement vertical doit être relatif à la marge intérieure de la page actuelle.

### LINE {#LINE}
```
public static int LINE
```


Non documenté.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Spécifie que le positionnement vertical doit être relatif aux marges de la page.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Spécifie que le positionnement vertical doit être relatif à la marge extérieure de la page actuelle.

### PAGE {#PAGE}
```
public static int PAGE
```


L'objet est positionné par rapport au bord supérieur de la page.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


L'objet est positionné par rapport au haut du paragraphe qui contient l'ancre.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


La valeur par défaut est [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


La valeur par défaut est [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Spécifie que le positionnement vertical doit être relatif à la marge supérieure de la page actuelle.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
