---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words per Java"
description: "Consente di specificare come il testo all'interno di un documento deve essere renderizzato quando si salva in formato SVG in Java."
type: docs
weight: 650
url: /it/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Consente di specificare come il testo all'interno di un documento deve essere renderizzato quando si salva in formato SVG.

 **Examples:** 

Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Configure the SvgSaveOptions object to save with no page borders or selectable text.
 SvgSaveOptions options = new SvgSaveOptions();
 {
     options.setFitToViewPort(true);
     options.setShowPageBorder(false);
     options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);
 }

 doc.save(getArtifactsDir() + "SvgSaveOptions.SaveLikeImage.svg", options);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Il testo è renderizzato usando curve. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | I font SVG sono usati per renderizzare il testo. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | I font installati sulla macchina di destinazione sono usati per renderizzare il testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Il testo è renderizzato usando curve. Nota, la selezione del testo non funzionerà se utilizzi questa opzione.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


I font SVG sono usati per renderizzare il testo. Nota, non tutti i browser supportano i font SVG.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


I font installati sulla macchina di destinazione sono usati per renderizzare il testo. Nota, se alcuni dei font usati nel documento non sono disponibili sulla macchina di destinazione, il documento può apparire diverso.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int svgTextOutputMode) {#toString-int}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
