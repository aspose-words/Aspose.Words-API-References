---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Dokumenttext in Java analysiert wird, um Datums- und Zeitwerte zu identifizieren."
type: docs
weight: 742
url: /de/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

Gibt an, wie Dokumenttext geparst wird, um Datums- und Zeitwerte zu identifizieren.

 **Examples:** 

Zeigt, wie die automatische Erkennung des Datums‑Zeit‑Formats angegeben wird.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Das in einem Dokument verwendete Datums‑Zeit‑Format wird automatisch ermittelt. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | Das für den aktuellen Thread festgelegte Datums‑Zeit‑Format wird zuerst zum Parsen von Zeichenkettenwerten verwendet. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Das in einem Dokument verwendete Datums‑Zeit‑Format wird automatisch ermittelt. Dies kann zusätzlichen Zeitaufwand bedeuten.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


Das für den aktuellen Thread festgelegte Datums‑Zeit‑Format wird zuerst zum Parsen von Zeichenkettenwerten verwendet. Wenn das Parsen fehlschlägt, werden weitere gängige Datums‑Zeit‑Formate ausprobiert.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
