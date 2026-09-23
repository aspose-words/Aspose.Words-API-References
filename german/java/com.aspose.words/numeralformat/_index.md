---
title: "NumeralFormat"
linktitle: "NumeralFormat"
second_title: "Aspose.Words für Java"
description: "Gibt das Symbolset an, das zur Darstellung von Zahlen beim Rendern in feste Seitenformate in Java verwendet wird."
type: docs
weight: 486
url: /de/java/com.aspose.words/numeralformat/
---

**Inheritance:**
java.lang.Object
```
public class NumeralFormat
```

Zeigt das Symbolset an, das zur Darstellung von Zahlen beim Rendern in feste Seitenformate verwendet wird.

 **Examples:** 

Zeigt, wie das beim Speichern in PDF verwendete Zahlenformat festgelegt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ARABIC_INDIC](#ARABIC-INDIC) | Im Arabischen verwendete Ziffern: \\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. |
| [CONTEXT](#CONTEXT) | Das Symbolset wird aus dem Kontext (Locale und RTL-Eigenschaft) bestimmt. |
| [EASTERN_ARABIC_INDIC](#EASTERN-ARABIC-INDIC) | Im Persischen und Urdu verwendete Ziffern: \\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. |
| [EUROPEAN](#EUROPEAN) | Europäische Ziffern: 0123456789. |
| [SYSTEM](#SYSTEM) | DIESE OPTION WIRD NICHT UNTERSTÜTZT. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String numeralFormatName)](#fromName-java.lang.String) |  |
| [getName(int numeralFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numeralFormat)](#toString-int) |  |
### ARABIC_INDIC {#ARABIC-INDIC}
```
public static int ARABIC_INDIC
```


Im Arabischen verwendete Ziffern: \\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. Unicode-Bereich U+0660 - u+0669.

### CONTEXT {#CONTEXT}
```
public static int CONTEXT
```


Das Symbolset wird aus dem Kontext (Locale und RTL-Eigenschaft) bestimmt.

### EASTERN_ARABIC_INDIC {#EASTERN-ARABIC-INDIC}
```
public static int EASTERN_ARABIC_INDIC
```


Im Persischen und Urdu verwendete Ziffern: \\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. Unicode-Bereich U+06F0 - u+06F9.

### EUROPEAN {#EUROPEAN}
```
public static int EUROPEAN
```


Europäische Ziffern: 0123456789.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


DIESE OPTION WIRD NICHT UNTERSTÜTZT. Das Symbolset wird aus den regionalen Einstellungen bestimmt.

### length {#length}
```
public static int length
```


### fromName(String numeralFormatName) {#fromName-java.lang.String}
```
public static int fromName(String numeralFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| numeralFormatName | java.lang.String |  |

**Returns:**
int
### getName(int numeralFormat) {#getName-int}
```
public static String getName(int numeralFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| numeralFormat | int |  |

**Returns:**
java.lang.String
