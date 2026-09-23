---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words für Java"
description: "Gibt Optionen an, die das Verhalten der ReportingEngine beim Erstellen eines Berichts in Java steuern."
type: docs
weight: 570
url: /de/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Gibt Optionen an, die das Verhalten von [ReportingEngine](../../com.aspose.words/reportingengine/) beim Erstellen eines Berichts steuern.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Gibt an, dass fehlende Objektmitglieder von der Engine als Null-Literale behandelt werden sollen. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Gibt an, dass die Engine Fehlermeldungen der Vorlagensyntax in Ausgabedokumente einbetten soll. |
| [NONE](#NONE) | Gibt Standardoptionen an. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Gibt an, dass die Engine Absätze entfernen soll, die nach dem Entfernen oder Ersetzen von Vorlagensyntax-Tags durch leere Werte leer werden. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Gibt an, dass die Engine EXIF \\u200b\\u200bimage orientation-Werte verwenden soll, um eingefügte JPEG-Bilder korrekt zu drehen. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Gibt an, dass die Engine die Vorlagensyntax in Feldresultaten ignorieren und Felder nach dem Erstellen eines Berichts aktualisieren soll. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Gibt an, dass die Engine die Kindknoten eines Abschnitts (Kopfzeilen, Fußzeilen, Körper) in einer Reihenfolge besuchen soll, die mit den Aspose.Words-Versionen vor 21.9 kompatibel ist. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Gibt an, dass fehlende Objektmitglieder von der Engine als Null‑Literale behandelt werden sollen. Diese Option wirkt sich nur auf den Zugriff auf Instanz‑ (also nicht‑statische) Objektmitglieder und Erweiterungsmethoden aus. Wenn diese Option nicht gesetzt ist, wirft die Engine eine Ausnahme, wenn ein fehlendes Objektmitglied gefunden wird.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Gibt an, dass die Engine Fehlermeldungen der Vorlagensyntax inline in Ausgabedokumente einfügen soll. Wenn diese Option nicht gesetzt ist, wirft die Engine eine Ausnahme, wenn ein Syntaxfehler auftritt.

### NONE {#NONE}
```
public static int NONE
```


Gibt Standardoptionen an.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Gibt an, dass die Engine Absätze entfernen soll, die nach dem Entfernen oder Ersetzen von Vorlagensyntax-Tags durch leere Werte leer werden.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Gibt an, dass die Engine EXIF \\u200b\\u200bimage orientation-Werte verwenden soll, um eingefügte JPEG-Bilder korrekt zu drehen.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Gibt an, dass die Engine die Vorlagensyntax in Feldresultaten ignorieren und Felder nach dem Erstellen eines Berichts aktualisieren soll.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Gibt an, dass die Engine die Kindknoten eines Abschnitts (Kopfzeilen, Fußzeilen, Körper) in einer Reihenfolge besuchen soll, die mit den Aspose.Words-Versionen vor 21.9 kompatibel ist.

 **Remarks:** 

Standardmäßig behandelt die Engine Kopf‑ und Fußzeilen, als wären sie mit Abschnittsumbrüchen verknüpft. Das heißt, beim Besuch der Kindknoten eines Abschnitts wird zuerst der Körper besucht und erst danach Kopf‑ und Fußzeilen. Dies entspricht dem Verhalten von Microsoft Word beim Kopieren/Einfügen oder Entfernen von mehrteiligen Inhalten und liefert in den meisten Szenarien korrektere Ergebnisse.

Vor Aspose.Words 21.9 verwendete die Engine eine andere Besuchsreihenfolge: Kindknoten eines Abschnitts wurden in der Reihenfolge besucht, in der sie im Dokument erscheinen. Wenden Sie diesen Wert auf [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/#setOptions-int) an, wenn Kompatibilität mit älteren Versionen von Aspose.Words erforderlich ist.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
