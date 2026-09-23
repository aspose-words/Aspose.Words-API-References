---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words für Java"
description: "Gibt das Modul an, das während des Ladens oder Speicherns eines Dokuments in Java eine Warnung erzeugt."
type: docs
weight: 719
url: /de/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Gibt das Modul an, das während des Ladens oder Speicherns eines Dokuments eine Warnung erzeugt.

 **Examples:** 

Zeigt, wie mit der Warnungsquelle gearbeitet wird.

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

Zeigt, wie zusätzliche Informationen zur Schriftartsubstitution abgerufen werden können.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CHM](#CHM) | Modul, das CHM‑Dateien liest. |
| [DOC](#DOC) | Modul, das binäre DOC‑Dateien liest/schreibt. |
| [DOCLING](#DOCLING) | Modul, das Docling‑JSON‑Dateien schreibt. |
| [DOCX](#DOCX) | Modul, das DOCX‑Dateien liest/schreibt. |
| [DRAWING_ML](#DRAWING-ML) | Modul, das DrawingML‑Formen rendert. |
| [EPUB](#EPUB) | Modul, das EPUB‑Dateien liest/schreibt. |
| [FONT](#FONT) | Modul, das Schriftartdateien liest. |
| [HTML](#HTML) | Modul, das HTML/MHTML‑Dateien liest/schreibt. |
| [IMAGE](#IMAGE) | Modul, das Bilder rendert. |
| [LAYOUT](#LAYOUT) | Modul, das ein Dokumentlayout erstellt. |
| [MARKDOWN](#MARKDOWN) | Modul, das Markdown-Dateien liest/schreibt. |
| [MATH_ML](#MATH-ML) | Modul, das W3C MathML-Dateien liest. |
| [METAFILE](#METAFILE) | Modul, das Metadateien rendert. |
| [NRX](#NRX) | Gemeinsame Module, die zwischen DOCX/WML-Lese-/Schreibmodulen gemeinsam genutzt werden. |
| [ODT](#ODT) | Modul, das ODT-Dateien liest/schreibt. |
| [OFFICE_MATH](#OFFICE-MATH) | Modul, das OfficeMath rendert. |
| [PDF](#PDF) | Modul, das PDF rendert. |
| [RTF](#RTF) | Modul, das RTF-Dateien liest/schreibt. |
| [SHAPES](#SHAPES) | Modul, das gewöhnliche Formen rendert. |
| [SVG](#SVG) | Modul, das SVG-Dateien liest. |
| [SVM](#SVM) | Modul, das Svm-Dateien liest. |
| [TEXT](#TEXT) | Modul, das Klartextdateien liest/schreibt. |
| [UNKNOWN](#UNKNOWN) | Die Warnungsquelle ist nicht angegeben. |
| [VALIDATOR](#VALIDATOR) | Modul, das Modellkonsistenz und Gültigkeit überprüft. |
| [WORD_ML](#WORD-ML) | Modul, das WML-Dateien liest/schreibt. |
| [XAML](#XAML) | Modul, das Xaml-Dateien liest/schreibt. |
| [XLSX](#XLSX) | Modul, das XLSX-Dateien schreibt. |
| [XML](#XML) | Modul, das XML-Dateien liest. |
| [XPS](#XPS) | Modul, das XPS rendert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


Modul, das CHM‑Dateien liest.

### DOC {#DOC}
```
public static int DOC
```


Modul, das binäre DOC‑Dateien liest/schreibt.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Modul, das Docling‑JSON‑Dateien schreibt.

### DOCX {#DOCX}
```
public static int DOCX
```


Modul, das DOCX‑Dateien liest/schreibt.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Modul, das DrawingML‑Formen rendert.

### EPUB {#EPUB}
```
public static int EPUB
```


Modul, das EPUB‑Dateien liest/schreibt.

### FONT {#FONT}
```
public static int FONT
```


Modul, das Schriftartdateien liest.

### HTML {#HTML}
```
public static int HTML
```


Modul, das HTML/MHTML‑Dateien liest/schreibt.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Modul, das Bilder rendert.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Modul, das ein Dokumentlayout erstellt.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Modul, das Markdown-Dateien liest/schreibt.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Modul, das W3C MathML-Dateien liest.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Modul, das Metadateien rendert.

### NRX {#NRX}
```
public static int NRX
```


Gemeinsame Module, die zwischen DOCX/WML-Lese-/Schreibmodulen gemeinsam genutzt werden.

### ODT {#ODT}
```
public static int ODT
```


Modul, das ODT-Dateien liest/schreibt.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Modul, das OfficeMath rendert.

### PDF {#PDF}
```
public static int PDF
```


Modul, das PDF rendert.

### RTF {#RTF}
```
public static int RTF
```


Modul, das RTF-Dateien liest/schreibt.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Modul, das gewöhnliche Formen rendert.

### SVG {#SVG}
```
public static int SVG
```


Modul, das SVG-Dateien liest.

### SVM {#SVM}
```
public static int SVM
```


Modul, das Svm-Dateien liest.

### TEXT {#TEXT}
```
public static int TEXT
```


Modul, das Klartextdateien liest/schreibt.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Die Warnungsquelle ist nicht angegeben.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Modul, das Modellkonsistenz und Gültigkeit überprüft.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Modul, das WML-Dateien liest/schreibt.

### XAML {#XAML}
```
public static int XAML
```


Modul, das Xaml-Dateien liest/schreibt.

### XLSX {#XLSX}
```
public static int XLSX
```


Modul, das XLSX-Dateien schreibt.

### XML {#XML}
```
public static int XML
```


Modul, das XML-Dateien liest.

### XPS {#XPS}
```
public static int XPS
```


Modul, das XPS rendert.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
