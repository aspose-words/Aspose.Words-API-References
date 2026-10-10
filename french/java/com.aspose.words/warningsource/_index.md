---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words pour Java"
description: "Spécifie le module qui génère un avertissement lors du chargement ou de l'enregistrement d'un document en Java."
type: docs
weight: 719
url: /fr/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Spécifie le module qui génère un avertissement lors du chargement ou de l'enregistrement du document.

 **Examples:** 

Montre comment travailler avec la source de l'avertissement.

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

Montre comment obtenir des informations supplémentaires sur la substitution de police.

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
## Champs

| Champ | Description |
| --- | --- |
| [CHM](#CHM) | Module qui lit les fichiers CHM. |
| [DOC](#DOC) | Module qui lit/écrit les fichiers DOC binaires. |
| [DOCLING](#DOCLING) | Module qui écrit des fichiers JSON Docling. |
| [DOCX](#DOCX) | Module qui lit/écrit des fichiers DOCX. |
| [DRAWING_ML](#DRAWING-ML) | Module qui rend les formes DrawingML. |
| [EPUB](#EPUB) | Module qui lit/écrit des fichiers EPUB. |
| [FONT](#FONT) | Module qui lit les fichiers de polices. |
| [HTML](#HTML) | Module qui lit/écrit des fichiers HTML/MHTML. |
| [IMAGE](#IMAGE) | Module qui rend les images. |
| [LAYOUT](#LAYOUT) | Module qui construit une mise en page de document. |
| [MARKDOWN](#MARKDOWN) | Module qui lit/écrit des fichiers Markdown. |
| [MATH_ML](#MATH-ML) | Module qui lit les fichiers W3C MathML. |
| [METAFILE](#METAFILE) | Module qui rend les métafichiers. |
| [NRX](#NRX) | Modules communs qui sont partagés entre les modules de lecture/écriture DOCX/WML. |
| [ODT](#ODT) | Module qui lit/écrit des fichiers ODT. |
| [OFFICE_MATH](#OFFICE-MATH) | Module qui rend OfficeMath. |
| [PDF](#PDF) | Module qui rend le PDF. |
| [RTF](#RTF) | Module qui lit/écrit des fichiers RTF. |
| [SHAPES](#SHAPES) | Module qui rend les formes ordinaires. |
| [SVG](#SVG) | Module qui lit les fichiers SVG. |
| [SVM](#SVM) | Module qui lit les fichiers Svm. |
| [TEXT](#TEXT) | Module qui lit/écrit des fichiers texte brut. |
| [UNKNOWN](#UNKNOWN) | La source de l'avertissement n'est pas spécifiée. |
| [VALIDATOR](#VALIDATOR) | Module qui vérifie la cohérence et la validité du modèle. |
| [WORD_ML](#WORD-ML) | Module qui lit/écrit des fichiers WML. |
| [XAML](#XAML) | Module qui lit/écrit des fichiers Xaml. |
| [XLSX](#XLSX) | Module qui écrit des fichiers XLSX. |
| [XML](#XML) | Module qui lit les fichiers XML. |
| [XPS](#XPS) | Module qui rend les fichiers XPS. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


Module qui lit les fichiers CHM.

### DOC {#DOC}
```
public static int DOC
```


Module qui lit/écrit les fichiers DOC binaires.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Module qui écrit des fichiers JSON Docling.

### DOCX {#DOCX}
```
public static int DOCX
```


Module qui lit/écrit des fichiers DOCX.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Module qui rend les formes DrawingML.

### EPUB {#EPUB}
```
public static int EPUB
```


Module qui lit/écrit des fichiers EPUB.

### FONT {#FONT}
```
public static int FONT
```


Module qui lit les fichiers de polices.

### HTML {#HTML}
```
public static int HTML
```


Module qui lit/écrit des fichiers HTML/MHTML.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Module qui rend les images.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Module qui construit une mise en page de document.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Module qui lit/écrit des fichiers Markdown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Module qui lit les fichiers W3C MathML.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Module qui rend les métafichiers.

### NRX {#NRX}
```
public static int NRX
```


Modules communs qui sont partagés entre les modules de lecture/écriture DOCX/WML.

### ODT {#ODT}
```
public static int ODT
```


Module qui lit/écrit des fichiers ODT.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Module qui rend OfficeMath.

### PDF {#PDF}
```
public static int PDF
```


Module qui rend le PDF.

### RTF {#RTF}
```
public static int RTF
```


Module qui lit/écrit des fichiers RTF.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Module qui rend les formes ordinaires.

### SVG {#SVG}
```
public static int SVG
```


Module qui lit les fichiers SVG.

### SVM {#SVM}
```
public static int SVM
```


Module qui lit les fichiers Svm.

### TEXT {#TEXT}
```
public static int TEXT
```


Module qui lit/écrit des fichiers texte brut.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


La source de l'avertissement n'est pas spécifiée.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Module qui vérifie la cohérence et la validité du modèle.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Module qui lit/écrit des fichiers WML.

### XAML {#XAML}
```
public static int XAML
```


Module qui lit/écrit des fichiers Xaml.

### XLSX {#XLSX}
```
public static int XLSX
```


Module qui écrit des fichiers XLSX.

### XML {#XML}
```
public static int XML
```


Module qui lit les fichiers XML.

### XPS {#XPS}
```
public static int XPS
```


Module qui rend les fichiers XPS.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
