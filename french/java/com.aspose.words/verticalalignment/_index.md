---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'alignement vertical d'un cadre de texte de forme flottante ou d'un tableau flottant en Java."
type: docs
weight: 713
url: /fr/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Spécifie l'alignement vertical d'une forme flottante, d'un cadre de texte ou d'un tableau flottant.

 **Examples:** 

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
| [BOTTOM](#BOTTOM) | Spécifie que l'objet doit être placé au bas de la base d'alignement vertical. |
| [CENTER](#CENTER) | Spécifie que l'objet doit être centré par rapport à la base d'alignement vertical. |
| [DEFAULT](#DEFAULT) | Identique à [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | Non documenté. |
| [INSIDE](#INSIDE) | Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal. |
| [NONE](#NONE) | L'objet est positionné explicitement, généralement en utilisant sa propriété **Top**. |
| [OUTSIDE](#OUTSIDE) | Spécifie que l'objet doit être à l'extérieur de la base d'alignement vertical. |
| [TOP](#TOP) | Spécifie que l'objet doit être en haut de la base d'alignement vertical. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Spécifie que l'objet doit être placé au bas de la base d'alignement vertical.

### CENTER {#CENTER}
```
public static int CENTER
```


Spécifie que l'objet doit être centré par rapport à la base d'alignement vertical.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Identique à [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


Non documenté. Il semble s'agir d'une valeur possible pour les paragraphes et tableaux flottants.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal.

### NONE {#NONE}
```
public static int NONE
```


L'objet est positionné explicitement, généralement en utilisant sa propriété **Top**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Spécifie que l'objet doit être à l'extérieur de la base d'alignement vertical.

### TOP {#TOP}
```
public static int TOP
```


Spécifie que l'objet doit être en haut de la base d'alignement vertical.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int verticalAlignment) {#toString-int}
```
public static String toString(int verticalAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
