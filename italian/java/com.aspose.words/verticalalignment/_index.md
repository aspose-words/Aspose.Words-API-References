---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento verticale di un frame di testo di forma fluttuante o di una tabella fluttuante in Java."
type: docs
weight: 713
url: /it/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Specifica l'allineamento verticale di una forma flottante, di un riquadro di testo o di una tabella flottante.

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
| [BOTTOM](#BOTTOM) | Specifica che l'oggetto deve trovarsi nella parte inferiore della base di allineamento verticale. |
| [CENTER](#CENTER) | Specifica che l'oggetto deve essere centrato rispetto alla base di allineamento verticale. |
| [DEFAULT](#DEFAULT) | Stesso di [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | Non documentato. |
| [INSIDE](#INSIDE) | Specifica che l'oggetto deve trovarsi all'interno della base di allineamento orizzontale. |
| [NONE](#NONE) | L'oggetto è posizionato esplicitamente, di solito usando la sua proprietà **Top**. |
| [OUTSIDE](#OUTSIDE) | Specifica che l'oggetto deve trovarsi al di fuori della base di allineamento verticale. |
| [TOP](#TOP) | Specifica che l'oggetto deve trovarsi nella parte superiore della base di allineamento verticale. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Specifica che l'oggetto deve trovarsi nella parte inferiore della base di allineamento verticale.

### CENTER {#CENTER}
```
public static int CENTER
```


Specifica che l'oggetto deve essere centrato rispetto alla base di allineamento verticale.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Stesso di [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


Non documentato. Sembra essere un valore possibile per paragrafi e tabelle flottanti.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Specifica che l'oggetto deve trovarsi all'interno della base di allineamento orizzontale.

### NONE {#NONE}
```
public static int NONE
```


L'oggetto è posizionato esplicitamente, di solito usando la sua proprietà **Top**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Specifica che l'oggetto deve trovarsi al di fuori della base di allineamento verticale.

### TOP {#TOP}
```
public static int TOP
```


Specifica che l'oggetto deve trovarsi nella parte superiore della base di allineamento verticale.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
