---
title: "TxtOfficeMathExportMode"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Aspose.Words OfficeMath in Java zu SaveFormat.TEXT exportiert."
type: docs
weight: 694
url: /de/java/com.aspose.words/txtofficemathexportmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtOfficeMathExportMode
```

Gibt an, wie Aspose.Words OfficeMath zu [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT) exportiert.

 **Examples:** 

Zeigt, wie man ein OfficeMath-Objekt als LaTeX in TXT exportiert.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 TxtSaveOptions saveOptions = new TxtSaveOptions();
 saveOptions.setOfficeMathExportMode(TxtOfficeMathExportMode.LATEX);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [LATEX](#LATEX) | Exportiere OfficeMath als LaTeX. |
| [TEXT](#TEXT) | Exportiere OfficeMath als Klartext. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String txtOfficeMathExportModeName)](#fromName-java.lang.String) |  |
| [getName(int txtOfficeMathExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int txtOfficeMathExportMode)](#toString-int) |  |
### LATEX {#LATEX}
```
public static int LATEX
```


Exportiere OfficeMath als LaTeX.

### TEXT {#TEXT}
```
public static int TEXT
```


Exportiere OfficeMath als Klartext.

### length {#length}
```
public static int length
```


### fromName(String txtOfficeMathExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtOfficeMathExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtOfficeMathExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int txtOfficeMathExportMode) {#getName-int}
```
public static String getName(int txtOfficeMathExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int txtOfficeMathExportMode) {#toString-int}
```
public static String toString(int txtOfficeMathExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| txtOfficeMathExportMode | int |  |

**Returns:**
java.lang.String
