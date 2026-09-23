---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le texte s’enroule autour d’une forme ou d’une image en Java."
type: docs
weight: 737
url: /fr/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Spécifie comment le texte s'enroule autour d'une forme ou d'une image.

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
| [INLINE](#INLINE) | La forme reste sur le même calque que le texte et est traitée comme un caractère. |
| [NONE](#NONE) | Pas d’enroulement du texte autour de la forme. |
| [SQUARE](#SQUARE) | Enroule le texte autour de tous les côtés de la boîte englobante carrée de la forme. |
| [THROUGH](#THROUGH) | Identique à Serré, mais enroule à l’intérieur des parties ouvertes de la forme. |
| [TIGHT](#TIGHT) | Enroule étroitement autour des bords de la forme, au lieu d’enrouler autour de la boîte englobante. |
| [TOP_BOTTOM](#TOP-BOTTOM) | Le texte s’arrête en haut de la forme et reprend sur la ligne située sous la forme. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


La forme reste sur le même calque que le texte et est traitée comme un caractère.

### NONE {#NONE}
```
public static int NONE
```


Pas d’enroulement du texte autour de la forme. La forme est placée derrière ou devant le texte.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Enroule le texte autour de tous les côtés de la boîte englobante carrée de la forme.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Identique à Serré, mais enroule à l’intérieur des parties ouvertes de la forme.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Enroule étroitement autour des bords de la forme, au lieu d’enrouler autour de la boîte englobante.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


Le texte s’arrête en haut de la forme et reprend sur la ligne située sous la forme.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapType) {#toString-int}
```
public static String toString(int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
