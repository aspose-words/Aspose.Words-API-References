---
title: "NumeralFormat"
linktitle: "NumeralFormat"
second_title: "Aspose.Words para Java"
description: "Indica el conjunto de símbolos que se utiliza para representar números al renderizar a formatos de página fija en Java."
type: docs
weight: 486
url: /es/java/com.aspose.words/numeralformat/
---

**Inheritance:**
java.lang.Object
```
public class NumeralFormat
```

Indica el conjunto de símbolos que se utiliza para representar números al renderizar a formatos de página fijos.

 **Examples:** 

Muestra cómo establecer el formato numeral utilizado al guardar en PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setLocaleId(1025);
 builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
 // use glyphs from the U+0660 to U+0669 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.Context" to
 // look up the locale to determine what number of glyphs to use.
 // Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
 // use glyphs from the U+06F0 to U+06F9 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
 // Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
 options.setNumeralFormat(numeralFormat);

 doc.save(getArtifactsDir() + "PdfSaveOptions.SetNumeralFormat.pdf", options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ARABIC_INDIC](#ARABIC-INDIC) | Números usados en árabe: \\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. |
| [CONTEXT](#CONTEXT) | El conjunto de símbolos se decide según el contexto (configuración regional y propiedad RTL). |
| [EASTERN_ARABIC_INDIC](#EASTERN-ARABIC-INDIC) | Números usados en persa y urdu: \\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. |
| [EUROPEAN](#EUROPEAN) | Números europeos: 0123456789. |
| [SYSTEM](#SYSTEM) | ESTA OPCIÓN NO ES COMPATIBLE. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String numeralFormatName)](#fromName-java.lang.String) |  |
| [getName(int numeralFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numeralFormat)](#toString-int) |  |
### ARABIC_INDIC {#ARABIC-INDIC}
```
public static int ARABIC_INDIC
```


Números usados en árabe: \\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. Rango Unicode U+0660 - u+0669.

### CONTEXT {#CONTEXT}
```
public static int CONTEXT
```


El conjunto de símbolos se decide según el contexto (configuración regional y propiedad RTL).

### EASTERN_ARABIC_INDIC {#EASTERN-ARABIC-INDIC}
```
public static int EASTERN_ARABIC_INDIC
```


Números usados en persa y urdu: \\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. Rango Unicode U+06F0 - u+06F9.

### EUROPEAN {#EUROPEAN}
```
public static int EUROPEAN
```


Números europeos: 0123456789.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


ESTA OPCIÓN NO ES COMPATIBLE. El conjunto de símbolos se decide a partir de la configuración regional.

### length {#length}
```
public static int length
```


### fromName(String numeralFormatName) {#fromName-java.lang.String}
```
public static int fromName(String numeralFormatName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| numeralFormatName | java.lang.String |  |

**Returns:**
int
### getName(int numeralFormat) {#getName-int}
```
public static String getName(int numeralFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| numeralFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numeralFormat) {#toString-int}
```
public static String toString(int numeralFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| numeralFormat | int |  |

**Returns:**
java.lang.String
