---
title: "FontSubstitutionReason"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words per Java"
description: "Specifica il motivo della sostituzione del carattere in Java."
type: docs
weight: 335
url: /it/java/com.aspose.words/fontsubstitutionreason/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionReason
```

Specifica il motivo della sostituzione del font.

 **Examples:** 

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
| [ALTERNATIVE_NAME](#ALTERNATIVE-NAME) | Sostituzione del carattere per nome alternativo dal documento. |
| [DEFAULT_FONT_SUBSTITUTION_RULE](#DEFAULT-FONT-SUBSTITUTION-RULE) | Sostituzione del carattere secondo la regola del carattere predefinito. |
| [FIRST_AVAILABLE_FONT](#FIRST-AVAILABLE-FONT) | Sostituzione del carattere con il primo carattere disponibile. |
| [FONT_CONFIG_SUBSTITUTION_RULE](#FONT-CONFIG-SUBSTITUTION-RULE) | Sostituzione del carattere secondo la regola di configurazione del carattere. |
| [FONT_INFO_SUBSTITUTION_RULE](#FONT-INFO-SUBSTITUTION-RULE) | Sostituzione del carattere secondo la regola delle informazioni del carattere. |
| [FONT_NAME_SUBSTITUTION_RULE](#FONT-NAME-SUBSTITUTION-RULE) | Sostituzione del carattere secondo la regola del nome del carattere. |
| [TABLE_SUBSTITUTION_RULE](#TABLE-SUBSTITUTION-RULE) | Sostituzione del carattere secondo la regola della tabella. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fontSubstitutionReasonName)](#fromName-java.lang.String) |  |
| [getName(int fontSubstitutionReason)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSubstitutionReason)](#toString-int) |  |
### ALTERNATIVE_NAME {#ALTERNATIVE-NAME}
```
public static int ALTERNATIVE_NAME
```


Sostituzione del carattere per nome alternativo dal documento.

### DEFAULT_FONT_SUBSTITUTION_RULE {#DEFAULT-FONT-SUBSTITUTION-RULE}
```
public static int DEFAULT_FONT_SUBSTITUTION_RULE
```


Sostituzione del carattere secondo la regola del carattere predefinito.

### FIRST_AVAILABLE_FONT {#FIRST-AVAILABLE-FONT}
```
public static int FIRST_AVAILABLE_FONT
```


Sostituzione del carattere con il primo carattere disponibile.

### FONT_CONFIG_SUBSTITUTION_RULE {#FONT-CONFIG-SUBSTITUTION-RULE}
```
public static int FONT_CONFIG_SUBSTITUTION_RULE
```


Sostituzione del carattere secondo la regola di configurazione del carattere.

### FONT_INFO_SUBSTITUTION_RULE {#FONT-INFO-SUBSTITUTION-RULE}
```
public static int FONT_INFO_SUBSTITUTION_RULE
```


Sostituzione del carattere secondo la regola delle informazioni del carattere.

### FONT_NAME_SUBSTITUTION_RULE {#FONT-NAME-SUBSTITUTION-RULE}
```
public static int FONT_NAME_SUBSTITUTION_RULE
```


Sostituzione del carattere secondo la regola del nome del carattere.

### TABLE_SUBSTITUTION_RULE {#TABLE-SUBSTITUTION-RULE}
```
public static int TABLE_SUBSTITUTION_RULE
```


Sostituzione del carattere secondo la regola della tabella.

### length {#length}
```
public static int length
```


### fromName(String fontSubstitutionReasonName) {#fromName-java.lang.String}
```
public static int fromName(String fontSubstitutionReasonName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontSubstitutionReasonName | java.lang.String |  |

**Returns:**
int
### getName(int fontSubstitutionReason) {#getName-int}
```
public static String getName(int fontSubstitutionReason)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontSubstitutionReason) {#toString-int}
```
public static String toString(int fontSubstitutionReason)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
