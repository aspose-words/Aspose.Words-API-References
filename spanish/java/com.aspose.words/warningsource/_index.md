---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words para Java"
description: "Especifica el módulo que genera una advertencia durante la carga o guardado del documento en Java."
type: docs
weight: 719
url: /es/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Especifica el módulo que produce una advertencia durante la carga o guardado del documento.

 **Examples:** 

Muestra cómo trabajar con la fuente de la advertencia.

```

 Document doc = new Document(getMyDir() + "Emphases markdown warning.docx");

 WarningInfoCollection warnings = new WarningInfoCollection();
 doc.setWarningCallback(warnings);
 doc.save(getArtifactsDir() + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

 for (WarningInfo warningInfo : warnings) {
     if (warningInfo.getSource() == WarningSource.MARKDOWN)
         Assert.assertEquals("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.getDescription());
 }
 
```

Muestra cómo obtener información adicional sobre la sustitución de fuentes.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 WarningInfoCollection callback = new WarningInfoCollection();
 doc.setWarningCallback(callback);

 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Arial", "Arvo", "Slab");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarnings.pdf");

 FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback.get(0);
 Assert.assertEquals(WarningSource.LAYOUT, warningInfo.getSource());
 Assert.assertEquals(WarningType.FONT_SUBSTITUTION, warningInfo.getWarningType());
 Assert.assertEquals(FontSubstitutionReason.TABLE_SUBSTITUTION_RULE, warningInfo.getReason());
 Assert.assertEquals("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo.getDescription());
 Assert.assertTrue(warningInfo.getRequestedBold());
 Assert.assertFalse(warningInfo.getRequestedItalic());
 Assert.assertEquals("Arial", warningInfo.getRequestedFamilyName());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CHM](#CHM) | Módulo que lee archivos CHM. |
| [DOC](#DOC) | Módulo que lee/escribe archivos DOC binarios. |
| [DOCLING](#DOCLING) | Módulo que escribe archivos JSON de Docling. |
| [DOCX](#DOCX) | Módulo que lee/escribe archivos DOCX. |
| [DRAWING_ML](#DRAWING-ML) | Módulo que renderiza formas DrawingML. |
| [EPUB](#EPUB) | Módulo que lee/escribe archivos EPUB. |
| [FONT](#FONT) | Módulo que lee archivos de fuentes. |
| [HTML](#HTML) | Módulo que lee/escribe archivos HTML/MHTML. |
| [IMAGE](#IMAGE) | Módulo que renderiza imágenes. |
| [LAYOUT](#LAYOUT) | Módulo que construye un diseño de documento. |
| [MARKDOWN](#MARKDOWN) | Módulo que lee/escribe archivos Markdown. |
| [MATH_ML](#MATH-ML) | Módulo que lee archivos MathML de W3C. |
| [METAFILE](#METAFILE) | Módulo que renderiza metaficheros. |
| [NRX](#NRX) | Módulos comunes que se comparten entre los módulos lector/escritor DOCX/WML. |
| [ODT](#ODT) | Módulo que lee/escribe archivos ODT. |
| [OFFICE_MATH](#OFFICE-MATH) | Módulo que renderiza OfficeMath. |
| [PDF](#PDF) | Módulo que renderiza PDF. |
| [RTF](#RTF) | Módulo que lee/escribe archivos RTF. |
| [SHAPES](#SHAPES) | Módulo que renderiza formas ordinarias. |
| [SVG](#SVG) | Módulo que lee archivos SVG. |
| [SVM](#SVM) | Módulo que lee archivos Svm. |
| [TEXT](#TEXT) | Módulo que lee/escribe archivos de texto sin formato. |
| [UNKNOWN](#UNKNOWN) | No se ha especificado la fuente de la advertencia. |
| [VALIDATOR](#VALIDATOR) | Módulo que verifica la consistencia y validez del modelo. |
| [WORD_ML](#WORD-ML) | Módulo que lee/escribe archivos WML. |
| [XAML](#XAML) | Módulo que lee/escribe archivos Xaml. |
| [XLSX](#XLSX) | Módulo que escribe archivos XLSX. |
| [XML](#XML) | Módulo que lee archivos XML. |
| [XPS](#XPS) | Módulo que renderiza XPS. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


Módulo que lee archivos CHM.

### DOC {#DOC}
```
public static int DOC
```


Módulo que lee/escribe archivos DOC binarios.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Módulo que escribe archivos JSON de Docling.

### DOCX {#DOCX}
```
public static int DOCX
```


Módulo que lee/escribe archivos DOCX.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Módulo que renderiza formas DrawingML.

### EPUB {#EPUB}
```
public static int EPUB
```


Módulo que lee/escribe archivos EPUB.

### FONT {#FONT}
```
public static int FONT
```


Módulo que lee archivos de fuentes.

### HTML {#HTML}
```
public static int HTML
```


Módulo que lee/escribe archivos HTML/MHTML.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Módulo que renderiza imágenes.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Módulo que construye un diseño de documento.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Módulo que lee/escribe archivos Markdown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Módulo que lee archivos MathML de W3C.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Módulo que renderiza metaficheros.

### NRX {#NRX}
```
public static int NRX
```


Módulos comunes que se comparten entre los módulos lector/escritor DOCX/WML.

### ODT {#ODT}
```
public static int ODT
```


Módulo que lee/escribe archivos ODT.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Módulo que renderiza OfficeMath.

### PDF {#PDF}
```
public static int PDF
```


Módulo que renderiza PDF.

### RTF {#RTF}
```
public static int RTF
```


Módulo que lee/escribe archivos RTF.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Módulo que renderiza formas ordinarias.

### SVG {#SVG}
```
public static int SVG
```


Módulo que lee archivos SVG.

### SVM {#SVM}
```
public static int SVM
```


Módulo que lee archivos Svm.

### TEXT {#TEXT}
```
public static int TEXT
```


Módulo que lee/escribe archivos de texto sin formato.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


No se ha especificado la fuente de la advertencia.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Módulo que verifica la consistencia y validez del modelo.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Módulo que lee/escribe archivos WML.

### XAML {#XAML}
```
public static int XAML
```


Módulo que lee/escribe archivos Xaml.

### XLSX {#XLSX}
```
public static int XLSX
```


Módulo que escribe archivos XLSX.

### XML {#XML}
```
public static int XML
```


Módulo que lee archivos XML.

### XPS {#XPS}
```
public static int XPS
```


Módulo que renderiza XPS.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningSource) {#toString-int}
```
public static String toString(int warningSource)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
