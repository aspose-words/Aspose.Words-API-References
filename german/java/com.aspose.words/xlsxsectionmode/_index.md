---
title: "XlsxSectionMode"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Abschnitte beim Speichern eines Dokuments im XLSX-Format in Java behandelt werden."
type: docs
weight: 744
url: /de/java/com.aspose.words/xlsxsectionmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxSectionMode
```

Gibt an, wie Abschnitte beim Speichern eines Dokuments im XLSX-Format behandelt werden.

 **Examples:** 

Zeigt, wie ein Dokument als separate Arbeitsblätter gespeichert wird.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Each section of a document will be created as a separate worksheet.
 // Use 'SingleWorksheet' to display all document on one worksheet.
 XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
 xlsxSaveOptions.setSectionMode(XlsxSectionMode.MULTIPLE_WORKSHEETS);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [MULTIPLE_WORKSHEETS](#MULTIPLE-WORKSHEETS) | Gibt an, dass für jeden Abschnitt eines Dokuments ein separates Arbeitsblatt erstellt wird. |
| [SINGLE_WORKSHEET](#SINGLE-WORKSHEET) | Gibt an, dass alle Abschnitte eines Dokuments in einem Arbeitsblatt gespeichert werden. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String xlsxSectionModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxSectionMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxSectionMode)](#toString-int) |  |
### MULTIPLE_WORKSHEETS {#MULTIPLE-WORKSHEETS}
```
public static int MULTIPLE_WORKSHEETS
```


Gibt an, dass für jeden Abschnitt eines Dokuments ein separates Arbeitsblatt erstellt wird.

### SINGLE_WORKSHEET {#SINGLE-WORKSHEET}
```
public static int SINGLE_WORKSHEET
```


Gibt an, dass alle Abschnitte eines Dokuments in einem Arbeitsblatt gespeichert werden.

### length {#length}
```
public static int length
```


### fromName(String xlsxSectionModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxSectionModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xlsxSectionModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxSectionMode) {#getName-int}
```
public static String getName(int xlsxSectionMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxSectionMode) {#toString-int}
```
public static String toString(int xlsxSectionMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
