---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words per Java"
description: "Specifica a cosa è relativa la posizione verticale di una forma o di un riquadro di testo in Java."
type: docs
weight: 563
url: /it/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Specifica a cosa è relativa la posizione verticale di una forma o di un riquadro di testo.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Specifica che il posizionamento verticale deve essere relativo al margine inferiore della pagina corrente. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Specifica che il posizionamento verticale deve essere relativo al margine interno della pagina corrente. |
| [LINE](#LINE) | Non documentato. |
| [MARGIN](#MARGIN) | Specifica che il posizionamento verticale deve essere relativo ai margini della pagina. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Specifica che il posizionamento verticale deve essere relativo al margine esterno della pagina corrente. |
| [PAGE](#PAGE) | L'oggetto è posizionato rispetto al bordo superiore della pagina. |
| [PARAGRAPH](#PARAGRAPH) | L'oggetto è posizionato rispetto alla parte superiore del paragrafo che contiene l'ancora. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | Il valore predefinito è [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | Il valore predefinito è [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Specifica che il posizionamento verticale deve essere relativo al margine superiore della pagina corrente. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Specifica che il posizionamento verticale deve essere relativo al margine inferiore della pagina corrente.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Specifica che il posizionamento verticale deve essere relativo al margine interno della pagina corrente.

### LINE {#LINE}
```
public static int LINE
```


Non documentato.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifica che il posizionamento verticale deve essere relativo ai margini della pagina.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Specifica che il posizionamento verticale deve essere relativo al margine esterno della pagina corrente.

### PAGE {#PAGE}
```
public static int PAGE
```


L'oggetto è posizionato rispetto al bordo superiore della pagina.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


L'oggetto è posizionato rispetto alla parte superiore del paragrafo che contiene l'ancora.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


Il valore predefinito è [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


Il valore predefinito è [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Specifica che il posizionamento verticale deve essere relativo al margine superiore della pagina corrente.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
