---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words per Java"
description: "Specifica a cosa è relativo la posizione orizzontale di una forma o di un riquadro di testo in Java."
type: docs
weight: 561
url: /it/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Specifica a cosa è relativa la posizione orizzontale di una forma o di un riquadro di testo.

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
| [CHARACTER](#CHARACTER) | L'oggetto è posizionato rispetto al lato sinistro del paragrafo. |
| [COLUMN](#COLUMN) | L'oggetto è posizionato rispetto al lato sinistro della colonna. |
| [DEFAULT](#DEFAULT) | Il valore predefinito è [COLUMN](../../com.aspose.words/relativehorizontalposition/#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Specifica che il posizionamento orizzontale deve essere relativo al margine interno della pagina corrente (il margine sinistro nelle pagine dispari, quello destro nelle pagine pari). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Specifica che il posizionamento orizzontale deve essere relativo al margine sinistro della pagina. |
| [MARGIN](#MARGIN) | Specifica che il posizionamento orizzontale deve essere relativo ai margini della pagina. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Specifica che il posizionamento orizzontale deve essere relativo al margine esterno della pagina corrente (il margine destro nelle pagine dispari, quello sinistro nelle pagine pari). |
| [PAGE](#PAGE) | L'oggetto è posizionato rispetto al bordo sinistro della pagina. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Specifica che il posizionamento orizzontale deve essere relativo al margine destro della pagina. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


L'oggetto è posizionato rispetto al lato sinistro del paragrafo.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


L'oggetto è posizionato rispetto al lato sinistro della colonna.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il valore predefinito è [COLUMN](../../com.aspose.words/relativehorizontalposition/#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Specifica che il posizionamento orizzontale deve essere relativo al margine interno della pagina corrente (il margine sinistro nelle pagine dispari, quello destro nelle pagine pari).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Specifica che il posizionamento orizzontale deve essere relativo al margine sinistro della pagina.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifica che il posizionamento orizzontale deve essere relativo ai margini della pagina.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Specifica che il posizionamento orizzontale deve essere relativo al margine esterno della pagina corrente (il margine destro nelle pagine dispari, quello sinistro nelle pagine pari).

### PAGE {#PAGE}
```
public static int PAGE
```


L'oggetto è posizionato rispetto al bordo sinistro della pagina.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Specifica che il posizionamento orizzontale deve essere relativo al margine destro della pagina.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
