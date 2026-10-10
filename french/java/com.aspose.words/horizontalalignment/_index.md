---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'alignement horizontal d'un cadre de texte de forme flottante ou d'un tableau flottant en Java."
type: docs
weight: 374
url: /fr/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Spécifie l’alignement horizontal d’une forme flottante, d’un cadre de texte ou d’un tableau flottant.

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
| [CENTER](#CENTER) | Spécifie que l'objet doit être centré par rapport à la base d'alignement horizontal. |
| [DEFAULT](#DEFAULT) | Identique à [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal. |
| [LEFT](#LEFT) | Spécifie que l'objet doit être aligné à gauche par rapport à la base d'alignement horizontal. |
| [NONE](#NONE) | L'objet est positionné explicitement, généralement en utilisant sa propriété **Left**. |
| [OUTSIDE](#OUTSIDE) | Spécifie que l'objet doit être en dehors de la base d'alignement horizontal. |
| [RIGHT](#RIGHT) | Spécifie que l'objet doit être aligné à droite par rapport à la base d'alignement horizontal. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Spécifie que l'objet doit être centré par rapport à la base d'alignement horizontal.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Identique à [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal.

### LEFT {#LEFT}
```
public static int LEFT
```


Spécifie que l'objet doit être aligné à gauche par rapport à la base d'alignement horizontal.

### NONE {#NONE}
```
public static int NONE
```


L'objet est positionné explicitement, généralement en utilisant sa propriété **Left**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Spécifie que l'objet doit être en dehors de la base d'alignement horizontal.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Spécifie que l'objet doit être aligné à droite par rapport à la base d'alignement horizontal.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalAlignment) {#toString-int}
```
public static String toString(int horizontalAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
