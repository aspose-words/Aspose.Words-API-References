---
title: "WarningSource"
linktitle: "WarningSource"
second_title: "Aspose.Words для Java"
description: "Указывает модуль, который генерирует предупреждение при загрузке или сохранении документа в Java."
type: docs
weight: 719
url: /ru/java/com.aspose.words/warningsource/
---

**Inheritance:**
java.lang.Object
```
public class WarningSource
```

Указывает модуль, который генерирует предупреждение при загрузке или сохранении документа.

 **Examples:** 

Показывает, как работать с источником предупреждения.

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

Показывает, как получить дополнительную информацию о замене шрифтов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CHM](#CHM) | Модуль, который читает файлы CHM. |
| [DOC](#DOC) | Модуль, который читает/записывает двоичные файлы DOC. |
| [DOCLING](#DOCLING) | Модуль, который записывает файлы Docling JSON. |
| [DOCX](#DOCX) | Модуль, который читает/записывает файлы DOCX. |
| [DRAWING_ML](#DRAWING-ML) | Модуль, который визуализирует фигуры DrawingML. |
| [EPUB](#EPUB) | Модуль, который читает/записывает файлы EPUB. |
| [FONT](#FONT) | Модуль, который читает файлы шрифтов. |
| [HTML](#HTML) | Модуль, который читает/записывает файлы HTML/MHTML. |
| [IMAGE](#IMAGE) | Модуль, который визуализирует изображения. |
| [LAYOUT](#LAYOUT) | Модуль, который создает макет документа. |
| [MARKDOWN](#MARKDOWN) | Модуль, который читает/записывает файлы Markdown. |
| [MATH_ML](#MATH-ML) | Модуль, который читает файлы W3C MathML. |
| [METAFILE](#METAFILE) | Модуль, который визуализирует метафайлы. |
| [NRX](#NRX) | Общие модули, которые используются совместно между модулями чтения/записи DOCX/WML. |
| [ODT](#ODT) | Модуль, который читает/записывает файлы ODT. |
| [OFFICE_MATH](#OFFICE-MATH) | Модуль, который визуализирует OfficeMath. |
| [PDF](#PDF) | Модуль, который визуализирует PDF. |
| [RTF](#RTF) | Модуль, который читает/записывает файлы RTF. |
| [SHAPES](#SHAPES) | Модуль, который визуализирует обычные фигуры. |
| [SVG](#SVG) | Модуль, который читает файлы SVG. |
| [SVM](#SVM) | Модуль, который читает файлы Svm. |
| [TEXT](#TEXT) | Модуль, который читает/записывает простые текстовые файлы. |
| [UNKNOWN](#UNKNOWN) | Источник предупреждения не указан. |
| [VALIDATOR](#VALIDATOR) | Модуль, который проверяет согласованность и корректность модели. |
| [WORD_ML](#WORD-ML) | Модуль, который читает/записывает файлы WML. |
| [XAML](#XAML) | Модуль, который читает/записывает файлы Xaml. |
| [XLSX](#XLSX) | Модуль, который записывает файлы XLSX. |
| [XML](#XML) | Модуль, который читает XML‑файлы. |
| [XPS](#XPS) | Модуль, который отображает XPS. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String warningSourceName)](#fromName-java.lang.String) |  |
| [getName(int warningSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningSource)](#toString-int) |  |
### CHM {#CHM}
```
public static int CHM
```


Модуль, который читает файлы CHM.

### DOC {#DOC}
```
public static int DOC
```


Модуль, который читает/записывает двоичные файлы DOC.

### DOCLING {#DOCLING}
```
public static int DOCLING
```


Модуль, который записывает файлы Docling JSON.

### DOCX {#DOCX}
```
public static int DOCX
```


Модуль, который читает/записывает файлы DOCX.

### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Модуль, который визуализирует фигуры DrawingML.

### EPUB {#EPUB}
```
public static int EPUB
```


Модуль, который читает/записывает файлы EPUB.

### FONT {#FONT}
```
public static int FONT
```


Модуль, который читает файлы шрифтов.

### HTML {#HTML}
```
public static int HTML
```


Модуль, который читает/записывает файлы HTML/MHTML.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Модуль, который визуализирует изображения.

### LAYOUT {#LAYOUT}
```
public static int LAYOUT
```


Модуль, который создает макет документа.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Модуль, который читает/записывает файлы Markdown.

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


Модуль, который читает файлы W3C MathML.

### METAFILE {#METAFILE}
```
public static int METAFILE
```


Модуль, который визуализирует метафайлы.

### NRX {#NRX}
```
public static int NRX
```


Общие модули, которые используются совместно между модулями чтения/записи DOCX/WML.

### ODT {#ODT}
```
public static int ODT
```


Модуль, который читает/записывает файлы ODT.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Модуль, который визуализирует OfficeMath.

### PDF {#PDF}
```
public static int PDF
```


Модуль, который визуализирует PDF.

### RTF {#RTF}
```
public static int RTF
```


Модуль, который читает/записывает файлы RTF.

### SHAPES {#SHAPES}
```
public static int SHAPES
```


Модуль, который визуализирует обычные фигуры.

### SVG {#SVG}
```
public static int SVG
```


Модуль, который читает файлы SVG.

### SVM {#SVM}
```
public static int SVM
```


Модуль, который читает файлы Svm.

### TEXT {#TEXT}
```
public static int TEXT
```


Модуль, который читает/записывает простые текстовые файлы.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Источник предупреждения не указан.

### VALIDATOR {#VALIDATOR}
```
public static int VALIDATOR
```


Модуль, который проверяет согласованность и корректность модели.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Модуль, который читает/записывает файлы WML.

### XAML {#XAML}
```
public static int XAML
```


Модуль, который читает/записывает файлы Xaml.

### XLSX {#XLSX}
```
public static int XLSX
```


Модуль, который записывает файлы XLSX.

### XML {#XML}
```
public static int XML
```


Модуль, который читает XML‑файлы.

### XPS {#XPS}
```
public static int XPS
```


Модуль, который отображает XPS.

### length {#length}
```
public static int length
```


### fromName(String warningSourceName) {#fromName-java.lang.String}
```
public static int fromName(String warningSourceName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| warningSourceName | java.lang.String |  |

**Returns:**
int
### getName(int warningSource) {#getName-int}
```
public static String getName(int warningSource)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| warningSource | int |  |

**Returns:**
java.lang.String
