---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ einer Warnung an, die von Aspose.Words beim Laden oder Speichern eines Dokuments in Java ausgegeben wird."
type: docs
weight: 720
url: /de/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Gibt den Typ einer Warnung an, die von Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben wird.

 **Examples:** 

Zeigt, wie die Eigenschaft zum Finden der besten Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftquellen festgelegt wird.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Allgemeiner Datenverlust, kein spezifischer Code. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Einige Texte/Zeichen/Bilder oder andere Daten fehlen entweder im Dokumentbaum nach dem Laden oder im erstellten Dokument nach dem Speichern. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Verlust eingebetteter Schriftinformationen beim Speichern des Dokuments. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Schrift wurde ersetzt. |
| [HINT](#HINT) | Warnt vor einem potenziellen Problem oder schlägt eine Verbesserung vor. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Allgemeiner erheblicher Formatierungsverlust, kein spezifischer Code. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | Das resultierende Dokument oder ein bestimmter Bereich darin kann im Vergleich zum Originaldokument erheblich anders aussehen. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Allgemeiner geringfügiger Formatierungsverlust, kein spezifischer Code. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | Das resultierende Dokument oder ein bestimmter Bereich darin kann im Vergleich zum Originaldokument etwas anders aussehen. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Allgemeiner unerwarteter Inhalt, kein spezifischer Code. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Einige Inhalte im Quelldokument konnten nicht erkannt werden (z. B. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Allgemeiner Datenverlust, kein spezifischer Code.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Einige Texte/Zeichen/Bilder oder andere Daten fehlen entweder im Dokumentbaum nach dem Laden oder im erstellten Dokument nach dem Speichern.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Verlust eingebetteter Schriftinformationen beim Speichern des Dokuments.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Schrift wurde ersetzt.

### HINT {#HINT}
```
public static int HINT
```


Warnt vor einem potenziellen Problem oder schlägt eine Verbesserung vor.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Allgemeiner erheblicher Formatierungsverlust, kein spezifischer Code.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


Das resultierende Dokument oder ein bestimmter Bereich darin kann im Vergleich zum Originaldokument erheblich anders aussehen.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Allgemeiner geringfügiger Formatierungsverlust, kein spezifischer Code.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


Das resultierende Dokument oder ein bestimmter Bereich darin kann im Vergleich zum Originaldokument etwas anders aussehen.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Allgemeiner unerwarteter Inhalt, kein spezifischer Code.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Einige Inhalte im Quelldokument konnten nicht erkannt werden (d. h. werden nicht unterstützt), dies kann Probleme verursachen oder zu Daten-/Formatierungsverlust führen.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
