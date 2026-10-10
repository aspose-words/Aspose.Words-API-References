---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words per Java"
description: "Specifica come il testo viene avvolto attorno a una forma o immagine in Java."
type: docs
weight: 737
url: /it/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Specifica come il testo si avvolge intorno a una forma o a un'immagine.

 **Examples:** 

Mostra come inserire un'immagine e usarla come filigrana.

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

Mostra come inserire un'immagine flottante al centro di una pagina.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [INLINE](#INLINE) | La forma rimane nello stesso livello del testo e viene trattata come un carattere. |
| [NONE](#NONE) | Nessun avvolgimento del testo attorno alla forma. |
| [SQUARE](#SQUARE) | Avvolge il testo attorno a tutti i lati del riquadro quadrato della forma. |
| [THROUGH](#THROUGH) | Come Tight, ma avvolge all'interno di tutte le parti della forma che sono aperte. |
| [TIGHT](#TIGHT) | Avvolge strettamente i bordi della forma, invece di avvolgere il riquadro. |
| [TOP_BOTTOM](#TOP-BOTTOM) | Il testo si ferma in cima alla forma e riprende sulla riga sotto la forma. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


La forma rimane nello stesso livello del testo e viene trattata come un carattere.

### NONE {#NONE}
```
public static int NONE
```


Nessun avvolgimento del testo attorno alla forma. La forma è posizionata dietro o davanti al testo.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Avvolge il testo attorno a tutti i lati del riquadro quadrato della forma.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Come Tight, ma avvolge all'interno di tutte le parti della forma che sono aperte.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Avvolge strettamente i bordi della forma, invece di avvolgere il riquadro.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


Il testo si ferma in cima alla forma e riprende sulla riga sotto la forma.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
