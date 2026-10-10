---
title: "FontSubstitutionReason"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words für Java"
description: "Gibt den Grund für die Schriftartsubstitution in Java an."
type: docs
weight: 335
url: /de/java/com.aspose.words/fontsubstitutionreason/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionReason
```

Gibt den Grund für die Schrift‑Ersetzung an.

 **Examples:** 

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
| [ALTERNATIVE_NAME](#ALTERNATIVE-NAME) | Schriftartsubstitution durch alternativen Namen aus dem Dokument. |
| [DEFAULT_FONT_SUBSTITUTION_RULE](#DEFAULT-FONT-SUBSTITUTION-RULE) | Schriftartsubstitution nach Standard‑Schriftartregel. |
| [FIRST_AVAILABLE_FONT](#FIRST-AVAILABLE-FONT) | Schriftartsubstitution mit der zuerst verfügbaren Schriftart. |
| [FONT_CONFIG_SUBSTITUTION_RULE](#FONT-CONFIG-SUBSTITUTION-RULE) | Schriftartsubstitution nach Schriftart‑Konfigurationsregel. |
| [FONT_INFO_SUBSTITUTION_RULE](#FONT-INFO-SUBSTITUTION-RULE) | Schriftartsubstitution nach Schriftart‑Info‑Regel. |
| [FONT_NAME_SUBSTITUTION_RULE](#FONT-NAME-SUBSTITUTION-RULE) | Schriftartsubstitution nach Schriftart‑Namensregel. |
| [TABLE_SUBSTITUTION_RULE](#TABLE-SUBSTITUTION-RULE) | Schriftart-Ersetzung nach Tabellenregel. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fontSubstitutionReasonName)](#fromName-java.lang.String) |  |
| [getName(int fontSubstitutionReason)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSubstitutionReason)](#toString-int) |  |
### ALTERNATIVE_NAME {#ALTERNATIVE-NAME}
```
public static int ALTERNATIVE_NAME
```


Schriftartsubstitution durch alternativen Namen aus dem Dokument.

### DEFAULT_FONT_SUBSTITUTION_RULE {#DEFAULT-FONT-SUBSTITUTION-RULE}
```
public static int DEFAULT_FONT_SUBSTITUTION_RULE
```


Schriftartsubstitution nach Standard‑Schriftartregel.

### FIRST_AVAILABLE_FONT {#FIRST-AVAILABLE-FONT}
```
public static int FIRST_AVAILABLE_FONT
```


Schriftartsubstitution mit der zuerst verfügbaren Schriftart.

### FONT_CONFIG_SUBSTITUTION_RULE {#FONT-CONFIG-SUBSTITUTION-RULE}
```
public static int FONT_CONFIG_SUBSTITUTION_RULE
```


Schriftartsubstitution nach Schriftart‑Konfigurationsregel.

### FONT_INFO_SUBSTITUTION_RULE {#FONT-INFO-SUBSTITUTION-RULE}
```
public static int FONT_INFO_SUBSTITUTION_RULE
```


Schriftartsubstitution nach Schriftart‑Info‑Regel.

### FONT_NAME_SUBSTITUTION_RULE {#FONT-NAME-SUBSTITUTION-RULE}
```
public static int FONT_NAME_SUBSTITUTION_RULE
```


Schriftartsubstitution nach Schriftart‑Namensregel.

### TABLE_SUBSTITUTION_RULE {#TABLE-SUBSTITUTION-RULE}
```
public static int TABLE_SUBSTITUTION_RULE
```


Schriftart-Ersetzung nach Tabellenregel.

### length {#length}
```
public static int length
```


### fromName(String fontSubstitutionReasonName) {#fromName-java.lang.String}
```
public static int fromName(String fontSubstitutionReasonName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontSubstitutionReasonName | java.lang.String |  |

**Returns:**
int
### getName(int fontSubstitutionReason) {#getName-int}
```
public static String getName(int fontSubstitutionReason)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
