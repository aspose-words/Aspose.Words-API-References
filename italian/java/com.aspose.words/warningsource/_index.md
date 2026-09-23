---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words per Java"
description: "Specifica il modulo che genera un avviso durante il caricamento o il salvataggio del documento in Java."
type: docs
weight: 719
url: /it/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Specifica il modulo che genera un avviso durante il caricamento o il salvataggio del documento.

 **Examples:** 

Mostra come lavorare con la sorgente dell'avviso.

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

Mostra come ottenere informazioni aggiuntive sulla sostituzione dei caratteri.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CHM](#CHM) | Modulo che legge file CHM. |
| [DOC](#DOC) | Modulo che legge/scrive file DOC binari. |
| [DOCLING](#DOCLING) | Modulo che scrive file JSON Docling. |
| [DOCX](#DOCX) | Modulo che legge/scrive file DOCX. |
| [DRAWING_ML](#DRAWING-ML) | Modulo che rende forme DrawingML. |
| [EPUB](#EPUB) | Modulo che legge/scrive file EPUB. |
| [FONT](#FONT) | Modulo che legge file di font. |
| [HTML](#HTML) | Modulo che legge/scrive file HTML/MHTML. |
| [IMAGE](#IMAGE) | Modulo che rende immagini. |
| [LAYOUT](#LAYOUT) | Modulo che costruisce un layout di documento. |
| [MARKDOWN](#MARKDOWN) | Modulo che legge/scrive file Markdown. |
| [MATH_ML](#MATH-ML) | Modulo che legge file W3C MathML. |
| [METAFILE](#METAFILE) | Modulo che rende metafile. |
| [NRX](#NRX) | Moduli comuni condivisi tra i moduli lettori/scrittori DOCX/WML. |
| [ODT](#ODT) | Modulo che legge/scrive file ODT. |
| [OFFICE_MATH](#OFFICE-MATH) | Modulo che rende OfficeMath. |
| [PDF](#PDF) | Modulo che rende PDF. |
| [RTF](#RTF) | Modulo che legge/scrive file RTF. |
| [SHAPES](#SHAPES) | Modulo che rende forme ordinarie. |
| [SVG](#SVG) | Modulo che legge file SVG. |
| [SVM](#SVM) | Modulo che legge file Svm. |
| [TEXT](#TEXT) | Modulo che legge/scrive file di testo semplice. |
| [UNKNOWN](#UNKNOWN) | La fonte dell'avviso non è specificata. |
| [VALIDATOR](#VALIDATOR) | Modulo che verifica la coerenza e la validità del modello. |
| [WORD_ML](#WORD-ML) | Modulo che legge/scrive file WML. |
| [XAML](#XAML) | Modulo che legge/scrive file Xaml. |
| [XLSX](#XLSX) | Modulo che scrive file XLSX. |
| [XML](#XML) | Modulo che legge file XML. |
| [XPS](#XPS) | Modulo che rende XPS. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


Modulo che legge file CHM.

### DOC {#DOC}
```
public static int DOC
```


Modulo che legge/scrive file DOC binari.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Modulo che scrive file JSON Docling.

### DOCX {#DOCX}
```
public static int DOCX
```


Modulo che legge/scrive file DOCX.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Modulo che rende forme DrawingML.

### EPUB {#EPUB}
```
public static int EPUB
```


Modulo che legge/scrive file EPUB.

### FONT {#FONT}
```
public static int FONT
```


Modulo che legge file di font.

### HTML {#HTML}
```
public static int HTML
```


Modulo che legge/scrive file HTML/MHTML.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Modulo che rende immagini.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Modulo che costruisce un layout di documento.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Modulo che legge/scrive file Markdown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Modulo che legge file W3C MathML.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Modulo che rende metafile.

### NRX {#NRX}
```
public static int NRX
```


Moduli comuni condivisi tra i moduli lettori/scrittori DOCX/WML.

### ODT {#ODT}
```
public static int ODT
```


Modulo che legge/scrive file ODT.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Modulo che rende OfficeMath.

### PDF {#PDF}
```
public static int PDF
```


Modulo che rende PDF.

### RTF {#RTF}
```
public static int RTF
```


Modulo che legge/scrive file RTF.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Modulo che rende forme ordinarie.

### SVG {#SVG}
```
public static int SVG
```


Modulo che legge file SVG.

### SVM {#SVM}
```
public static int SVM
```


Modulo che legge file Svm.

### TEXT {#TEXT}
```
public static int TEXT
```


Modulo che legge/scrive file di testo semplice.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


La fonte dell'avviso non è specificata.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Modulo che verifica la coerenza e la validità del modello.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Modulo che legge/scrive file WML.

### XAML {#XAML}
```
public static int XAML
```


Modulo che legge/scrive file Xaml.

### XLSX {#XLSX}
```
public static int XLSX
```


Modulo che scrive file XLSX.

### XML {#XML}
```
public static int XML
```


Modulo che legge file XML.

### XPS {#XPS}
```
public static int XPS
```


Modulo che rende XPS.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
