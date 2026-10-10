---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words Java için"
description: "Java'da belge yükleme veya kaydetme sırasında uyarı üreten modülü belirtir."
type: docs
weight: 719
url: /tr/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Belge yükleme veya kaydetme sırasında bir uyarı üreten modülü belirtir.

 **Examples:** 

Uyarı kaynağıyla nasıl çalışılacağını gösterir.

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

Yazı tipi ikamesi hakkında ek bilgi nasıl alınacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CHM](#CHM) | CHM dosyalarını okuyan modül. |
| [DOC](#DOC) | İkili DOC dosyalarını okuyan/yazdıran modül. |
| [DOCLING](#DOCLING) | Docling JSON dosyalarını yazan modül. |
| [DOCX](#DOCX) | DOCX dosyalarını okuyan/yazan modül. |
| [DRAWING_ML](#DRAWING-ML) | DrawingML şekillerini işleyen modül. |
| [EPUB](#EPUB) | EPUB dosyalarını okuyan/yazan modül. |
| [FONT](#FONT) | Yazı tipi dosyalarını okuyan modül. |
| [HTML](#HTML) | HTML/MHTML dosyalarını okuyan/yazan modül. |
| [IMAGE](#IMAGE) | Görüntüleri işleyen modül. |
| [LAYOUT](#LAYOUT) | Belge düzenini oluşturan modül. |
| [MARKDOWN](#MARKDOWN) | Markdown dosyalarını okuyan/yazan modül. |
| [MATH_ML](#MATH-ML) | W3C MathML dosyalarını okuyan modül. |
| [METAFILE](#METAFILE) | Metadosyaları işleyen modül. |
| [NRX](#NRX) | DOCX/WML okuma/yazma modülleri arasında paylaşılan ortak modüller. |
| [ODT](#ODT) | ODT dosyalarını okuyan/yazan modül. |
| [OFFICE_MATH](#OFFICE-MATH) | OfficeMath'ı işleyen modül. |
| [PDF](#PDF) | PDF'yi renderlayan modül. |
| [RTF](#RTF) | RTF dosyalarını okuyan/yazan modül. |
| [SHAPES](#SHAPES) | Sıradan şekilleri renderlayan modül. |
| [SVG](#SVG) | SVG dosyalarını okuyan modül. |
| [SVM](#SVM) | Svm dosyalarını okuyan modül. |
| [TEXT](#TEXT) | Düz metin dosyalarını okuyan/yazan modül. |
| [UNKNOWN](#UNKNOWN) | Uyarı kaynağı belirtilmemiş. |
| [VALIDATOR](#VALIDATOR) | Model tutarlılığını ve geçerliliğini doğrulayan modül. |
| [WORD_ML](#WORD-ML) | WML dosyalarını okuyan/yazan modül. |
| [XAML](#XAML) | Xaml dosyalarını okuyan/yazan modül. |
| [XLSX](#XLSX) | XLSX dosyalarını yazan modül. |
| [XML](#XML) | XML dosyalarını okuyan modül. |
| [XPS](#XPS) | XPS oluşturan modül. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


CHM dosyalarını okuyan modül.

### DOC {#DOC}
```
public static int DOC
```


İkili DOC dosyalarını okuyan/yazdıran modül.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Docling JSON dosyalarını yazan modül.

### DOCX {#DOCX}
```
public static int DOCX
```


DOCX dosyalarını okuyan/yazan modül.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


DrawingML şekillerini işleyen modül.

### EPUB {#EPUB}
```
public static int EPUB
```


EPUB dosyalarını okuyan/yazan modül.

### FONT {#FONT}
```
public static int FONT
```


Yazı tipi dosyalarını okuyan modül.

### HTML {#HTML}
```
public static int HTML
```


HTML/MHTML dosyalarını okuyan/yazan modül.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Görüntüleri işleyen modül.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Belge düzenini oluşturan modül.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Markdown dosyalarını okuyan/yazan modül.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


W3C MathML dosyalarını okuyan modül.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Metadosyaları işleyen modül.

### NRX {#NRX}
```
public static int NRX
```


DOCX/WML okuma/yazma modülleri arasında paylaşılan ortak modüller.

### ODT {#ODT}
```
public static int ODT
```


ODT dosyalarını okuyan/yazan modül.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


OfficeMath'ı işleyen modül.

### PDF {#PDF}
```
public static int PDF
```


PDF'yi renderlayan modül.

### RTF {#RTF}
```
public static int RTF
```


RTF dosyalarını okuyan/yazan modül.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Sıradan şekilleri renderlayan modül.

### SVG {#SVG}
```
public static int SVG
```


SVG dosyalarını okuyan modül.

### SVM {#SVM}
```
public static int SVM
```


Svm dosyalarını okuyan modül.

### TEXT {#TEXT}
```
public static int TEXT
```


Düz metin dosyalarını okuyan/yazan modül.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Uyarı kaynağı belirtilmemiş.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Model tutarlılığını ve geçerliliğini doğrulayan modül.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


WML dosyalarını okuyan/yazan modül.

### XAML {#XAML}
```
public static int XAML
```


Xaml dosyalarını okuyan/yazan modül.

### XLSX {#XLSX}
```
public static int XLSX
```


XLSX dosyalarını yazan modül.

### XML {#XML}
```
public static int XML
```


XML dosyalarını okuyan modül.

### XPS {#XPS}
```
public static int XPS
```


XPS oluşturan modül.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
