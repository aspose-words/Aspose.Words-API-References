---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words per Java"
description: "Definisce un layout per il rendering di più pagine in un unico output in Java."
type: docs
weight: 472
url: /it/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Definisce un layout per il rendering di più pagine in un'unica uscita.

 **Remarks:** 

Utilizza uno dei metodi statici di fabbrica per creare una configurazione di layout.

 **Examples:** 

Mostra come salvare il documento in un'immagine JPG con le impostazioni di layout multi-pagina.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBackColor()](#getBackColor) | Restituisce il colore di sfondo dell'output. |
| [getBorderColor()](#getBorderColor) | Restituisce il colore del bordo delle pagine. |
| [getBorderWidth()](#getBorderWidth) | Restituisce la larghezza del bordo delle pagine. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Crea un layout in cui le pagine sono renderizzate da sinistra a destra, dall'alto verso il basso, in una griglia con il numero specificato di colonne. |
| [horizontal(float horizontalGap)](#horizontal-float) | Crea un layout in cui tutte le pagine specificate sono renderizzate orizzontalmente affiancate, da sinistra a destra, in un unico output. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Imposta il colore di sfondo dell'output. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Imposta il colore del bordo delle pagine. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Imposta la larghezza del bordo delle pagine. |
| [singlePage()](#singlePage) | Crea un layout che renderizza solo la prima delle pagine specificate. |
| [tiffFrames()](#tiffFrames) | Crea un layout in cui ogni pagina è renderizzata come un fotogramma separato in un'immagine TIFF multi-fotogramma. |
| [vertical(float verticalGap)](#vertical-float) | Crea un layout in cui tutte le pagine specificate sono renderizzate verticalmente una sotto l'altra in un unico output. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Restituisce il colore di sfondo dell'output. Il valore predefinito è java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - Il colore di sfondo dell'output.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Restituisce il colore del bordo delle pagine. Il valore predefinito è java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - Il colore del bordo delle pagine.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Ottiene la larghezza del bordo della pagina. Il valore predefinito è 0.

**Returns:**
float - La larghezza del bordo della pagina.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Crea un layout in cui le pagine sono renderizzate da sinistra a destra, dall'alto verso il basso, in una griglia con il numero specificato di colonne.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| colonne | int | Il numero di colonne nel layout. Deve essere maggiore di zero. |
| gapOrizzontale | float | Lo spazio orizzontale tra le colonne in punti. |
| gapVerticale | float | Lo spazio verticale tra le righe in punti. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Crea un layout in cui tutte le pagine specificate sono renderizzate orizzontalmente affiancate, da sinistra a destra, in un unico output.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gapOrizzontale | float | Lo spazio orizzontale tra le pagine in punti. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Imposta il colore di sfondo dell'output. Il valore predefinito è java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Il colore di sfondo dell'output. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Imposta il colore del bordo della pagina. Il valore predefinito è java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Il colore del bordo della pagina. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Imposta la larghezza del bordo della pagina. Il valore predefinito è 0.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | float | La larghezza del bordo della pagina. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Crea un layout che renderizza solo la prima delle pagine specificate.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Crea un layout in cui ogni pagina viene renderizzata come un frame separato in un'immagine TIFF a più frame. Applicabile solo ai formati immagine TIFF.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Crea un layout in cui tutte le pagine specificate sono renderizzate verticalmente una sotto l'altra in un unico output.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gapVerticale | float | Lo spazio verticale tra le pagine in punti. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
