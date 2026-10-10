---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words para Java"
description: "Permite especificar cómo se debe renderizar el texto dentro de un documento al guardarlo en formato SVG en Java."
type: docs
weight: 650
url: /es/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Permite especificar cómo debe renderizarse el texto dentro de un documento al guardarlo en formato SVG.

 **Examples:** 

Muestra cómo imitar las propiedades de las imágenes al convertir un documento .docx a .svg.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | El texto se renderiza usando curvas. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | Se utilizan fuentes SVG para renderizar el texto. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Se utilizan las fuentes instaladas en la máquina de destino para renderizar el texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


El texto se renderiza usando curvas. Nota, la selección de texto no funcionará si usa esta opción.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


Se utilizan fuentes SVG para renderizar el texto. Nota, no todos los navegadores admiten fuentes SVG.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Se utilizan las fuentes instaladas en la máquina de destino para renderizar el texto. Nota, si algunas de las fuentes usadas en el documento no están disponibles en la máquina de destino, el documento puede verse diferente.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
