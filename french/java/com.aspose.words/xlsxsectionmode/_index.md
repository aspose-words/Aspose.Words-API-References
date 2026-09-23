---
title: "XlsxSectionMode"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les sections sont gérées lors de l'enregistrement d'un document au format XLSX en Java."
type: docs
weight: 744
url: /fr/java/com.aspose.words/xlsxsectionmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxSectionMode
```

Spécifie comment les sections sont gérées lors de l'enregistrement d'un document au format XLSX.

 **Examples:** 

Montre comment enregistrer le document en tant que feuilles de calcul séparées.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Each section of a document will be created as a separate worksheet.
 // Use 'SingleWorksheet' to display all document on one worksheet.
 XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
 xlsxSaveOptions.setSectionMode(XlsxSectionMode.MULTIPLE_WORKSHEETS);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [MULTIPLE_WORKSHEETS](#MULTIPLE-WORKSHEETS) | Spécifie qu'une feuille de calcul séparée est créée pour chaque section d'un document. |
| [SINGLE_WORKSHEET](#SINGLE-WORKSHEET) | Spécifie que toutes les sections d'un document sont enregistrées sur une seule feuille de calcul. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String xlsxSectionModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxSectionMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxSectionMode)](#toString-int) |  |
### MULTIPLE_WORKSHEETS {#MULTIPLE-WORKSHEETS}
```
public static int MULTIPLE_WORKSHEETS
```


Spécifie qu'une feuille de calcul séparée est créée pour chaque section d'un document.

### SINGLE_WORKSHEET {#SINGLE-WORKSHEET}
```
public static int SINGLE_WORKSHEET
```


Spécifie que toutes les sections d'un document sont enregistrées sur une seule feuille de calcul.

### length {#length}
```
public static int length
```


### fromName(String xlsxSectionModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxSectionModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xlsxSectionModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxSectionMode) {#getName-int}
```
public static String getName(int xlsxSectionMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
