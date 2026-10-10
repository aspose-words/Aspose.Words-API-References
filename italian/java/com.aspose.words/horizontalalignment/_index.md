---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento orizzontale di un frame di testo di forma fluttuante o di una tabella fluttuante in Java."
type: docs
weight: 374
url: /it/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Specifica l'allineamento orizzontale di una forma fluttuante, di un riquadro di testo o di una tabella fluttuante.

 **Examples:** 

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
| [CENTER](#CENTER) | Specifica che l'oggetto deve essere centrato rispetto alla base di allineamento orizzontale. |
| [DEFAULT](#DEFAULT) | Uguale a [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Specifica che l'oggetto deve trovarsi all'interno della base di allineamento orizzontale. |
| [LEFT](#LEFT) | Specifica che l'oggetto deve essere allineato a sinistra alla base di allineamento orizzontale. |
| [NONE](#NONE) | L'oggetto è posizionato esplicitamente, di solito usando la sua proprietà **Left**. |
| [OUTSIDE](#OUTSIDE) | Specifica che l'oggetto deve essere al di fuori della base di allineamento orizzontale. |
| [RIGHT](#RIGHT) | Specifica che l'oggetto deve essere allineato a destra alla base di allineamento orizzontale. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Specifica che l'oggetto deve essere centrato rispetto alla base di allineamento orizzontale.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Uguale a [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Specifica che l'oggetto deve trovarsi all'interno della base di allineamento orizzontale.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifica che l'oggetto deve essere allineato a sinistra alla base di allineamento orizzontale.

### NONE {#NONE}
```
public static int NONE
```


L'oggetto è posizionato esplicitamente, di solito usando la sua proprietà **Left**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Specifica che l'oggetto deve essere al di fuori della base di allineamento orizzontale.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifica che l'oggetto deve essere allineato a destra alla base di allineamento orizzontale.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
