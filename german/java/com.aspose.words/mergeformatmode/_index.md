---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie die Formatierung beim Zusammenführen mehrerer Dokumente in Java zusammengeführt wird."
type: docs
weight: 464
url: /de/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Gibt an, wie Formatierungen beim Zusammenführen mehrerer Dokumente zusammengeführt werden.

 **Examples:** 

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Bedeutet, dass das Quelldokument seine ursprüngliche Formatierung beibehält, wie Schriftarten, -größen, -farben, Einzüge und alle anderen auf den Inhalt angewendeten Formatierungselemente. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Behalte das Layout der Originaldokumente im endgültigen Dokument bei. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Kombiniere die Formatierung der zusammengeführten Dokumente. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Bedeutet, dass das Quelldokument seine ursprüngliche Formatierung beibehält, wie Schriftarten, -größen, -farben, Einzüge und alle anderen auf den Inhalt angewendeten Formatierungselemente.

 **Remarks:** 

Durch die Verwendung dieser Option stellen Sie sicher, dass der kopierte Inhalt so erscheint, wie er in der Originalquelle war, unabhängig von den Formatierungseinstellungen des ersten Dokuments in der Merge-Warteschlange.

Diese Option hat keine Auswirkung, wenn die Eingabe- und Ausgabeformate PDF sind.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Behalte das Layout der Originaldokumente im endgültigen Dokument bei.

 **Remarks:** 

Im Allgemeinen sieht es so aus, als würden Sie die Originaldokumente ausdrucken und sie manuell mit Klebstoff zusammenkleben.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Kombiniere die Formatierung der zusammengeführten Dokumente.

 **Remarks:** 

Durch die Verwendung dieser Option passt Aspose.Words die Formatierung des ersten Dokuments an die Struktur und das Aussehen des zweiten Dokuments an, behält jedoch einen Teil der ursprünglichen Formatierung bei. Diese Option ist nützlich, wenn Sie das Gesamterscheinungsbild des Zieldokuments beibehalten möchten, aber dennoch bestimmte Formatierungsaspekte des Originaldokuments erhalten wollen.

Diese Option hat keine Auswirkung, wenn die Eingabe- und Ausgabeformate PDF sind.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
